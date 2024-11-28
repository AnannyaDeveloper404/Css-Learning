# CSS Detailed Notes

## **CSS How To**

CSS can be added to HTML in three ways:

1. **Inline CSS**

   - CSS is written directly inside an HTML element using the `style` attribute.
   - Example:
     ```html
     <p style="color: red;">This is a red paragraph.</p>
     ```
   - Use when applying unique styles to a single element.

2. **Internal CSS**

   - Defined within a `<style>` tag in the `<head>` section of an HTML document.
   - Example:
     ```html
     <head>
       <style>
         p {
           color: blue;
         }
       </style>
     </head>
     ```
   - Useful for styling a single HTML document.

3. **External CSS**
   - Styles are written in a separate `.css` file and linked using the `<link>` tag in the HTML `<head>`.
   - Example:
     ```html
     <head>
       <link rel="stylesheet" href="styles.css" />
     </head>
     ```
   - Best for maintaining consistency across multiple web pages.

---

## **CSS Comments**

- Syntax: `/* comment */`
- Used to add notes or explanations for better readability.
- Example:
  ```css
  /* This sets the background color */
  body {
    background-color: lightblue;
  }
  ```
- Comments are ignored by the browser.

---

## **CSS Colors**

CSS supports multiple ways to define colors:

1. **Color Names**

   - Example: `red`, `blue`, `green`, etc.
   - Usage:
     ```css
     h1 {
       color: red;
     }
     ```

2. **HEX Values**

   - Format: `#RRGGBB`
   - Example: `#ff0000` (red), `#00ff00` (green)
   - Usage:
     ```css
     p {
       color: #00ff00;
     }
     ```

3. **RGB Values**

   - Format: `rgb(red, green, blue)`
   - Example: `rgb(255, 0, 0)`
   - Usage:
     ```css
     div {
       color: rgb(255, 0, 0);
     }
     ```

4. **HSL Values**

   - Format: `hsl(hue, saturation, lightness)`
   - Example: `hsl(0, 100%, 50%)` (red)
   - Usage:
     ```css
     span {
       color: hsl(0, 100%, 50%);
     }
     ```

5. **RGBA and HSLA**
   - Add transparency using the `a` (alpha) value.
   - Example:
     ```css
     p {
       color: rgba(255, 0, 0, 0.5); /* Semi-transparent red */
     }
     ```

---

## **CSS Backgrounds**

### **Background Color**

- Defines the background color of an element.
- Example:
  ```css
  body {
    background-color: lightblue;
  }
  ```

### **Background Image**

- Sets an image as the background.
- Example:
  ```css
  body {
    background-image: url("background.jpg");
  }
  ```

### **Background Repeat**

- Controls if/how a background image repeats.
- Values:
  - `repeat`: Repeats both horizontally and vertically (default).
  - `repeat-x`: Repeats horizontally.
  - `repeat-y`: Repeats vertically.
  - `no-repeat`: No repetition.
- Example:
  ```css
  body {
    background-repeat: no-repeat;
  }
  ```

### **Background Attachment**

- Determines if a background scrolls with the page or is fixed.
- Values:
  - `scroll`: Background scrolls with the content (default).
  - `fixed`: Background stays fixed.
- Example:
  ```css
  body {
    background-attachment: fixed;
  }
  ```

### **Background Shorthand**

- Combines all background properties into one.
- Syntax:
  ```css
  background: color image position/size repeat attachment;
  ```
- Example:
  ```css
  background: lightblue url("background.jpg") no-repeat fixed center;
  ```

---

## **CSS Borders**

- Defines the border around an element.
- Properties:
  - `border-width`: Thickness of the border.
  - `border-style`: Style of the border (`solid`, `dashed`, `none`).
  - `border-color`: Color of the border.
- Example:
  ```css
  div {
    border: 2px solid black;
  }
  ```

---

## **CSS Margins**

- Creates space outside an element.
- Syntax:
  ```css
  margin: top right bottom left;
  ```
- Example:
  ```css
  p {
    margin: 10px 20px 10px 20px;
  }
  ```

---

## **CSS Padding**

- Creates space inside an element, between the content and the border.
- Syntax:
  ```css
  padding: top right bottom left;
  ```
- Example:
  ```css
  p {
    padding: 10px 20px;
  }
  ```

---

## **CSS Box Model**

The box model includes:

1. **Content**: The content of the element.
2. **Padding**: Space between the content and the border.
3. **Border**: Surrounds the padding (or content if padding is not specified).
4. **Margin**: Space outside the border.

- Example:
  ```css
  div {
    margin: 10px;
    padding: 15px;
    border: 1px solid black;
  }
  ```

---

## **CSS Outline**

- Similar to `border` but does not occupy space.
- Properties:
  - `outline-width`: Thickness of the outline.
  - `outline-style`: Style of the outline.
  - `outline-color`: Color of the outline.
- Example:
  ```css
  button {
    outline: 2px dashed blue;
  }
  ```

---

## **CSS Display**

- Controls the layout behavior of an element.
- Common values:
  - `block`: Element takes up the entire width.
  - `inline`: Element does not break the line.
  - `flex`: Makes the element a flex container.
  - `grid`: Makes the element a grid container.
  - `none`: Hides the element.
- Example:
  ```css
  div {
    display: flex;
  }
  ```

---

## **CSS Position**

- Specifies the positioning method of an element.
- Values:
  - `static`: Default position.
  - `relative`: Position relative to its normal position.
  - `absolute`: Position relative to its nearest positioned ancestor.
  - `fixed`: Position relative to the viewport.
  - `sticky`: Toggles between `relative` and `fixed`.
- Example:
  ```css
  div {
    position: absolute;
    top: 10px;
    left: 20px;
  }
  ```

---

## **CSS Z-index**

- Controls the stack order of elements.
- Higher values are placed in front of lower values.
- Example:
  ```css
  div {
    position: relative;
    z-index: 10;
  }
  ```

---

## **CSS Overflow**

- Determines what happens to content that overflows an element's box.
- Values:
  - `visible`: Content is not clipped (default).
  - `hidden`: Content is clipped and not scrollable.
  - `scroll`: Content is clipped and scrollable.
  - `auto`: ScrollBars appear only if needed.
- Example:
  ```css
  div {
    overflow: auto;
  }
  ```
