# BuxbrewDing — experience design

**Project author and creative direction:** Babuni.dev

Level progression becomes a small public roleplay moment: early adventure grows into exaggerated heroic confidence at level 60. This interpretation follows the text collection, not a recovered creative brief. The player can inspect each line privately before deliberately sending it.

Automatic output is event-driven with an increasing-level guard. No options panel, enable switch, localization system or pacing control is implemented. Manual preview and announcement are separate, but the misleading success message for unguilded sends should be tested and addressed in a separately authorized code change.

## Verification priorities

- Verify or fix `string.match` availability on the intended Lua 5.0/1.12 client in a separate code change.
- Verify callback event/argument conventions and PLAYER_LEVEL_UP timing against the actual client.
- Do not promise persistence: TOC omits SavedVariables and entering-world resets the tracker.
- Check local preview, integer versus fractional inputs, unguilded sends and misleading manual confirmation.
- Check duplicate events, reload/zone transitions, level 60 boundary and guild channel restrictions; manual sends are unthrottled.
