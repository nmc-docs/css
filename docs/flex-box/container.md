---
sidebar_position: 2
---

# Container

## Thuộc tính áp dụng cho flex container

| Property          | Value                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `display`         | `flex`: chỉ định kiểu hiển thị flexbox cho container                                                                                                                                                                                                                                                                                                                                                     |
| `flex-direction`  | `row`: các items sẽ được hiển thị theo chiều ngang <br />`row-reverse`: các item sẽ được hiển thị theo chiều ngang nhưng thứ tự bị đảo lộn lại <br />`column`: các items sẽ được hiển thị theo chiều dọc <br />`column-reverse`: các item sẽ được hiển thị theo chiều dọc nhưng thứ tự bị đảo lộn lại                                                                                                    |
| `justify-content` | `flex-start:` các items sẽ được đặt ở đầu của container<br />`flex-end`: các items sẽ được đặt ở cuối của container<br />`center`: các items sẽ được đặt ở giữa của container<br />`space-between`: Tạo khoảng trống đều nhau **GIỮA** các items <br />`space-around`: Tạo khoảng trống ở **TRƯỚC, GIỮA, SAU** các items<br />`space-evenly`: Tạo khoảng trống đều nhau ở **TRƯỚC, GIỮA, SAU** các items |
| `gap`             | `apx bpx` <br />**a** : độ rộng khoảng trống giữa các item theo chiều ngang <br />**b** : độ rộng khoảng trống giữa các item theo chiều dọc                                                                                                                                                                                                                                                              |
| `align-items`     | `stretch`: tất cả items sẽ trải dài hết container `br`: tất cả items sẽ ở chính giữa container <br />`flex-start`: tất cả items sẽ ở trên cùng của container <br />`flex-end`: tất cả items sẽ ở dưới cùng của container                                                                                                                                                                                 |
| `flex-wrap`       | Khi ta kéo nhỏ trình duyệt, các items của bên trong container có thể bị thu hẹp, không giữ được hình dạng ban đầu. Vì vậy `flex-wrap` giúp chúng ta có thể đưa các items không đủ chỗ để hiển thị sẽ hiển thị ở phía dưới hoặc trên <br />`wrap`: Các items không đủ chỗ để hiển thị sẽ hiển thị xuống bên dưới <br />`wrap-reverse`: Các items không đủ chỗ để hiển thị sẽ hiển thị ở bên trên          |

- Hình ảnh minh họa các giá trị của thuộc tính `justify-content` với `flex-direction: row`:

![1695740514889](image/container/1695740514889.png "Flex start")

![1695740525994](image/container/1695740525994.png "flex-end")

![1695740541945](image/container/1695740541945.png "center")

![1695740554063](image/container/1695740554063.png "space-between")

![1695740566580](image/container/1695740566580.png "space-around")

![1695740585635](image/container/1695740585635.png "space-evenly")

- Hình ảnh minh họa các giá trị của thuộc tính `align-items `với `flex-direction: row`:

![1695740612120](image/container/1695740612120.png "Ví dụ lần lượt cho các giá trị stretch, center, flex-start, flex-end")
