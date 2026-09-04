# 🚀 #100Devs — Class 04: Intro to CSS

## 📌 Class Overview
- Introduction to Cascading Style Sheets (CSS), covering core syntax, the cascade, typography integration, relationship selectors, and the specificity hierarchy.

## 📝 Key Lecture Concepts
- **Separation of Concerns & Linking Styles:**
  - Keep CSS in a dedicated external file (e.g., `css/style.css`).
  - Linked in the `<head>` using `<link rel="stylesheet" href="css/style.css">`.
  - Inline CSS is avoided in modern development, with HTML email development being the main industry exception.
- **CSS Syntax Anatomy:**
  - **Rule / Ruleset:** The entire code block defining styles for a selector.
  - **Selector:** The targeted element(s) (e.g., `h1`, `.card`, `#hero`).
  - **Declaration Block:** Everything contained inside the curly braces `{ ... }`.
  - **Declaration:** A single property-value pair (e.g., `color: red;`).
- **The Cascade:**
  - CSS is read top-to-bottom.
  - If rules have equal specificity, the rule written furthest down in the stylesheet overrides earlier rules.
- **Color Systems in CSS:**
  - **Keywords:** Named colors (`red`, `blue`). Quick to test, but limits palette options.
  - **Hex Codes:** Six-character hexadecimal representation (`#FF0000`).
  - **RGB / RGBA:** `rgb(255, 0, 0)` or `rgba(255, 0, 0, 1)`. The `a` stands for Alpha (opacity/transparency from `0` to `1`).
  - **HSL / HSLA:** Hue, Saturation, Lightness, and Alpha. Popular among designers for intuitive color adjustments.
- **Typography & Font Fallbacks:**
  - Fonts are files loaded by the browser (commonly via Google Fonts CDN).
  - Link the font stylesheet in the `<head>` and declare the rules in your CSS.
  - **Font Stack:** Always provide fallbacks ending in a generic family (e.g., `font-family: 'Source Sans Pro', Helvetica, sans-serif;`).
- **Relationship Selectors:**
  - **Descendant (`A B`):** Targets any `B` nested anywhere inside `A` (`section p`).
  - **Direct Child (`A > B`):** Targets `B` only if it is an immediate child of `A` (`section > p`).
  - **Adjacent Sibling (`A + B`):** Targets `B` only if it directly follows sibling `A` (`p + p`).
- **Classes vs. IDs:**
  - **Classes (`.class-name`):** Reusable styles applied to multiple elements across a page.
  - **IDs (`#id-name`):** Unique identifiers that target exactly one element. Avoid using IDs for styling.
- **Specificity & `!important`:**
  - Resolves conflicts when multiple selectors target the same element.
  - Hierarchy (lowest to highest): Elements $\rightarrow$ Classes/Attributes $\rightarrow$ IDs $\rightarrow$ Inline styles.
  - `!important` overrides normal specificity and cascade rules. Avoid using it unless hotfixing an urgent bug with no other option.

## 💻 Class 04 Homework Assignments
- [ ] Build layout and styles: Simple Site lab (`homework/simple-site/`)
- [ ] Read Shay Howe: [Getting to Know CSS](https://learn.shayhowe.com/html-css/getting-to-know-css/)
- [ ] Read [Learn Layout](http://learnlayout.com/)