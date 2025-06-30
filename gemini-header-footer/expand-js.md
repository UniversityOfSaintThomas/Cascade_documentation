# Expand JavaScript

## `expand.js`

### **High-Level Overview**

This script enables **expandable UI elements** (like toggles, popups, or accordion groups) using the `data-expand` attribute, while also supporting **focus trapping** for accessibility inside popups or modals. It's meant to be run once on page load or when the DOM is ready.

---

### **Main Parts**

#### 1. **Focus Trap Utility**

An object called `focusTrap` has two methods:

-   `on(container)`

    -   Finds all focusable elements inside the given container.
    -   Adds a keydown listener to trap focus using Tab / Shift+Tab.
    -   Ensures focus stays inside the container (like a modal or popup).
    -   Focuses the first element when activated.

-   `off(container)`

    -   Removes the keydown listener and disables the trap.

---

#### 2. **Finding Expand Targets**

```js
const targets = document.querySelectorAll("[data-expand]");
```

This grabs every element with a `data-expand` attribute. These elements become interactive expand/collapse triggers.

---

### **Per-Target Behavior**

Each target behaves differently depending on the `data-expand` value:

#### ✅ Default Toggle (`data-expand` without value):

-   Toggles its own `aria-expanded` state on click.

---

#### ✅ Group Toggle (`data-expand="group"`):

-   Finds sibling items within the same `data-expand-group` container.
-   On click:

    -   Expands the clicked item.
    -   Collapses the others in the same group (accordion behavior).

---

#### ✅ Popup Toggle (`data-expand="popup"`):

-   This supports additional attributes:

    -   `data-expand-lock`: activates **focus trap** on popup
    -   `data-expand-toggle="someName"`: sets a `data-someName` attribute on `<html>` for styling

-   On click:

    -   Toggles the expanded state.
    -   Optionally applies/removes a data attribute on `<html>`.
    -   Optionally enables/disables focus trap inside the popup container.

**Also adds listeners to:**

-   Close the popup when clicking outside.
-   Close the popup on `Escape`.

---

### **Accessibility Touchpoints**

-   Uses `aria-expanded` to indicate toggle state.
-   Keeps focus inside interactive areas (like popups).
-   Supports keyboard navigation and ESC to dismiss.

---

### **Why the ESLint disables?**

-   `no-param-reassign`: The `focusTrap.on()` function modifies `container.__trapHandler`.
-   `no-underscore-dangle`: Uses `__trapHandler` as a custom property on DOM nodes.

---

### **Summary**

This script powers accessible UI components:

-   **Toggles**
-   **Accordion-style groups**
-   **Popups with focus trapping**
