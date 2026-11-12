---
name: dietary-guard
description: Check every recipe, suggestion, substitution, meal plan and shopping list against the household's allergies, intolerances and dietary restrictions before it reaches the user.
---

# Dietary guard

Run this check **every time** before presenting food to the user. It is the most important skill in this agent.

## Know the rules first

- Read the **Who's eating** table in `kitchen-profile.md`. If the user says who a meal is for ("dinner for me and Sam"), check only those people. If they don't say, check the whole household.
- If anyone eating has no entry, ask once: "Any allergies or foods to avoid for <name>?" Record the answer, including "none".
- Record restrictions in the user's own words, with severity. Don't upgrade or downgrade one, and don't guess at causes.

## The check

For each ingredient (including those inside sauces, stocks, spice blends and garnishes):

1. **Direct match.** Is the ingredient itself restricted?
2. **Hidden sources.** Common traps include:
   - fish: Worcestershire sauce, Caesar dressing, fish sauce
   - wheat or gluten: soy sauce, stock cubes, malt vinegar
   - nuts: pesto, marzipan, praline, some curry pastes
   - milk: ghee, casein, whey, some breads and margarines
   - egg: mayo, aioli, fresh pasta, some glazes
   - sesame: tahini, za'atar, some breads
   - shellfish: oyster sauce, shrimp paste
   - pork: gelatin, lard, some sausages and stocks
   - alcohol: cooking wine, vanilla extract, some sauces

   If unsure, look it up (see `sources.md`) and say you checked.
3. **Cross-contact risk.** For `severe` allergies, flag shared fryers, bulk bins, bakery items, and "may contain" style products, such as oats for gluten or chocolate for nuts.
4. **Restriction rules.** Apply the restriction as the user defines it. Vegetarian and vegan, halal and kosher, low-FODMAP, and medical diets differ between people. Ask when the rule is ambiguous, for example "Does vegetarian include fish for you?"

## How to report

- **Passes:** add one quiet line, such as "✅ No nuts or dairy in the ingredients. Check labels on the stock and the curry paste."
- **Conflicts:** name the ingredient and the person, then offer a substitution through recipe-adapter. Never present an unsafe version as the main option.
- **No safe version:** say so plainly and suggest a different recipe.
- Mark label-check items with ⚠️ on shopping lists.
- Never write "safe for allergies" or "allergen-free" as a guarantee. Say "contains no <allergen> in its listed ingredients" and remind the user about labels.

## If the user overrides

If the user knowingly includes a restricted ingredient ("Sam's not eating tonight", "I'm OK with a little dairy"), go with it for that meal. Ask whether the profile should change, but don't change it without a yes.
