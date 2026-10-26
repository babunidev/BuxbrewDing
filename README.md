# BuxbrewDing

**Author:** Babuni.dev

A guild level-up announcer with 60 prewritten roleplay messages. The current source attempts automatic guild announcements on increasing levels up to 60 and provides local previews plus explicit manual sends.

## Installation and use

Install `BuxbrewDing.lua` and `BuxbrewDing.toc` under `Interface/AddOns/BuxbrewDing/`, restart the client and enable it. The TOC declares interface 11200 and version 1.0; actual compatibility is unverified.

| Command | Source behavior |
| --- | --- |
| `/buxbrew 30` | Local preview for level 30 |
| `/buxbrew test 30` or `/buxbrew preview 30` | Local preview |
| `/buxbrew announce 30` or `/buxbrew send 30` | Attempts a real guild message |
| `/buxbrew help` | Lists commands |

Numeric inputs are range-checked from 1 to 60, but integer validation is absent. Manual announcements can name a level other than the player's current one. Preview is local; announce/send affects guild chat and has no rate limiter.

**Known source limitations:** `string.match` is used despite the 1.12 target, so stock Lua 5.0 compatibility needs correction or verified client support. The TOC omits `SavedVariables`; `BuxbrewDing_LastLevel` is a runtime global, not demonstrated persistent storage.

## Limitations and verification

- Verify or fix `string.match` availability on the intended Lua 5.0/1.12 client in a separate code change.
- Verify callback event/argument conventions and PLAYER_LEVEL_UP timing against the actual client.
- Do not promise persistence: TOC omits SavedVariables and entering-world resets the tracker.
- Check local preview, integer versus fractional inputs, unguilded sends and misleading manual confirmation.
- Check duplicate events, reload/zone transitions, level 60 boundary and guild channel restrictions; manual sends are unthrottled.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [1e068a6](https://github.com/babunidev/BuxbrewDing/commit/1e068a611a4dc848416d93800c6cb087e19eaf4b). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Documentation

- [Concept](CONCEPT.md) · [Design](docs/DESIGN.md) · [Content](docs/CONTENT.md)
- [Architecture](docs/ARCHITECTURE.md) · [Decisions](docs/DECISIONS.md)
- [Roadmap](ROADMAP.md) · [Changelog](CHANGELOG.md) · [Development journal](docs/DEVLOG.md)
- [AI collaboration](docs/AI_COLLABORATION.md) · [Contributor instructions](AGENTS.md)

The [historical README](docs/HISTORICAL_README.md) is retained verbatim as prior documentation, including any outdated claims. Current source and the qualifications above take precedence.
