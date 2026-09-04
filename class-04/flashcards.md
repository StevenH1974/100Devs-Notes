# 🗂️ #100Devs — Class 04: Flashcards Log

## CSS Syntax & Architecture
1. **Front:** In CSS terminology, what is the difference between a declaration and a declaration block?
   **Back:** A declaration is a single property-value pair (e.g., `color: red;`), while a declaration block is the entire group of declarations enclosed inside curly braces `{ ... }`.

2. **Front:** What is a CSS Rule (or Ruleset)?
   **Back:** The combination of a selector and its declaration block.

3. **Front:** How does the CSS "Cascade" determine which style wins when two rules have identical specificity?
   **Back:** The declaration written lowest (most recently) in the stylesheet overrides the one declared above it.

4. **Front:** In `rgba(255, 0, 0, 0.5)`, what does the fourth parameter represent?
   **Back:** The Alpha channel, which controls opacity/transparency on a scale from `0` (completely transparent) to `1` (completely opaque).

5. **Front:** Why must you always include generic font fallbacks at the end of a `font-family` declaration?
   **Back:** To ensure the browser displays a readable default font (e.g., `sans-serif`, `serif`, or `monospace`) if the custom or system font fails to load.

## Selectors & Specificity
6. **Front:** What is the difference between `section p` and `section > p`?
   **Back:** `section p` selects every `<p>` element nested at any level inside the section (descendant), while `section > p` selects only `<p>` elements that are direct children.

7. **Front:** What does the adjacent sibling selector `h2 + p` do?
   **Back:** It targets only the `<p>` element that comes immediately after an `<h2>` element at the same nesting level.

8. **Front:** What is the standard CSS specificity hierarchy from lowest to highest priority?
   **Back:** 
   1. Element/type selectors
   2. Classes, attributes, and pseudo-classes
   3. IDs
   4. Inline styles

9. **Front:** Why should you avoid using `!important` in production stylesheets?
   **Back:** It breaks the natural cascade and specificity rules, making code difficult to override, maintain, and debug later.