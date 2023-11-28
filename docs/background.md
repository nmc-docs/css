---
sidebar_position: 8
---

# Background

- **Background** dùng để tạo kiểu cho nền.

| Property                | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `background-color`      | Tên màu ở hệ RGB hoặc hex<br />`transparent`: màu trong suốt                                                                                                                                                                                                                                                                                                                                                                                                             |
| `background-image`      | Tạo kiểu nền là hình ảnh hoặc màu linear gradient<br />`linear-gradient(...)`<br />`url("Link to image")`                                                                                                                                                                                                                                                                                                                                                                |
| `background-attachment` | `scroll`: ảnh nền bị cuộn lên khi ta cuộn xuống<br />`fixed`: ảnh nền luôn được cố định khi ta cuộn lên/xuống                                                                                                                                                                                                                                                                                                                                                            |
| `background-repeat`     | `no-repeat`: không lặp lại ảnh nền<br />`repeat`: nếu kích thước ảnh nền không vừa với container, ảnh nền đó sẽ được lặp lại theo chiểu dọc lẫn chiều ngang để phủ toàn bộ container<br />`repeat-x`: ảnh nền lặp lại theo chiều ngang<br />`repeat-y`: ảnh nền lặp lại theo chiều dọc                                                                                                                                                                                   |
| `background-position`   | `top`, `bottom`, `left`, `right`, `center`: Thiết lập vị trí của ảnh nền so với container (trên, dưới, trái, phải, giữa)                                                                                                                                                                                                                                                                                                                                                 |
| `background-size`       | Thiết lập kích thước cho hình nền<br />`apx bpx`: Thiết lập kích thước hình nền ở dạng pixel, giá trị thứ nhất là chiều dài, giá trị thứ hai là chiều cao<br />`x% y%`: Thiết lập kích thước ở dạng phần trăm so với kích thước của phần tử cha<br />`cover`: Thay đổi kích thước của ảnh nền sao cho nó vừa khớp với container, mặc khi kích thước của ảnh nền bị méo, bị xén bớt<br />`contain`: Thay đổi kích thước hình nền để đảm bảo hình ảnh được hiển thị đầy đủ |
| `background-clip`       | `border-box`: ảnh nền được bao phủ từ phần border của container trở vào trong<br />`padding-box`: ảnh nền được bao phủ từ phần padding của container trở vào trong<br />`content-box`: ảnh nền được bao phủ từ phần content của container trở vào trong<br />`text`: ảnh nền chỉ bao phủ bên text                                                                                                                                                                        |

:::tip

Ta thường sử dụng `background-clip: text` để làm chữ có màu linear gradient

Ví dụ:

```css
h1 {
  background-image: linear-gradient(
    268.67deg,
    rgb(255, 240, 102) 15.69%,
    rgb(255, 163, 26) 55.54%,
    rgb(255, 0, 115) 99%
  );
  background-clip: text;
  -webkit-background-clip: text;
  color: transparent;
}
```
