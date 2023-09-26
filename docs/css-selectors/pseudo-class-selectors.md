---
sidebar_position: 4
---

# Pseudo-class selectors

- **Pseudo-class** được sử dụng để xác định trạng thái đặc biệt của một phần tử, như khi ta hover vào phần tử, hoặc focus vào phần tử đó.
- Cú pháp:

```css
selector:pseudo-class {
  property: value;
}
```

- Các **Pseudo-class** hay dùng:

| Pseudo-class   | Ý nghĩa                                                                                                                                                            |
| -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `:active`      | Tạo kiểu cho thẻ khi nhấp và giữ chuột vào nó                                                                                                                      |
| `:hover`       | Tạo kiểu cho thẻ khi di chuyển chuột qua nó                                                                                                                        |
| `:focus`       | Tạo kiểu khi ta focus vào phần tử, áp dụng với `<input/>`,`<select>`                                                                                               |
| `:valid`       | Tạo kiểu cho thẻ `<input/>` khi người dùng nhập hợp lệ                                                                                                             |
| `:invalid`     | Tạo kiểu cho thẻ `<input/>` khi người dùng nhập không hợp lệ                                                                                                       |
| `:checked`     | Tạo kiểu khi người dùng tick vào ô check-box. Áp dụng cho thẻ `<input/>` với `type = "radio"` hoặc `type = "checkbox"`                                             |
| `:enabled`     | Tạo kiểu cho `<input/>` khi được enabled                                                                                                                           |
| `:disabled`    | Tạo kiểu cho `<input/>` khi bị disabled                                                                                                                            |
| `:first-child` | Tạo kiểu cho selector khi selector là**CON** đầu tiên của thẻ cha nó                                                                                               |
| `:last-child`  | Tạo kiểu cho selector khi selector là**CON** cuối cùng của thẻ cha nó                                                                                              |
| `:nth-child()` | Tạo kiểu cho thẻ con tương ứng với vị trí do ta chỉ địnhVí dụ: tạo kiểu cho những thẻ `<li>` ở vị trí chẵn `li:nth-child(even) { background-color: lightyellow; }` |
| `:not()`       | Tạo kiểu cho phần tử trừ những phần tử cụ thể                                                                                                                      |

```scss
//Phần tử <li></li> đầu tiên của thẻ cha <ul></ul> sẽ được style
ul {
  li:first-child {
    font-weight: bold;
    color: blue;
  }
}
```

```scss
// Style cho những thẻ <li></li> nằm bên trong thẻ <ul></ul> mà có số thứ tự chẵn
ul {
  li:nth-child(even) {
    color: blue;
  }
}
```

```scss
//Style cho thẻ <p></p> mà không chứa class = "text"
p:not(.text) {
  color: aqua;
}
```
