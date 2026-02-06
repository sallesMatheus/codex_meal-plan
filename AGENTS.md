# Agent Instructions (Codex)

## Repo + workflow rules
- You are working inside /workspaces/codex_meal-plan
- Make changes directly to files in this repo (not docs-only).
- After each milestone:
  - run: git status
  - then: git add .
  - git commit -m "<clear message>"
  - git push
- Always keep the app runnable (npm run dev should work).
- If a command fails: diagnose and propose the next command(s); do not stop.

## Secrets
- Never read, print, or commit .env
- Never ask to paste keys into chat.
- Assume .env already exists locally with:
  - VITE_SUPABASE_URL
  - VITE_SUPABASE_ANON_KEY

## Tech
- React + Vite
- Supabase JS client in src/supabaseClient.js

## Supabase schema already exists
Tables:
- households, household_members, meals, meal_ingredients, week_plans, week_plan_items
RLS policies are enabled.

## Product
Build a shared meal planner for 2 users:
- Email magic-link login
- Auto-create household on first login, and add current user to household_members
- Invite code flow: user can share a code/link so second user joins same household
- Pages: Meals (CRUD), Week Planner (assign meals to days), Shopping List (aggregate ingredients)
