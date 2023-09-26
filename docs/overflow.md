---
sidebar_position: 12
---

# Overflow

- Thuộc tính **overflow** chỉ định điều gì sẽ xảy ra nếu nội dung tràn vào hộp của phần tử
- Thuộc tính này chỉ định cắt nội dung hoặc thêm thanh cuộn khi nội dung của phần tử quá lớn để vừa với một khu vực được chỉ định

| Property     | Value                                                                                                                                                                                                                                                                                                                                                               |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `overflow`   | `visible`: phần nội dung tràn không được cắt bớt, nó sẽ tràn ra ngoài box<br />`hidden`: phần nội dung tràn sẽ được cắt bớt không hiển thị<br />`scroll`: phần nội dung tràn được cắt bớt, một thanh cuộn được thêm vào để xem phần còn lại của nội dung, thanh cuộn vẫn xuất hiện kể cả khi không tràn<br />`auto`: chỉ khi nội dung tràn mới xuất hiện thanh cuộn |
| `overflow-x` | Giống `overflow` nhưng là theo chiều ngang                                                                                                                                                                                                                                                                                                                          |
| `overflow-y` | Giống `overflow` nhưng là theo chiều dọc                                                                                                                                                                                                                                                                                                                            |

:::caution

Lưu ý: thuộc tính `overflow` chỉ hoạt động đối với phần tử được chỉ định chiều dài / chiều cao

:::
