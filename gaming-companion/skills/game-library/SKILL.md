---
name: game-library
description: Manage the player's game library, backlog, ratings and journal, and answer "what should I play?" with two or three picks tuned to their mood, time and taste.
---

# Game library and "what should I play?"

## Files

- `games.md`: one table row per game. Keep the columns as they are, and add rows rather than rewriting the table.
- `journal.md`: dated verdict lines, newest first.
- `player-profile.md`: platforms, likes and avoids, session length.

## Logging

- **Adding games.** When the player mentions owning or starting a game, add a row. If they list several at once ("my Steam backlog is X, Y, Z"), add them all with status `backlog`, and ask about the platform once for the whole batch, not once per game.
- **Status changes.** Update the row when the player says they started, paused, finished or dropped a game. For `finished` or `dropped`, ask for a quick rating and a one-line reason, then add a journal line. If they skip it, log the status anyway.
- **Ratings.** Only record a rating the player gave you. Never estimate one.
- **Duplicates.** Match titles loosely (editions, remasters, "GOTY"), and ask before merging rows that might be different games.
- **Imports.** If they paste a library export or list, add every row in one pass and say how many were added.

## "What should I play?"

1. Work out the constraints from the message, or ask once if they're missing. Constraints are time available ("30 min", "whole evening"), mood ("chill", "challenge", "story", "with friends"), energy level and platform. Don't ask for anything you can already infer.
2. Build candidates in this order: `paused` and `playing` games (lowest friction), then `backlog`, then wishlist games released at a fair price, only if they've asked for something new.
3. Score each candidate by fit with the session length (no 40-minute unskippable openings for a 30-minute slot; HowLongToBeat in `sources.md` helps with this), fit with the mood tags, similarity to games they rated 8 or higher, and distance from what they dropped and why. Give a mild boost to games they haven't touched in a long time but rated highly while playing.
4. Reply with **two or three picks**. Give each one a one-line reason tied to their history, for example "same loop as Hades, which you gave a 9, and runs are about 25 minutes." If a pick is paused, offer a "where was I" recap (session-notes skill).
5. If they reject the picks, ask what was off and log the dislike in the profile when it's a lasting preference.

## Recommending games they don't own

Only do this when asked. Base picks on top-rated journal entries and stated loves, and check release status and price with a live lookup before quoting them. Don't add these games to `games.md`; offer to add them to `wishlist.md` instead.

## Stats on request

You can summarize the backlog by status, hours and platform, list the "shortest unfinished" games, or show "highest-rated this year". Count from the files and don't estimate.
