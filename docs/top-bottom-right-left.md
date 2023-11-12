---
sidebar_position: 20
---

# Top, left, right, bottom

- Các thuộc tính `top`, `left`, `right`, và `bottom` là các thuộc tính CSS được sử dụng để định vị các phần tử

| Property | Description                                                            |
| -------- | ---------------------------------------------------------------------- |
| `top`    | Đặt khoảng cách từ phần trên của phần tử đến phần trên của phần tử cha |
| `left`   | Đặt khoảng cách từ phần trái của phần tử đến phần trái của phần tử cha |
| `right`  | Đặt khoảng cách từ phần phải của phần tử đến phần phải của phần tử cha |
| `bottom` | Đặt khoảng cách từ phần dưới của phần tử đến phần dưới của phần tử cha |

:::note

- Lưu ý: Các thuộc tính `top`, `left`, `right`, `bottom` chỉ hoạt động đối với phần tử có `position` **KHÔNG PHẢI** là `static` (tức chỉ hoạt động với các phần tử có `position` là `relative`, `absolute`, `fixed`)

:::

- Các thuộc tính `left`, `right`, `bottom`, `top` sẽ di chuyển phần tử theo cách:
  - Nếu phần tử có `position: relative`: di chuyển phần tử so với vị trí ban đầu của nó
  - Nếu phần tử có `position: absolute` hoặc `position: fixed`: di chuyển phần tử so với **mép ngoài cùng** của phần tử cha gần nhất có `position` khác `static`, nếu không có phần tử cha thỏa mãn, sẽ di chuyển so với thẻ `<body>`

:::info

Nếu phần tử có thuộc tính `top`, `bottom`, `left`, `right` có giá trị đơn vị là **%** thì giá trị phần trăm đó được tính theo phần trăm **width** / **height** của phần tử cha, ví dụ:

```html
<div class="w-[500px] h-[150px] relative">
  <div class="w-12 h-12 absolute left-[25%]">
    Phần tử con này sẽ cách phần tử cha về phía bên trái 25% so với chiều dài
    của phần tử cha. Tức 25% của 500px là 125px
  </div>
</div>
```

:::

## inset

- Thuộc tính `inset` là một cách viết ngắn gọn cho việc thiết lập vị trí (`top`, `bottom`, `right`, `left`) cho phần tử

| Property | Value                                                                                         |
| -------- | --------------------------------------------------------------------------------------------- |
| `inset`  | `apx bpx cpx dpx`: Thiết lập vị trí trên, phải, dưới, trái cho phần tử con so với phần tử cha |

![1698587467049](image/position/1698587467049.png)
