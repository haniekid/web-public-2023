# Nội dung Buổi 6: CSS GRID

👉Ứng dụng web ngày nay giao diện ngày càng phức tạp nên việc chỉ sử dụng flexbox thực sự vẫn chưa tối ưu. Vì thế mà CSS Grid được sinh ra để giải quyết vấn đề này!!
Tuy nhiên grid chưa được nhiều trình duyệt hỗ trợ như flexbox nên việc sử dụng vẫn còn chưa rộng rãi.

## **Tổng quan**

1. Grid container:

- Là phần tử cha chứa tất cả các phần tử con trực tiếp của nó nằm trong grid.
- Xác định vị trí ban đầu của các đường kẻ trong grid, cả dọc và ngang.

2. Grid items:

- Các phần tử con trực tiếp của grid container được ngăn cách nhau bằng các đường lines

3. Grid Columns: Phần đường dọc của các grid-item được gọi là cột

![Grid Columns](https://www.w3schools.com/css/grid_columns.png)

2. Grid Rows: Phần đường ngang của các grid-item được gọi là hàng
   ![Grid Rows](https://www.w3schools.com/css/grid_rows.png)

3. Grid Gaps: Khoảng cách giữa các cột/dòng gọi là gap

![Grid Gaps](https://www.w3schools.com/css/grid_gaps.png)

4. Grid Lines: Viền nằm giữa các cột và hàng.
   ![Grid Lines](https://www.w3schools.com/css/grid_lines.png)

5. Grid Tracks:
   ![Grid Tracks](https://evondev.com/wp-content/uploads/2018/08/grid-tracks.png)

   Mở F12 (Inspect Code) để nhìn thấy grid tracks một cách rõ ràng

   track columns/rows = columns/rows + 1;
   track start: 1

6. Grid Cells: Đơn vị nhỏ nhất, hay ô lưới, (vd: nằm giữa grid row line 1 và line 2, grid column line 1 và line 2)

7. Grid Area: Tổng không gian, có thể gồm nhiều cells

## **Sử dụng CSS GRID**

1. Định nghĩa một grid(lưới): biến một div thành một grid container

```css
.grid-container {
  display: grid;
}
```

2. Tạo các cột và dòng
   Có thể chia số cột và hàng tùy ý (thường dựa vào design thiết kế là 12 cột bằng nhau, đôi khi 8…)

Syntax:
`grid-template-columns`: [cột_1] [cột_2] [cột_3]... [cột_n];
`grid-template-rows`: [hàng_1] [hàng_2] [hàng_3]... [hàng_n];

```css
grid-template-columns: 100px 200px 150px;
grid-template-rows: 100px 200px 100px;
```

Đơn vị ở đây các bạn có thể dùng px, %, rem, em, vw, vh, auto,
_Ngoài ra: Grid có hỗ trợ thêm đơn vị fr (để phân bổ các items có tỷ lệ với nhau)_

### **fraction-unit(fr)**

```css
.grid-container {
  grid-template-columns: 1fr 2fr 1fr 3fr;
}
```

_Shorthand: repeat()_

```css
grid-template-columns: 10% repeat(4, 20%) 10%;
```

3. Grid-gap

- Tạo khoảng cách giữa các phần tử với nhau theo cột và hàng.
- Gồm 2 thuộc tính: `grid-row-gap` va `grid-column-gap`
- Shorthand: `grid-gap`: [grid-row-gap] [grid-column-gap];

4. Grid column, Grid row

- Xét vị trí cho các items

.grid-item{
`grid-column-start`
`grid-column-end`
`grid-row-start`
`grid-row-end`
}

_Shorthand: `grid-row`, `grid-column`_

```css
.grid-item {
  grid-column: <start-line> / <end-line>
  grid-row: <start-line> / <end-line>
}
```

5.  Grid areas:

```css
.grid-container {
  grid-template-areas: ;
}

.grid-item {
  grid-area: h1;
}
```

6.Span

.item {
grid-column: <start-line> / span <value>;
grid-row: <start-line> / span <value>;
}

7. grid-auto-flow

- grid implicit , explicit tracks: Khi container không đủ chỗ chứa cho item thì item sẽ bị rớt ra ngoài tạo nên 1 hàng mới và tạo nên các đường đánh dấu mới(gọi là Implicit Tracks)
- Vì vậy, khi muốn xét chiều cao cho phần tử thừa đó ta sử dụng `grid-auto-flow` kết hợp với `grid-auto-rows`

```css
.grid-container {
  grid-auto-flow: row;
  grid-auto-rows: 250px;
}
```

### Khác

Ngoài ra còn có thể sử dụng: `align-items`, `align-self`, `justify-content`, `justify-items`, `place-items`, `justify-self`, `place-self`,...

_👉Tìm hiểu thêm tại: https://css-tricks.com/snippets/css/complete-guide-grid/_

_Example:_

https://gridbyexample.com/examples/
