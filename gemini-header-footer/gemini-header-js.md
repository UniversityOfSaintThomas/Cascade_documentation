# Gemini Header JavaScript

## `gemini-header.js`

### **High-Level Purpose**

This script powers **accessible, interactive headers** for a site that appears to have **two header variants** (`.Header__main` and `.HeaderLanding__main`). It handles:

-   Menu and submenu toggling
-   Smooth scrolling to headers
-   Focus trapping for keyboard users
-   Resetting state on resize or outside clicks
-   Search input focus

---

### **Main Features & Behavior**

#### ✅ 1. **Focus Trap Utility**

Like the previous file, it traps keyboard focus inside an element (like a submenu) so users tabbing around won’t escape unintentionally.

-   `focusTrap.on(container)` keeps Tab/Shift+Tab cycling inside `container`.
-   `focusTrap.off(container)` removes the trap.

---

#### ✅ 2. **`initHeader(prefix, headerSelector)`**

This function wires up header behavior. It's called twice:

```js
initHeader("Header__", ".Header__main");
initHeader("HeaderLanding__", ".HeaderLanding__main");
```

##### Inside each header, it handles:

---

#### 📌 **Menu Toggle Buttons**

Selector: `.Header__menu-toggle` or `.HeaderLanding__menu-toggle`

-   Scrolls the header into view if it’s not at the top.
-   On window resize:

    -   Resets the open menu (`data-menu-active` removed)
    -   Collapses any open menus via `aria-expanded="false"`

---

#### 📌 **Submenu Toggles**

Selector: `.Header__subnav-toggle` or `.HeaderLanding__subnav-toggle`

-   Toggles a dropdown-like submenu.

-   Uses `aria-expanded` to reflect state.

-   Only one submenu can be expanded at a time.

-   Adds `data-sub-menu-active` to `<html>` when a submenu is open.

-   Enables **focus trap** inside the submenu's parent container when open.

-   Applies `data-state="active"` to inactive toggles, possibly for dimming or visual context.

-   Closes all submenus and resets state when user clicks outside.

---

#### 📌 **Search Toggle Buttons**

Selector: `.Header__search-toggle` or `.HeaderLanding__search-toggle`

-   On click, waits briefly and then focuses the associated input element (if open).
-   Useful for mobile search dropdowns or overlays.

---

### **Accessibility Notes**

-   Proper use of `aria-expanded`
-   Focus management for keyboard navigation
-   State reset on outside clicks and window resizes

---

### **Summary**

This script powers interactive headers that are:

-   **Responsive** (reset on resize)
-   **Accessible** (keyboard focus + ARIA)
-   **User-friendly** (smooth scroll, one-open-at-a-time submenus)
