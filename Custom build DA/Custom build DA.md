# CustomBuild là gì 
CustomBuild là công cụ quản lý phần mềm của DirectAdmin. Nó chủ yếu được chạy qua dòng lệnh cho đến năm 2014, khi một plugin được phát triển để cho phép người dùng quản lý phần mềm của 

# Build PHP
### 1 Ta truy cập vào thư mục custombuild

- cd /usr/local/directadmin/custombuild

### 2 Tạo 4 php mode :
- ./build set php1_mode php-fpm
- ./build set php2_mode php-fpm
- ./build set php3_mode php-fpm
- ./build set php4_mode php-fpm

<img src="img/1.PNG">

### 3 Gán các phiên bản php cho từng mode

- ./build set php1_release 5.6
- ./build set php2_release 7.2
- ./build set php3_release 7.3
- ./build set php4_release 7.4

<img src="img/3.PNG">

### 4 Kiểm tra lại phiên bản đã cài
<img src="img/4.png">


