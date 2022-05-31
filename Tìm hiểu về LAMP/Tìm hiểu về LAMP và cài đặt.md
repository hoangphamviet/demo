## I Tìm hiểu về LAMP 
- 1 LAMP là gì ?
- LAMP là chữ viết tắt thường được dùng để chỉ sự sử dụng các phần mềm Linux, Apache, MySQL và ngôn ngữ văn lệnh PHP hay Perl hay Python để tạo nên một môi trường máy chủ Web có khả năng chứa và phân phối các trang Web động.
- Các chức năng cụ thể các bạn có thể hiểu nhanh là LAMP hoạt động từ các phần mềm Linux, với máy chủ web là Apache, máy chủ cơ sở dữ liệu MariaDB hoặc MySQL và nội dung file động được xử lý bởi PHP.
- LAMP là dạng mã nguồn mở với lợi thế miễn phí, nên các năm gần đây LAMP luôn được cộng động tin tưởng sử dụng bởi tính ổn định, dễ dàng cài đặt cũng như dễ dàng vận hành.
## Cài đặt LAMP
- Bước 1: Cài đặt Apache Web Server
- Bước 2: Cài đặt MariaDB
+ yum install -y mariadb mariadb-server
+ systemctl start mariadb :
khởi động dịch vụ mariadb
- Bước 3 : Cài đặt PHP
+ yum install -y yum-utils http://rpms.remirepo.net/enterprise/remi-release-7.rpm
- Sau khi cài đặt gói Remi xong, các bạn cần chọn phiên bản PHP mà mình cần cài đặt và kích hoạt gói chứa phiên bản PHP đó. Ở hướng dẫn này mình sẽ cài đặt PHP 8.0 nên sẽ kích hoạt gói bằng lệnh sau.
- yum-config-manager --enable remi-php80
- Khi module remi-80 của PHP đã được bật, có thể tiến hành cài đặt PHP và các PHP Extension cần thiết bằng lệnh
+ yum install -y php php-ldap php-zip php-embedded php-cli php-mysql php-common php-gd php-xml php-mbstring php-mcrypt php-pdo php-soap php-json php-simplexml php-process php-curl php-bcmath php-snmp php-pspell php-gmp php-intl php-imap perl-LWP-Protocol-https php-pear-Net-SMTP php-enchant php-pear php-devel php-zlib php-xmlrpc php-tidy php-opcache php-cli php-pecl-zip unzip gcc .
- Bước 4: Cấu hình Virtual Host (Apache):
- Virtual Host là file cấu hình trong Apache để cho phép nhiều Domain cùng chạy trên một máy chủ. Tất cả các file vhost sẽ nằm trong thư mục tại đường dẫn  /etc/httpd/conf.d/.

- website là hoangphamviet.com và vhost của nó tương ứng sẽ là /etc/httpd/conf.d/hoangphamviet.com.conf
- tạo file hoangphamviet.com.conf
+ touch /etc/httpd/conf.d/hoangphamviet.com.conf
- chỉnh sửa file hoangphamviet.com.conf
+ nano /etc/httpd/conf.d/hoangphamviet.com.conf

<img src="img/1.PNG">


- tạo thư mục chứa mã nguồn website:
+ mkdir -p /var/www/hoangphamviet.com/html  
- Phân quyền thực thi cho thư mục  :  
chown -R apache:apache /var/www/hoangphamviet.com
- khởi động lại dịch vụ apache:
+ systemctl restart httpd 
  
-  cấu hình file hosts trên window server để truy cập:
+ Windows/System32/drivers/etc/hosts

<img src="img/2.PNG">

- Truy cập 
<img src="img/3.PNG">