# I DirectAdmin là gì ?
### DirectAdmin là 1 trong những bản điều khiển (hay còn gọi control panel) dành cho những người quản trị web hosting được sử dụng phổ biến hiện nay với giao diện đơn giản, trực quan , dễ dàng sử dụng. 
###  DirectAdmin cung cấp cho người dùng nhiều tính năng như quản lý domain, subdomain, DNS, FTP, cơ sở dữ liệu, tạo email theo tên miền , tạo SSH key, bảo mật SSL,..., dễ dàng upload và quản lý các file với File Manager .

### DirectAdmin chạy tốt trong Linux và các bản phân phối chính của nó CentOS, Ubuntu, Debian, Red Hat,.... Hệ điều hành dựa trên Windows sẽ không được hỗ trợ.

# Ưu điểm và Nhược điểm
### Ưu điểm 
- Giao diện trực quan , sử dụng dễ dàng 
- Gói đăng ký giả cả phù hợp.
- Hỗ trợ : Ngoài sự hộ trỡ của nhà cung cấp dịch vụ lưu trữ, bạn có thể nhận được sự trợ giúp trực tiếp của kỹ thuật của  DirectAdmin
- Tính ổn định, phục hồi sự cố tự động
- Tốc độ xử lý nhanh , ít tiêu tốn tài nguyên
- Hỗ trợ nhiều phân cấp user
- Manual configuration: Directmin admin cung cấp hầu hết tính năng thông qua giao diện website, nhưng người dùng cũng có thể config thủ công bằng cách sử dụng command line.
### Nhược điểm
- Khả năng thêm các chức năng: các tính năng còn hạn chế so với các phần mềm khác
- Khả năng chỉnh sửa file: DirectAdmin không tương thích với dòng font unicode nên rất khó để sửa khi file sử dụng các ngôn ngữ không phải là tiếng Anh.
- Cộng đồng người dùng ít: Bạn sẽ khó tìm được các câu trả lời hướng dẫn cho DirectAdmin khi gặp một vấn đề nâng cao, khó khăn nào đó vì không có quá nhiều cộng động sử dụng DirectAdmin.
- Giao diện khá nâng cao với người dùng: Người dùng mới có thể gặp khó khăn trong việc tìm kiếm tính năng cần sử dụng. Directadmin được phân chia thành nhiều cấp, và nó mất thời gian để xác định vị trí tính năng mình cần.


# II Tìm hiểu về các chức năng của DirectAdmin
### Các chức năng của Admin 

- <img src="img/8.PNG">

- Access Level tại cấp độ truy cập ta chọn vào cấp độ Admin

###  1. Server Management
### 1.1 Create Admin :
- Tạo thêm tài khoản admin mới
- <img src="img/9.PNG">
- Ta sẽ điền các thông tin như tài khoản, mật khẩu , mail  sau đó ấn submit để tạo
- <img src="img/10.PNG">
- Sau đó ta thấy tài khoản được tạo thành công
- <img src="img/11.PNG">
- Ta có thể xem danh sách tài khoản đã tạo.
- <img src="img/12.PNG">
- <img src="img/13.PNG">
- Ta có thể xem các thông số tài nguyên của tài khoản.
- <img src="img/14.PNG">
- Ta xem được các thông tin tài nguyên như : băng thông , dung lượng ổ đĩa, tên miền, tài khoản người dùng,mail,....
- <img src="img/15.PNG">
- Chức năng modify ta sẽ cấu hình tài nguyên của tài khoản:
- <img src="img/16.PNG">
- <img src="img/17.PNG">
- Sau khi cấu hình xong ta ấn save để lưu.
- Xóa tài khoản 
- <img src="img/18.PNG">
- Xem tài nguyên , dữ liệu tài khoản đã sử dụng
- <img src="img/19.PNG">
- <img src="img/20.PNG">
- Suspended(cấm) tài khoản
- <img src="img/22.PNG">
- Tại chế độ select ta chọn tài khoản muốn suspended, reason chọn lý do và ấn suspend
- <img src="img/23.png">
- <img src="img/24.PNG">
- Thay đổi mật khẩu 
- <img src="img/25.PNG">
- Điền thông tin tài khoản , mật khẩu mới muốn đổi.
- <img src="img/26.PNG">
- Quản lý các ticket
- <img src="img/27.PNG">
- <img src="img/28.PNG">
- Quản lý các tài khoản đại lý 
- <img src="img/29.PNG">
- Trước muốn tạo tài khoản đại lý ta phải tạo các gói Manage Reseller Packages 
- <img src="img/30.PNG">
- Tùy chỉnh cấu hình các gói tài nguyên cho đại lý rồi ta chọn save để lưu lại.
- <img src="img/31.PNG">
- <img src="img/32.PNG">
- Tạo tài khoản đại lý điền đầy đủ các thông tin tài khoản, email, mật khẩu, domain, chọn gói tài nguyên
- <img src="img/33.PNG">
- <img src="img/34.PNG">
###  2. Admin Tools
- <img src="img/35.PNG">
- IP Management thêm địa chỉ IP
- <img src="img/36.PNG">
- <img src="img/37.PNG">
- DNS Administration quản lý các bản ghi
- <img src="img/38.PNG">
- Ta thấy được các domain trong server , nhấn vào domain bất kì ta có thể chỉnh sửa được các bản ghi của domain đó.
- <img src="img/39.PNG">
- vd ta thêm bản ghi a 
- <img src="img/40.PNG">
- <img src="img/41.PNG">
- Move Users between Resellers di chuyển các tài khoản người dùng với các đại lý
- <img src="img/42.PNG">
- <img src="img/43.PNG">
- System Information xem các thông tin hệ thống bao gồm : tổng bộ nhớ, các phiên bản đang được chạy, tốc độ xử lý,....
- <img src="img/44.PNG">
- Service Monitor dịch vụ giám sát, các dịch vụ đang được chạy , trạng thái, bộ nhớ sử dụng, ta có thể bật , tắt , khởi động lại các dịch vụ 
- <img src="img/45.PNG">
- Log viewer xem các file lỗi các phần mềm , dịch vụ trong hệ thống 
- <img src="img/46.PNG">
- File Editor chỉnh sửa trực tiếp các file cấu hình
- <img src="img/47.PNG">
- Process Monitor theo dõi các tiến trình.
- <img src="img/48.PNG">
###  3. Extra Features
- <img src="img/49.PNG">
- Complete Usage Statistics xem thống kế chi tiết băng thông , ổ đĩa sử dụng,...
- <img src="img/50.PNG">
- Custom HTTPD Configurations xem và chỉnh sửa file cấu hình vhost 
- <img src="img/51.PNG">
- <img src="img/52.PNG">
- PHP Configuration cấu hình PHP
- <img src="img/53.PNG">
- Brute Force Monitor
 theo dõi các ip đăng nhập vào tài khoản quản trị số lần đăng nhập thất bại.
- <img src="img/54.PNG">
- ConfigServer Security & Firewall cấu hình và chức năng sử dụng tường lửa
- <img src="img/56.PNG">
- <img src="img/57.PNG">
- <img src="img/58.PNG">
- Tại đây ta có thể sử dụng các chức năng của tường lửa csf , cấu hình,... thực hiện trực tiếp trên giao diện ...
- Administrator Settings tùy chỉnh thông tin admin, cài đặt quản trị viên: thông báo cho các quản trị viên khi có dịch vụ gặp sự cố,...Cài đặt máy chủ: tên máy chủ, thời gian chờ,...bảo vệ khôi phục mật khẩu bị mất tự động, các danh sách ip bị chặn, xóa ip ra khỏi danh sách, email giới hạn mail hàng ngày có mỗi người dùng,....
- <img src="img/59.PNG">
- <img src="img/60.PNG">
- Licensing / Updates thông tin giấy phép,..
- <img src="img/61.PNG">
- Plugin Manager
- <img src="img/62.PNG">











 

















































