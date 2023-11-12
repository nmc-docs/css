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

:::caution

- Lưu ý: Các thuộc tính `top`, `left`, `right`, `bottom` chỉ hoạt động đối với phần tử có `position` **KHÔNG PHẢI** là `static` (tức chỉ hoạt động với các phần tử có `position` là `relative`, `absolute`, `fixed`)

:::

- Các thuộc tính `left`, `right`, `bottom`, `top` sẽ di chuyển phần tử theo cách:
  - Nếu phần tử có `position: relative`: di chuyển phần tử so với vị trí ban đầu của nó
  - Nếu phần tử có `position: absolute` hoặc `position: fixed`: di chuyển phần tử so với **mép ngoài cùng** của phần tử cha gần nhất có `position` khác `static`, nếu không có phần tử cha thỏa mãn, sẽ di chuyển so với thẻ `<body>`

:::info

Nếu phần tử có thuộc tính `top`, `bottom`, `left`, `right` có giá trị đơn vị là **%** thì giá trị phần trăm đó được tính theo phần trăm **width** / **height** của:

- Phần [content](./layout-of-element) của phần tử cha nếu nó có `position: relative`
- Toàn bộ chiều dài, chiều cao của phần tử cha (bao gồm **padding**, **border**) nếu nó có `position: absolute, fixed`
- Ví dụ:

```html
<div className="h-[400px] w-[360px] bg-red-500 relative p-4">
  <div className="w-8 h-8 bg-yellow-400 relative top-[100%]"></div>
  <div className="w-8 h-8 bg-blue-400 absolute left-[30%] top-[100%]"></div>
</div>
```

![1699777340076](image/top-bottom-right-left/1699777340076.png)

:::

## inset

- Thuộc tính `inset` là một cách viết ngắn gọn cho việc thiết lập vị trí (`top`, `bottom`, `right`, `left`) cho phần tử

| Property | Value                                                                                         |
| -------- | --------------------------------------------------------------------------------------------- |
| `inset`  | `apx bpx cpx dpx`: Thiết lập vị trí trên, phải, dưới, trái cho phần tử con so với phần tử cha |

![1698587467049](image/position/1698587467049.png)
