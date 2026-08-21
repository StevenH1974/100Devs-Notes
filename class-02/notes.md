Class 2 - foundational HTML concepts, semantics, and structure.

## 📖 Shay Howe: Lesson 1 Notes — Building Your First Web Page

### Core HTML Concepts & Vocabulary
- **HTML (HyperText Markup Language):** Gives web content structure and semantic meaning.
- **CSS (Cascading Style Sheets):** Presentation language used to style appearance (color, layout, sizing).
- **Elements vs. Attributes:** 
  - *Elements:* Designators defining page structure/objects (`<h1>`, `<p>`, `<a>`, `<div>`).
  - *Attributes:* Properties providing extra details (`id`, `class`, `src`, `href`).
- **Self-Closing Elements:** Void tags that do not require a closing tag (e.g., `<br>`, `<img>`, `<input>`, `<link>`, `<meta>`).

### HTML5 Boilerplate Structure
The minimal essential markup required for a valid HTML document:
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <title>Page Title</title>
    <link rel="stylesheet" href="assets/stylesheets/main.css">
  </head>
  <body>
    <h1>Heading</h1>
    <p>Content goes here.</p>
  </body>
</html>

Essential CSS Terminology & Rulesets:
    **Rule Set: Consists of a selector followed by a declaration block inside {}.

    **Selector: Designates which HTML element(s) to target.

    **Declaration: Property and value pair separated by a colon and ended with a semicolon (color: orange;).

    **Selector Hierarchy:
        **Type Selector (e.g., div): Targets all elements of a specific HTML type.

        **Class Selector (e.g., .awesome): Targets groups of elements using the class attribute. Reusable.

        **ID Selector (e.g., #header): Targets a single, unique element per page using the id attribute.

Project Organization & Linking
    **External stylesheets are linked inside the <head> using <link rel="stylesheet" href="path/to/file.css">.

    **CSS Reset: A stylesheet technique used to reduce browser inconsistencies by neutralizing default browser margins, padding, and font sizes.
Source: Shay Howe — Learn to Code HTML & CSS (Lesson 1)






Anki Flashcards created from this class:

Front: What is the main structural difference between `<div>` and `<span>`?
`<div>` is a block-level generic container (takes up the full line width), while `<span>` is an inline generic container (only takes up as much width as its content).

Why use `<header>` or `<section> instead of using `<div>` everywhere?
`<header>` and `<section>` are semantic HTML tags that ive structural meanings to screen readers, search engines, and developers, whereas `<div>` carries no semantic meaning

In an `<a>` tag, what does the `<href>` attribute stand for and what is its purpose?
`<href>` stands for Hypertext Reference. It specifies the destination URL or file path that the link points to.

What are the heading tags in HTML, and how are they prioritized?
`<h1>` through `<h6>`, where `<h1>` represents the highest rank/most important heading and `<h6>` represents the lowest.

What is the primary purpose of the `<alt>` attribute on an `<img>` tag?
It provides alternative descriptive text for screen readers (accessibility) and displays as fallback text if the image fails to load.

***

### 2. Today's 5 Anki Flashcards (Lesson 1 Focused)

Here are 5 high-yield cards built directly from your notes covering CSS anatomy, selectors, and linking.

1. **Front:** What are the three main components of a CSS Rule Set?
   **Back:** A **selector** (targets the element), a **property** (what is being styled), and a **value** (how it is styled). Example: `p { color: orange; }`.

2. **Front:** How do you target an HTML class versus an HTML ID in CSS?
   **Back:** A class selector uses a leading period (`.classname`), while an ID selector uses a leading hash symbol (`#id-name`).

3. **Front:** What is the structural rule regarding the use of the `id` attribute on a web page?
   **Back:** An `id` value must be completely unique and can only be used **once** per HTML page.

4. **Front:** What HTML tag and attributes are used to link an external CSS file inside the `<head>`?
   **Back:** `<link rel="stylesheet" href="path/to/style.css">`

5. **Front:** What is the primary purpose of a "CSS Reset"?
   **Back:** It wipes out default browser styles (margins, padding, font defaults) so the web page renders consistently across all different browsers.