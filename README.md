# TaoLayoutChoTrangWeb
Bước 1: Tạo file header.php. Đây là file hiển thị phần header của layout.

Mã HTML:

<h1>City Gallery</h1> 
Mã css để định dạng phần header:

div.container {
    width: 100%;
    border: 1px solid gray;
}
header, footer {
    padding: 1em;
    color: white;
    background-color: black;
    clear: left;
    text-align: center;
} 
Bước 2: Tạo file nav.php. Đây là file hiển thị menu của layout.

Mã HTML:

<ul>
  <li><a href="#">London</a></li>
  <li><a href="#">Paris</a></li>
  <li><a href="#">Tokyo</a></li>
</ul>
Mã css để định dạng phần header:

nav {
    float: left;
    max-width: 160px;
    margin: 0;
    padding: 1em;
}
nav ul {
    list-style-type: none;
    padding: 0;
}
nav ul a {
    text-decoration: none;
}
Bước 3: Tạo file content.php. Đây là file hiển thị phần nội dung chính của layout.

Mã HTML:

<h1>London</h1>
<p>London is the capital city of England. It is the most populous city in the  United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
<p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
Mã css để định dạng phần header:

article {
    margin-left: 170px;
    border-left: 1px solid gray;
    padding: 1em;
    overflow: hidden;
}
Bước 4: Tạo file footer.php. Đây là file hiển thị phần footer của layout.

Mã HTML:

Copyright &copy; W3Schools.com 
Code css để định dạng phần footer (chung selector với phần header):

header, footer {
    padding: 1em;
    color: white;
    background-color: black;
    clear: left;
    text-align: center;
}
Bước 5: Tạo file index.php. File chứa mã HTML cho toàn bộ layout và nhúng các file con vừa tạo ở trên vào từng phần tương ứng.

Sử dụng lệnh include để đưa từng nội dung của các trang vào.

<?php   include("tentrangcanduavao.php"); ?>
Mã HTML:

<html>
    <head>
        <link rel="stylesheet" type="text/css"href="style.css">
    </head>
    <body>
        <div class="container">
            <header><?php  include "header.php";  ?></header>
            <nav><?php include "nav.php";  ?></nav>
            <article> <?php include "content.php"; ?></article>
            <footer><?php include "footer.php";?></footer>
        </div>
    </body>
</html>
Bước 6: Chạy chương trình. 

- Truy cập trang index.php và quan sát kết quả.

- Thay lệnh include bằng lệnh require, so sánh kết quả. 
