---
sidebar_position: 18
---

# Animation

- **Định nghĩa**: animation cho phép tạo các hiệu ứng phức tạp hơn bằng cách sử dụng các **keyframe** để xác định nhiều giai đoạn của hiệu ứng.
- **Cách hoạt động** :
  - Có thể chạy tự động mà không cần sự kiện kích hoạt.
  - Dựa trên `@keyframes` để xác định các bước thay đổi của thuộc tính CSS.
  - Hỗ trợ lặp lại, tạm dừng, và kiểm soát chi tiết hơn.

## Sự khác nhau giữa Transition và Animation

| Tiêu chí        | Transition                                     | Animation                                |
| --------------- | ---------------------------------------------- | ---------------------------------------- |
| **Kích hoạt**   | Cần sự kiện (hover, click, toggle class, v.v.) | Có thể tự động hoặc do sự kiện           |
| **Độ phức tạp** | Đơn giản, chuyển đổi giữa 2 trạng thái         | Phức tạp, nhiều trạng thái qua keyframes |
| **Lặp lại**     | Không hỗ trợ lặp lại                           | Hỗ trợ lặp lại (infinite hoặc số lần)    |
| **Kiểm soát**   | Giới hạn, chỉ định thuộc tính cụ thể           | Linh hoạt, kiểm soát nhiều giai đoạn     |

![1695743254839](image/animation/1695743254839.png "Ảnh mô tả sự khác nhau giữa Transition với Animation")

## Định nghĩa một animation

- Cú pháp:

```css
@keyframes animationName {
    keyframes-selector { css-styles }
}
```

:::info

Trong đó:

- **animationName** : tên của hiệu ứng
- **keyframes-selector** : Các mốc của animation, giá trị từ 0-100% hoặc `from` (tương đương 0%), `to` (tương đương 100%)
- **css-styles** : tạo kiểu CSS cho animation

:::

- Ví dụ:

```css
@keyframes moving {
  0% {
    top: 0px;
  }
  25% {
    top: 200px;
  }
  50% {
    top: 100px;
  }
  75% {
    top: 200px;
  }
  100% {
    top: 0;
  }
}
```

```css
@keyframes moving {
  from {
    top: 0;
    width: 100px;
    background-color: red;
  }
  to {
    top: 200px;
    width: 300px;
    background-color: yellow;
  }
}
```

## Các thuộc tính cho Animation

| Property                    | Value                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| --------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `animation-name`            | Là tên của hiệu ứng ([animationName](#định-nghĩa-một-animation))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| `animation-duration`        | `as`: Chỉ định chu kỳ của animation                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| `animation-timing-function` | `linear`: Tốc độ của animation ổn định từ khi bắt đầu đến khi kết thúc<br />`ease`: (Giá trị mặc định). Hiệu ứng ban đầu chậm, sau đó nhanh và kết thúc chậm<br />`ease-in`: Hiệu ứng ban đầu chậm<br />`ease-out`: Hiệu ứng kết thúc chậm<br />`ease-in-out`: Hiệu ứng ban đầu và kết thúc đều chậm                                                                                                                                                                                                                                                                                                                                |
| `animation-delay`           | `as`: Chỉ định thời gian delay trước khi animation chạy                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| `animation-iteration-count` | Một**number** : chỉ định số lần animation chạy<br />`infinite`: Chỉ định animation sẽ chạy vô hạn không dừng                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| `animation-direction`       | `normal`: (Giá trị mặc định). Animation sẽ chạy theo hướng ban đầu được chỉ định<br />`reverse`: Animation chạy ngược với hướng ban đầu được chỉ định. Ví dụ chỉ định animation chạy từ trái sang phải. Nhưng với giá trị `reverse`, animation sẽ chạy theo hướng từ phải sang trái<br />`alternate`: Animation sẽ chạy theo kiểu chạy tới - chạy lui. Hoạt động khi thuộc tính `animation-iteration-count` có giá trị từ **2** trở lên hoặc `infinite`<br />`alternate-reverse`: Animation sẽ chạy theo kiểu chạy lui - chạy tới. Hoạt động khi thuộc tính `animation-iteration-count` có giá trị từ **2** trở lên hoặc `infinite` |
| `animation-fill-mode`       | `forwards`: Khi animation chạy xong. Phần tử sẽ đứng yên tại vị trí nó kết thúc<br />`backwards`: Khi animation chạy xong. Phần tử sẽ quay trở lại vị trí ban đầu nó xuất phát                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| `animation-play-state`      | `paused`: Chỉ định animation dừng lại<br />`running`: Chỉ định animation hoạt động                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| `animation`                 | **Name** **Duration** **Timing-function** **Delay** **Iteration-count** **Direction** **Fill-mode** **Play-state** <br />Cú pháp viết tắt cho tất cả thuộc tính trên theo thứ tự được chỉ định                                                                                                                                                                                                                                                                                                                                                                                                                                      |

:::caution[Lưu ý]

- Trong React, nếu một component có animation thì animation đó sẽ chỉ chạy 1 lần duy nhất khi **component mounted**, còn component re-render thì nó sẽ **KHÔNG** chạy lại.
- Còn trong trường hợp ta có 2 class định nghĩa 2 animation khác nhau và chỉ định chúng trong class theo điều kiện thì lúc này nó sẽ được chạy lại, ví dụ:

```tsx
import React from "react";

const MyComponent = () => {
  const [animationType, setAnimationType] = React.useState("in");
  return (
    <>
      <div
        className={`${animationType === "in" ? "animated-in" : "animated-out"}`}
      >
        MyComponent
      </div>
      <button
        onClick={() => setAnimationType(animationType === "in" ? "out" : "in")}
      >
        Toggle animation
      </button>
    </>
  );
};

export default MyComponent;
```

👉`animationType` từ `"in"` sang `"out"`: `animated-out` sẽ được chạy và ngược lại. Còn nếu `animationType` không thay đổi (`"in" -> "in", "out" -> "out"`) thì sẽ không chạy lại

:::
