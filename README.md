# Complete CSS Reference Guide

## Table of Contents
1. [CSS Basics](#level-1-css-basics)
2. [Color System & Background](#level-2-color-system--background)
3. [Text Properties](#level-3-text-properties)
4. [Box Model](#level-4-box-model)
5. [Display & Position](#level-5-display--position)
6. [Flexbox, Grid & Media Queries](#level-6-flexbox-grid--media-queries)
7. [Animation, Transition & Transform](#level-7-animation-transition--transform)

---

## Level 1: CSS Basics

### What is CSS?
**CSS (Cascading Style Sheets)** is used to control the visual presentation of HTML elements.
- **Style**: Sets the look and feel
- **Colors & Fonts**: Customizes text and background
- **Layout**: Controls position and size
- **Selectors**: Targets specific HTML elements

### Basic Syntax
```css
selector {
    property: value;
}
```
- **Selector**: The HTML element you want to style
- **Property**: The attribute you want to change (color, font, etc.)
- **Value**: The specific style you want to apply

### Including CSS Styles

#### 1. Inline Styling
```html
<p style="color: red;">This text is red</p>
```
- Applied directly to HTML elements
- Ideal for one-off changes
- Limited reusability

#### 2. Internal Styling
```html
<head>
    <style>
        p { color: red; }
    </style>
</head>
```
- Placed within `<style>` tags in HTML head
- More organized than inline styles
- Reusable within the same page

#### 3. External Styling
```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```
- Separate .css file linked to HTML
- Most reusable across multiple pages
- Best practice for larger projects

### CSS Selectors

#### Element Selector
```css
p {
    color: blue;
}
```
Targets all elements of a specific type.

#### Universal Selector
```css
* {
    margin: 0;
    padding: 0;
}
```
Targets all elements on the page.

#### ID Selector
```css
#unique-id {
    background-color: yellow;
}
```
- Uses hash (#) symbol
- Targets element with specific ID
- Should be unique per page

#### Class Selector
```css
.my-class {
    font-size: 16px;
}
```
- Uses dot (.) symbol
- Can be applied to multiple elements
- Reusable for consistent styling

#### Group Selector
```css
h1, h2, h3 {
    font-family: Arial, sans-serif;
}
```
Styles multiple elements simultaneously using commas.

#### Descendant Selector
```css
div p {
    color: green;
}
```
Targets elements nested within other elements (separated by spaces).

### Comments
```css
/* This is a CSS comment */
/* 
   Multi-line
   comment
*/
```

---

## Level 2: Color System & Background

### Background Color
```css
.element {
    background-color: red;
}
```

### Color Systems

#### RGB Color Model
```css
.element {
    color: rgb(255, 0, 0); /* Red */
    background-color: rgb(0, 255, 0); /* Green */
}
```
- Values range from 0-255 for Red, Green, Blue

#### RGBA (with Alpha Channel)
```css
.element {
    background-color: rgba(255, 0, 0, 0.5); /* 50% transparent red */
}
```
- Alpha value ranges from 0 (transparent) to 1 (opaque)

#### HEX Color Model
```css
.element {
    color: #FF0000; /* Red */
    background-color: #00FF00; /* Green */
}
```
- Uses 6-digit hexadecimal values (#RRGGBB)

### Dimensions
```css
.box {
    width: 200px;
    height: 150px;
    min-width: 100px;
    max-width: 300px;
}
```

### Background Image
```css
.banner {
    background-image: url('image.jpg');
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    background-attachment: fixed;
}

/* Shorthand */
.banner {
    background: #fff url('image.jpg') no-repeat center/cover fixed;
}
```

### Visibility
```css
.hidden {
    visibility: hidden; /* Hidden but occupies space */
}
.gone {
    display: none; /* Completely removed from layout */
}
```

---

## Level 3: Text Properties

### Text Alignment
```css
.text {
    text-align: left;    /* left, right, center, justify */
}
```

### Text Decoration
```css
.link {
    text-decoration: none;           /* Remove underline */
    text-decoration: underline;      /* Add underline */
    text-decoration: line-through;   /* Strike-through */
    text-decoration-color: red;      /* Color of decoration */
    text-decoration-style: dashed;   /* Style of decoration */
}
```

### Text Transform
```css
.text {
    text-transform: uppercase;   /* UPPERCASE */
    text-transform: lowercase;   /* lowercase */
    text-transform: capitalize;  /* Capitalize First Letter */
    text-transform: none;        /* No transformation */
}
```

### Line Height
```css
.paragraph {
    line-height: 1.5;    /* 1.5 times the font size */
    line-height: 24px;   /* Fixed pixel value */
}
```

### Font Properties
```css
.text {
    font-size: 16px;
    font-weight: bold;        /* normal, bold, bolder, 100-900 */
    font-style: italic;       /* normal, italic, oblique */
    font-family: Arial, sans-serif;
}

/* Font family with fallbacks */
.text {
    font-family: "Times New Roman", Times, serif;
}
```

### Icons with Fonts
Use Font Awesome or similar icon fonts:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
<i class="fab fa-linkedin"></i>
<i class="fab fa-github"></i>
```

---

## Level 4: Box Model

### The CSS Box Model
Every element consists of four parts:
1. **Content**: The actual content (text, images, etc.)
2. **Padding**: Space between content and border
3. **Border**: The outline around padding and content
4. **Margin**: Space outside the border

```css
.box {
    width: 200px;
    height: 100px;
    padding: 20px;
    border: 2px solid black;
    margin: 10px;
}
```

### Padding
```css
.element {
    padding: 10px;                    /* All sides */
    padding: 10px 20px;              /* Top/bottom, left/right */
    padding: 10px 15px 20px 25px;    /* Top, right, bottom, left (clockwise) */
    
    /* Individual sides */
    padding-top: 10px;
    padding-right: 15px;
    padding-bottom: 20px;
    padding-left: 25px;
}
```

### Margin
```css
.element {
    margin: 10px;                    /* All sides */
    margin: 10px 20px;              /* Top/bottom, left/right */
    margin: 10px 15px 20px 25px;    /* Top, right, bottom, left (clockwise) */
    margin: 0 auto;                 /* Center horizontally */
    
    /* Individual sides */
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 20px;
    margin-left: 25px;
}
```

### Border
```css
.element {
    border: 2px solid black;        /* Width, style, color */
    border-width: 2px;
    border-style: solid;            /* solid, dashed, dotted, double */
    border-color: black;
    border-radius: 5px;             /* Rounded corners */
    
    /* Individual sides */
    border-top: 1px solid red;
    border-right: 2px dashed blue;
}
```

### Box Sizing
```css
.element {
    box-sizing: content-box;    /* Default: width/height = content only */
    box-sizing: border-box;     /* Width/height includes padding and border */
}
```

---

## Level 5: Display & Position

### Display Property

#### Block Elements
```css
.block {
    display: block;
}
```
- Start on new line
- Take full width available
- Can set width and height
- Examples: `<div>`, `<p>`, `<h1>`

#### Inline Elements
```css
.inline {
    display: inline;
}
```
- Stay in line with text
- Width/height cannot be set
- No line breaks
- Examples: `<span>`, `<a>`, `<strong>`

#### Inline-Block Elements
```css
.inline-block {
    display: inline-block;
}
```
- Stay inline but can have width/height
- Best of both worlds

#### Hide Elements
```css
.hidden {
    display: none;        /* Completely removes from layout */
    visibility: hidden;   /* Hidden but takes space */
}
```

### Responsive Units

#### Relative Units
```css
.element {
    width: 50%;           /* 50% of parent */
    font-size: 1.2em;     /* 1.2 times parent font size */
    font-size: 1.5rem;    /* 1.5 times root font size */
    width: 50vw;          /* 50% of viewport width */
    height: 100vh;        /* 100% of viewport height */
}
```

### Position Property
```css
.element {
    position: static;     /* Default: normal document flow */
    position: relative;   /* Relative to normal position */
    position: absolute;   /* Relative to positioned ancestor */
    position: fixed;      /* Relative to viewport */
    position: sticky;     /* Sticky positioning */
    
    top: 10px;
    right: 20px;
    bottom: 30px;
    left: 40px;
    z-index: 999;         /* Stacking order */
}
```

### Semantic HTML Tags
```html
<header>Page header</header>
<nav>Navigation menu</nav>
<main>Main content</main>
<section>Section of content</section>
<article>Independent article</article>
<aside>Sidebar content</aside>
<footer>Page footer</footer>
```

---

## Level 6: Flexbox, Grid & Media Queries

### Flexbox

#### Flex Container
```css
.container {
    display: flex;
    flex-direction: row;              /* row, column, row-reverse, column-reverse */
    justify-content: center;          /* flex-start, flex-end, center, space-between, space-around, space-evenly */
    align-items: center;              /* flex-start, flex-end, center, stretch, baseline */
    flex-wrap: wrap;                  /* nowrap, wrap, wrap-reverse */
    align-content: center;            /* For wrapped lines */
}
```

#### Flex Items
```css
.item {
    flex-grow: 1;        /* How much to grow */
    flex-shrink: 0;      /* How much to shrink */
    flex-basis: 200px;   /* Initial size */
    flex: 1 0 200px;     /* Shorthand: grow shrink basis */
    align-self: flex-end; /* Override container's align-items */
    order: 2;            /* Change display order */
}
```

### CSS Grid

#### Grid Container
```css
.grid-container {
    display: grid;
    grid-template-columns: 200px 1fr 100px;    /* Fixed, flexible, fixed */
    grid-template-rows: auto 1fr auto;         /* Header, content, footer */
    gap: 20px;                                 /* Space between items */
    grid-template-areas: 
        "header header header"
        "sidebar main aside"
        "footer footer footer";
}
```

#### Grid Items
```css
.grid-item {
    grid-column: 1 / 3;              /* Span columns 1 to 3 */
    grid-row: 2 / 4;                 /* Span rows 2 to 4 */
    grid-area: header;               /* Use named area */
}
```

### Media Queries
```css
/* Mobile first approach */
.container {
    width: 100%;
}

/* Tablet */
@media (min-width: 768px) {
    .container {
        width: 750px;
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .container {
        width: 1000px;
    }
}

/* Combine conditions */
@media (min-width: 768px) and (max-width: 1023px) {
    /* Tablet only styles */
}

/* Orientation */
@media (orientation: landscape) {
    /* Landscape styles */
}
```

---

## Level 7: Animation, Transition & Transform

### Pseudo Classes
```css
.button:hover {
    background-color: blue;
}

.input:focus {
    border-color: green;
}

.list-item:first-child {
    margin-top: 0;
}

.list-item:last-child {
    margin-bottom: 0;
}

.list-item:nth-child(odd) {
    background-color: #f0f0f0;
}
```

### Transitions
```css
.element {
    transition: all 0.3s ease-in-out;
    
    /* Or individual properties */
    transition-property: background-color, transform;
    transition-duration: 0.3s;
    transition-timing-function: ease-in-out;
    transition-delay: 0.1s;
}

.element:hover {
    background-color: red;
    transform: scale(1.1);
}
```

### Transforms
```css
.element {
    /* 2D Transforms */
    transform: translateX(50px);           /* Move horizontally */
    transform: translateY(30px);           /* Move vertically */
    transform: translate(50px, 30px);      /* Move both directions */
    transform: rotate(45deg);              /* Rotate */
    transform: scale(1.5);                 /* Scale uniformly */
    transform: scaleX(2);                  /* Scale horizontally */
    transform: scaleY(0.5);               /* Scale vertically */
    transform: skew(15deg, 5deg);         /* Skew */
    
    /* Combine transforms */
    transform: translate(50px, 30px) rotate(45deg) scale(1.2);
    
    /* 3D Transforms */
    transform: rotateX(45deg);
    transform: rotateY(45deg);
    transform: rotateZ(45deg);
    transform: translateZ(50px);
}
```

### Animations
```css
/* Define keyframes */
@keyframes slideIn {
    0% {
        transform: translateX(-100%);
        opacity: 0;
    }
    100% {
        transform: translateX(0);
        opacity: 1;
    }
}

/* Apply animation */
.animated {
    animation: slideIn 0.5s ease-in-out;
    
    /* Or individual properties */
    animation-name: slideIn;
    animation-duration: 0.5s;
    animation-timing-function: ease-in-out;
    animation-delay: 0.2s;
    animation-iteration-count: infinite;    /* Or specific number */
    animation-direction: alternate;         /* normal, reverse, alternate, alternate-reverse */
    animation-fill-mode: forwards;         /* none, forwards, backwards, both */
    animation-play-state: paused;          /* running, paused */
}

/* Complex animation */
@keyframes bounce {
    0%, 20%, 53%, 80%, 100% {
        animation-timing-function: cubic-bezier(0.215, 0.610, 0.355, 1.000);
        transform: translate3d(0,0,0);
    }
    40%, 43% {
        animation-timing-function: cubic-bezier(0.755, 0.050, 0.855, 0.060);
        transform: translate3d(0, -30px, 0);
    }
    70% {
        animation-timing-function: cubic-bezier(0.755, 0.050, 0.855, 0.060);
        transform: translate3d(0, -15px, 0);
    }
    90% {
        transform: translate3d(0,-4px,0);
    }
}
```

### Float Property (Legacy)
```css
.image {
    float: left;     /* left, right, none */
    clear: both;     /* Clear floated elements */
}
```

---

## Practice Exercises Summary

### Level 1: Basic Practice
- Create headings with colored text
- Practice all three ways of including CSS
- Use different selectors (element, class, ID)
- Create group selectors for multiple elements

### Level 2: Colors & Background
- Create divs with background colors and opacity
- Add background images with different properties
- Practice RGB, RGBA, and HEX color formats

### Level 3: Text Styling
- Center and transform text
- Apply different font families and weights
- Use Font Awesome icons
- Create nested div structures with different font sizes

### Level 4: Box Model
- Create boxes and observe box model in dev tools
- Practice padding, margin, and border properties
- Create circular elements with border-radius
- Compare different box-sizing values

### Level 5: Layout
- Build semantic webpage structure (header, nav, main, footer)
- Practice different display values
- Use positioning for fixed elements
- Implement z-index for layering

### Level 6: Advanced Layout
- Create responsive navigation with flexbox
- Center content using flexbox
- Build flexible layouts with grow/shrink
- Implement responsive design with media queries

### Level 7: Animations
- Create smooth loading animations
- Build progress bars with transitions
- Implement hover effects and transformations

---

## Useful Resources

- **MDN Documentation**: https://developer.mozilla.org/
- **Font Awesome Icons**: https://fontawesome.com
- **CSS Tricks**: https://css-tricks.com
- **Can I Use**: https://caniuse.com (browser compatibility)

---

## Browser Developer Tools

- **Right-click → Inspect Element**: Access developer tools
- **Elements Panel**: View and edit HTML/CSS live
- **Styles Panel**: See applied CSS rules
- **Box Model Visualization**: Understand spacing and dimensions
- **Network Tab**: Monitor resource loading
- **Performance Tab**: Analyze page performance

Remember: Changes in dev tools are temporary and reset on page reload!