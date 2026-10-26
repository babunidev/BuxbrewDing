# BuxbrewDing — concept

**Project author and creative direction:** Babuni.dev

A guild level-up announcer with 60 prewritten roleplay messages. The current source attempts automatic guild announcements on increasing levels up to 60 and provides local previews plus explicit manual sends.

Level progression becomes a small public roleplay moment: early adventure grows into exaggerated heroic confidence at level 60. This interpretation follows the text collection, not a recovered creative brief. The player can inspect each line privately before deliberately sending it.

Automatic output is event-driven with an increasing-level guard. No options panel, enable switch, localization system or pacing control is implemented. Manual preview and announcement are separate, but the misleading success message for unguilded sends should be tested and addressed in a separately authorized code change.

## Evidence and status

Reviewed on 2026-10-26 against `main` at [1e068a6](https://github.com/babunidev/BuxbrewDing/commit/1e068a611a4dc848416d93800c6cb087e19eaf4b). Current Lua, TOC, README and dated commit history were inspected. Source describes implementation; it does not establish successful operation. Historical intent is reconstructed only where labeled. No in-client test or automated test was executed during this documentation pass.

## Preserved earlier documentation

The following earlier record is retained verbatim. Statements about unavailable history or pending verification describe that earlier snapshot; the dated evidence above supplements it.

# BuxbrewDing — concept

**Author:** Babuni.dev

A character-driven guild level-up announcer for WoW 1.12, with RP text for levels 1 through 60.

## Design visible in the repository

The level itself shapes each prewritten message; guild announcements and local previews have separate paths.

This concept is reconstructed from README.md, main addon Lua file and .toc manifest; original idea and authorship belong to Babuni.dev. No unrecorded decisions are invented.
