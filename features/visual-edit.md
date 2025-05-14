---
title: "Visual Edit"
description: "Tailwind-native visual controls for easy refinement."
icon: "computer-mouse"
---

Lovable brings programming into the hands of everyone. **Visual Edits** is our Figma-like interface that lets you visually update your app—directly on the canvas—while keeping full control over the underlying Tailwind code.

No prompts, no guessing. Just click, tweak, and ship.

## How to Use Visual Edit

<iframe width="100%" height="315" src="https://www.youtube.com/embed/b-O7Ew0Q2ig?si=qnEZvVf9PZ0prOZM" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen />

1. **Activate Visual Edit** from the editor toolbar or via shortcut.
2. **Hover \+ Click** on any element—text, images, buttons, layouts.
3. **Edit visually**:
   - Change text content
   - Adjust spacing and layout
   - Modify colors, fonts, sizes
   - Apply or override Tailwind classes
4. **Select parent elements** for structural or layout-level changes.
5. **Use AI prompts** for complex tasks—but only if you want to.
6. **Preview in real-time** before hitting save.

All updates are applied instantly—no rebuilds, no AI wait times, no code confusion.

## Why It Matters

Visual Edits shortens the feedback loop between **idea → UI update**:

- **No-code meets pro-level control**\
  Designers get pixel-perfect control, and devs get clean, maintainable code.
- **Faster iteration, zero frustration**\
  No more guessing how CSS will behave—see it live, tweak in real-time.
- **Hot Module Reloading**\
  Thanks to Vite-powered Dev Servers, saved edits refresh instantly—without page reloads.
- **Smarter Editing with AST**\
  Behind the scenes, your code is converted into an Abstract Syntax Tree (AST) right in the browser. This allows safe, precise updates—no fragile regex hacks.
- **Scalable Infrastructure**\
  Every Visual Edit runs on ephemeral, containerized cloud dev servers—4,000\+ of them—so your experience stays fast and consistent no matter your app’s complexity.
- **Tailwind-native**\
  Whether you're using presets or writing your own classes, edits are always valid Tailwind. No locked-in styles.

## Common Use Cases

- Change button colors or font weights on the fly.
- Resize and align layout elements visually.
- Rewrite CTA copy inline.
- Add Tailwind classes to fine-tune spacing, shadows, borders, and more.
- Preview edits across breakpoints and themes instantly.

## Under the Hood (for devs)

We built Visual Edits by moving the code layer closer to the visual layer:

- **Stable JSX Tagging**\
  Every generated component is tagged at compile-time using a custom Vite plugin, so edits map directly back to JSX source.
- **In-browser AST**\
  The full codebase is parsed into an interactive AST client-side using Babel & SWC. This enables live updates and custom class handling—all without waiting on servers.
- **Live Tailwind Generator**\
  Changes reflect immediately with our real-time Tailwind parser. You see the update before you save it.
- **Hot Module Replacement (HMR)**\
  When you do save, we generate clean JSX/TSX, compute diffs, and instantly trigger HMR to update the app.

## Built for Everyone

Whether you're:

- A **non-technical founder** making your product shine
- A **designer** refining spacing and hierarchy
- A **developer** polishing the details with real-time feedback

Visual Edits fits right into your workflow.

## Resources:

- [📼 Launch video](https://www.youtube.com/watch?v=3FrKcqDGfe0&t=11s)
- [📢 Feature launch: Introducing Visual Edits](https://lovable.dev/blog/introducing-visual-edits)
- [🔧 Technical deep-dive](https://x.com/emilahlback/status/1894488375517671795) by Emil Ahlbäck
- [🛠️ Engineering: How We Built Visual Edits](https://lovable.dev/blog/visual-edits)

## Final Notes

Visual Edits is part of our mission to bring the power of software creation to everyone—not just coders. It’s free, fast, and built to scale with your imagination.

[Try it out.](https://lovable.dev/) Tweak something. Fall in love with iteration again.