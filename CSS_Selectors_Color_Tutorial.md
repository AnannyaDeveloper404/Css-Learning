# CSS Selectors & Color Cheatsheet

## CSS Selectors

### 1. **Basic Selectors**

- `*` – Selects **all** elements
- `element` – Selects all instances of a **specific element** (e.g., `div`, `p`, etc.)
- `.class` – Selects all elements with a **specific class**
- `#id` – Selects an element with a **specific ID**

### 2. **Attribute Selectors**

- `[attribute]` – Selects elements with a specific **attribute** (e.g., `[type="text"]`)
- `[attribute^="value"]` – Selects elements where the attribute starts with a specific **value**
- `[attribute$="value"]` – Selects elements where the attribute ends with a specific **value**
- `[attribute*="value"]` – Selects elements where the attribute contains a **value**

  ```css
  input[type] {
    border: 1px solid #000;
  }
  input[type="submit"] {
    background-color: green;
    color: white;
  }
  a[href^="https://"]
  {
    color: green;
  }
  a[href$=".pdf"] {
    color: red;
  }
  ```

### 3. **Combinators**

- `element1 element2` – Selects all instances of `element2` **inside** `element1`
- `element1 > element2` – Selects all `element2` elements that are **direct children** of `element1`
- `element1 + element2` – Selects the `element2` that is **immediately after** `element1`
- `element1 ~ element2` – Selects all `element2` elements that are **siblings** of `element1`

### 4. **Pseudo-classes**

- `:hover` – Selects an element when it is **hovered**
- `:nth-child(n)` – Selects the **nth child** of its parent
- `:first-child` – Selects the **first child**
- `:last-child` – Selects the **last child**
- `:not(selector)` – Selects all elements **not** matching the selector

### 5. **Pseudo-elements**

- `::before` – Inserts content **before** an element's content
- `::after` – Inserts content **after** an element's content
- `::first-letter` – Styles the **first letter** of an element
- `::first-line` – Styles the **first line** of an element

---

## CSS Color

### 1. **Named Colors**

- Use predefined color names like `red`, `blue`, `green`, `black`, `white`, etc.

### 2. **HEX Colors**

- `#RRGGBB` or `#RGB` – Define colors in **hexadecimal** values
  - Example: `#FF5733` (Bright Orange)

### 3. **RGB Colors**

- `rgb(red, green, blue)` – Define colors using **RGB** values (0-255)
  - Example: `rgb(255, 87, 51)`

### 4. **RGBA Colors**

- `rgba(red, green, blue, alpha)` – Same as RGB but with **opacity** (0 to 1)
  - Example: `rgba(255, 87, 51, 0.5)` (50% transparent orange)

### 5. **HSL Colors**

- `hsl(hue, saturation%, lightness%)` – Define colors using **hue**, **saturation**, and **lightness**
  - Example: `hsl(9, 100%, 60%)` (Bright Orange)

### 6. **HSLA Colors**

- `hsla(hue, saturation%, lightness%, alpha)` – Same as HSL but with **opacity**
  - Example: `hsla(9, 100%, 60%, 0.5)` (50% transparent orange)

### 7. **Opacity**

- `opacity: 0.5;` – Sets the opacity of the entire element, where 0 is fully transparent and 1 is fully opaque.

---

## Tips

- **Cascade and Specificity**: ID (`#`) > Class (`.`) > Element (`tag`)
- **Shorthand Properties**: Combine multiple styles into one for efficiency.
  - Example: `border: 1px solid black;`
