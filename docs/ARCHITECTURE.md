# BuxbrewDing — architecture

**Project author and creative direction:** Babuni.dev

`LevelMessages` maps integers 1 through 60 to fixed English strings. `PreviewLevel` prints locally; `AnnounceLevelToGuild` checks `IsInGuild()` before `SendChatMessage`. Both use a generic fallback when no exact table key exists.

A frame registers `PLAYER_ENTERING_WORLD` and `PLAYER_LEVEL_UP`. Entering the world sets `BuxbrewDing_LastLevel` to the player's current level without announcing. The level-up branch uses numeric `arg1`, falling back to `UnitLevel`, and sends only when the new level exceeds the tracked one and is at most 60. It advances the tracked level even if the player is not in a guild.

The slash handler trims text, calls `string.match`, lowercases the command and routes previews or sends. Its manual-send branch prints “Announced” after calling the helper, even when the helper declined for lack of guild membership. It does not update the automatic event tracker. No automated tests exist in the inspected tree.

Despite comments calling the global a saved variable, the TOC has no SavedVariables declaration. Entering-world initialization further means this is an in-session duplicate guard, not evidence of a durable announcement ledger.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [1e068a6](https://github.com/babunidev/BuxbrewDing/commit/1e068a611a4dc848416d93800c6cb087e19eaf4b). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewDing — architecture

**Author:** Babuni.dev

BuxbrewDing.lua contains level-specific messages, a last-announced-level saved variable, a preview helper and PLAYER_LEVEL_UP event handling; /buxbrew accepts preview requests.

Evidence: README.md, main addon Lua file and .toc manifest. Code inspection describes implementation intent, not verified behavior on a running client.
