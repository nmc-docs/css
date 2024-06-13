---
sidebar_position: 17
---

# Z-index

- Thuộc tính `z-index` thiết lập thứ tự xếp chồng nhau của một thành phần vị trí. Thứ tự chồng nhau được sắp xếp dựa theo giá trị số, thành phần HTML nào có chỉ số `z-index` cao hơn sẽ nằm trên, ngược lại sẽ nằm dưới, giá trị mặc định là 0, có thể sử dụng số âm.
- `z-index` hoạt động khi phần tử có `position` là `relative`, `fixed`, `absolute`.
- `z-index` của một phần tử phụ thuộc vào `z-index` của cha gần nhất nó, luôn \<= `z-index` của thẻ cha

| Property  | Value          |
| --------- | -------------- |
| `z-index` | Một **number** |
