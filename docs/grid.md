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
| `grid-template-rows`    | `x1px x2px x3px ...`: Thiết lập chiều cao của từng hàng (hàng 1,2,3,...)<br />`auto auto auto...`: Chiều cao của từng hàng sẽ được tự động tính toán dựa trên chiều cao của container<br />`repeat(x, ypx)`: Thiết lập `x` hàng, mỗi hàng cao `y px`<br />`repeat(x, minmax(0, 1fr))`: Thiết lập x hàng, chiều cao mỗi hàng tự động được tính sao cho vừa khớp với container                                 |
| `grid-template-columns` | `x1px x2px x3px ...`: Thiết lập độ rộng của từng cột (cột 1,2,3,...)<br />`auto auto auto...`: Chiều rộng của từng cột sẽ được tự động tính toán dựa trên độ rộng của container<br />`repeat(x, ypx)`: Thiết lập `x` cột, mỗi cột rộng `y px`<br />`repeat(x, minmax(0, 1fr))`: Thiết lập `x` cột, chiều rộng mỗi cột tự động được tính sao cho vừa khớp với container                                       |

## Thuộc tính áp dụng cho grid items

| Property      | Value                                                                                                                                                                                     |
| ------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `grid-area`   | `a / b / span c / span d`<br />**a** : chỉ số hàng của item<br />**b** : chỉ số cột của item<br />**c** : số lượng hàng mà item sẽ trải dài<br />**d** : số lượng cột mà item sẽ trải dài |
| `grid-row`    | `x / span y`<br />**x**: chỉ số hàng của item<br />**y**: số lượng hàng mà item sẽ trải dài                                                                                               |
| `grid-column` | `x / span y`<br />**x**: chỉ số cột của item<br />**y**: số lượng cột mà item sẽ trải dài                                                                                                 |

## Đơn vị `fr` và `auto` khi chia hàng/cột trong grid

### 👉 **`1fr`**

- `fr` = _fractional unit_ = đơn vị tỷ lệ linh hoạt.
- `1fr` nghĩa là hàng/cột đầu tiên sẽ chiếm **phần không gian còn lại** sau khi các hàng/cột khác (như `auto`) đã chiếm xong phần kích thước của chúng.
- Nó tự co giãn để lấp đầy khoảng trống.

### 👉 **`auto`**

- `auto` nghĩa là hàng này sẽ có độ cao **tự động**, tùy theo nội dung bên trong.
- Nếu nội dung cao 50px → hàng là 50px.
- Nếu nội dung nhiều hơn → hàng tự mở rộng tương ứng, nhưng **không chiếm toàn bộ không gian**, chỉ vừa đủ.

## Giá trị `repeat()`

:::info

- Hàm `repeat(x, size)` để chỉ định grid chia làm `x` hàng/cột, mỗi hàng/cột sẽ có chiều rộng/cao là `size`

:::

- Ví dụ: `repeat(3, 100px)` → 3 cột, mỗi cột 100px.

- Ví dụ: `repeat(4, minmax(0, 1fr))`:

  - Định nghĩa kích thước cột có thể:
    - **Nhỏ nhất** : `0` → có thể co lại đến 0 nếu thiếu không gian.
    - **Lớn nhất** : `1fr` → khi đủ không gian, mỗi cột sẽ chia đều theo tỷ lệ phần còn lại.
  - 🎯 Kết quả cuối cùng: `repeat(x, minmax(0, 1fr))` = x cột, đều nhau, co giãn an toàn, không gây overflow.

  - Lý do thường dùng `minmax(0, 1fr)` thay vì 1fr trực tiếp:
    - Tránh lỗi overflow nội dung
    - Trong nhiều layout, `1fr` có thể không nhỏ hơn nội dung bên trong, gây tràn hoặc làm bố cục bị rối.
      `minmax(0, 1fr)` cho phép co lại về 0, nên bố cục luôn mượt.

- Ví dụ tạo **4 cột chia đều**:

```css
grid-template-columns: repeat(4, minmax(0, 1fr));
```

- Ví dụ tạo lưới **tự động chia đều** tùy width container:

```css
grid-template-columns: repeat(auto-fit, minmax(0, 1fr));
```
