# Bootstrap

## Mục tiêu chung

* Nắm được template cơ bản của bootstrap, cách import bootstrap vào file html
* Khái niệm `responsive` cơ bản và hệ thống lưới (grid system) của bootstrap
* Các class cho các tag cơ bản của bootstrap

## Hướng dẫn chung

* Đọc tài liệu trên trang chủ của bootstrap, tập trung vào các phần sau:
	* [Getting started](http://getbootstrap.com/getting-started/)
	* [Basic CSS](http://getbootstrap.com/css/)
* Khuyến khích tìm hiểu thêm các phần components và javascript
	* [Components](http://getbootstrap.com/components/)
	* [Javscript](http://getbootstrap.com/javascript/)

## Guideline

### 1. Template cơ bản

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Bootstrap 101 Template</title>

    <!-- Bootstrap -->
    <link href="css/bootstrap.min.css" rel="stylesheet"><!-- file css của bootstrap -->

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
  </head>
  <body>
    <h1>Hello, world!</h1>

	<!-- Hiểu được tại sao phần javascript nên đặt ở cuối thẻ body: Phải đặt ở cuối vì nếu để ở đầu thì js sẽ được load trước và các thao tác trên DOM sẽ bị lỗi vì các phần tử HTML chưa được load
	 -->
    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="js/bootstrap.min.js"></script><!-- file javascript của bootstrap -->
  </body>
</html>
```

### 2. Grid system

```html
<!-- Khái niệm responsive? Responsive là thiết kế phù hợp với tất cả các kích thước màn hình-->
<!-- Hiểu được cách tạo grid trong bootstrap -->
<!-- Phân biệt được sự khác nhau giữa các prefix: .col-xs-, .col-sm-, .col-md-, .col-lg-: 
	- .col-xs-: dùng cho các thiết bị mobile < 768px
	- .col-sm-: dùng cho các thiết bị tablet >= 768px
	- .col-md-: dùng cho các desktop >= 992px
	- .col-lg-: dùng cho >= 1200px
-->

<div class="container-fluid"><!-- Phân biệt class container-fluid và container: container-fluid là chiều rồng là 100% màn hình hiện tại, còn container là chiều rộng cố định với các kích thước màn hình  -->

<div class="row">
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
</div>

<!-- Biết được cách mix các suffix trong cùng 1 row -->
<div class="row">
  <div class="col-md-2">.col-md-2</div>
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-6">.col-md-6</div>
</div>

<!-- Sử dụng nhiều prefix phục vụ cho responsive -->
<div class="row">
  <div class="col-lg-6 col-xs-12">khi to sẽ là 6, khi nhỏ sẽ là 12</div>
  <div class="col-lg-6 col-xs-12">khi to sẽ là 6, khi nhỏ sẽ là 12</div>
</div>

<!-- Cách sử dụng offset -->
<div class="row">
  <div class="col-md-3 col-md-offset-3">.col-md-3 .col-md-offset-3</div>
  <div class="col-md-3 col-md-offset-3">.col-md-3 .col-md-offset-3</div>
</div>

<!-- Cách lồng các cấu trúc grid -->
<div class="row">
  <div class="col-sm-9">
    Level 1: .col-sm-9
    <div class="row">
      <div class="col-xs-8 col-sm-6">
        Level 2: .col-xs-8 .col-sm-6
      </div>
      <div class="col-xs-4 col-sm-6">
        Level 2: .col-xs-4 .col-sm-6
      </div>
    </div>
  </div>
</div>

</div>
```

### 3. Các class cho các thẻ cơ bản

* [Typography](http://getbootstrap.com/css/#type)
* [Code](http://getbootstrap.com/css/#code)
* [Table](http://getbootstrap.com/css/#tables)
* [Image](http://getbootstrap.com/css/#images)
* [Button](http://getbootstrap.com/css/#buttons)
* [Form](http://getbootstrap.com/css/#forms)

Trong đó chú ý các vấn đề sau:

* Màu sắc của các class và ý nghĩa của các loại màu sắc đó
* Các group, ví dụ như `form-group`, `form-control`

### 4. Các class helper, utilities

* [Helper classes](http://getbootstrap.com/css/#helper-classes)
* [Responsive utilities](http://getbootstrap.com/css/#responsive-utilities)

## Bài tập

##### 1. Viết báo cáo trả lời cho các câu hỏi trong quá trình tìm hiểu.

##### 2. Áp dụng bootstrap, css lại trang jobeet, sử dụng một trong các [template](http://getbootstrap.com/getting-started/#examples) của bootstrap

(khuyến khích sử dụng template starter http://getbootstrap.com/examples/starter-template/)