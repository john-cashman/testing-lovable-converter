---
title: "Debugging Prompts"
description: "Debug workflows, with strategies, sample prompts, troubleshooting flows, and deep debugging mindset examples."
icon: "bug"
---

Building with AI is fast and fun – until something goes wrong. Errors, unexpected behaviors, or “the AI did something weird” moments are part of the process. This guide will help you navigate **AI-based debugging workflows in Lovable**. We’ll cover how to quickly fix simple issues, strategies for tougher bugs, using Lovable’s chat for debugging, and even prompt recipes to systematically squash bugs. Debugging with an AI assistant is a new skill, but with structure and the right prompts, you can resolve problems efficiently and even turn them into learning opportunities. 

## Advanced Debugging Prompts

Sometimes you need a heavy-duty prompt to dig into a problem or review your project’s health. Here are some structured prompt examples for deep debugging or optimization scenarios. These can be used in Chat mode to get a thorough analysis without immediately changing code.

### Full System Review (Codebase Audit)

If your project has grown large or you suspect there are structural issues, a full codebase audit prompt can be useful. This asks the AI to analyze the entire project for cleanliness, correct architecture, and any misplaced code. It’s like asking “Is everything organized the way it should be?”

**Example Prompt – Codebase Audit:**

```
Perform a comprehensive **audit of the entire codebase** to check if the architecture is clean, modular, and optimized:

- Identify any files, components, or logic that are in the wrong place or could be better organized. Are there any instances of code that don’t belong in their current file (misplaced logic)?
- Evaluate if we have a clear separation of concerns (e.g., data handling vs UI vs state management). Point out any overly coupled sections of code.
- Highlight any areas of the code that are overly complex or not following best practices.
- Provide a report with specific recommendations to improve structure and maintainability, **without making any code changes yet**. 

Break down the suggestions into an ordered list of steps we could take, from most critical to optional enhancements.

*(This is a read-only analysis; do not modify the code during this audit.)*
```

This prompt is long, but it directs the AI to act like a code reviewer or architect. We’ve asked it to find mislocated code, check modularity, and even prioritize the fixes​. The AI might respond with something like:

- \_“1. **__Separate API calls from components:__** The \_`ProjectList`_component is directly fetching data. Suggestion: move data fetching to a dedicated hook or context to keep components pure UI.​_

1. **Reduce coupling in Task logic:** The task completion toggle is updating both state and directly writing to localStorage. This should be refactored to have a single source of truth.​
2. **Organize utility functions:** There are utility functions in `App.tsx` that would be better placed in a `utils` folder (e.g., date formatting functions).
3. ...”\*

Each point might come with explanation and maybe references to specific files. Such a report helps you see the forest for the trees. It’s especially useful if you’ve been focusing on one feature at a time and haven’t looked at the overall structure in a while.

After getting this output, you can decide which refactoring tasks to tackle (maybe even prompt the AI to implement some of those recommendations one by one).

### Safe Approach for Fragile Updates

When you know the area you’re changing is delicate (maybe a complex authentication flow or a core algorithm), it’s wise to prepend a _cautionary guideline_ in your prompt. This doesn’t find bugs per se, but it helps prevent them by telling the AI to be extra careful. We saw an example in the Prompt Library section for locking files. Here’s a similar pattern focusing on not breaking things.

**Example Prompt – Fragile Update Guidance:**

```
The next change is in a **critical part of the app**, so proceed with **utmost caution**. 

- Carefully examine all related code and dependencies *before* making changes.
- **Avoid any modifications** to unrelated components or files.
- If there’s any uncertainty, pause and explain your thought process before continuing.
- Ensure thorough testing after the change to confirm nothing else is affected.

**Task:** Update the user authentication logic to support OAuth login via Google, on top of existing email/password without breaking either flow.

*(Be extremely careful and double-check each step during implementation.)*
```

By including the italicized guidelines and bold warnings, you’re basically setting the AI’s “mindset” to be cautious​. The AI might then take a more measured approach, e.g., first explaining what it will do, or implementing the OAuth addition while explicitly noting that it left the email/password intact. This prompt doesn’t output a solution immediately; rather, it influences _how_ the AI will perform the task to minimize introducing new bugs.

This strategy is useful for **fragile sections**: authentication, payment processing, data migration – anything where a small mistake can break a lot. It’s a preemptive debugging measure.

### Performance Optimization Check

If your app works correctly but is **slow** or resource-heavy, you can use a prompt to have the AI analyze performance. This might involve reviewing data fetching patterns, looking at rendering inefficiencies, or suggesting optimizations (caching, memoization, etc.). It’s like asking, “How can we make this faster and smoother?”

**Example Prompt – Performance Audit:**

```
Our app is functional but seems **sluggish**. Please **analyze the project for performance bottlenecks** and suggest optimizations:

- Check for any unnecessary database or network calls (e.g., duplicate fetches or N+1 query patterns).
- Identify components that might be re-rendering too often or doing heavy work on the main thread.
- Look at our use of assets (images, scripts): are there any large bundles or unoptimized assets affecting load time?
- Suggest improvements like caching frequently used data, using React memo or lazy loading where appropriate, and any other ways to speed up the app.

Provide the analysis and recommendations in a list. Do not make code changes yet – just tell us what to improve for better performance.
```

Running this in Chat mode will give you a diagnostic report. The AI might say for example:

- _“Data fetching:_ The `ProjectList` component fetches data on every render. This could be improved by caching or moving the fetch to a higher context so it doesn’t repeat unnecessarily​. Consider using a state or context to store projects once fetched.
- _Re-renders:_ The `TaskItem` component is not memoized and re-renders every time any parent state changes. If we have many tasks, this can slow down interactions. Suggestion: use `React.memo` for `TaskItem` to prevent needless re-renders​.
- _Assets:_ Noticed an image (logo) that is 2MB. That’s quite large; compress or use a smaller resolution for faster loading.
- _Bundle size:_ All pages are in one bundle. Consider code-splitting (dynamic `import()` for large modules) so initial load is faster.
- ...”\*

Each suggestion comes from common performance best practices​. You can then decide which ones to implement. Maybe you prompt Lovable to apply one of them: _“Implement caching for project data using context as suggested.”_ By addressing these, you improve user experience and possibly reduce costs (fewer calls, less computation).

### Handling Persistent Errors

What about errors that just won’t go away or keep coming back in slight variations? This can happen if the root cause isn’t addressed. For example, you fix one thing, but the underlying problem surfaces as a new error elsewhere. Here’s a strategy for that:

- **Ask the AI what it has tried already.** Sometimes after a few “Try to Fix” attempts or manual prompts, it’s unclear what’s been changed. Use: \_“What solutions have we tried so far for this error?”\_​. The AI can list the attempts, which helps you avoid repeating the same fixes.
- **Have the AI explain the error in simple terms.** _“Explain in simple terms why this error occurs.”_ This can reveal if the AI (and you) truly understand it. You might catch a misconception here.
- **Consider an alternate approach.** Ask: \_“Given this error keeps happening, can we try a different approach to achieve the goal?”\_​. The AI might suggest a different implementation strategy that bypasses the problematic area.
- **Revert and replay.** In worst-case scenarios, you might roll back a few steps (Lovable lets you restore older versions). Then proceed with smaller changes. You can even tell the AI: _“We’re going to undo the last changes and try a more incremental approach.”_ This resets the context a bit and often avoids the rut you were in.

Finally, if a specific component is “dead” (not working at all, no matter what), isolate it. Create a fresh minimal version of that component via prompt to see if it works, then slowly integrate it back into your project. This is akin to turning things off and on again, but with code – sometimes starting fresh on a piece is easier than trying to patch an overly broken one.

Throughout all this, maintain a dialogue with the AI. Treat it like a collaborator: _“We fixed X but now Y is acting up. What’s the relationship between X and Y? Could the fix have caused Y’s issue?”_ The AI might make connections you didn’t see.

## Sample Debugging Flows

To cement these ideas, let’s walk through two common debugging scenarios with example flows:

### The “stuck in error loop."

You prompted something complex, and now the app won’t build, and Try to Fix failed twice.

_Flow:_ 

  
  
  
  
  
  
  
</Steps>

Throughout, you specifically described the error and had the AI confirm its understanding, rather than just blindly hitting fix repeatedly.

### The “feature not working right.”

You added a notification feature, but emails aren’t sending.

_Flow:_ 

  
  
  
  
  
</Steps>

Essentially, by describing what you expect (an email) and what happened (nothing, with a log snippet), the AI was able to guide the investigation.

### The “UI element disappeared.”

You refactored something and now a whole section of the UI is just gone (a “dead component”).

_Flow:_

  
  
  
</Steps>

In this flow, the key was to notice the component was completely gone and communicate that. The AI helped pinpoint _why_ (not rendered vs rendered but empty, etc.).

In all these cases, _communication and incremental steps_ are your friends. Use the AI’s strength in recalling details (like what it did before) and analyzing logs or errors. And use your strength in steering the process – you understand the high-level goal and can decide when to try a different angle.

## Root Cause Analysis, Rollback, and Progressive Enhancement

A few final pieces of advice:

### Root Cause vs. Symptom

Always ask “why did this happen?” not just “what to do now?”. The AI can help find the root cause so that when you fix something, it stays fixed. For example, an AI quick fix might silence an error but not address the underlying logic bug. If you suspect that, dig deeper:

This leads to more robust solutions.

### **Rollback wisely:**

Lovable allows you to roll back to previous versions. Don’t hesitate to use that if the code has become too tangled by a series of bad fixes. It’s often faster to rewind and try a different approach. If you do rollback, let the AI know what you’re doing (so it doesn’t get confused by code that suddenly looks different). For instance:

This way, the AI has context that we undid some changes and are taking another shot.

### **Progressive enhancement:**

When adding new features (especially complex ones), build them in small, testable increments. This isn’t just a prompting tip – it’s a development philosophy that pairs well with AI. If something breaks, you know exactly which small step caused it. Prompt by prompt, you enhance the app, which also means prompt by prompt you can debug in isolation. If you ever find yourself writing a paragraph-long prompt with multiple feature changes at once, consider splitting it into multiple prompts. You’ll thank yourself later when troubleshooting is needed.

### **Document as you go:**

It’s helpful to keep notes (or even ask the AI to summarize what was done after a session). This is similar to the reverse meta prompting – it creates a history of fixes. E.g., after resolving a tough bug, you might prompt:

The AI’s summary can be saved in a `README` or log. This is great for future you, or anyone else on the project, to understand what happened.

### **Know when to ask for human help:**

Sometimes, despite all efforts, you might hit a wall (maybe a true bug in the Lovable platform or something outside your/AI control). The Lovable community and support are there for you. There’s no shame in reaching out on their Discord or forums with a question. Often, others have faced a similar issue. Use the AI to gather as much info as possible first (so you can provide details), and then ask the community if needed.

## Community Debugging Guidebook

This guidebook was shared in our community Discord—it might be useful for debugging your project:

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
</AccordionGroup>