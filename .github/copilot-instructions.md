# GitHub Copilot Instructions

## Project Overview
This is a vanilla web application built with HTML, CSS, and JavaScript — no frameworks or libraries.

## Language & Stack
- HTML, CSS, and JavaScript only
- No external frameworks (no React, Vue, Angular, etc.)
- No build tools or transpilers unless explicitly introduced

## CSS Style
- Design mobile-first — write base styles for small screens, then use media queries to scale up
- Use flexbox
- Use relative units (rem, em, %) over fixed units (px) where possible
- Breakpoints should be consistent across the project (e.g. 480px, 768px, 1024px, 1280px)
- Avoid fixed widths and heights that would break at different screen sizes

## UI Design
- Aim for a clean, minimal aesthetic — avoid clutter, unnecessary decoration, and visual noise
- Use whitespace generously to give elements room to breathe
- Maintain consistent spacing and alignment throughout — use a spacing scale (e.g. multiples of 4px or 8px)
- Establish a clear typography hierarchy with distinct styles for headings, subheadings, and body text
- Use a limited, cohesive color palette — avoid introducing colors arbitrarily
- Ensure accessible color contrast that meets WCAG AA standards at minimum (4.5:1 for text)
- Interactive elements (buttons, links, inputs) should have clear, visible focus and hover states
- Keep the UI feeling intentional — every element should have a clear purpose

## SEO
- Always include a unique, descriptive <title> and <meta name="description"> on every page
- Add Open Graph tags (og:title, og:description, og:image) for social sharing previews
- Use semantic HTML elements (<header>, <main>, <nav>, <article>, <footer>) instead of generic <div> elements
- Use heading tags (h1–h6) in proper hierarchical order — only one <h1> per page
- Always include descriptive alt attributes on images
- Use descriptive, keyword-friendly image filenames (e.g. blue-running-shoes.jpg not img001.jpg)
- Lazy load images where appropriate (loading="lazy")
- Use descriptive anchor text for links rather than generic phrases like "click here"
- Ensure all internal links are crawlable (avoid JavaScript-only navigation where possible)

## Code Style

### Naming
- Use clear, descriptive, self-documenting names for variables, functions, and classes
- Avoid abbreviations unless they are universally understood (e.g. `id`, `url`)
- Boolean variables should read as questions: `isVisible`, `hasError`, `canSubmit`
- Functions should be named as actions: `fetchUserData()`, `renderCard()`, `validateForm()`

### DRY (Don't Repeat Yourself)
- Extract repeated logic into reusable functions
- Reuse existing utility functions rather than duplicating logic
- Group related functionality into modules or clearly separated sections

### Comments
- Avoid unnecessary comments — let the code speak for itself through meaningful naming
- Only add comments when explaining non-obvious logic or important decisions
- Do not add comments that simply restate what the code does

## Error Handling
- Always include error handling for any operation that could fail
- Use `try/catch` blocks for async operations and anything that may throw
- Provide meaningful, descriptive error messages that help diagnose the issue
- Handle edge cases explicitly (e.g. null/undefined checks, empty arrays, failed fetches)
- Never silently swallow errors — always log or surface them appropriately

## Testing
- Write tests for all new code
- Include both unit tests and integration tests
- Unit tests should cover individual functions and edge cases in isolation
- Integration tests should verify that components and modules work correctly together
- Tests should be easy to read and serve as living documentation of expected behavior

## General Guidelines
- Keep functions small and focused on a single responsibility
- Prefer readability over cleverness
- Be consistent with existing patterns in the codebase and if no patterns exist, use widely accepted best practices
- Avoid global variables where possible — prefer scoped or modular patterns