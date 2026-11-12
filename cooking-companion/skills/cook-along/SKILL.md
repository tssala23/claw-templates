---
name: cook-along
description: Walk the user through a recipe step by step while they cook — prep list, one step at a time, timers, doneness cues, rescue tips and food-safety checks.
---

# Cook-along mode

Start when the user says "let's cook", "walk me through it" or similar.

## Before the heat goes on

1. Confirm the recipe and servings (after any recipe-adapter changes).
2. Give a **mise en place list**: everything to get out, chop and measure first, grouped so it's quick to do.
3. Mention anything that takes a while to get going, such as preheating the oven, boiling water or bringing butter to room temperature.

## During cooking

- **One step per message.** Keep each short: the action, the amount, the heat level, and a **doneness cue** ("until the onions are soft and golden, about 8 minutes").
- Wait for "next", "done" or a question before moving on.
- When a step has a wait, say how long and what to do meanwhile ("While that simmers for 15 minutes, make the salad").
- If the user's platform supports reminders, offer to set a timer. Otherwise tell them clearly when to check.
- If they say "back" or "repeat", repeat the step without restarting.

## Rescue tips

When something goes wrong, give one fast fix first, then an explanation only if they want it:
- too salty: add acid, more unsalted base, or a starch
- sauce split: add a splash of cold liquid and whisk off the heat
- burnt bottom: don't scrape it, and transfer the rest
- too thin: reduce it or add a slurry
- too spicy: add dairy, sugar, acid or more base, as long as dietary-guard allows the fix

## Food safety

- Give safe minimum internal temperatures for meat, poultry, fish, eggs and reheated leftovers **from official sources only** (see `sources.md`), with the unit the user prefers.
- Flag raw-meat cross-contamination: separate boards, washing hands, and not reusing marinade unless it's boiled.
- For allergies, remind the user to prep the allergen-free portion first, with clean tools.
- Don't give food-safety numbers from memory if you can look them up. If you can't verify one, say so and suggest using a thermometer and checking the official guidance.

## Wrap up

When they're done, ask for a quick 1–5 rating and any changes (recipe-box). Offer to log leftovers and deduct the ingredients they used (meal-planner).
