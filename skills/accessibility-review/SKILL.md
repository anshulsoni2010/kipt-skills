---
name: accessibility-review
description: Reviews UI code such as React, Vue or HTML components for
  accessibility problems against WCAG basics, with fixes. Use when the user
  asks for an accessibility or a11y review, or to check a component, form
  or page for screen reader and keyboard support.
---

# Accessibility review

Check the changed UI code for:

1. **Semantics**: buttons are button elements, links are a elements,
   headings are in order, lists use list elements.
2. **Names**: every input has a label, every icon-only button has an
   accessible name, images have useful alt text or empty alt if decorative.
3. **Keyboard**: everything clickable is reachable with Tab and works with
   Enter or Space. Focus is visible. Dialogs trap and return focus.
4. **Color**: text contrast meets 4.5:1 (3:1 for large text). Color is not
   the only way information is shown.
5. **Motion**: animations respect prefers-reduced-motion.
6. **Forms**: errors are announced and tied to their field.

For each issue give the file and line, who it affects, and the fix as a
code snippet.
