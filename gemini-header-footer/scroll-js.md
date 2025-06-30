# Scroll JavaScript

## `scroll.js`

### **High-Level Purpose**

This script adds a data attribute (`data-scroll`) to the `<html>` element based on the user's scroll direction or position **relative to the header**. It also adds a CSS hook (`.js-header`) to `<body>` for styling Gemini-specific headers.

---

### **Behavior Breakdown**

#### ✅ 1. **Setup and Safety Check**

```js
if (!header) return;
```

-   If `.js-header` isn’t found in the DOM, the script exits early to avoid errors.

#### ✅ 2. **Class Hook**

```js
body.classList.add("js-header");
```

-   Adds a class to `<body>` so styles can specifically target pages using this header script.

---

### **Scroll Behavior Logic:**

#### 🧠 It tracks:

-   The **bottom position** of the header
-   The **scroll direction** by comparing the last known scroll position to the current one

#### 👇 The logic:

-   If the header has scrolled _off screen_:

    -   Compare current scroll to previous scroll:

        -   Scrolling **up** → `data-scroll="up"`
        -   Scrolling **down** → `data-scroll="down"`

-   If the header is still _on screen_:

    -   Set `data-scroll="top"`

This allows you to style based on scroll behavior:

```css
[data-scroll="down"] .js-header {
	opacity: 0;
}
[data-scroll="up"] .js-header {
	opacity: 1;
}
[data-scroll="top"] .js-header {
	background: transparent;
}
```

---

### **Events:**

-   Runs `update()` on both:

    -   `window.load` (in case page loads mid-scroll)
    -   `window.scroll` (tracks scroll live)

---

### **Summary**

This script supports **dynamic header behavior**:

-   Tracks scroll direction
-   Adds scroll state (`top`, `up`, `down`) to `<html>`
-   Adds `.js-header` to `<body>` for CSS targeting
