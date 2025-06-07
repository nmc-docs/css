---
sidebar_position: 3
---

# Item

## Thuộc tính áp dụng cho flex items

| Property      | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `flex-basis`  | `apx`: chỉ định chiều dài cho item theo đơn vị **px**<br />`a%`: chiều dài cho item được tính theo phần trăm của chiều dài container<br />`auto`: chiều dài cho item sẽ vừa khít với nội dung bên trong nó                                                                                                                                                                                                                                                                                                       |
| `flex-grow`   | ➡️Là một**number** . Chiều dài còn lại của container sẽ được chia đều theo tỷ lệ cho những item có thuộc tính này.<br />Ví dụ: `flex-grow` của các item1, item2, item3 lần lượt là: `4 2 3`, `width` của container là **1800px** thì chiều dài của các item1, item2, item3 lần lượt là: **800px** , **400px** , **600px**<br />Ví dụ: `flex-grow` của item cuối cùng trong container là `1`, các item kia không có `flex-grow` thì chiều dài của item cuối cùng đó sẽ chiếm hết chiều dài còn lại của container. |
| `flex-shrink` | `0`: kích thước phần tử con sẽ không bị co lại khi kích thước của container không đủ chỗ chứa do bị thu nhỏ lại. Lúc này sẽ xuất hiện thanh scroll ngang<br />`1`: Đây là giá trị mặc định. Nếu không có giá trị cụ thể nào được đặt cho `flex-shrink`, các phần tử con của flex container sẽ **co lại khi cần thiết** để phù hợp với không gian chứa (container) – và tất cả sẽ co lại **tỷ lệ thuận với nhau** .                                                                                               |
| `flex`        | `<flex-grow> <flex-shrink> <flex-basis>`: Là cú pháp viết tắt cho 3 thuộc tính bên trên                                                                                                                                                                                                                                                                                                                                                                                                                          |
| `align-self`  | ➡️Thuộc tính này hoạt động giống như thuộc tính `align-items` nhưng nó chỉ định riêng cho 1 phần tử:<br />`stretch`: item sẽ trải dài hết container<br />`center`: item sẽ ở chính giữa container<br />`flex-start`: item sẽ ở trên cùng của container<br />`flex-end`: item sẽ ở dưới cùng của container                                                                                                                                                                                                        |

## flex-basis

- Thuộc tính CSS `flex-basis` được dùng để **xác định kích thước ban đầu của một phần tử con trong flexbox** , **trước khi phân chia không gian còn lại** giữa các phần tử.

* `flex-basis` quyết định **kích thước chính** (main size) của phần tử theo **trục chính (main axis)** của flex container.
* Trục chính phụ thuộc vào `flex-direction`:
  - Nếu `flex-direction: row` (mặc định) → trục chính là **chiều ngang** → `flex-basis` là **chiều rộng** .
  - Nếu `flex-direction: column` → trục chính là **chiều dọc** → `flex-basis` là **chiều cao** .
* Ví dụ:

```css
.item {
  flex-basis: 200px;
}
```

Phần tử `.item` sẽ có kích thước ban đầu là 200px theo trục chính. Sau đó, nếu có không gian dư hoặc thiếu, nó sẽ co giãn tùy theo các thuộc tính `flex-grow` và `flex-shrink`.

- So sánh với `width`, `height`:
  - `flex-basis` **ưu tiên hơn** `width` / `height` trong môi trường flexbox.
  - Nếu ta đặt cả `width` và `flex-basis`, thì `flex-basis` sẽ được dùng **nếu `flex` được áp dụng** .
