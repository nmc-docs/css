---
sidebar_position: 24
---

# clip-path

- Thuộc tính CSS `clip-path` được sử dụng để cắt (clip) một phần của phần tử HTML, chỉ hiển thị vùng được xác định bởi một hình dạng hoặc đường dẫn cụ thể. Nó thường được dùng để tạo các hình dạng tùy chỉnh, chẳng hạn như hình tròn, đa giác, hoặc các hình dạng phức tạp khác.

## Các giá trị của `clip-path`

**1. Hình dạng cơ bản (Basic Shapes):**

- `circle()`: Tạo hình tròn. Cú pháp: `circle(radius at x y)`.
- `ellipse()`: Tạo hình elip. Cú pháp: `ellipse(rx ry at x y)`.
- `inset()`: Tạo hình chữ nhật với khoảng cách từ các cạnh. Cú pháp: `inset(top right bottom left)`.
- `polygon()`: Tạo đa giác với các điểm tọa độ. Cú pháp: `polygon(x1 y1, x2 y2, ...)`.
- `rect()`: (Đã lỗi thời, ít sử dụng) Tạo hình chữ nhật.

**2. Đường dẫn (Path):**

- `path()`: Sử dụng đường dẫn SVG để cắt. Cú pháp: `path('d="M10 10 L90 90"')`.

**3. URL:**

- `url()`: Tham chiếu đến một phần tử SVG `<clipPath>`.

## Một số ví dụ:

**1. Cắt hình tròn:**

```html
<div class="circle"></div>

<style>
  .circle {
    width: 200px;
    height: 200px;
    background: blue;
    clip-path: circle(50% at 50% 50%);
  }
</style>
```

- Kết quả: Hiển thị một hình tròn có bán kính bằng 50% chiều rộng của phần tử, tâm tại vị trí chính giữa (50%, 50%).

**2. Cắt hình chữ nhật với inset:**

```html
<div class="inset"></div>

<style>
  .inset {
    width: 200px;
    height: 200px;
    background: green;
    clip-path: inset(20px 40px 20px 40px);
  }
</style>
```

- Kết quả: Hiển thị một hình chữ nhật với khoảng cách 20px từ trên/dưới và 40px từ trái/phải.

**3. Tạo hiệu ứng Dropdown:**

- Ví dụ sau sử dụng TailwindCSS để tạo hiệu ứng Dropdown sử dụng `clip-path`:

```html
<div className="relative inline-block bg-gray-200 p-4 group">
  Hover me
  <div
    className="absolute top-full left-0 bg-red-200 shadow-lg p-4 transition-all duration-300 ease-in-out [clip-path:inset(0_0_100%_0)] group-hover:[clip-path:inset(0_0_0_0)]"
  >
    <ul className="list-none m-0 p-0">
      <li className="px-4 py-2 cursor-pointer hover:bg-gray-100">Item 1</li>
      <li className="px-4 py-2 cursor-pointer hover:bg-gray-100">Item 2</li>
      <li className="px-4 py-2 cursor-pointer hover:bg-gray-100">Item 3</li>
    </ul>
  </div>
</div>
```

:::note[Lưu ý]

- Trong CSS, khi sử dụng `clip-path` để cắt một phần tử, **phần không gian bị cắt không nhận sự kiện hover hay click**. Lý do là `clip-path` chỉ ảnh hưởng đến phần hiển thị trực quan của phần tử, nhưng vùng tương tác (hitbox) của phần tử vẫn dựa trên hình dạng gốc của nó, bao gồm cả phần bị cắt.
- Phần nằm ngoài vùng này sẽ bị ẩn đi (trở nên trong suốt), nhưng chúng vẫn tồn tại trong DOM và vẫn thuộc về phần tử.

:::
