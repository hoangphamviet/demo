# Tìm hiểu về Plesk 
## Plesk là gì ?
### - Plesk là một phần mềm quản lý hosting trên windows và linux, hỗ trợ các dịch vụ về website , tên miền (domain), cơ sở dữ liệu, email, DNS,...

<img src="img/1.PNG">

## Ưu điểm và nhược điểm 

### Ưu điểm 
- Dễ dàng sử dụng trên cả hai nền tảng hệ điều hành window và linux.
- Có độ ổn định và tin cậy cao
- Có đầy đủ các tính năng hữu ích từ cơ bản đến nâng cao, hỗ trợ việc quản lý hosting và website.
- Giao diện đơn giản , thân thiện với người dùng.
- Tính linh hoạt và tiện dụng cao. Phần mềm Plesk là hệ thống quản lý hosting  có tích hợp thiết kế web , thanh toán tự động và giao diện storefront SaaS.
- Dễ dàng thiết lập nhiều hosting cùng 1 lúc dễ dàng dựa trên cấu hình định sẵn.
- Có thể tạo ra nhiều tài khoản FTP kết hợp với cấu trúc web linh hoạt.

### Nhược điểm
- Mối lo ngại về bảo mật: Mặc dù Plesk đã làm rất tốt trong việc tiếp nhận và sửa chữa các lỗ hổng bảo mật , nhưng điểm mấu chốt là có 1 lịch sử lo ngại về bảo mật.
- Vấn đề sao lưu và khôi phục: Plesk làm tốt hơn nhiều thứ so với các đối thủ cạnh tranh nhưng lại thua ở các chức năng quan trọng này. Tùy chọn sao lưu và khôi phục cần nhiều dung lượng đĩa trống và hầu hết các trường hợp thì các tệp lớn phải được chuyển sang máy chủ phụ.
- Phức tạp: Không giống như Cpanel , việc cài đặt các tập lệnh không phải là dễ dàng. Do đó đối với người mới có thể gặp chút khó khăn cần làm quen.

# II Cài đặt Plesk trên windows server

### B1 tải bộ cài đặt tự động trên trang “http://autoinstall-win.pp.parallels.com/plesk-installer.exe”

### B2 mở file  “plesk-installer” vừa được tải về ở trên và chạy file cài đặt.

### B3 hệ thống sẽ tự mở trang web cài đặt Plesk hoặc ta có thể truy cập trực tiếp “http://localhost:8447” để vào trang cài đặt, sau đó ta nhập thông tin tài khoản mật khẩu để đăng nhập.

<img src="img/6.PNG">

### B4 Chọn cài đặt hoặc gỡ bỏ Plesk , chọn khởi tạo mật khẩu cho trình cài đặt


<img src="img/7.PNG">

### B5 Sau đó ta tiến hành cài đặt , rồi ấn ok hoàn tất

<img src="img/2.PNG">

<img src="img/3.PNG">

### B6 Sau đó ta đăng nhập vào hệ thống, điền 1 số thông tin

<img src="img/4.PNG">


### B7 Sau khi hoàn tất , ta thấy giao diện như sau

<img src="img/5.PNG">


# III Một số thao tác chức năng của Plesk

### 1 Thêm người dùng

- Tại giao diện ta chọn vào người dùng

<img src="img/9.PNG">

- Chọn tạo người dùng

<img src="img/10.PNG">

- Điền thông tin cho tài khoản

<img src="img/11.PNG">

- Ấn đồng ý để xác nhận

<img src="img/13.PNG">

- Ta thấy tài khoản sẽ được tạo thành công

<img src="img/12.PNG">

### 2 Thêm tên miền, tạo 1 trang web

- Ta chọn vào trang web và tên miền

<img src="img/14.PNG">

- Chọn vào thêm miền

<img src="img/15.PNG">

- Lựa chọn 1 trong 5 phương pháp tạo trang web , ở đây ta lựa chọn tạo trang với wordpress

<img src="img/16.PNG">

- Chọn tên miền tạm thời nếu chưa có tên miền đăng ký và chọn thêm tên miền

<img src="img/18.PNG">

- Đợi quá trình cài đặt diễn ra

<img src="img/19.PNG">

- Chọn cài đặt

<img src="img/20.PNG">

- Sau đó ta xem được trang wp vừa tạo

<img src="img/21.PNG">



### 3 Tạo thêm các service plan.
- Ta vào giao diện nhà cung cấp dịch vụ

<img src="img/22.PNG">

- Chọn vào gói dịch vụ

<img src="img/23.PNG">

- Thêm gói dịch vụ

<img src="img/24.PNG">

- Đặt tên cho gói dịch vụ

<img src="img/25.PNG">

- Xác định các tài nguyên được cung cấp cho gói dịch vụ.
<img src="img/26.PNG">
<img src="img/27.PNG">

- Dung lượng cho plan
- Thông báo khi dung lượng đạt đến ngưỡng nào đó
- Lưu lượng dữ liệu chuyển từ các web. 
- Thông báo khi dung lượng đạt đến ngưỡng nào đó.
- Số lượng tên miền chính, tên miền phụ, bí danh.
- Số lượng hộp thư mail, dung lượng hòm thư , tổng dung lượng lưu trữ của các hộp thư ,...
- Số lượng tài khoản FTP được sử dụng để truy cập file và các thư mục.
- Số lượng cơ sở dữ liệu tối đa được tạo.
- Dung lượng tối đa của MYSQL/ MS SQL
- Dung lượng tối đa của file database
- Dung lượng tối đa của file log
- Thời hạn của plan.
- Số lượng trang web wp cài đặt và quản lý tối đa, các bản sao lưu, số lượng trang web có chức năng cập nhật thông minh
- Thu thập dữ liệu của rank tracker

- Ấn đồng ý để tạo plan
- Ta thấy plan đã được tạo thành công

<img src="img/29.PNG">

### 4 Gán plan cho người dùng.

- Chọn khách hàng, thêm khách hàng
<img src="img/30.PNG">

- Điền các thông tin, chọn plan muốn gán vào.

<img src="img/31.PNG">
<img src="img/32.PNG">

### 5 Một số thao tác với hosting

### 5.1 Quản lý các tập tin, quản lý source code 

<img src="img/33.PNG">

<img src="img/34.PNG">

- Ta có thể thay đổi chỉnh sửa code của trang web

<img src="img/35.PNG">

<img src="img/36.PNG">

### 5.2 Upload source code lên

- Thư mục để tải code lên

<img src="img/37.PNG">

<img src="img/38.PNG">

### 5.3 Cài đặt ứng dụng

- Tại trang quản lý ta chọn ứng dụng

<img src="img/39.PNG">

- ta sẽ cài wp cho trang web

<img src="img/40.PNG">

- xem trước wp sau khi đã cài đặt

<img src="img/41.PNG">

### 5.4 Cơ sở dữ liệu

- Tại giao diện quản lý ta chọn cơ sở dữ liệu
<img src="img/45.PNG">

-
<img src="img/42.PNG">
<img src="img/44.PNG">

### 5.5 Thống kê

<img src="img/46.PNG">




































































