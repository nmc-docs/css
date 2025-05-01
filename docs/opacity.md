---
sidebar_position: 15
---

# Opacity

- **Opacity** là thuộc tính tạo độ mờ cho phần tử

| Property  | Value                                                                       |
| --------- | --------------------------------------------------------------------------- |
| `opacity` | `a`: Với a là giá trị từ 0 đến 1. Độ rõ nét của phần tử tăng dần từ 0 đến 1 |

:::note[Lưu ý]

- Khi một phần tử nhận `opacity: 0`, nó chỉ làm phần tử trong suốt, nhưng phần tử đó vẫn hiện diện trong DOM, chiếm chỗ trong layout, và vẫn tương tác được với chuột hoặc bàn phím. Nếu không muốn phần tử nhận sự kiện, hãy kết hợp với thuộc tính `pointer-events: none`

:::
