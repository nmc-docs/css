---
sidebar_position: 16
---

# Object fit

- **Object-fit** là thuộc tính được sử dụng để resized `<img>` hay `<video>` để vừa với container. Để sử dụng thuộc tính này cần chỉ định `width` và `height` cho phần tử.

| Property     | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `object-fit` | `fill`: Đây là giá trị mặc định. Ảnh/video có thể bị bóp méo để vừa khít với toàn bộ box<br />`contain`: Ảnh/video sẽ được thay đổi kích thước nhưng vẫn giữ nguyên tỷ lệ như ban đầu sao cho vừa với box (không nhất thiết phải vừa khít với box, có thể vừa khít với box theo chiều ngang hoặc dọc)<br />`cover`: Ảnh/video sẽ có thể bị cắt bớt, thay đổi kích thước để vừa giữ nguyên tỷ lệ như ban đầu, vừa khít với toàn bộ box<br />`none`: Kích thước ảnh được giữ nguyên như ban đầu, nhưng không vượt quá kích thước của box |

:::note

- Điểm giống nhau giữa 2 giá trị `contain` và `cover`:
  - Đều giữ nguyên tỉ lệ kích thước ảnh (ảnh không bị méo)
- Điểm khác nhau:
  - `contain`: Ảnh có thể không fill toàn bộ box nhưng sẽ không bị cắt xén
  - `cover`: Ảnh fill toàn bộ box nhưng có thể bị cắt xén (không hiển thị đẩy đủ ảnh)

:::
