---
name: meal-planner
description: Suggest meals and weekly plans, answer "what can I make with…", track the pantry and leftovers, and build shopping lists — all passing the dietary guard.
---

# Meal planner, pantry and shopping

## "What can I make with…?"

1. Combine what they listed with `pantry.md` and the staples in it.
2. Suggest **two or three dishes** that use the most of it and need the fewest extra ingredients. List any missing items.
3. Favour items marked to use soon.
4. Run every suggestion through **dietary-guard**.

## Weekly plans

1. Ask, or infer from `kitchen-profile.md`: how many dinners (and lunches?), who's eating which nights, busy nights, and budget.
2. Build the plan so that:
   - busy nights get recipes of 30 minutes or less, or leftovers
   - perishables are used early in the week
   - ingredients are shared across meals (half a bunch of coriander shouldn't go to waste)
   - one cook-once, eat-twice meal or batch cook is included where it fits
   - there's variety in protein and cuisine
   - at least one new recipe is mixed with the user's highly rated favourites from `recipe-box.md`
3. Show it as a short table. Write it to `meal-plan.md` **only after the user approves.**
4. Suggest prep-ahead tasks, such as "Sunday: cook the rice and marinate the chicken".

## Shopping list

- Build it from the approved plan minus what's in `pantry.md`, with quantities combined across recipes.
- Group by store section in `shopping-list.md`, and mark allergen label-check items with ⚠️.
- Note where a cheaper or seasonal swap is available. Don't place orders.

## Pantry

- Update `pantry.md` when the user says they bought, used or threw out something. Keep it rough; precise counts aren't the goal.
- After a planned meal, offer to deduct its main ingredients.
- When asked "what's going off?", list the items to use soon, with a quick idea for each.

## Leftovers

- Log leftovers in the fridge or freezer table with the date.
- Suggest makeover meals, such as roast chicken into fried rice or chili into stuffed potatoes.
- For how long leftovers keep and how to reheat them, use the official food-safety guidance in `sources.md`, and give the source.

## Nutrition

You can describe a meal in plain terms ("protein-rich", "lots of veg") and pass on the nutrition numbers that a recipe source publishes. Don't calculate or invent nutrition figures, and don't set calorie or macro targets. Suggest a dietitian for that.
