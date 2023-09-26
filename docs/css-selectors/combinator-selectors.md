---
sidebar_position: 3
---

# Combinator selectors

- **Combinator selectors** là cách tạo kiểu dựa trên mối quan hệ. Gồm có 4 loại:

## Descendant Selector (space)

```css
/* Tạo kiểu cho tất cả thẻ <p> nằm bên trong thẻ <div> */
div p {
  background-color: yellow;
}
```

## Child Selector (>)

```css
/* Tạo kiểu cho tất cả thẻ <p> có “cha” gần nhất là thẻ <div> */
div > p {
  background-color: yellow;
}
```

## Adjacent Sibling Selector (+)

```css
/* Tạo kiểu cho thẻ <p> nằm ngay sau thẻ <div> */
div + p {
  background-color: yellow;
  color: blue;
}
```

## General Sibling Selector (~)

```css
/* Tạo kiểu cho tất cả thẻ <p> nằm sau thẻ <div> */
div ~ p {
  background-color: yellow;
}
```
