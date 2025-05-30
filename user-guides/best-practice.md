---
title: "Best Practices"
description: "Getting the Most Out of Lovable"
icon: "dumbbell"
---

This guide helps all users—new or experienced—get up to speed quickly and avoid common pitfalls when building on Lovable.

## 1. Set Your Foundation: Use the Knowledge File

**Why it matters:** The [_Knowledge_](https://docs.lovable.dev/features/knowledge) file is your project’s brain. It gets sent with every prompt and helps the AI understand the full context.

**What to include:**

- Your product vision (think of it like a PRD)
- User journeys and personas
- Key features and functionality
- Design systems and UI guidance
- Role-specific behavior (e.g. Admin, User, Investor)

## 2. [Prompting](https://docs.lovable.dev/tips-tricks/prompting-one) Best Practices

**Clear, verbose prompts = better output.** Think of the AI like your engineering partner—it only knows what you tell it.

**Prompting tips:**

- Be specific: Mention the exact page (e.g. `/dashboard`) and expected behavior.
- Use natural language

  ```
  I want users with the role Investor to access this component, but not Admins.
  ```
- Add screenshots: Especially useful for describing bugs or UX issues.
- Add guardrails: Tell the AI what **not** to touch. E.g.

  ```
  Do not edit /shared/Layout.tsx.
  ```
- Repeat important instructions across prompts. The AI’s memory can be limiting.
- Avoid trying to implement 5 things at once. Break work into smaller, testable chunks. Use Chat Mode between each block to validate before moving on.

  ```
  **Feature Breakdown Template:**
  Create the new page
  Add UI layout
  Connect the data
  Add logic + edge cases
  Test per role
  ```
- If your app has multiple roles (e.g. Admin, Investor, Startup), always define _which role_ the prompt applies to. This helps avoid bugs caused by shared logic/components.

  ```
  As an Investor, I want to view the company dashboard, but I shouldn’t be able to edit it. Please isolate this feature to the Investor role only.
  ```

## 3. Use Chat Mode Early and Often

[**Chat mode**](https://docs.lovable.dev/features/labs#chat-mode) = your AI co-pilot. It helps you debug, brainstorm, and plan implementations—without editing your code until you’re ready.

**When to switch to Chat Mode:**

- After 2–3 failed “Try to Fix” attempts
- When debugging complex logic or database issues
- When planning new features

  ```
  Suggest 3 ways to implement X
  ```

## 4. Avoid Common Pitfalls with Supabase

**Heads-up:** [Supabase](https://docs.lovable.dev/integrations/supabase) does not revert cleanly. If you revert a version, your database schema may break.

**Best practices:**

- Connect Supabase **after** front-end is stable
- If you must revert, prompt the AI:

  ```
  Please validate the SQL schema at T=0 and ensure no breaking changes have occurred.
  ```
- Always test database-linked features before publishing

## 5. Use Visual Edit for Quick UI Fixes

The [**Visual Edit tool**](https://docs.lovable.dev/features/visual-edit) is free and fast. Use it instead of prompts for:

- Changing text, colors, fonts, layout tweaks
- Editing multiple small elements at once
- Safe, credit-free commits (with undo available)

## 6. Use [GitHub](https://docs.lovable.dev/integrations/git-integration) \+ Version Control Wisely

- Every edit is a commit. Use **pinning** to mark stable versions. After every working feature: **Pin it**
- After every bug: **Compare versions visually.** You can prompt with:

  ```
  Compare version at T–1 to T–0. What changed? What might be breaking?
  ```
- Come back to a stable version if you feel the AI has broken too much things.
- Use **GitHub branching** at your own risk. Avoid deleting branches before switching back to `main` in Lovable to prevent project sync issues.

## 7. When All Else Fails, Remix

Many users realize: doing it all over takes less time the second time.

- [Remix](https://docs.lovable.dev/user-guides/quickstart#remix-an-existing-project:~:text=you%20to%20reuse-,the,-current%20state%20of) creates a clean copy of your project at T=0.
- Rebuild with better prompting \+ clearer knowledge
- Use your old project as reference only

**Use cases:**

- You're stuck in a buggy loop
- You want to restart clean with preserved history
- You need to disconnect Superbase and try a new path

## 8. Stay Patient, Stay Calm

You’re not alone. AI can be magical one moment and frustrating the next. The final 5% of any build is often the slowest—but the most important.

## 9. Use the Docs & Ask for Help

- [Documentation](https://docs.lovable.dev) contains walkthroughs, templates, SEO tips, integrations, and more. You can ask questions directly in the doc AI assistant.
- Join the [Discord community](https://discord.gg/lovable-dev) for peer support.
- When ready, submit your project to [Lovable Launch](https://docs.lovable.dev/features/launched).

## 10. Bonus Tips

- Add a voice note prompt using dictation (e.g. On Mac, use the mic to dictate long prompts) for long prompts. You’ll craft better input faster—especially useful when frustrated or tired.
- Use the “`I am frustrated…`” prompt pattern to nudge better AI focus
- After a major edit, always recheck multiple roles and their behavior (especially with conditional logic)
- Store stable versions as fallbacks for quick debugging
- If you're seeing unexpected side effects, this helps avoid bugs caused by overly generic logic.

  ```
  Create a component specifically for [role X] and do not reuse shared components unless clearly scoped.
  ```