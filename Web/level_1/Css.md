# CSS: Cascading Style Sheets

CSS stands for Cascading Style Sheets. It's a language used to describe the presentation of a document written in HTML or XML. Think of HTML as the structure and content of your webpage, like the foundation and walls of a house. CSS is then used to style that content, like choosing the paint colors, furniture, and decorations.

## What CSS Does

Here's a breakdown of what CSS does:

* **Controls Visual Presentation:** CSS determines how elements on a webpage should look. This includes things like:
    * Colors of text and backgrounds
    * Fonts and their sizes
    * Spacing between elements (margins and padding)
    * Positioning and layout of elements
    * Borders and shadows
    * And much more!

* **Separates Content from Presentation:**  By using CSS, you keep the content (HTML) separate from how it looks (CSS). This makes your code cleaner, easier to maintain, and more flexible.

* **Improves Consistency:** You can define styles once and apply them across your entire website, ensuring a consistent look and feel.

* **Enables Responsive Design:** CSS allows you to create websites that adapt to different screen sizes and devices, providing an optimal viewing experience on desktops, tablets, and phones.


## Example

Let's say you have a simple HTML paragraph:

```html
<p>This is a paragraph of text.</p>
``` 
# Building Blocks of CSS

CSS (Cascading Style Sheets) is the language we use to style the visual presentation of HTML elements on web pages. Think of it as the makeup artist for websites, controlling aspects like colors, fonts, layout, and responsiveness.

**Key Building Blocks**

1. **Selectors:** These are the targeting mechanisms of CSS. They pinpoint the HTML elements you want to style. Selectors can identify elements based on:
    * Tag name (e.g., `p`, `h1`, `div`)
    * Class (e.g., `.highlight`, `.button`)
    * ID (e.g., `#main-content`, `#navigation`)
    * Attributes (e.g., `[type="submit"]`, `[href^="https"]`)
    * Relationships within the document structure (e.g., `ul li` for list items within unordered lists, `p > a` for links within paragraphs)

    ```css
    .highlight { color: red; } /* Selects all elements with the class "highlight" */
    ```

2. **Properties and Values:**
    * **Properties** are the styling features you want to change (e.g., `color`, `font-size`, `margin`).
    * **Values** are the specific settings applied to those properties (e.g., `blue`, `16px`, `10px`).

    ```css
    p {
      color: black; 
      font-size: 14px; 
      margin-top: 20px; 
    }
    ```

3. **Declarations and Declaration Blocks:**
    * A **declaration** is a property-value pair (e.g., `color: blue;`).
    * **Declarations** are grouped within curly braces `{}` to create a **declaration block**.

    ```css
    h1 {
      color: blue; 
      font-size: 36px; 
    }
    ```

4. **Rulesets:** A ruleset combines a selector and a declaration block to define the complete style for the selected elements.

    ```css
    p { /* Selector */
      color: black; /* Declaration */
      font-size: 14px; /* Declaration */
    } /* Declaration block */
    ```

5. **Cascade and Inheritance:**
    * **Cascade:**  This is the mechanism that resolves conflicts when multiple styles apply to the same element. It prioritizes styles based on importance, specificity, and source order.
    * **Inheritance:** Some CSS properties are passed down from parent elements to their children. For instance, if you set the `font-family` on a `<div>`, the text within nested elements (like `<p>` or `<h1>`) will usually inherit that font.

6. **Box Model:** This is a fundamental concept in CSS that treats every HTML element as a rectangular box with the following components:
    * **Content:** The actual text, images, or other media within the element.
    * **Padding:** The space between the content and the element's border.
    * **Border:** A line that can surround the padding and content.
    * **Margin:** The space outside the border, separating the element from adjacent elements.

7. **Units:** Units define the magnitude of CSS property values. Common units include:
    * **Pixels (px):** Fixed-size units.
    * **Percentages (%):** Relative to the parent element.
    * **Ems (em):** Relative to the element's font size.
    * **Rems (rem):** Relative to the root font size of the document.

By understanding these building blocks, you gain a solid foundation for creating effective, well-structured, and visually appealing styles for your web pages.


# CSS Selectors: Type, Class, and ID

In CSS, selectors are patterns used to select the element(s) you want to style. They act as the bridge between your CSS rules and the HTML elements they affect. Here's a breakdown of three fundamental selector types:

## 1. Type Selectors

*   **Target:** HTML elements based on their tag name.
*   **Syntax:** Simply use the tag name directly.
*   **Example:** `p { color: blue; }` - This will make all paragraph (`<p>`) elements on the page have blue text.

## 2. Class Selectors

*   **Target:** HTML elements based on the value of their `class` attribute. This allows you to style multiple elements with the same styles, even if they have different tag names.
*   **Syntax:** Use a period (`.`) followed by the class name.
*   **Example:** `.highlight { background-color: yellow; }` - This will give a yellow background to all elements with the attribute `class="highlight"` (e.g., `<p class="highlight">`, `<div class="highlight">`).

## 3. ID Selectors

*   **Target:** A single, unique element based on the value of its `id` attribute. IDs should be unique within an HTML document.
*   **Syntax:** Use a hash symbol (`#`) followed by the ID name.
*   **Example:** `#main-navigation { font-size: 1.2em; }` - This will increase the font size of the element with the attribute `id="main-navigation"` (e.g., `<nav id="main-navigation">`).

## Key Differences and When to Use

*   **Type selectors:** Broad, targeting all elements of a specific type. Ideal for general styling applied to every instance of an element.
*   **Class selectors:** More specific and reusable. Use them to style multiple elements consistently or create reusable styles.
*   **ID selectors:** The most specific, targeting only one unique element. Use them when you need to style a single, specific element on the page.

## Important Considerations

*   **Specificity:** You can combine these selectors for increased specificity (e.g., `div.container p` targets `<p>` elements within a `<div>` with class "container").
*   **Case-sensitivity:** Class and ID names are case-sensitive.
*   **Naming conventions:** Use descriptive names that reflect the element's purpose (e.g., "main-navigation" or "error-message") rather than generic names like "red" or "box."

By understanding these selector types, you can precisely target and style the elements you want to customize on your web pages.

# CSS Attribute Selectors

Attribute selectors in CSS provide a powerful way to target HTML elements based on their attributes and attribute values. This allows for very specific and flexible styling beyond what's possible with type, class, or ID selectors alone.

## Basic Syntax

Attribute selectors use square brackets `[]` to enclose the attribute you're targeting.

*   `[attribute]`: Selects all elements with the specified attribute, regardless of its value.
    *   Example: `a[href]` selects all `<a>` elements with an `href` attribute (all links).

## Selecting by Value

You can refine your selection by specifying the attribute's value:

*   `[attribute="value"]`: Selects elements where the attribute's value exactly matches the specified value.
    *   Example: `input[type="submit"]` selects all `<input>` elements with `type="submit"`.

## Substring Matching

CSS provides options for selecting attributes based on partial value matches:

*   `[attribute*="value"]`: Selects elements where the attribute value contains the specified substring.
    *   Example: `img[src*="logo"]` selects all `<img>` elements with "logo" anywhere in their `src` attribute.
*   `[attribute^="value"]`: Selects elements where the attribute value starts with the specified substring.
    *   Example: `a[href^="https"]` selects links where the `href` attribute begins with "https".
*   `[attribute$="value"]`: Selects elements where the attribute value ends with the specified substring.
    *   Example: `a[href$=".pdf"]` selects links where the `href` attribute ends with ".pdf".

## Other Useful Attribute Selectors

*   `[attribute~="value"]`: Selects elements where the attribute value is a space-separated list of words, and one of those words is the specified value. Useful for targeting elements with multiple classes.
    *   Example: `div[class~="highlight"]` selects all `<div>` elements with the class "highlight," even if they have other classes.
*   `[attribute|="value"]`:  Selects elements where the attribute value is exactly the specified value, or the specified value followed by a hyphen (-). Often used for language subcodes.
    *   Example: `[lang|="en"]` selects elements with `lang="en"` or `lang="en-US"`.

## Why Use Attribute Selectors?

*   **Specificity:** Target elements with laser precision.
*   **Flexibility:** Style elements without relying on classes or IDs.
*   **Maintainability:** Make your CSS less dependent on HTML structure changes.
*   **Dynamic Styling:** Style elements based on attributes that might change (e.g., form validation).

## Example Scenario

To style all external links differently from internal links:

```css
a[href^="http"] { 
  color: green; 
  text-decoration: underline;
}
```

# CSS Pseudo-classes and Pseudo-elements

Pseudo-classes and pseudo-elements are special selectors in CSS that allow you to style elements based on their state or add special effects to them. They extend the capabilities of regular selectors, providing more control over the appearance of your web pages.

## Pseudo-classes

*   **What they are:** Pseudo-classes select elements based on a specific state or condition. It's like dynamically applying a class to an element without changing the HTML.
*   **Syntax:** Keywords that start with a single colon (`:`).
*   **Examples:**
    *   `:hover`: Selects an element when the user hovers the mouse over it.
    *   `:active`: Selects an element when it is being activated (e.g., clicked).
    *   `:focus`: Selects an element when it has focus (e.g., a selected form field).
    *   `:first-child`: Selects the first child element of its parent.
    *   `:nth-child(n)`: Selects the nth child element of its parent.
    *   `:visited`: Selects links that the user has already visited.
    *   `:disabled`: Selects form elements that are disabled.

## Pseudo-elements

*   **What they are:** Pseudo-elements select a specific part of an element or create virtual elements not defined in the HTML.
*   **Syntax:** Keywords that start with a double colon (`::`).
*   **Examples:**
    *   `::before`: Inserts content before the content of an element.
    *   `::after`: Inserts content after the content of an element.
    *   `::first-letter`: Selects the first letter of an element.
    *   `::first-line`: Selects the first line of an element.
    *   `::selection`: Selects the portion of an element that is currently selected by the user.
    *   `::placeholder`: Selects the placeholder text in a form field.

## Key Differences

*   **State vs. Structure:** Pseudo-classes target elements based on their state (e.g., `:hover`), while pseudo-elements target specific parts of an element or generate content (e.g., `::before`).
*   **Single vs. Double Colon:** Though most browsers support both single and double colons, the double colon (`::`) is the modern standard for pseudo-elements to distinguish them from pseudo-classes.

## Use Cases

*   **Interactive Effects:** Use `:hover`, `:active`, and `:focus` to create visual feedback on user interactions (e.g., changing button colors on hover).
*   **Styling Specific Parts:** Use `::first-letter` or `::first-line` to style the first letter or line of text within an element.
*   **Adding Content:** Use `::before` and `::after` to add decorative elements (e.g., icons, quotation marks) or extra information without modifying the HTML.

## Example

```css
a:hover {
  text-decoration: underline;
}

p::first-letter {
  font-size: 2em;
  font-weight: bold;
}
```
# CSS Combinators

## Prerequisites

* Basic software installed (text editor, web browser)
* Basic knowledge of working with files
* HTML basics (study [Introduction to HTML](link-to-html-intro))
* An idea of how CSS works (study [CSS first steps](link-to-css-first-steps))

## Objective

To learn about the different combinator selectors that can be used in CSS.

## What are Combinators?

Combinators in CSS allow you to specify the relationship between selectors, giving you fine-grained control over which elements are targeted by your styles. They let you select elements based on their position relative to other elements in the document structure.

## Types of Combinators

There are four main types of combinators:

1. **Descendant Selector (space)**
   * Selects all descendants of an element.
   * `A B` selects any `B` element that is a descendant (child, grandchild, etc.) of an `A` element.
   * Example: `div p` selects all `<p>` elements inside any `<div>`.

2. **Child Selector (`>`)**
   * Selects only direct children of an element.
   * `A > B` selects any `B` element that is a direct child of an `A` element.
   * Example: `ul > li` selects all `<li>` elements that are direct children of a `<ul>` element (but not `<li>` elements nested within other `<li>` elements).

3. **Adjacent Sibling Selector (`+`)**
   * Selects the element that is immediately after another element and shares the same parent.
   * `A + B` selects the `B` element that is immediately preceded by an `A` element, and both are children of the same parent.
   * Example: `h2 + p` selects the first `<p>` element that comes immediately after an `<h2>` element.

4. **General Sibling Selector (`~`)**
   * Selects all elements that are siblings of a specific element (i.e., share the same parent) and appear after it.
   * `A ~ B` selects all `B` elements that are siblings of an `A` element and appear after it.
   * Example: `h2 ~ p` selects all `<p>` elements that are siblings of an `<h2>` and appear after it.

## Examples

```html
<div>
  <p>Paragraph 1</p>
  <ul>
    <li>List item 1</li>
    <li>List item 2</li>
  </ul>
  <p>Paragraph 2</p>
</div> 


