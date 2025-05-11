---
sidebar_position: 2
---

# Width, height

| Property     | Value                                                                                                                                                                                            |
| ------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `width`      | `apx, a%`: Thiết lập chiều rộng cho phần tử, nếu đơn vị là % thì kích thước sẽ tính theo % chiều rộng của phần tử cha<br />`fit-content`: chiều rộng phần tử vừa khít với nội dung bên trong nó  |
| `height`     | `apx, a%`: Thiết lập chiều cao cho phần tử, nếu đơn vị là % thì kích thước sẽ tính theo % chiều cao của phần tử cha<br />`fit-content`: chiều cao của phần tử vừa khít với nội dung bên trong nó |
| `min-width`  | `apx, a%`: Thiết lập chiều rộng tối thiểu cho phần tử                                                                                                                                            |
| `min-height` | `apx, a%`: Thiết lập chiều cao tối thiểu cho phần tử                                                                                                                                             |
| `max-width`  | `apx, a%`: Thiết lập chiều rộng tối đa cho phần tử                                                                                                                                               |
| `max-height` | `apx, a%`: Thiết lập chiều cao tối đa cho phần tử                                                                                                                                                |

:::note[Chú ý]

- Nếu thuộc tính trên có giá trị phần trăm thì:
  - Nếu phần tử có `position: relative`: Được tính theo phần trăm phần **content** của phần tử cha.
  - Nếu phần tử có `position: absolute`: Được tính theo phần trăm phần của phần **padding + content + border** của phần tử cha.
  - Xem thêm về **content**, **padding**, **border** [tại đây](./layout-of-element)
- Đối với phần tử có `display: block` thì giá trị mặc định của **width là 100% so với phần tử cha**. Còn nếu nó có `display: inline` hoặc `display: inline-block` thì width sẽ phụ thuộc vào nội dung bên trong nó.
- Mặc dù giá trị mặc định là `width: 100%` đối với phần tử có `display: block` nhưng width của nó có thể lớn hơn phần tử cha và tràn ra ngoài nếu nội dung bên trong quá dài. Khi đó ta phải ép `width: 100%` hoặc sử dụng [overflow](./overflow)

:::
