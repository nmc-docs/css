---
sidebar_position: 13
---

# Transition

- **Transition** tạo hiệu ứng thay đổi giữa **HAI** trạng thái của một hay nhiều thuộc tính

| Property                     | Value                                                                                                                                                                                                                               |
| ---------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `transition-property`        | **Property** : chỉ định thuộc tính cụ thể để tạo hiệu ứng<br />`all`: tất cả các thuộc tính đều được chỉ định hiệu ứng                                                                                                              |
| `transition-duration`        | `as`: Chỉ định thời gian mà hiệu ứng hoạt động                                                                                                                                                                                      |
| `transition-timing-function` | `linear`: Tạo hiệu ứng với cùng tốc độ từ đầu đến cuối<br />`ease-in`: Tạo hiệu ứng với tốc độ ban đầu chậm<br />`ease-out`: Tạo hiệu ứng với tốc độ kết thúc chậm<br />`ease-in-out`: Tạo hiệu ứng với tốc độ chậm từ đầu đến cuối |
| `transition-delay`           | `as`: Chỉ định khoảng thời gian delay trước khi transition hoạt động                                                                                                                                                                |
| `transition`                 | **Property - Duration - Timing Function - Delay** : là cú pháp viết tắt cho 4 thuộc tính trên theo thứ tự.<br />Thuộc tính này có thể gồm nhiều bộ, mỗi bộ cách nhau bởi dấu `,`<br />Ví dụ: `transition: width 2s, height 4s;`     |

- Ví dụ về transition:

```css
.transition {
  width: 50px;
  height: 50px;
  background-color: blue;
  transition: all 2s linear;
}

.transition:hover {
  width: 300px;
}
```
