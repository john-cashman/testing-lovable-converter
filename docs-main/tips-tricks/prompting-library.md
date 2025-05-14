---
title: "Prompt Library"
description: "List of prompting strategies and approaches."
icon: "book"
---

_Welcome to the prompt library\\\!_ Here we’ve collected a set of reusable prompt patterns and examples for common scenarios when building with AI. Think of these as templates or inspiration that you can tailor to your own project. Each section covers a particular use case – from kicking off a new project to integrating payments – with guidance on when to use it and an example prompt.

Feel free to copy these, modify the details, and use them in Lovable or any AI builder. The tone is official yet casual – just like talking to a colleague – and each prompt provides enough context so the AI knows exactly what to do.

## Starting Projects

**Example Prompt – Starting a New Project:**

```
I need a **task management** application with:
- **Tech Stack:** Next.js frontend, Tailwind CSS for styling, Supabase for auth and database.
- **Core Features:** Project and task creation, assigning tasks to users, due date reminders, and a dashboard overview.

Start by building the **main dashboard page**, containing:
- A header with navigation,
- A list of projects with their status,
- and a button to create a new project.

Provide dummy data for now, and ensure the design is clean and responsive.
```

```
Create a new component called [ComponentName] with these features: [list features]. Make it responsive and accessible with proper keyboard navigation. Include proper TypeScript typings for props, and use Tailwind for styling.
```

```
Explain how this function works in simple terms, highlighting its inputs, outputs, and any side effects: [paste function]. What edge cases does it handle or miss? How could it be improved?
```

This prompt follows a proven structure for new projects​. It first states the app type and tech stack, then lists core features, and finally tells the AI where to begin (the main dashboard page, with specifics). By doing this, you give Lovable a clear roadmap to initiate the project. _(Pro tip: It’s often wise to start with an empty project and build up gradually, so the AI doesn’t get overwhelmed​.)_

## UI/UX Design

Lovable has pretty good taste out of the box, but a targeted prompt can help achieve a specific aesthetic or UX improvement​. For example, you might want to restyle a button, improve form layout, or ensure consistency in spacing.

**Example Prompt – UI Only Changes:**

```
The app UI should be improved, **without changing any functionality**. 

- Keep all existing logic and state management as is.
- **Visual Enhancements:** Update the styling of the dashboard page: use a modern card design for each project listing, improve the color scheme for better contrast, and increase padding for a cleaner layout.
- Ensure these changes do **not break any functionality or data flow**.

*Goal:* purely cosmetic improvements for a more polished look, with the app behaving exactly as before.
```

```
Enhance the visual appeal of this component: [paste component]. Add animations, improve spacing, create a polished look while maintaining accessibility standards and responsive behavior.
```

```
Create a comprehensive design system for my application with a color palette, typography scale, spacing system, and component variants. Include dark mode support and ensure all components are accessible (WCAG AA compliant).
```

```
Design a responsive dashboard layout with [describe key metrics/widgets]. It should work well on mobile, tablet, and desktop with appropriate layout shifts. Include a sidebar navigation that collapses on mobile.
```

```
Transform this desktop-only component into a mobile-first design with responsive breakpoints: [paste component]. Prioritize content and interactions for small screens first, then enhance for larger screens.
```

```
Add subtle, performant animations to this component to enhance user experience: [paste component]. Include enter/exit animations, hover states, and micro-interactions that provide feedback without being distracting.
```

```
Analyze and optimize the user flow for [describe task/goal]. Map out each step of the journey, identify friction points, and suggest UI improvements to create a more intuitive experience with fewer steps.
```

```
Review these components for accessibility issues and suggest improvements: [paste components]. Check for proper keyboard navigation, screen reader support, sufficient color contrast, and appropriate ARIA attributes.
```

In this prompt, we explicitly say to make solely visual enhancements and not affect how the app works​. This is crucial – it tells the AI “don’t touch the logic.” We list specifics (card design, color contrast, spacing) so the AI knows what aspects of the UI to tweak. This kind of prompt is perfect after you’ve built features and want to beautify the interface.

## Responsiveness

**Example Prompt – Mobile Responsiveness:**

```
Our app needs to be **fully responsive** across mobile, tablet, and desktop.

- Follow a **mobile-first** strategy: prioritize the layout for small screens, then adjust for larger screens.
- Use modern UI/UX best practices for responsive design. (For Tailwind CSS, use the standard breakpoints `sm, md, lg, xl` – no custom breakpoints unless necessary.)
- Ensure every page (especially the dashboard and project detail pages) reflows properly on a small screen: elements should stack or resize as needed, text should remain readable, and no content should overflow off-screen.
- **Do not change the core design or functionality**, just make sure it flexibly adapts to different screen sizes.

After making changes, please double-check the layout at iPhone 12 dimensions and a typical desktop width.
```

In this prompt, we explicitly instruct the AI to make all designs responsive at every breakpoint, focusing on mobile first​. We even reference Tailwind’s standard breakpoints to guide the implementation. We clarify that the design and functionality shouldn’t fundamentally change; it should just work well on smaller screens. This sets a clear expectation: the outcome should look the same design-wise, but fluidly resize and re-stack for responsiveness.

## Refactoring

**Example Prompt – Safe File Refactor:**

```
Refactor the **ProjectList component file**, but **keep its behavior and UI exactly the same**. 

Goals:
- Improve the code structure and readability (simplify complex functions, break into smaller ones if needed).
- Remove any unused variables or imports.
- Ensure the file follows best practices and is well-documented.

Do **not** introduce any new features or change how the component works for the user – this is purely a code cleanup for maintainability. If any part of the code is unclear, add a brief comment for clarification.
```

```
Review this code and suggest improvements for readability, performance, and maintainability: [paste code]. Focus on TypeScript best practices, proper error handling, and adherence to React patterns.
```

```
Suggest a folder structure for a [type] application with these features: [list features]. Include guidelines for organizing components, hooks, utilities, and types with proper separation of concerns.
```

```
I'm getting this error: [paste error]. Here's the relevant code: [paste code]. Can you help me understand what's causing it and how to fix it? Please explain why the solution works.
```

This prompt clearly states the component to refactor and the constraints (no functional changes allowed). It prioritizes structure and maintainability​. The AI will go through the file, maybe reordering functions, renaming things for clarity, commenting tricky parts, etc., but the output of the app should remain identical. This helps prevent the dreaded scenario of a “refactor” accidentally breaking something.

For bigger refactoring efforts (like many files or an entire project), consider having the AI **analyze the codebase first**. You can use a prompt to get a report on what could be improved and where (see the Debugging section’s _Full System Review_ prompt for an idea). Then, apply changes incrementally. Refactor in small pieces and test as you go, rather than one massive overhaul.

## App Types

```
Create a starter e-commerce store with product listing, search, filtering, cart functionality, and checkout process. Include user accounts, order history, and basic product management. Focus on a clean, conversion-oriented UI.
```

```
Build a basic CMS for managing blog posts or articles with an admin dashboard. Include features for creating, editing, and publishing content with rich text formatting, image uploads, and basic SEO management.
```

```
Create a project management app with task boards, lists, and cards. Include features for task assignment, due dates, labels, comments, and progress tracking. Implement drag-and-drop functionality and user collaboration.
```

```
Build a social media feed component with posts, comments, likes, and sharing functionality. Include user profiles, follow/unfollow mechanics, and a notification system. Ensure the design is responsive and supports infinite scrolling.
```

```
Create an analytics dashboard with multiple chart types (bar, line, pie), data filtering options, date range selection, and exportable reports. Include responsive design and skeleton loading states for data fetching.
```

```
Build a SaaS application starter with user authentication, subscription management, a settings page, and a basic dashboard. Include role-based access control, account management, and a well-structured architecture for future expansion.
```

```
Create a chat interface with an AI assistant that helps users with [describe task/purpose]. Include conversation history, typing indicators, message threading, and the ability to provide feedback on AI responses.
```

```
Build a tool that uses AI to generate [describe content type] based on user inputs and parameters. Include options to refine the generated content, save favorites, and export in different formats.
```

```
Implement a recommendation component for [describe items] based on user behavior and preferences. Include the ability to provide feedback on recommendations, see why items were recommended, and discover new options.
```

```
Enhance the search experience for [describe content] with AI-powered features like natural language understanding, semantic search, and intelligent ranking of results. Include search suggestions and auto-complete.
```

```
Create a dashboard that uses AI to analyze [describe data] and present insights in an accessible way. Include visualizations, plain-language explanations of trends, and the ability to ask questions about the data.
```

```
Implement a system for personalizing the user experience based on behavior and preferences. Include customizable UI elements, content recommendations, and settings that allow users to control their personalization.
```

## React Development

```
Create a custom React hook called use[Name] that handles [functionality]. It should handle proper state initialization, cleanup, memoization of values, and TypeScript typing. Include example usage and error handling.
```

```
Refactor this component to use React Context instead of prop drilling: [paste component]. Create a proper context provider with typed state and actions, and separate the business logic from UI rendering.
```

```
Optimize this React component to prevent unnecessary re-renders: [paste component]. Use memo, useMemo, and useCallback where appropriate. Add explanatory comments about why each optimization is needed.
```

```
Create a form with validation for [describe form fields and validation rules]. Use react-hook-form with zod schema validation, proper error handling, and submission handling that includes loading states.
```

```
Implement a data fetching pattern for [describe the data] using React Query. Include proper loading states, error handling, optimistic updates, and data synchronization strategies.
```

```
Create a smooth transition animation for [describe the element] when it [describe the action]. Use CSS transitions or Framer Motion, ensuring the animation works well across devices and doesn't harm performance.
```

## Locking Files / Limiting Scope

**Example Prompt – Limit Scope of Changes:**

```
Please **focus only on the Dashboard page** for this change. 

- Do **not modify** the `LoginPage.tsx` or `AuthProvider.tsx` files at all (authentication is working well, and we want to keep it intact).
- Concentrate your code edits on `Dashboard.tsx` and related dashboard components **only**.

Task: Add a new section to the Dashboard that shows “Tasks due this week”. Make sure to fetch the relevant tasks from the database. 

*(Again, no changes to login or auth files – those are off-limits.)*
```

Here we included a very direct constraint: \_“refrain from altering pages X or Y and focus changes solely on page Z.”\_​. By repeating this in the prompt, we guide the AI’s attention. The task itself (adding a dashboard section) is given, but we wrapped it with instructions about scope. This greatly reduces the chance of Lovable tinkering with your login system while trying to add a dashboard feature.

Another scenario is when updating a very delicate feature. In such cases, you can combine scope limitation with a cautionary tone. For example: ****_____“This update is sensitive; proceed very carefully and avoid touching anything unrelated”_____****. This was demonstrated in a prompt like: \_“This update is quite delicate... Steer clear of shortcuts or assumptions — take a moment to seek clarification if unsure. Precision is crucial.”\_​. Including a line like that sets the AI’s “mindset” to be extra cautious.

## Planning

**Example Prompt – Planning a Feature Implementation:**

```
Before writing any code, **plan out the implementation** of the new Notifications feature.

- List each step required to add email notifications when a task is overdue.
- Consider both frontend (UI changes, if any) and backend (creating scheduled checks or triggers) aspects.
- Ensure the plan keeps the current functionality stable – we can’t break anything existing.
- Provide the plan as an ordered list (1, 2, 3, ...), with a brief explanation of each step.

Once you outline the plan, pause for review. **Do not make any code changes yet.**
```

This prompt tells the AI to act as a planner. It asks for a sequenced plan to implement an “email notifications for overdue tasks” feature. We explicitly say not to code yet (so we’d run this in Chat mode or just trust that the AI will output a plan). The AI might respond with something like:

1. **Add a timestamp field** to tasks for due date (if not already present).
2. **Create a server-side function** (or scheduled job) to check for overdue tasks periodically.
3. **Integrate email sending** using an email service (e.g., Resend or SMTP) when an overdue task is found.
4. **Update the UI** to allow users to toggle notifications on/off for a task (optional setting).
5. **Test the flow** with a task that just passed its due time to ensure an email is sent.

By reviewing such a plan, you can catch any issues (maybe we realize we need a new DB table, or maybe step 4 is out-of-scope for now, etc.) _before_ any coding happens. It’s a lot easier to tweak the plan than to rewrite bad code. Planning prompts save time in complex features by getting the approach right from the start​.

## Stripe Setup

**Example Prompt – Integrating Stripe Payments:**

```
I want to **add Stripe payments** to the app.

- Use **Stripe in test mode** for now.
- We have a product in Stripe with ID `prod_12345` and a price ID `price_67890` (one-time purchase).
- Implement a checkout button on the **Pricing page** that starts a Stripe checkout for that product.
- After successful payment, redirect the user to `/payment-success`. If the payment is canceled, redirect to `/payment-cancelled`.

Important:
- Assume API keys and webhook secrets are configured securely (do **not** hard-code them).
- Do **not** modify any other pages or features unrelated to payments.

Once done, provide any webhook endpoint setup instructions I need (e.g., URL to add in Stripe dashboard for post-payment events).
```

This prompt gives all the key details for Stripe: test mode, product IDs, what happens on success/cancel, and where to put the checkout button. It explicitly says not to touch anything else. The AI (and Lovable’s Stripe integration helper) will use this to scaffold the Stripe integration. Under the hood, Lovable might create a serverless function (if using Supabase) to handle webhooks, etc., but you don’t have to prompt that separately – the instruction here is usually enough for a basic setup​.

_Note:_ We included a line about API keys being secure because we never want secret keys in the prompt. The docs remind us: \_“Use your Stripe Secret Key in the Supabase Edge Function secrets, and avoid including them in the prompt”\_​. So by telling the AI “assume it’s configured,” you ensure the code will reference an environment variable or config, not a plaintext key.

After running this prompt, test the payment flow with Stripe’s test card numbers. If something isn’t working (e.g., the webhook), Lovable might show errors which you can then debug or refine with another prompt.

## Supabase & Backend

```
Enhance the visual appeal of this component: [paste component]. Add animations, improve spacing, create a polished look while maintaining accessibility standards and responsive behavior.
```

```
Design a database schema for [describe your application] with these entity relationships: [describe relationships]. Include foreign key constraints, indexes for performance, and proper data types with considerations for scalability.
```

```
Create a service to fetch data from [API name] and implement caching, error retry logic, and request throttling. Set up proper TypeScript interfaces for the response data and handle API versioning gracefully.
```

```
Create Row Level Security policies for a multi-tenant application with these tables: [list tables]. Implement proper user isolation, role-based access, and handle hierarchical data access with considerations for performance.
```

```
Create a Supabase Edge Function to handle [describe functionality] with proper error handling, input validation, and security checks. Include rate limiting and proper environment variable usage.
```

```
Implement real-time data synchronization for [describe feature] using Supabase subscriptions. Handle connection management, graceful degradation when offline, and conflict resolution.
```

```
Implement a robust search feature for [describe content type] with filtering, sorting, and highlighting of matched terms. Include typeahead suggestions, recent searches, and proper handling of no-results scenarios.
```

```
Create a data table/grid for [describe data] with sorting, filtering, pagination, column resizing, and row selection. Include features for exporting data and customizing visible columns.
```

```
Build a system for importing and exporting [describe data] in various formats (CSV, JSON, etc.). Include validation, progress indicators, error handling, and the ability to map fields during import.
```

```
Create a set of interactive charts for [describe data/metrics] using Recharts. Include different visualization types (bar, line, pie), time period selection, drill-down capabilities, and responsive behavior.
```

```
Implement a strategy for synchronizing offline data changes with a backend when connectivity is restored. Handle conflict resolution, optimistic UI updates, and provide visual indicators for sync status.
```

```
Create a multi-step form wizard for collecting [describe data] with validation, progress tracking, the ability to save drafts, and a summary review before submission. Handle conditional form fields based on previous answers.
```

## Workflow

```
Connect this Lovable project to GitHub and set up a good workflow for contributions. Include branch protection rules, PR templates, and CI/CD workflow configuration with automatic preview deployments.
```

```
Refactor this large component into smaller, more manageable components: [paste component]. Extract reusable parts, implement proper prop passing, maintain state management, and ensure the refactoring doesn't break existing functionality.
```

```
Suggest a testing strategy for [component/feature] including what to test and how. Include unit tests for business logic, integration tests for data flow, and UI tests for critical user flows with best practices for mocking dependencies.
```

```
Implement comprehensive error handling for this async function: [paste function]. Include retry logic, fallback mechanisms, proper error reporting, user-friendly error messages, and logging for debugging purposes.
```

```
Set up a deployment pipeline for this application that includes staging and production environments, automatic database migrations, environment-specific configurations, and rollback capabilities.
```

```
Analyze and optimize this user flow: [describe flow]. Suggest improvements for user experience, reduce friction points, implement progressive enhancement, and ensure accessibility throughout.
```

## Using Chat Mode vs Default Mode

**Example use case – Default vs Chat:**

Suppose you suspect there is outdated code in your project that needs cleaning up. In Default mode, you might directly prompt:

Lovable could try to both identify and possibly start refactoring it in one go​. But maybe you actually want to be careful and just get advice. In that case, you’d switch to Chat mode and ask something like:

Now the AI will _discuss_ this with you, rather than immediately rewriting files.

Similarly, if you have an error and you want the AI to analyze it, Chat mode is safer. You can copy an error message and ask:

The AI will explain and propose a solution. Once you agree, you might switch to Default mode or explicitly instruct to apply the fix.

In summary, **use Default Mode for straightforward building** (“do X for me”), and **use Chat Mode for troubleshooting or design discussions** (“why or how should we do X?”). One concrete workflow is: _Brainstorm in Chat (get a plan or identify issues), then execute in Default._ This approach is even recommended: for example, \_use Chat Mode to have the AI analyze errors before making changes\_​. It’s like using ChatGPT for advice and then applying the changes once you’re confident.

_(Make sure Chat-Only Mode is enabled in your settings under Labs if you don’t see it​. This mode ensures the AI won’t write code to your project until you say so, which is perfect for safe experimentation.)_

## Writing Knowledge Bases and PRDs

This might sound like a lot, but writing it down pays off. **The AI will use this info on every prompt to stay aligned with your project’s needs​.** It’s like giving the AI long-term memory about your app. You typically set this up once (and update as needed).

After populating the knowledge base, you can literally tell the AI to use it. For example, your very first prompt to Lovable might be: \_“Before writing any code, please **__review the Knowledge Base__** and confirm you understand the project.”\_​ This lets the AI summarize or acknowledge the context, and you can catch if it missed something.

**Example Prompt – Using the Knowledge Base:**

```
User: Before you write any code, please review the Knowledge Base and share your understanding of my project.
AI (likely response): “Sure. Based on the Knowledge Base: You’re building a task management app for teams. The app flow is Users sign up -> see a dashboard -> create projects and tasks. The tech stack is Next.js for frontend, Supabase for backend (authentication and database). Core features include project creation, task assignments, and a reporting dashboard. In-scope features: task CRUD, user roles, email notifications; Out-of-scope: real-time collaboration. The design should follow a clean corporate style with Tailwind CSS, and it needs to be responsive. Backend uses Supabase with row-level security for multi-tenant data separation...” (and so on).
```

This kind of summary from the AI confirms it has ingested your specifications correctly. If it misunderstood anything, you can correct it in Chat mode. Once confirmed, you proceed with building (the AI now “knows” the overall plan).

Writing a PRD and filling the Knowledge Base might feel like extra upfront work, but it **pays dividends throughout development**. It reduces errors and AI hallucinations because the AI always has a reference for what the app should do​​. It’s especially helpful for larger projects that can’t be built in one or two prompts. Think of it as seeding the AI with the same understanding you have in your head.

Lastly, maintain the Knowledge Base as your project evolves. If you add a major feature or change the scope, update the PRD/Knowledge Base document. This way, future prompts will consider the new information. It’s much easier than re-explaining context every time. In essence, the Knowledge Base \+ PRD is your AI project handbook – it keeps everyone (you and the AI) on the same page about what you’re building and how.