# Development rules — BuxbrewDing

**Author:** Babuni.dev

Preserve project-specific player experience and source comments. Human direction belongs to Babuni.dev; credit AI separately. Existing code is evidence of an approach, not proof of historic approval or runtime verification. Record proposed, implemented and tested separately. With material edits update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG. Preserve third-party credits.

## Evidence and maintenance rules

- Read the actual branch, Lua, TOC, README and relevant dated diffs before editing. Keep source behavior, proposals and tested results separate.
- Preserve Babuni.dev as project author; identify AI drafting, analysis or code assistance separately. Preserve historical records, aliases, license terms and third-party credit.
- Never treat a comment, version label or manifest interface as proof of runtime compatibility. Never claim tests were run without recording the command, environment and outcome.
- For material changes update README, CONCEPT, ROADMAP, CHANGELOG and docs/DEVLOG, plus architecture/design/content where affected. Link evidence and retain uncertainty.
- Documentation-only work must not change Lua, TOC, tests or assets. Check the diff and all relative documentation links before publishing.

## Repository-specific constraints

- Verify or fix `string.match` availability on the intended Lua 5.0/1.12 client in a separate code change.
- Verify callback event/argument conventions and PLAYER_LEVEL_UP timing against the actual client.
- Do not promise persistence: TOC omits SavedVariables and entering-world resets the tracker.
- Check local preview, integer versus fractional inputs, unguilded sends and misleading manual confirmation.
- Check duplicate events, reload/zone transitions, level 60 boundary and guild channel restrictions; manual sends are unthrottled.
