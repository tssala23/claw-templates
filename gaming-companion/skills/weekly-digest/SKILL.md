---
name: weekly-digest
description: Build the weekly digest of wishlist price drops, releases in the next two weeks, and patch notes for games the player is actively playing.
---

# Weekly digest

The `weekly-digest` automation runs this skill. It is installed paused, so turn it on only when the player agrees, and set the schedule's time zone to the one in `player-profile.md`. The player can also ask for a digest at any time.

## Inputs

- `wishlist.md`: titles, stores and target prices.
- `games.md`: games with status `playing` (for patch notes), plus anything `paused` that they played in the last month.
- `player-profile.md`: region, currency, platforms and stores.
- `sources.md`: price trackers for deals, and per-game sources for patches.

## What to check

1. **Price drops.** For each wishlist game, check the current price on the player's stores in their region and currency. Report it if it's at or under the target price, or 25% or more off when no target is set. Give the price, the discount, the store and when the sale ends if that's listed. Never estimate a price. If you can't verify it, leave the game out.
2. **Releases.** List wishlist games and announced sequels or DLC for games they rated 8 or higher that release in the next 14 days on their platforms. Include date shifts and delays since the last digest.
3. **Patches.** Note new patches or balance updates for `playing` games since the last digest. Give each one line, and flag anything that affects a saved build (see builds-and-achievements).
4. **Free stuff (optional).** Add notable free games or free weekends on their platforms only if the profile says they want them.

## Format

Keep it short and scannable, with no more than about 12 lines in total:

```
🎮 Gaming Companion weekly — <date>
💸 Deals: <Title> $X (-Y%) at <store>, ends <date>
📅 Releasing: <Title> — <date> (<platform>)
🛠️ Patches: <Title> <version> — <one line>; affects your build: yes/no
```

Skip any section that's empty. If nothing changed at all, send one line: "Quiet week, nothing new on your list." Link each item to its source.

## Never

Don't buy, pre-order or add anything to a store cart. Don't move wishlist games into `games.md`. Record the date of the last digest at the bottom of `wishlist.md` (`Last digest: YYYY-MM-DD`) so the next run knows what's new.
