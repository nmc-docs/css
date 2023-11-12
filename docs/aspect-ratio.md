---
sidebar_position: 21
---

# aspect-ratio

- Trong CSS, `aspect ratio` (tỷ lệ cạnh) thường được sử dụng để chỉ định mối quan hệ giữa chiều rộng và chiều cao của một phần tử. Nó giúp duy trì tỷ lệ kích thước của một phần tử,
- Ví dụ:

```css
.container {
  width: 300px; /* Chiều rộng của phần tử container */
  aspect-ratio: 1 / 1; /* Tỷ lệ khía cạnh 16:9 */
}
```

:::info

Trong đoạn mã trên, `.container` có chiều rộng là 300px và tỷ lệ cạnh là 1:1. Bất kỳ thay đổi nào về chiều rộng của `.container` cũng sẽ ảnh hưởng đến chiều cao của nó sao cho tỷ lệ giữa chiều rộng và chiều cao luôn duy trì ở mức 1:1.

:::
