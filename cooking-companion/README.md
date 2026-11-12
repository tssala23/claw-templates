# Cooking Companion — OpenClaw Template

<p align="center"><img src="assets/cooking-companion.png" alt="Cooking Companion mascot" width="320"></p>

A warm, practical friend in the kitchen. Cooking Companion:

- **Finds recipes** from trusted sites and your own recipe box, and gives two or three options with links instead of a wall of results.
- **Remembers dietary needs** for everyone in the household (allergies with severity, intolerances, religious, ethical and medical restrictions, and dislikes) and checks *every* suggestion against them, including hidden sources like fish in Worcestershire sauce.
- **Suggests meals and weekly plans** around your schedule, what's in the pantry, and what's about to go off.
- **Adapts recipes**: scales servings, substitutes ingredients for diet or availability, converts units and regional names, swaps equipment (oven to air fryer or Instant Pot), and simplifies for beginners or busy nights.
- **Builds shopping lists** grouped by store section, with ⚠️ on items whose allergen labels need checking.
- **Cooks along with you**: a prep list, one step at a time, doneness cues, rescue tips for split sauces and over-salted soups, and food-safety temperatures from official sources.
- **Learns your taste**: ratings and notes ("less chili next time") are applied automatically.
- **Optional automations** (installed paused): a Sunday meal plan and shopping list, and a midweek "use it up" nudge.

Everything is plain Markdown in the agent workspace (`kitchen-profile.md`, `recipe-box.md`, `pantry.md`, `meal-plan.md`, `shopping-list.md`, `sources.md`). It needs no API keys or plugins.

## Guardrails

- Allergies and restrictions are hard rules, and it never claims a dish is allergen-*safe*, only that no listed ingredient contains the allergen. It always reminds you to check labels.
- Food-safety numbers come from official sources (FoodSafety.gov, USDA FSIS, UK FSA), not recipe blogs.
- It doesn't set calorie or macro targets or prescribe medical diets. It cooks to the rules you or your clinician give it.
- It never orders groceries, buys anything, or contacts anyone.
- It saves recipes as a link, the ingredients, and a short method in its own words, not copied write-ups.

## Layout

```
cooking-companion/
├── package.json
├── CLAW.md                 # manifest frontmatter + agent prompt (becomes SOUL.md)
├── workspace/
│   ├── kitchen-profile.md  # household dietary needs, equipment, tastes
│   ├── recipe-box.md
│   ├── pantry.md
│   ├── meal-plan.md
│   ├── shopping-list.md
│   └── sources.md          # trusted recipe sites + official food-safety/allergen refs
├── assets/cooking-companion.png  # mascot / listing image
└── skills/
    ├── dietary-guard/SKILL.md
    ├── recipe-box/SKILL.md
    ├── recipe-adapter/SKILL.md
    ├── meal-planner/SKILL.md
    └── cook-along/SKILL.md
```

## Validate, build and publish

```bash
openclaw templates validate .
openclaw templates build . --out ./cooking-companion-0.1.0.tgz
clawhub package publish ./cooking-companion-0.1.0.tgz --family template --dry-run
clawhub package publish ./cooking-companion-0.1.0.tgz --family template --wait
```
