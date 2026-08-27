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

## Essential CSS Terminology & Rulesets:
    **Rule Set: Consists of a selector followed by a declaration block inside {}.

    **Selector: Designates which HTML element(s) to target.

    **Declaration: Property and value pair separated by a colon and ended with a semicolon (color: orange;).

    **Selector Hierarchy:
        **Type Selector (e.g., div): Targets all elements of a specific HTML type.

        **Class Selector (e.g., .awesome): Targets groups of elements using the class attribute. Reusable.

        **ID Selector (e.g., #header): Targets a single, unique element per page using the id attribute.

## Project Organization & Linking
    **External stylesheets are linked inside the <head> using <link rel="stylesheet" href="path/to/file.css">.

    **CSS Reset: A stylesheet technique used to reduce browser inconsistencies by neutralizing default browser margins, padding, and font sizes.
Source: Shay Howe — Learn to Code HTML & CSS (Lesson 1)


## 📖 Shay Howe: Lesson 2 Notes — Getting to Know HTML

### Block vs. Inline Element Rules
- **Block-Level:** Begins on a new line, stacks vertically, and occupies the full available width. Can contain other block elements or inline elements.
- **Inline-Level:** Stays in normal document flow without breaking onto a new line, occupying only its content's width. Can wrap other inline elements, **cannot** wrap block-level elements.

### Text-Formatting Semantics: Importance vs. Style
- **`<strong>` vs `<b>`:**
  - `<strong>`: Represents *strong importance* or urgency (preferred semantic tag for bolding).
  - `<b>`: Represents *stylistically offset* text without adding semantic importance.
- **`<em>` vs `<i>`:**
  - `<em>`: Represents *stressed emphasis* (preferred semantic tag for italics).
  - `<i>`: Represents text in an *alternative voice, tone, or technical term*.

### Document Structural & Layout Tags
- **`<header>`:** Used inside the `<body>` for introductory content, page headers, or section headings (not to be confused with the metadata `<head>` tag)[cite: 2].
- **`<nav>`:** Contains major primary navigation links (e.g., site-wide menus, tables of contents)[cite: 2].
- **`<article>` vs `<section>`:** Used for document outlining; use `<div>` if grouping strictly for CSS styling[cite: 2].
- **`<aside>`:** Holds tangentially related content outside the main flow, such as sidebars, author bios, or callout boxes[cite: 2].

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lesson 2)](https://learn.shayhowe.com/html-css/getting-to-know-html/)*[cite: 2]

## 📖 Shay Howe: Lesson 3 Notes — Getting to Know CSS

### The Cascade & Specificity
- **The Cascade:** CSS rules read and execute from top to bottom. If two competing rules have equal specificity, the rule declared lowest in the stylesheet wins.
- **Inheritance:** Certain properties (like `color` and `font-family`) applied to a parent element cascade down to its child elements automatically.
- **Specificity Hierarchy:** Determines which rule wins when selectors compete:
  1. Inline styles (highest specificity)
  2. ID selectors (`#header`)
  3. Class, pseudo-class, and attribute selectors (`.btn`, `:hover`)
  4. Type/element selectors (`p`, `div`) (lowest specificity)

### Properties & Values
- **Colors:** Can be defined via keywords (`red`), Hex codes (`#ffffff`), RGB (`rgb(255, 0, 0)`), or HSL (`hsl(0, 100%, 50%)`).
- **Units of Measurement:**
  - *Absolute Units:* `px` (pixels) — fixed sizing that does not alter based on other elements.
  - *Relative Units:* `em` (relative to parent font size), `rem` (relative to root `<html>` font size), `%` (percentage of parent container).

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lesson 3)](https://learn.shayhowe.com/html-css/getting-to-know-css/)*


## 📖 Shay Howe: Lesson 4 Notes — Opening the Box Model

### The Box Model Anatomy
Every element on a web page is rendered as a rectangular box consisting of four distinct layers (from inside out):
1. **Content:** The core text, image, or media. Dimensions set by `width` and `height`.
2. **Padding:** Transparent spacing clearing the area around the content, inside the border. Inherits element background.
3. **Border:** Wraps around the padding and content (`border: 1px solid black;`).
4. **Margin:** Transparent spacing clearing an area outside the border, separating the element from neighbors.

### Box Sizing: `content-box` vs. `border-box`
- **Default (`box-sizing: content-box`):** `width` and `height` only apply to the content. Adding padding or borders increases the total rendered size of the element on screen:
  - *Total Rendered Width* = `width` + `padding-left` + `padding-right` + `border-left` + `border-right` + `margin-left` + `margin-right`
- **Modern Standard (`box-sizing: border-box`):** `width` and `height` encompass content, padding, and borders. Padding and borders are absorbed inward, keeping the declared box dimensions exact:
  - *Total Rendered Width* = `width` + `margin-left` + `margin-right`

### Margin & Padding Shorthand
- **4 Values:** `margin: 10px 20px 15px 5px;` (Top, Right, Bottom, Left — Clockwise)
- **2 Values:** `margin: 10px 20px;` (Top/Bottom, Left/Right)
- **Margin Auto:** `margin: 0 auto;` horizontally centers a block-level element with a declared width.

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lesson 4)](https://learn.shayhowe.com/html-css/opening-the-box-model/)*


## 📖 Shay Howe: Lesson 5 Notes — Positioning Content

### Floating Elements (`float`)
- **Purpose:** Originally designed to wrap text around images, `float` became the primary early layout tool to place block-level elements side-by-side horizontally.
- **Values:** `float: left;` or `float: right;`.
- **Behavior:** Removes an element from the normal document flow and shifts it to the left or right of its parent container until it touches the container edge or another floated element.

### Multi-Column Layouts with Floats
- To create 2-column or 3-column layouts, assign explicit percentage or pixel widths to each column and apply `float: left;` to all columns.
- Ensure total column widths, padding, margins, and borders do not exceed 100% of the parent width (or elements will wrap to the next line). Use `box-sizing: border-box;` to prevent width calculation overflows.

### Containing Floats & Collapsing Parents (The "Clearfix")
- **The Problem (Parent Collapse):** When all child elements inside a container are floated, they are removed from the normal flow, causing the parent container's height to collapse to `0px`.
- **Clearing Floats (`clear` property):**
  - Values: `clear: left;`, `clear: right;`, `clear: both;`.
  - Applied to an element placed *after* floated elements to prevent content from wrapping around them and push it below.
- **Modern Clearfix Technique:** Applying a pseudo-element rule to the parent container so it expands to encompass its floated children automatically:
```css
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}


## 📖 Shay Howe: Lesson 6 Notes — Working with Typography

### Core Text Styling Properties
- **`color`:** Defines text color using keywords, Hex, RGB, or HSL.
- **`font-family`:** Declares font choices using a **font stack** (e.g., `font-family: "Helvetica Neue", Arial, sans-serif;`). The browser uses the first available font on the user's system, falling back to a generic family (`sans-serif`, `serif`, `monospace`).
- **`font-size`:** Sets the size of the font using absolute units (`px`) or relative units (`rem`, `em`, `%`).
- **`font-style`:** Controls font slant (`normal`, `italic`, `oblique`).
- **`font-weight`:** Sets stroke thickness using keywords (`normal`, `bold`) or numeric values (`100` to `900`, where `400` is normal and `700` is bold).
- **`font-variant`:** Used primarily for stylistic variants like small caps (`font-variant: small-caps;`).

### Text Layout & Spacing Properties
- **`line-height`:** Sets the vertical space between lines of text (leading). Unitless values (e.g., `line-height: 1.5;`) are preferred because they scale proportionally with `font-size`.
- **`text-align`:** Aligns text within its container (`left`, `right`, `center`, `justify`).
- **`text-decoration`:** Adds or removes text decorations (`underline`, `line-through`, `none` — commonly used to remove default hyperlink underlines).
- **`letter-spacing`:** Adjusts the tracking (space between individual characters).
- **`word-spacing`:** Adjusts the space between whole words.
- **`text-transform`:** Manages capitalization dynamically without altering HTML source (`uppercase`, `lowercase`, `capitalize`).

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lesson 6)](https://learn.shayhowe.com/html-css/working-with-typography/)*


## 📖 Shay Howe: Lesson 7 Notes — Setting Backgrounds & Gradients

### Background Colors & Images
- **`background-color`:** Sets a solid background color using keywords, Hex, RGB, HSL, or RGBA/HSLA (for opacity/transparency via alpha channel).
- **`background-image`:** Applies an image using the `url()` functional notation:
  ```css
  background-image: url("images/pattern.png");


	Image Controls:
⚬	background-repeat: Controls tiling (no-repeat, repeat-x, repeat-y, repeat).
⚬	background-position: Sets placement (top left, center, 50% 50%, 10px 20px).
⚬	background-size: Adjusts scaling (auto, cover, contain, explicit dimensions).
⚬	Multiple Background Images: Layer multiple images by separating declarations with commas (the first listed image sits closest to the viewer on top).
Gradient Backgrounds
⚬	Nature of Gradients: Gradients are treated as images in CSS and are declared using the background-image property.
⚬	Linear Gradients (linear-gradient()):
⚬	Syntax: background-image: linear-gradient(direction, color-stop-1, color-stop-2, ...);
⚬	Directions: Keywords (to right, to bottom right) or angles (90deg, 180deg).
⚬	Color Stops: Define where colors transition along the gradient line (e.g., linear-gradient(to right, red 20%, blue 80%)).
⚬	Radial Gradients (radial-gradient()): Transition colors outward from a central point.
* Source: Shay Howe — Learn to Code HTML & CSS (Lesson 7)

## 📖 Shay Howe: Lesson 8 Notes — Creating Lists

### HTML List Types & Attributes
- **Unordered Lists (`<ul>`):** For collections where order does not matter (renders bullet points by default).
- **Ordered Lists (`<ol>`):** For sequential collections (renders numbers by default).
  - `reversed`: Boolean attribute that reverses the numbering count from highest to lowest.
  - `start`: Sets the starting integer for the list (e.g., `start="5"`).
  - `value`: Attribute placed directly on an individual `<li>` to manually override its specific numeric position.
- **Description Lists (`<dl>`):** Used for key/value pairs, glossaries, or metadata pairings:
  - `<dt>`: Description Term (the name/concept).
  - `<dd>`: Description Details (the definition or value).

### Nested Lists
- Lists placed inside another list must be nested **inside** an `<li>` element, not directly inside the parent `<ul>` or `<ol>`.

### CSS List Styling
- **`list-style-type`:** Controls marker type (`disc`, `circle`, `square`, `decimal`, `none` — commonly used to reset navigation menus).
- **`list-style-position`:** Places markers `inside` or `outside` the list item content flow.
- **`list-style-image`:** Replaces standard bullets with custom image assets using `url()`.
- **Horizontal Lists for Navigation:** Setting `display: inline;` or `display: inline-block;` (or Flexbox) on `<li>` elements to convert vertical lists into horizontal navbars.

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lesson 8)](https://learn.shayhowe.com/html-css/creating-lists/)*



## 📖 Shay Howe: Lesson 9 Notes — Adding Media

### Images (`<img>`)
- Replaced inline element requiring `src` and accessible `alt` attributes.
- Native sizing via `width` and `height` attributes helps prevent layout shifts while the page loads.

### Audio & Video (`<audio>` & `<video>`)
- Native HTML5 multimedia containers using `src` or nested `<source>` tags for multi-format fallback (e.g., MP4, WebM).
- **Core Attributes:**
  - `controls`: Displays native play/pause/volume browser controls.
  - `autoplay`: Starts media automatically (often requires `muted` to work in modern browsers).
  - `loop`: Plays media continuously in a loop.
  - `poster` (video only): Specifies an image placeholder shown before the video plays.

### Figures & Captions
- `<figure>`: Encapsulates media (images, diagrams, code snippets) referenced in the main text.
- `<figcaption>`: Provides a semantic caption directly associated with the parent `<figure>`.

---

## 📖 Shay Howe: Lesson 10 Notes — Building Forms

### Form Basics & Submission
- `<form action="url" method="GET|POST">`: The wrapper for data collection.
  - `action`: Destination endpoint where data is sent.
  - `method`: HTTP transfer protocol (`GET` appends parameters to URL; `POST` sends payload in request body).

### Essential Input Controls & Elements
- `<input>`: Self-closing element controlled via the `type` attribute (`text`, `email`, `password`, `number`, `checkbox`, `radio`, `submit`, `hidden`).
- `<label for="id">`: Associates descriptive text with an input via matching `id` for accessibility and hit-area expansion.
- `<textarea>`: Multi-line text input (requires closing tag `</textarea>`).
- `<select>` & `<option>`: Dropdown menus.
- `<fieldset>` & `<legend>`: Groups related form controls and provides a caption.

### Essential Form Attributes
- `name`: Key sent in the form submission key-value pair (e.g., `name="username"` $\rightarrow$ `username=Steven`).
- `value`: Initial default content or specific submitted value.
- `placeholder`: Brief temporary hint displayed when input is empty.
- `required`: Prevents submission if the field is empty.
- `disabled`: Prevents interaction and excludes the field from form submission.

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lessons 9 & 10)](https://learn.shayhowe.com/html-css/)*


## 📖 Shay Howe: Lesson 11 Notes — Making Tables

### Semantic Table Structure
- `<table>`: The wrapper container for all tabular data.
- `<thead>`, `<tbody>`, `<tfoot>`: Structural semantic wrappers separating the table header, body data, and footer summaries.
- `<tr>`: Table row.
- `<th>`: Table header cell (bold/centered by default; screen-reader accessible via `scope="col"` or `scope="row"`).
- `<td>`: Table data cell.

### Advanced Table Attributes & CSS
- `colspan`: Expands a cell across multiple columns horizontally.
- `rowspan`: Expands a cell across multiple rows vertically.
- `border-collapse: collapse;`: Merges adjacent cell borders into a clean single line instead of standard double borders.

---

## 📖 Shay Howe: Lesson 12 Notes — Writing Best Practice Code

### Architecture & Maintainability
- **HTML Standards:** Use semantic tags, enforce lowercase tag/attribute names, self-close void elements cleanly, and write accessible `alt` tags.
- **CSS Standards:** Organize stylesheets logically (Reset/Normalize $\rightarrow$ Typography $\rightarrow$ Layout $\rightarrow$ Components), use meaningful class names over rigid IDs, and minimize selector specificity.
- **Code Comments:** Use `<!-- HTML comments -->` and `/* CSS comments */` to demarcate major layout sections.

---
*Source: [Shay Howe — Learn to Code HTML & CSS (Lessons 11 & 12)](https://learn.shayhowe.com/html-css/)*




# Anki Flashcards created from this class:

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

   ## Todays 5 Anki Flashcards (Lesson 2 Focused)

1. Front: What is the rule regarding nesting block-level elements inside inline-level elements?
Back: Inline-level elements cannot wrap block-level elements; they can only wrap other inline elements.

2. Front: What is the semantic difference between <strong> and <b>?
Back: <strong> indicates strong importance/urgency[cite: 2], while <b> is used strictly to stylistically offset text without adding importance.

3. Front: What is the semantic difference between <em> and <i>?
Back: <em> indicates stressed emphasis[cite: 2], while <i> represents text spoken in an alternative voice, tone, or technical term[cite: 2].

4. Front: What is the primary semantic purpose of the <aside> element?
Back: It holds tangentially related content separate from the main flow, such as sidebars, author details, or callout boxes.

5. Front: When should you use a <div> instead of structural semantic tags like <article> or <section>?
Back: Use a <div> when content is being grouped purely for CSS styling or layout purposes, without adding meaning to the document outline.

  ## 🗂️ Additional Flashcards Log (Saturday Review)
1. Front: What is the difference between a relative URL and an absolute URL when linking files/pages?
Back: An absolute URL contains the complete internet address (e.g., [https://example.com/page](https://example.com/page)), while a relative URL points to a file within the same website/directory structure (e.g., assets/stylesheets/main.css).

2. Front: What is the primary purpose of the HTML <main> tag?
Back: It specifies the dominant, unique content of the body of a document. A page should only contain one element, excluding repeating content like sidebars, navbars, footer.

3. Front: What does the <time> tag do, and why use its datetime attribute?
Back: It represents a specific period in time or date. The datetime attribute formats the date in a machine-readable format for search engines and calendar apps.

4. Front: What is the purpose of the <meta charset="UTF-8"> tag insde the head tag?
Back: It tells the browser which character encoding standard to use (UTF-8), ensuring almost all human languages and special characters display correctly without breaking. 

5. Front: In basic CSS terminology, what is the difference between a property and a value?
Back: A property is the style feature being modified (color, font, etc), while a value is the specific setting applied to the property (orange, 16px, etc). 


## Additional flashcard log (Monday)
1. Front: What is "The Cascade" in CSS?
Back: The process by which CSS applies styles from top to bottom. When conflicting declaration have equal specificity, the rule appearing lowest in te document or stylesheet takes precedence.

2. Front: What is the basic order of CSS specifity from lowest to highest?
Back: Type/element selectors -> class/attribute selectors -> ID selectors -> Inline styles.

3. Front: In CSS, what is the difference between em and rem relative units?
Back: em is relative to the font-size of its direct parent element, while rem (root em) is relative to the font-size of the root element. 

4. Name the four layers of the CSS Box Model from innermost to outermost?
Content-> Padding->Border->Margin.

5. What is the difference between CSS Padding and CSS Margin?
Padding creates space inside the border (surrouding the content and showing the background color), while Margin creates empty space outside the border (pushing other elements away).

6. How does box-sizing: border-box change standard CSS width calculation compared to box-sizing: content box?
In border-box, declared width includes padding and borders (they push inward), whereas defalut content-box adds padding and borders onto the declared width, expanding the total size.

7. How does the four-value CSS shorthand poprerty apply values (e.g., padding: 10px 20px 15px 5px;)?
It applies clockwise: top, right, bottom, left (TRBL/"Trouble").

8. What is required to horizontally center a block-level element using margin: 0 auto;?
The element must have an explicity defined width (otherwise it occupies 100% width and cannot center). 


***

### 2.  CSS Anki Flashcards

1. **Front:** What happens to an element when you apply `float: left` or `float: right` to it?
   **Back:** It is taken out of normal document flow and pushed to the far left or right of its parent container, allowing text and inline elements to wrap around it.

2. **Front:** Why does a parent container's height collapse to 0 when all of its child elements are floated?
   **Back:** Floated elements are removed from normal document flow, so the parent container cannot calculate their height and collapses unless floats are cleared or contained.

3. **Front:** What does the CSS property `clear: both;` do?
   **Back:** It forces an element to move down below any preceding floated elements on both the left and right, rather than wrapping alongside them.

4. **Front:** What is a "Clearfix" in CSS?
   **Back:** A CSS technique (often using a `::after` pseudo-element with `clear: both;`) applied to a parent element so it dynamically expands to contain its floated children.

5. What is a "font stack" in CSS and why is it used?
A prioritized list of fallback font families declared in front-family (ending in a generic family like sans-serif) so the browser has backups if a primary font is not installed on the user's system.

6. Why is using untless value for line-height (ex. line-height: 1.5;) considered best practice?
Unitless values act as proportional multiplieris that automatically scale based on the element's (or its children's) font-size, preventing overlapping text when font sizes change.

7. What is the difference beteen letter-spacing and word-spacing in CSS?
Letter-spacing controls the spacing between individual characters (tracking), while word-spacing controls the space between words.

8. What CSS property is used to remove the default underline from HTML hyperlinks (tags)?
text-decoration: none;

9. What does text-transform: capitalize; do to text?
It transforms the first character of each word to uppercase without altering the underlying HTML text. 


***

### 2. High-Yield CSS Anki Flashcards

1. **Front:** In CSS, which property is used to apply a linear gradient, and why?
   **Back:** The `background-image` (or shorthand `background`) property, because CSS gradients are programmatically generated and treated as image assets by the browser engine.

2. **Front:** In the CSS `linear-gradient()` function, what is the default direction if none is explicitly declared?
   **Back:** From top to bottom (`to bottom` or `180deg`).

3. **Front:** What is the difference between `background-size: cover` and `background-size: contain`?
   **Back:** `cover` scales the image to completely fill the entire container (some cropping may occur), while `contain` scales the image to fit entirely inside the container without any cropping.

4. **Front:** When declaring multiple background images in CSS, which image is rendered in the front layer?
   **Back:** The first image listed in the comma-separated declaration renders on top (closest to the viewer).

***

1. What are the 3 core elements that make up an HTML Description List?
Description list wrapper <dl>, Description Term <dt>, Description Details <dd>

What does the reversed attribute do on an <ol> element?
It reverses the numbering of the ordered list items so they count downward instead of upward.

What is the correct HTML syntax rule when nesting a sub-list inside a parent list? 
The sub list (<ul> or <ol>) must be nested directly inside an individual <li> element of the parent list.

What CSS declarion is used on list to completely remove default bullet points or numbering?
list-style-type: none; (or shorthand list-style: none;)

Why is it best practice to use nested <source> tags inside <video> instead of a single src attribute?
It allows developers to provide multiple video formats. The broswer scans top to bottom and plays the first format its engine supports.

What is the semantic difference between wrapping an image in <figure> with <figcaption> versus a standard <p> tag?
  <figure> semantically isolates self-contained media referenced in the text, and <figcaption> explicitly associated the descriptive text with that exact media asset for screen readers and search engines.

    What is the primary difference between method="GET" and method ="POST" in an HTML form?
    GET appends form data directly to the URL query string, while POST transmits the data inside the HTTP request body. 

    Why must an HTML <input> element have a name attribute?
    The name attribute acts as the key in the key-value pair sent to the server when the form is submitted. Without name, the inputs value is ignored. 

    In an HTML table, what is the purpose of the colspan and rowspan attributes?
    colspan spans a single cell across multiple horizontal columns, while rowspan spans a cell across multiple vertical rows.

    What CSS property removes the defalut space between table cell borders and merges them into a single line?
    border-collapse; collapse;

    What is the semantic role of <thead>, <tbody> and <tfoot> in HTML tables?
      They group table roqs in logical secions (header labels, body data, and summary caluclations/footers), improving accessibility and multi-page print rendering. 

      

