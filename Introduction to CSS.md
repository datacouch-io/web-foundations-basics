## Introduction to CSS

#### What is CSS?

CSS stands for Cascading Style Sheets. It is a foundational technology in modern web development, responsible for controlling the visual presentation of HTML documents. By defining how elements are displayed, CSS enables developers to create visually engaging and consistent user experiences across different devices and browsers.

#### The Role of CSS in Web Development

CSS plays a vital role in separating content from presentation. While HTML is used to structure the content (such as headings, paragraphs, images, and links), CSS determines how that content appears — including layout, colors, typography, spacing, and responsiveness. This separation allows for greater maintainability, flexibility, and adaptability in web projects. With CSS, you can modify the look and feel of an entire website without changing the underlying HTML structure.

Example: By writing a single CSS rule, you can change the background color of all your website's headings at once, without touching each heading's HTML.

#### Basic CSS Syntax

CSS rules follow a consistent syntax format:
```
selector {
property: value;
}
```
-   Selector: Targets the HTML element(s) you want to style.
-   Property: The aspect of the element to style (such as color, font-size, or margin).
-   Value: The setting you assign to the property (such as blue, 16px, or 10px).
    

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeX2MkcY-aZ2_iqy1wIXn36Dqqd1fDZ1TEWJIGbPJOjPLcEEruLFmwy9Kcesjr0FCcg0iCUAlW5IQt5d-raaAEzoVOsJr7pO2-n8WrWsY8MxQeO7HMDFyDUXk0beBb-hDi6Lsyz0g?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig: An illustration showing the structure of a CSS rule, with the selector, property, and value labeled in different colors.)

Example:
```
p {
color: #3366cc;
}
```
This rule changes the text color of all `<p>` (paragraph) elements to a specific shade of blue.

#### Types of CSS Selectors

CSS selectors target HTML elements in various ways. Below are the main types of selectors, with practical examples:

-   **Element Selector**
	-   Targets all instances of a specific HTML tag.
	-   This code selects every `<h1>` element and sets the font size.
-   **Class Selector**
	-   Targets elements with a specific class attribute. Prefixed by a dot (.).
	-   This rule styles every element with class="highlight" to have a yellow background.
    

-   **ID Selector**
    

	-   Targets a single, unique element with a specific id attribute. Prefixed by a hash (#).
	-   Styles the element with id="main-header" for centered text.
    

-   **Group Selector**
    

	-   Applies the same styles to multiple selectors, separated by commas.
	    
	-   Gives all headings `(<h2>, <h3>, <h4>)` a bottom margin.
    

-   **Universal Selector**
    

	-   Targets all elements on the page using an asterisk (*).
	-   This sets a global CSS property for every element.
    

-   **Descendant Selector**
    
	-   Targets elements that are nested within a specific parent element.
	-   Removes the underline from all `<a>` (links) inside `<nav>` elements.
    

### Applying Styles

In CSS3, styles can be applied to HTML documents in three main ways: inline styles, internal (embedded) styles, and external stylesheets. Choosing the right approach depends on factors such as project size, maintainability, and reusability. Understanding these methods is crucial for any professional web developer.

#### 1. Inline Styles (Using the style Attribute)

Inline styles are written directly in the relevant HTML element using the style attribute.

<p style="color: green; font-weight: bold;">This text is styled inline.</p>

-   Usage: Best suited for quick, specific changes or when testing single elements.
    
-   Pros: Easy and immediate effect, no need to create separate CSS files.
    
-   Cons: Not maintainable for larger projects, leads to duplicated code, and hard to apply site-wide changes. Inline styles have high specificity, which can make overriding them more complex.
    

#### 2. Internal Styles (Using the <style> Tag)

Internal or embedded styles are placed inside a <style> tag within the <head> section of an HTML document. All style rules in this block affect the elements on that page only.
```
<head>
<style>
h1 {
color: navy;
letter-spacing: 2px;
}
.highlight {
background-color: #ececec;
padding: 8px;
}
</style>
</head>
<body>
<h1>Header Styled Internally</h1>
<p class="highlight">Highlighted paragraph.</p>
</body>
```
  

-   Usage: Good for small websites or single pages where styles do not need to be reused elsewhere.
    
-   Pros: Keeps style management within one HTML file; faster for simple demos or prototypes.
    
-   Cons: Does not allow sharing styles across multiple pages, making larger sites hard to maintain and less efficient to update.
    

#### 3. External Stylesheets (Using the <link> Element)

The most scalable and recommended approach is to place CSS rules in a separate .css file, then reference this file in the HTML using the `<link>` element inside the `<head>`.
```
<head>

<link rel="stylesheet" href="styles.css">

</head>

/* styles.css */

body {

color: #222;

font-family: 'Segoe UI', Arial, sans-serif;

}

.button-primary {

background-color: #0057b8;

color: #fff;

border-radius: 4px;

}
```
  

-   Usage: Essential for professional, multi-page websites and when reusing styles across many pages.
    
-   Pros:
    

	-   Keeps codebase organized and styles separate from structure.
	    
	-   Enables caching and faster loading after the first visit.
	    
	-   Effortless updates across all linked pages by editing a single file.
    

-   Cons:
    

	-   Requires at least two files (HTML and CSS).
	    
	-   Dependent on correct file paths and network availability for styles to load.
    

#### Comparative Overview

| **Method**         | **Best For**                | **Pros**                      | **Cons**                                |
|--------------------|-----------------------------|-------------------------------|------------------------------------------|
| **Inline**         | Quick, local edits           | Simple, instant effect        | Hard to maintain, not reusable           |
| **Internal (`<style>`)** | Single pages, prototypes     | Centralized for one file     | Not reusable across pages                |
| **External (`<link>`)**  | Multi-page sites, production | Reusable, scalable, organized | Requires separate CSS file               |

Industry best practice is to use external stylesheets for most projects, as they provide the greatest flexibility, consistency, and long-term maintainability.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXewYD5gsnAf_rTuXkdm2oasaFmwWf0rMR5Mqc74RNEpbvvEA2ONrXME5y0etgomEK77UNizp-DDyvmHS6TPkfRFat-Vym2JUWEyLhuNtXAymCKopx94XVvMo9TJHd9KmYcSPpIXlw?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig: Create a visual comparing inline, internal, and external CSS — show an HTML file with arrows pointing to the location of inline styles within an element, internal styles in the <head>  <style> tag, and external styles referenced in the <head> by <link>.)

### Common CSS Properties

#### Color Properties

CSS offers multiple ways to define colors, providing flexibility for design and readability. The main options are:

-   Named Colors:This sets the text color of all `<h1>` headings to the named color red.
    
-   Hex Codes:Uses a six-digit hexadecimal value to define a specific shade of blue for all `<p>` elements.
    
-   RGB and RGBA:rgb uses red, green, and blue values (0-255), while rgba adds alpha for transparency.
    
-   HSL:hsl sets color using hue (degrees), saturation, and lightness (percentages).
    

#### Font and Typography Properties

Typography enhances readability and branding. The most common font-related CSS properties include:

-   Font Family:Defines a prioritized list of fonts for the entire document. If the first is unavailable, the next is used.
    
-   Font Size:Specifies the size of text using absolute units (px) or relative units (rem, em).
    
-   Font Weight:Adjusts the boldness or thickness of the font.
    
-   Line Height:Controls the vertical spacing between lines for improved legibility.
    

#### Text Properties

Text properties allow you to manage alignment, decoration, and capitalization styles:

-   Text Align:Makes the content of the element centered horizontally.
    
-   Text Decoration:Removes underlines from links or applies effects like line-through to text.
    
-   Text Transform:Converts text to uppercase, lowercase, or capitalizes each word.
    

#### Spacing: Margin and Padding

Controlling the space around and within elements is essential for layout:

-   Margin: Defines space outside an element’s border.
    
-   Padding: Sets space inside an element, between the content and the border.
    
```
.box {
margin: 20px;
padding: 10px 30px;
}
```

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf5bWbPjamef9YuIFoT4hGfVHbHCywHcA12kskhE6_95xqj7Ts0jjIvNedjzxkTjL993oY9r8uFZN-8dRmMUloOr-pM3KNvuLcAtthK5ktGU0QS_EfvPEpot7KbfetHhJVnnyYWnQ?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig: Illustrate the difference between margin and padding using colored boxes, labels for "content," "padding," and "margin.")

#### Borders and Border Radius

CSS borders frame elements, while border-radius creates rounded corners:

-   Basic Border:Adds a 2-pixel solid border to any element with class image-frame.
    
-   Border Radius:border-radius with a fixed value creates rounded corners, while 50% makes circular shapes for square elements.
    

#### Comprehensive Example
```
<div class="sample">Sample Box</div>
.sample {
color: #fff;
background-color: hsl(220, 70%, 55%);
font-family: Arial, sans-serif;
font-size: 1.3em;
font-weight: 600;
text-align: center;
padding: 20px 40px;
margin: 15px;
border: 3px dashed #222;
border-radius: 16px;
}
```
This code creates a visually distinct box demonstrating the combination of color, font, text alignment, spacing, borders, and border-radius.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe7ynpmA-vluPQ-W0bfotFcYDHwBRiGNoMkd8WXDJpm_gOPmW1K_kKM5P0VKpsfTGiC4suoSAYm6H5PZe2J6VQzhHyJADlxEGRfW0XbNUFMLCAk-WPIpQjUVjttyGrEHEBXYmLDWQ?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig:  A side-by-side layout showing how varying font-size, color, margin, and padding affect the appearance of sample HTML boxes. Label each visual change.)

### CSS Box Model

#### The Four Layers of the Box Model

The CSS Box Model is a cornerstone concept in web design, defining how elements are structured, sized, and spaced on web pages. Every HTML element is represented as a rectangular box made of distinct layers:

-   Content: The innermost area, holding text, images, or other nested elements. Its dimensions are set by properties like width and height.
    
-   Padding: The space inside the box, between the content and the border. Padding increases the space around content without affecting neighboring elements.
    
-   Border: Surrounds the padding (or content, if no padding is set). Borders can be styled with thickness, color, and type (solid, dashed, etc.).
    
-   Margin: The outermost layer, creating space outside the border to separate the element from others on the page.
    

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXf16sTX6ay9FYbhTchi3K615qoWqyS9f0EgynhR__N9Tx-M0fkr0gP2L-XkVgafkkg_HwRkcmIPehbtifTGhVN-FH7AnwgL0CTjileC29v2m2ezc-sjbQNbzcca_Gy-zJGukB7wcg?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig: A labeled CSS Box Model illustration with each area—content, padding, border, margin—displayed in distinct colors.)

#### Impact of Each Layer on Layout and Sizing

The box model influences both the appearance and the space each element occupies. By default, the total width of an element is calculated as:

> Total width = content width + left/right padding + left/right border +
> left/right margin
> 
> Total height = content height + top/bottom padding + top/bottom border +
>  top/bottom margin

Thus, increasing padding or borders will widen an element beyond its base content size, while margins push the element away from its neighbors.  
CSS property box-sizing—when set to border-box—changes this calculation so that padding and border are included within the declared width/height, helping to avoid layout surprises.

#### Hands-on Example: Manipulating the Box Model

Consider the following code, which styles a sample box to visibly illustrate each box model layer:
```
<div class="box-model-demo">Box Model Layers</div>  
  
.box-model-demo {  
width: 220px; /* Content width */  
height: 80px; /* Content height */  
padding: 18px  28px; /* Space inside the box */  
border: 4px solid #3677be; /* Colored border */  
margin: 30px  12px; /* Space outside the box */  
background: #e6f0fa; /* Content background */  
box-sizing: content-box;  
}
```
What does each part do?

-   Content: The text "Box Model Layers" in the center uses a background color for emphasis.
    
-   Padding: Adds extra space inside the box, so text doesn't touch the border—visible as light space around the text.
    
-   Border: Creates a colored outline that further increases the visible box size.
    
-   Margin: Adds space outside the border, separating the box from other page elements.
    

Try adjusting values for padding, border, and margin to directly see how the box's appearance and page spacing change.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfpdtaew0G8TBAxBb9dcaV42M3HFtQNyWRb7sZzA2qkiYrX0xjOf2DdCMMys8ldz4SSy07xyKmYqfi5kMqDxH-PtSSN3OieAyAj-yXBYDILB0Zd3AkiuDNe42SKBmO_Nw?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig: Generate a labeled diagram of the CSS Box Model showing content, padding, border, and margin, each area distinguished by separate colors and annotated labels.)

### Advanced Selectors

As web projects become more complex, CSS3 offers advanced selectors that give you granular control over which elements to style. Mastering these selectors empowers you to build concise, maintainable, and responsive stylesheets. This section covers attribute selectors, pseudo-classes, pseudo-elements, and combinators—each with practical examples and explanations for real-world applications.

#### Attribute Selectors

Attribute selectors allow you to style elements based on the presence or value of HTML attributes. They are invaluable for targeting specific types of form fields, links, or custom attributes without adding extra classes or IDs.

-   Exact Match:This rule targets only <input> fields where type is exactly "text", such as standard text boxes.
    
	```
	input[type="text"] {
	border: 1px solid #2d6cdf;
	background: #f4f8ff;
	}
	```
-   Prefix Match:This styles all links whose href attribute starts with "https", so secure links stand out.
    
	```
	a[href^="https"] {
	color: #219150;
	font-weight: bold;
	}
	```
-   Substring and Suffix Matches:Use *= for substring matches and $= for suffix (ending) matches. For example, make all PDF links visually distinct.
    
	```
	img[alt*="icon"] {
	width: 32px;
	height: 32px;
	}

	a[href$=".pdf"] {
	color: #c14415;
	text-decoration: underline dotted;
	}
	```
#### Pseudo-Classes

Pseudo-classes enable you to style elements based on their interactive state or position in the document tree. They are commonly used for user interactions and dynamic styling.

-   :hover – Styles elements when the user hovers over them with a mouse.Enhances button feedback for improved user experience.
    
	```
	button:hover {
	background: #273b7a;
	color: #fff;
	cursor: pointer;
	}
	```
-   :focus – Applies styles when an element (like a form field) gains focus, usually by keyboard interaction.Improves accessibility and highlights fields users are currently interacting with.
    
	```
	input:focus {
	outline: 2px solid #ffb300;
	background: #fffbe8;
	}
	```
-   :nth-child() – Targets elements based on their position among siblings.This will color every even-numbered list item, perfect for striped tables or lists.
    
	```
	li:nth-child(even) {
	background: #f0f2fa;
	}
	```
#### Pseudo-Elements

Pseudo-elements let you style distinct parts of elements or insert content via CSS without altering the HTML. They are especially useful for decorations, icons, and design accents.

-   ::before and ::after::before inserts content before the element; ::after adds content after. This approach is great for icons, arrows, or highlighting sections.
    
	```
	h2::before {
	content: "★ ";
	color: gold;
	}

	button::after {
	content: " ➔";
	font-size: 1em;
	color: #1976d2;
	}
	```
-   Custom underline effect:Visually enhance links with a block-level element for unique hover animations.
    
	```
	a::after {
	content: "";
	display: block;
	width: 100%;
	height: 2px;
	background: #48c774;
	transition: background 0.2s;
	}
	```
#### Combinators

Combinators allow you to select elements based on relationships in the document structure. They make it possible to create efficient CSS that applies only to specific scenarios.

-   Descendant (space):Targets all `<li>` items within `<ul>` inside a `<nav>`, regardless of depth.
    
	```
	nav ul li {
	list-style: square;
	}
	```
-   Child (>):Applies styles only to direct `<h3>` children of `<section>` (not grandchildren).
    
	```
	section > h3 {
	margin-top: 2em;
	color: #283593;
	}
	```
-   Adjacent Sibling (+):Targets the <input> immediately following a <label> tag for consistent form styling.
    
	```
	label + input {
	border-color: #ec407a;
	}
	```
-   General Sibling (~):Styles all `<p>` siblings that come after any `<h4>` in the same parent.
	```    
	h4 ~ p {
	color: #6d4c41;
	}
	```
![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXct9Me3dQHMdtPB0SYdpUXV8OP6c5ErQX_hzlRtpZcOhDgrJNCgcETlamKWhCqTG8Vr1dJQlQyrUY8nx8yV0koENu4sKHQDC1enRO6zLZhcT5VKCLAYOFKcfRJUMYswBIPRqTpj1w?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig:  A visual example of a webpage, highlighting elements selected by different advanced selectors such as attribute selectors, :hover, :nth-child(), ::before, and combinators. Visually indicate which selector matches each highlighted element.)

### Units in CSS

CSS uses a variety of measurement units to specify lengths, sizes, and positions for elements. Understanding the difference between absolute and relative units is crucial for creating layouts that are both visually appealing and responsive across devices.

#### Absolute Units

-   Pixels (px): The most common absolute unit in web design. Pixels are fixed-size dots on the screen, and do not scale based on device or user settings. For example:This sets the heading font size to exactly 32 pixels on all screens.
    
	```
	h1 {
	font-size: 32px;
	}
	```
-   Centimeters (cm) and Inches (in): Intended for printed documents. For on-screen display, their physical size may vary depending on device and user settings.
    
	```
	div.print-me {
	width: 8cm;
	height: 3in;
	}
	```
When to use absolute units: Use them when you require precise, unchanging dimensions (such as for pixel-perfect graphics or print styles). However, they lack flexibility and do not respond to user preferences or different screen sizes, making them less suitable for modern, accessible web design.

#### Relative Units

-   Percentages (%): Express sizes in relation to a parent element. For example:This makes the image adjust its size to fit its container, supporting fluid layouts.
    
	```
	img {
	width: 100%;
	}
	```
-   Em (em): Relative to the font size of the element itself. Stacks if used on child elements.
    
	```
	.note {
	font-size: 1.2em; /* 1.2 times the parent's font size */
	padding: 2em; /* Padding is 2 x the element's font size */
	}
	```
-   Rem (rem): Stands for root em, and is relative to the html element's font size (usually 16px by default).
    
	```
	body {
	font-size: 16px;
	}

	h2 {
	font-size: 2rem; /* Always 32px regardless of nesting */
	}
	```
-   Viewport Width and Height (vw, vh): Based on a percentage of the browser’s viewport dimensions.
    
	```
	.hero {
	width: 80vw; /* 80% of the viewport width */
	height: 60vh; /* 60% of the viewport height */
	}
	```
When to use relative units: They are vital for flexible, scalable, and accessible web design. Relative units allow elements to adjust as parent sizes, user preferences, or screen sizes change. For example, using em, rem, %, and vw/vh helps build responsive layouts and ensures better accessibility as users zoom or increase their default font size.

#### Comparing Scaling: px vs em vs rem
```
/* HTML example */

<div class="box-px">Box (100px)</div>
<div class="box-em">Box (6em)</div>
<div class="box-rem">Box (6rem)</div>

/* CSS */

.box-px {
width: 100px;
background: #d4eaff;
}

.box-em {
width: 6em;
font-size: 20px; /* 6em = 120px here */
background: #b0ffd0;
}

.box-rem {
width: 6rem; /* 6 * root font-size (e.g., 16px) = 96px */
background: #ffe6b8;
}
```
-   Box (100px): Always 100 pixels wide.
    
-   Box (6em): Grows larger or smaller depending on its own font size.
    
-   Box (6rem): Consistent size relative to the site's root font size, regardless of local styles.
    

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcmq8D9idJC2-0bldTZbngraE7SzGeL6VIpOa8DnYb-dPwEnSBH7dXpQb5BqGEJJfQDuGVJ0PJllFHgiSyJJLT3TZH93NokxYQD3pPTZaGTP0UgA1j24FNndu7Q6I-D8i3L2wPFAg?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(Fig: Show a side-by-side comparison of boxes styled with px, em, and rem to illustrate how box width scales differently based on unit type and inheritance.)

Summary: Choose relative units for scalable, accessible, and responsive layouts, and reserve absolute units for precise control in fixed contexts or print styling.

### Display and Positioning

#### Understanding display Property Values

The display property in CSS fundamentally determines how an HTML element is rendered on the page, how it interacts with neighboring elements, and how its box model behaves. Below are the most important values:

-   block: Elements with display: block; occupy the full available width, starting on a new line. Common block elements include `<div>, <p>,` and `<h1>–<h6>`.
    
	```
	div {
	display: block;
	}
	```
-   inline: Inline elements (display: inline;) do not start on a new line, only occupying as much width as their content. Examples: `<span>`, `<a>`, `<strong>`. They can't have width/height set.
	    
	```
	span {
	display: inline;
	}
	```
-   inline-block: Combines inline flow with block-level sizing. Elements flow inline but accept width, height, margin, and padding.
    
	```
	.badge {
	display: inline-block;
	width: 50px;
	height: 20px;
	padding: 2px 5px;
	}
	```
-   none: Removes the element from the document flow entirely—it won't be rendered or occupy space.
    
	```
	.hidden {
	display: none;
	}
	```
-   flex: Turns an element into a flex container, enabling powerful, 1-dimensional layouts for its immediate children (see Flexbox section).
    
	```
	.nav-bar {
	display: flex;
	justify-content: space-between;
	}
	```
-   grid: Makes an element a grid container, providing a 2-dimensional layout system for complex arrangements (see Grid Layout section).
    
	```
	.gallery {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	}
	```
#### Positioning Elements with the position Property

The position property dictates how elements are positioned in the normal flow and allows for precise placement using offsets (top, right, bottom, left):

-   static: Default. Elements follow normal document flow. Offset properties have no effect.
    
	```
	.normal {
	position: static;
	}
	```
-   relative: Positioned relative to its normal place, allowing shifts with top, left, etc., without affecting other elements' positions.
	```
	.relative-box {
	position: relative;
	top: 10px;
	left: 20px;
	}
	```
-   absolute: Removed from normal flow and positioned with respect to the nearest parent with position other than static. If none, it’s placed relative to the page itself.
    
	```
	.abs-note {
	position: absolute;
	top: 50px;
	right: 30px;
	}
	```
-   fixed: Positioned relative to the browser window (viewport) and stays fixed when scrolling.
    
	```
	.fixed-header {
	position: fixed;
	top: 0;
	width: 100%;
	background: #072a4f;
	}
	```
-   sticky: Hybrid positioning; treated as relative by default, but switches to fixed when the element crosses a defined threshold (like scrolling past an offset).
    

.sticky-menu {

position: sticky;

top: 0;

background: #e2eaf3;

}

#### The z-index Property and Stacking Context

When elements overlap, z-index determines their front-to-back stacking order, but only works on positioned elements (position other than static). A higher z-index means the element appears on top of lower values.
```
	.modal {
	position: fixed;
	z-index: 1000;
	}
	.overlay {
	position: fixed;
	z-index: 900;
	}
```
If elements share the same stacking context (e.g., share a positioned ancestor), their z-index values are compared. Some properties (like opacity, transform) can also trigger a new stacking context.

-   Tip: If z-index seems to have no effect, check that the element (and its ancestors) are positioned and if unintentional stacking contexts might exist.
    

#### Layout Scenarios: Code Examples

-   Overlaying a Modal Dialog:
    
	```
	<div class="overlay"></div>

	<div class="modal">Modal Content</div>

	  

	.overlay {

	position: fixed;

	top: 0; left: 0; right: 0; bottom: 0;

	background: rgba(0,0,0,0.35);

	z-index: 900;

	}

	.modal {

	position: fixed;

	top: 50%; left: 50%;

	transform: translate(-50%, -50%);

	background: #fff;

	padding: 24px;

	z-index: 1000;

	border-radius: 8px;

	}
	```
-   Sticky Navigation Menu:
    
	```
	<nav class="sticky-menu">Main Navigation</nav>

	.sticky-menu {

	position: sticky;

	top: 0;

	background: #d6ebff;

	border-bottom: 1px solid #5493c7;

	z-index: 10;

	}
	```
-   Absolute Position Relative to Parent:Here, .abs-right is positioned relative to its parent .container.
    
	```
	<div class="container">

	Container

	<span class="abs-right">Badge</span>

	</div>

	  

	.container {

	position: relative;

	background: #f4faff;

	}

	.abs-right {

	position: absolute;

	top: 10px;

	right: 10px;

	background: #ffecb3;

	padding: 4px 10px;

	border-radius: 12px;

	}
	```
  

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXfAFEYnix5bBVzDsijFKH0VlZGDh5qw8litksO_3aDXPEKxlh8vyxX6aOZkbJzmmmZMxNXHMeGV8AQI-oeQpWUrUIO2EQn2M7U6Z_7xC7V_9_yq1vIUktArmnC6n8EV39sGnAcU1Q?key=9f0DCTl_Vyj7aGUqQzQjWQ)

(IFig: Illustrate a layout with differently colored boxes that use position: static, relative, absolute, fixed, and sticky. Show how each element is anchored and how scrolling changes their position. Include callouts explaining how the offsets and stacking behavior differ for each.)
