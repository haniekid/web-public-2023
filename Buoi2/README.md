# Nội dung Buổi 2

### **CSS**

- CSS viết tắt của Cascading Style Sheets.
- CSS tạo phong cách và định kiểu cho trang web được viết dưới dạng ngôn ngữ đánh dấu, như là HTML.
- CSS giúp bạn kiểm soát bố cục của nhiều trang web cùng một lúc.

```html
Selector {property: value;}
```

![syntax](https://www.w3schools.com/css/img_selector.gif)

### **Các cách sử dụng css**

1. Inline CSS: Viết css trực tiếp trên đối tượng

```html
<h1 style="text-align: center;">
  Tớ là
  <span style="color: rgb(228, 97, 97); font-size: 24px; font-weight:bold"
    >Thu Hà</span
  >
  đây :3
</h1>
```

_Lưu ý: Khi cấu trúc trang web càng lớn, việc quản lý file sẽ khó khăn nếu sử dụng `Inline css`, vì nó chỉ áp dụng cho 1 element_

2. Internal CSS:

- Sử dụng thẻ `<style>` trong chính file html
- Đặt trong mục `<head></head>` của file html, được cấu trúc bằng cặp thẻ `<style></styl>`
- Viết css ở đầu trang web -> áp dụng kiểu dáng cho toàn bộ trang web

```html
<head>
  <style>
    h1 {
      color: white;
      background–color: purple;
    }
    .content {
      color: red;
      background–color: white;
      text-align: center;
    }
  </style>
</head>
```

3. External CSS:

- Viết css ở 1 file riêng biệt, đặt tên là `<name>.css` (\*.css)
- Có thể tham chiếu đến nhiều trang web khác nhau
- Sử dụng thẻ `<link>` để nhúng file vào phần `<head></head>` của file html

Ví dụ: file `style.css`

```css
body {
  font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
  color: darkseagreen;
}

.content {
  color: red;
  background–color: white;
  text-align: center;
}
```

file `index.html`

```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="myStyle.css" />
  </head>
  <body>
    <h1>H1 works!</h1>
    <p class="content">My content is loading...</p>
  </body>
</html>
```

### **Chú thích trong CSS**

- Chú thích sẽ được trình duyệt bỏ qua, không hiển thị trên trang web
- Chú thích 1 dòng hoặc nhiều dòng: `/* ........ */`
- Phím tắt: `Ctrl + /`

### **Các thuộc tính CSS cơ bản**

1. CSS Backgrounds

- `background-color`: màu nền

```css
background-color: rgba(0, 128, 0, 0.3);
```

- `background-image`: ảnh nền
- `background-attachment`: hình nền cuộn hay cố định

Ngoài ra còn có: background-position, background-attachment, background-repeat...

> Shorthand:
> background: background-color background-image background-repeat background-position

```css
background: #ffffff url("img_tree.png") no-repeat right top;
```

2. CSS Height, Width

- `length`: Set giá trị tùy chỉnh với đơn vị: px, cm, etc, vh, vw..
- `auto`: Giá trị mặc định theo trình duyệt
- `%`: Set giá trị theo phần trăm của phần tử cha
- `initial`: Set theo giá trị mặc định của nó
- `inherit`: Set theo giá trị kế thừa từ phần tử cha

`max-width`: Set chiều dài tối đa

```css
p {
  max-width: 40%;
}
```

`min-width`: Set chiều dài tối thiểu

_Tương tự cho `min-height` và `max-height`_

3. CSS Fonts

- `font-family`: tùy chỉnh font chữ
- `font-size`: tùy chỉnh kích thước chữ
- `font-weight`: chọn chế độ bình thường hay in đậm
- `font-style`: in thường, in nghiêng, hay in xiên
- `font-variant`: chữ in hoa có kích cỡ nhỏ hơn chữ in hoa bình thường) của một font chữ.

```css
h1 {
  font-style: italic;
  font-variant: small-caps;
  font-weight: bold;
  font-size: 14px;
  font-family: "Roboto", sans-serif;
}
```

> Shorthand:
> font: font-style font-variant font-weight font-size/line-height font-family

```css
h1 {
  font: italic small-caps bold 14px “Roboto”, sans-serif;
}
```

4. CSS Text

- `color`: màu chữ
- `text-align`: căn chỉnh text(trái, phải, giữa, căn đều)

```html
<p>
  Lorem ipsum dolor sit amet, consectetur adipisicing elit.
  <a href="#">Hey guys</a> Repellat, quia?
</p>
```

```css
p {
  text-indent: 50px;
  text-align: justify;
  letter-spacing: 3px;
}
```

Ngoài ra còn có : text-decoration, text-transform, letter-spacing, text-indent, ....

5. CSS Borders

> Shorthand:
> border: border-width border-style (required) border-color

```css
p {
  border: 2px solid red;
  border-radius: 5px;
}
```

`border-radius`: đường viền tròn

### **Box Model**

![syntax](https://images.viblo.asia/full/4192fc75-db46-405e-a8aa-67d9c5ba2e2a.png)

- Bất kì element nào trên một trang web, đều được trình duyệt (browser) thể hiện dưới dạng một hình chữ nhật
- `content`: Vùng chứa nội dung; thường là text, hình ảnh, video
- `padding`: Phần đệm trong suốt bao quanh content
- `border`: Đường viền bao quanh phần nội dung và phần đệm
- `margin`: Lề bao quanh vùng border

Ví dụ:

![syntax](https://images.viblo.asia/7b08f130-4ff1-4555-96f9-f7228665f28f.jpg)

`box-sizing`: mặc định là content-box

_Sử dụng `box-sizing : box-sizing `thì phần width sẽ bao gồm thêm cả padding và border_

![syntax](https://images.viblo.asia/48e74ebe-d32e-41db-b116-5dd5bbe36a40.jpg)

### **Reset CSS**

- Luôn đặt đầu tiên trong các file CSS

```css
* {
  margin: 0;
  padding: 0;
  border: 0;
  box-sizing: border-box;
}
```
