---
sidebar_position: 7
---

# Grid

- **Grid** là kiểu hiển thị bố cục dạng lưới
- **Grid** gồm hai phần:
  - **Container**
  - **Item**

## Thuộc tính áp dụng cho grid container

| Property                | Value                                                                                                                                                                                                                                                                                                                                                                                                        |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `display`               | `grid` : chỉ định kiểu hiển thị dạng lưới cho container                                                                                                                                                                                                                                                                                                                                                      |
| `grid-template`         | `a1px b1px c1px … n1px / a2px b2px c2px ... n2px`<br />**a1, b1, c1, … , n1** : chiều cao của từng hàng theo thứ tự (bắt đầu từ 1)<br />**a2, b2, c2, ... , n2** : chiều rộng của từng cột theo thứ tự (bắt đầu từ 1)<br />- Có bao nhiêu giá trị tương ứng với bấy nhiêu hàng/ cột<br />`auto auto … auto`: Chiều dài của cột/ Chiều cao của hàng được xác định bởi chiều dài/ chiều cao của Grid Container |
| `gap`                   | `apx bpx`<br />**a** : độ rộng khoảng trống giữa các hàng<br />**b** : độ rộng khoảng trống giữa các cột item                                                                                                                                                                                                                                                                                                |
| `grid-template-rows`    | `x1px x2px x3px ...`: Thiết lập chiều cao của từng hàng (hàng 1,2,3,...)<br />`auto auto auto...`: Chiều cao của từng hàng sẽ được tự động tính toán dựa trên chiều cao của container                                                                                                                                                                                                                        |
| `grid-template-columns` | `x1px x2px x3px ...`: Thiết lập độ rộng của từng cột (cột 1,2,3,...)<br />`auto auto auto...`: Chiều rộng của từng cột sẽ được tự động tính toán dựa trên độ rộng của container                                                                                                                                                                                                                              |

## Thuộc tính áp dụng cho grid items

| Property      | Value                                                                                                                                                                                     |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `grid-area`   | `a / b / span c / span d`<br />**a** : chỉ số hàng của item<br />**b** : chỉ số cột của item<br />**c** : số lượng hàng mà item sẽ trải dài<br />**d** : số lượng cột mà item sẽ trải dài |
| `grid-row`    | `x / span y`<br />**x**: chỉ số hàng của item<br />**y**: số lượng hàng mà item sẽ trải dài                                                                                               |
| `grid-column` | `x / span y`<br />**x**: chỉ số cột của item<br />**y**: số lượng cột mà item sẽ trải dài                                                                                                 |
