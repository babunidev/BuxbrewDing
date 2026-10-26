# BuxbrewDing — roadmap

**Project author and creative direction:** Babuni.dev

## Current implementation

A guild level-up announcer with 60 prewritten roleplay messages. The current source attempts automatic guild announcements on increasing levels up to 60 and provides local previews plus explicit manual sends.

## Proposed verification work

- [ ] Verify or fix `string.match` availability on the intended Lua 5.0/1.12 client in a separate code change.
- [ ] Verify callback event/argument conventions and PLAYER_LEVEL_UP timing against the actual client.
- [ ] Do not promise persistence: TOC omits SavedVariables and entering-world resets the tracker.
- [ ] Check local preview, integer versus fractional inputs, unguilded sends and misleading manual confirmation.
- [ ] Check duplicate events, reload/zone transitions, level 60 boundary and guild channel restrictions; manual sends are unthrottled.

No new gameplay feature or release is approved by this documentation pass. Resolve compatibility findings in a separately scoped implementation change and update this record with actual test results.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewDing — roadmap

**Author:** Babuni.dev

## Present

Source and addon metadata exist. No live-game test was conducted during this documentation pass.

## Verification work, not approved new features

Confirm guild-message behavior and compatibility with Vanilla Lua; the source comment still contains an earlier author alias.

## Future development

No additional feature is approved by this reconstruction. Record new direction before implementation.
