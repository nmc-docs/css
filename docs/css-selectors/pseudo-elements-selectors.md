---
sidebar_position: 5
---

# Pseudo-elements selectors

- **Pseudo-Elements** được sử dụng để tạo lớp giả cho phần tử. Lớp giả này cũng thuộc phần tử đó
- Ví dụ, nó có thể được sử dụng để:
  - Tạo kiểu cho chữ cái đầu tiên, hoặc dòng đầu tiên của phần tử.
  - Biểu thị phần "giả" trước hoặc sau nội dung của phần tử
- Cú pháp:

```css
selector::pseudo-element {
  property: value;
}
```

- Các **Pseudo-Elements** hay dùng

| Pseudo Elements  | Ý nghĩa                                                                          |
| ---------------- | -------------------------------------------------------------------------------- |
| `::after`        | Tạo lớp giả ở sau cùng của nội dung phần tử                                      |
| `::before`       | Tạo lớp giả ở trước nội dung phần tử                                             |
| `::first-letter` | Tạo kiểu với kí tự đầu tiên của nội dung                                         |
| `::marker`       | Tạo kiểu cho điểm đánh dấu của một mục danh sách, áp dụng cho thẻ `<ul>`,`<li>`… |
| `::selection`    | Tạo kiểu văn bản khi người dùng bôi đen một đoạn text                            |
| `::placeholder`  | Tạo kiểu cho phần text placeholder trong thẻ `<input/>`                          |

- Ví dụ:

```css
/* Tạo kiểu cho ký tự đầu tiên của thẻ <p> */
p::first-letter {
  font-size: xx-large;
}

/* Tạo kiểu cho phần placeholder text của thẻ <input/> */
input::placeholder {
  color: brown;
}
```

:::caution

Chú ý: `::after` và `::before` cần có thuộc tính `content: ""`, `position: absolute` thì nó mới hoạt động

:::
