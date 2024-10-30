# CSS Tutorial

## CSS Syntax

A CSS rule consists of:

- **Selector**: Points to the HTML element to style.
- **Declaration Block**: Contains style declarations enclosed in curly braces `{}`.

### Declaration Block Details

- Each declaration includes a **property name** and **value**, separated by a colon.
- Multiple declarations are separated by semicolons.

### Example

In the example below, all `<p>` elements are styled to have red text color and be center-aligned:

```css
p {
  color: red;
  text-align: center;
}
```

### Explanation

- `p`: The selector, targeting `<p>` elements.
- `color`: A property, with `red` as its value.
- `text-align`: A property, with `center` as its value.

## CSS Selectors

### Overview

CSS selectors are used to "find" and style specific HTML elements on a page. There are five main categories of CSS selectors:

1. **Simple Selectors**: Select elements by name, `id`, or `class`.
2. **Combinator Selectors**: Select elements based on relationships.
3. **Pseudo-Class Selectors**: Select elements in a specific state.
4. **Pseudo-Element Selectors**: Style a specific part of an element.
5. **Attribute Selectors**: Select elements based on attribute values.

### Basic CSS Selectors

#### 1. Element Selector

Selects HTML elements by their tag name.

```css
p {
  text-align: center;
  color: red;
}
```

#### 2. `id` Selector

Selects an element by its unique `id` attribute. Use `#` followed by the `id`.

```css
#para1 {
  text-align: center;
  color: red;
}
```

> **Note**: `id` names cannot start with a number.

#### 3. Class Selector

Selects elements with a specific `class` attribute. Use `.` followed by the class name.

```css
.center {
  text-align: center;
  color: red;
}
```

To apply the class only to specific elements:

```css
p.center {
  text-align: center;
  color: red;
}
```

> **Note**: Class names cannot start with a number.

#### 4. Universal Selector

Selects all HTML elements on the page.

```css
* {
  text-align: center;
  color: blue;
}
```

#### 5. Grouping Selector

Groups multiple selectors to apply the same styles, reducing code redundancy.

```css
h1,
h2,
p {
  text-align: center;
  color: red;
}
```

### Summary

CSS selectors enable precise styling control over HTML elements. By combining different types of selectors, you can apply styles in an organized and efficient way.

## 1. Color Names

You can specify colors using predefined names:

- Examples: `Tomato`, `Orange`, `DodgerBlue`, `Gray`, `Violet`

## 2. Background and Text Colors

Define colors for backgrounds and text using inline styles:

```html
<h1 style="background-color:DodgerBlue;">Hello World</h1>
<p style="background-color:Tomato;">Lorem ipsum...</p>
```

## 3. RGB Colors

Define colors using RGB values with the format `rgb(red, green, blue)`, where values range from `0` to `255`.

- Example: `rgb(255, 0, 0)` (Red), `rgb(0, 0, 0)` (Black), `rgb(255, 255, 255)` (White)

## 4. RGBA Colors

RGBA extends RGB with an alpha (opacity) value:

- Format: `rgba(red, green, blue, alpha)`, where `alpha` ranges from `0.0` (fully transparent) to `1.0` (fully opaque).
- Example: `rgba(255, 99, 71, 0.5)`

## 5. HEX Colors

Specify colors using hexadecimal values with the format `#RRGGBB`.

- Example: `#ff0000` (Red), `#000000` (Black), `#ffffff` (White)

**Shorthand HEX**: Hex colors can be shortened when pairs are the same, e.g., `#ffcc99` becomes `#fc9`.

## 6. HSL Colors

Use HSL format for hue, saturation, and lightness:

- Format: `hsl(hue, saturation, lightness)`, where `hue` is on a 0-360° color wheel, and `saturation`/`lightness` are percentages.
- Example: `hsl(0, 100%, 50%)` (Red), `hsl(240, 100%, 50%)` (Blue)

## 7. HSLA Colors

HSLA extends HSL with an alpha (opacity) value:

- Format: `hsla(hue, saturation, lightness, alpha)`.
- Example: `hsla(9, 100%, 64%, 0.5)`

### Shades of Gray

For gray shades in RGB or HSL, use equal values:

- RGB Example: `rgb(90, 90, 90)`
- HSL Example: `hsl(0, 0%, 50%)`

## CSS Backgrounds

### 1. Background Color

Sets the background color of an element.

```css
element {
  background-color: color;
}
```

- Example:
  ```css
  div {
    background-color: lightblue;
  }
  ```

## 2. Background Image

Applies an image as the background.

```css
element {
  background-image: url("image-path.jpg");
}
```

- Example:
  ```css
  body {
    background-image: url("background.jpg");
  }
  ```

## 3. Background Repeat

Controls how the background image is repeated.

```css
element {
  background-repeat: repeat | repeat-x | repeat-y | no-repeat;
}
```

- Options:
  - `repeat`: Repeats both horizontally and vertically (default).
  - `repeat-x`: Repeats horizontally only.
  - `repeat-y`: Repeats vertically only.
  - `no-repeat`: No repetition.
- Example:
  ```css
  div {
    background-image: url("pattern.png");
    background-repeat: no-repeat;
  }
  ```

## 4. Background Position

Specifies the position of the background image.

```css
element {
  background-position: top | right | bottom | left | center | x% y%;
}
```

- Example:
  ```css
  div {
    background-image: url("image.jpg");
    background-position: center;
  }
  ```

## 5. Background Size

Defines the size of the background image.

```css
element {
  background-size: auto | cover | contain | width height;
}
```

- Options:
  - `cover`: Scales the image to cover the element’s entire area.
  - `contain`: Scales the image to fit within the element.
  - `width height`: Set custom width and height in units or percentages.
- Example:
  ```css
  div {
    background-image: url("image.jpg");
    background-size: cover;
  }
  ```

## 6. Background Attachment

Determines whether the background scrolls with the page or is fixed.

```css
element {
  background-attachment: scroll | fixed | local;
}
```

- Options:
  - `scroll`: Background scrolls with the element’s content (default).
  - `fixed`: Background stays fixed in place when scrolling.
  - `local`: Background scrolls with the element’s content.
- Example:
  ```css
  div {
    background-image: url("image.jpg");
    background-attachment: fixed;
  }
  ```

## 7. Background Clip

Specifies the area where the background is painted.

```css
element {
  background-clip: border-box | padding-box | content-box;
}
```

- Options:
  - `border-box`: Extends the background to the border (default).
  - `padding-box`: Extends the background to the edge of the padding.
  - `content-box`: Restricts the background to the content area.
- Example:
  ```css
  div {
    background-color: lightblue;
    background-clip: padding-box;
  }
  ```

## 8. Background Origin

Defines where the background positioning area begins.

```css
element {
  background-origin: border-box | padding-box | content-box;
}
```

- Example:
  ```css
  div {
    background-image: url("pattern.png");
    background-origin: padding-box;
  }
  ```

## 9. Shorthand Background Property

Combine multiple background properties in one line.

```css
element {
  background: color image repeat attachment position / size;
}
```

- Example:
  ```css
  div {
    background: #ffddcc url("image.jpg") no-repeat fixed center / cover;
  }
  ```

### Quick Tips

- **Use `background` shorthand** for simpler code.
- **Combine `background-size: cover`** with `background-position: center` for responsive full-screen backgrounds.

## CSS Borders

## CSS Margins

## CSS Padding

## CSS Height/Width

## CSS Outline

## CSS Text

## CSS Fonts

## CSS Icons

## CSS Links

## CSS Lists

## CSS Tables

## CSS Display

## CSS Max-width

## CSS Position

## CSS Z-index

## CSS Overflow

## CSS Float

## CSS Inline-block

## CSS Align

## CSS Combinators

## CSS Pseudo-classes

## CSS Pseudo-elements

## CSS Opacity

## CSS Navigation Bar

## CSS Dropdowns

## CSS Image Gallery

## CSS Image Sprites

## CSS Attr Selectors

## CSS Forms

## CSS Counters

## CSS Website Layout

## CSS Units

## CSS Specificity

## CSS !important

## CSS Math Functions

````markdown
# CSS Flexbox & Grid Cheat Sheet

## Flexbox

### 1. Container Properties

#### `display: flex;`

Turns an element into a flex container, enabling flexbox for its children.

```css
.container {
  display: flex;
}
```
````

#### `flex-direction`

Defines the main axis direction for flex items.

```css
.container {
  flex-direction: row | row-reverse | column | column-reverse;
}
```

- `row` (default): Left to right.
- `column`: Top to bottom.

#### `justify-content`

Aligns items along the main axis.

```css
.container {
  justify-content: flex-start | flex-end | center | space-between | space-around
    | space-evenly;
}
```

#### `align-items`

Aligns items along the cross axis.

```css
.container {
  align-items: flex-start | flex-end | center | baseline | stretch;
}
```

#### `align-content`

Aligns rows along the cross axis when there's extra space.

```css
.container {
  align-content: flex-start | flex-end | center | space-between | space-around |
    stretch;
}
```

### 2. Item Properties

#### `flex`

Shorthand for `flex-grow`, `flex-shrink`, and `flex-basis`.

```css
.item {
  flex: grow shrink basis;
}
```

- Example:
  ```css
  .item {
    flex: 1 1 200px;
  }
  ```

#### `align-self`

Overrides `align-items` for a single item.

```css
.item {
  align-self: auto | flex-start | flex-end | center | baseline | stretch;
}
```

#### `order`

Controls the order of items.

```css
.item {
  order: 1; /* Default is 0 */
}
```

---

## CSS Grid

### 1. Container Properties

#### `display: grid;`

Turns an element into a grid container.

```css
.container {
  display: grid;
}
```

#### `grid-template-columns` & `grid-template-rows`

Defines columns and rows in the grid.

```css
.container {
  grid-template-columns: 100px 200px 1fr;
  grid-template-rows: 100px auto;
}
```

- Use `fr` to create flexible grid tracks.

#### `gap`

Defines the space between rows and columns.

```css
.container {
  gap: 10px; /* gap: row-gap column-gap; */
}
```

#### `grid-template-areas`

Defines layout regions by naming grid areas.

```css
.container {
  grid-template-areas:
    "header header header"
    "sidebar content content"
    "footer footer footer";
}
```

- Assign items to areas with `grid-area`.

#### `justify-items`

Aligns items horizontally within their grid area.

```css
.container {
  justify-items: start | end | center | stretch;
}
```

#### `align-items`

Aligns items vertically within their grid area.

```css
.container {
  align-items: start | end | center | stretch;
}
```

### 2. Item Properties

#### `grid-column` & `grid-row`

Specifies the column or row span for an item.

```css
.item {
  grid-column: start / end;
  grid-row: start / end;
}
```

- Example:
  ```css
  .item {
    grid-column: 1 / 3; /* Spans columns 1 to 3 */
  }
  ```

#### `grid-area`

Assigns an item to a named grid area or custom position.

```css
.item {
  grid-area: area-name | row-start / column-start / row-end / column-end;
}
```

- Example:
  ```css
  .header {
    grid-area: header;
  }
  ```

---

## Quick Reference Table

| Property               | Flexbox               | Grid                         |
| ---------------------- | --------------------- | ---------------------------- |
| Main Layout            | `display: flex;`      | `display: grid;`             |
| Direction              | `flex-direction`      | `grid-template-columns/rows` |
| Main Axis Alignment    | `justify-content`     | `justify-items`              |
| Cross Axis Alignment   | `align-items`         | `align-items`                |
| Spacing Between Items  | `gap`                 | `gap`                        |
| Item-Specific Position | `order`, `align-self` | `grid-column`, `grid-row`    |

```

```
