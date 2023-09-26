---
sidebar_position: 6
---

# Attribute selectors

- **Attribute Selectors** cho phép tạo kiểu với một thuộc tính nhất ở trong thẻ
- Cú pháp:

```css
/Tên thẻ/[attribute = value]
```

- Ví dụ:

```css
/* <a> elements with a title attribute */
a[title] {
  color: purple;
}

/* <a> elements with an href matching "https://example.org" */
a[href="https://example.org"]
{
  color: green;
}

/* <a> elements with an href containing "example" */
a[href*="example"] {
  font-size: 2em;
}

/* <a> elements with an href ending ".org" */
a[href$=".org"] {
  font-style: italic;
}

/* <a> elements whose class attribute contains the word "logo" */
a[class~="logo"] {
  padding: 2px;
}
```
