# Nội dung Buổi 1

### **I. Cài đặt IDE, Extensions**

1.  Visual Studio Code: Text Editor viết code tạo website
2.  Live Server
3.  Auto close tag, auto reame tag, HTML CSS support

### **HTML**

- Hypertext Markup Language: Ngôn ngữ đánh dấu siêu văn bản => **KHÔNG PHẢI NGÔN NGỮ LẬP TRÌNH**
- Được sử dụng để tạo và cấu trúc các thành phần trong trang web hoặc ứng dụng
- File HTML được tạo thành từ nhiều phần tử (elements)
- Một element thường có một cặp thẻ đóng và mở và chữa nội dung ở giữa
  ![enter image description here](https://blog.hubspot.com/hs-fs/hubfs/html-elements-diagram.png?width=650&name=html-elements-diagram.png)

### **Cấu trúc 1 file đuôi .html**

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <h1>The Main Heading</h1>
    <h2>A catchy subheading</h2>
    <p>First paragraph</p>
  </body>
</html>
```

- `<!DOCTYPE html>`: khai báo kiểu dữ liệu hiển thị
- `<html> và </html>`: cặp thẻ bắt buộc, element cấp cao nhất, có nhiệm vụ đóng gói tất cả nội dung của trang HTML
- `<head> và </head>`: khai báo các thông tin meta của trang web như: tiêu đề trang, charset
- `<title> và </title>`: cặp thẻ nằm bên trong thẻ `<head>`, dùng để khai báo tiêu đề của trang
- `<body> và </body>`: cặp thẻ dùng để đóng gói tất cả các nội dung sẽ hiển thị trên trang
- `<h1></h1>, <h2></h2>`: định dạng dữ liệu dạng heading. Thông thường có 6 cấp độ heading trong HTML, trải dài từ `<h1>` tới `<h6>`. Trong đó, `<h1>` là cấp độ heading cao nhất và `<h6>` là cấp độ heading thấp nhất.
- `<p> và </p>`: cặp thẻ chứa các đoạn văn bản của trang web

### **Các tag cơ bản thông dụng của HTML**

1. HTML Headings

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

_Lưu ý: một page chỉ có một thẻ h1_

2. HTML Paragraphs

- p: Hiển thị đoạn văn bản
- hr: Là 1 tag rỗng, không có end tag, dùng để hiển thị 1 đoạn line ngăn cách
- br: Là 1 tag rỗng, không có end tag, dùng để xuống dòng trong cùng 1 đoạn văn bản mà không cần phải thêm nhiều tag.

3. HTML Text Formatting

```html
<b>Chữ này in đậm</b>
<i>Chữ này bị nghiên</i>
<p>Chữ này bị<sub>thụt xuống</sub> và <sup>thụt lên</sup></p>
<u>Chữ này gạch chân</u>
```

4. HTML Links

```html
<a href="url">Liên kết</a>
```

5. HTML Images

```html
<img src="https://picsum.photos/100/100" alt="Some random image" />
```

6. HTML Tables

```html
<table style="width:100%">
  <caption>
    Monthly savings
  </caption>
  <thead>
    <tr>
      <th>Month</th>
      <th>Savings</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>January</td>
      <td>$100</td>
    </tr>
    <tr>
      <td>February</td>
      <td>$50</td>
    </tr>
  </tbody>
  <tfoot>
    <tr style="background-color: #FFE4B5">
      <td><b>Total: </b></td>
      <td style="color: red"><b>$150</b></td>
    </tr>
  </tfoot>
</table>
```

![enter image description here](https://images.viblo.asia/1a460544-c9e6-4eba-a07c-935f5e6cbc90.png)

Ngoài các tags hay sử dụng trong table như: `<table>, <tr>, <th>, <td>, <thead>, <tbody>, <tfoot>` thì còn 3 tags nữa ít sử dụng hơn.

- `<caption>`: Hiển thị cation của table.
- `<colgroup>`: Được sử dụng để định dạng cho một nhóm cột trong <table>.
- `<col>`: Được sử dụng để xác định giá trị thuộc tính cho một hoặc nhiều cột trong `<table>`
  <br/>
- CSS **border-collapse**: Thuộc tính thu gọn lại border cho các cell trong table. Thường được set default là 0.
- CSS **border-spacing:** Thuộc tính dùng để set các khoảng cách giữa các cell trong table. Thường được set default là 0.
- Attr **colspan**: Gộp nhiều cột lại với nhau
- Attr **rowspan**: Gộp nhiều dòng lại với nhau.

7. HTML Lists

```html
<ul>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ul>
<ol>
  <li>Coffee</li>
  <li>Tea</li>
  <li>Milk</li>
</ol>
```

| **unordered `<ul>`** | **ordered `<ol>`** |
| -------------------- | ------------------ |
| list-style-type      | type               |
| disc                 | 1                  |
| circle               | A                  |
| square               | a                  |
| none                 | I                  |
|                      | i                  |
