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



# II Reseller Level
- <img src="img/63.PNG">

## Account Management
- <img src="img/64.PNG">
- Add New User ( thêm tài khoản người dùng mới)
- ta điền thông tin cần thiết rồi chọn submit để tạo tài khoản.
- <img src="img/65.PNG">
- <img src="img/66.PNG">
- <img src="img/67.PNG">
- List Users : xem danh sách các user
- Manage Tickets: quản lý các ticket

- <img src="img/68.PNG">

- Add Package : tạo các gói tài nguyên cho người dùng
- Manage User Packages : quản lý các gói.
- Edit User Message : chỉnh sửa tin nhắn của người dùng.
## Reseller Tools

- <img src="img/69.PNG">
- Change Passwords : thay đổi mật khẩu cho người dùng
- <img src="img/70.PNG">
- Reseller Statistics : thống kê ta xem được ổ đĩa , băng thông,domains, subdomains,...
- <img src="img/71.PNG">
- IP Management : quản lý ip , ta xem trạng thái , số lượng user
- <img src="img/72.PNG">
- Skin Manager: quản lý giao diện ta có thể thay đổi giao diện bất kỳ,
- <img src="img/73.PNG">
## Extre Features
- <img src="img/74.PNG">
- System Info : xem thông tin hệ thông
- Nameservers : tên các máy chủ
- ConfigServer Security & Firewall: tường lửa và cấu hình
- Message All Users : gửi tin nhắn đến các người dùng
- <img src="img/75.PNG">
- Contact Administrator ; chức năng này giúp đại lý trao đổi thông tin với người quản trị 
- <img src="img/76.PNG">

# Chức năng của user
- Ta đăng nhập tài khoản user
- <img src="img/77.PNG">
- Domain Setup: ta có thể thay đổi các cấu hình domain , thêm, xóa các domain.
- <img src="img/78.PNG">
- Ta có thể thay đổi các giá trị của domain như băng thông , lưu lượng ổ đĩa các phiên bản PHP
- tạo mới 1 tên miền khác, điền thông tin cần thiết
- <img src="img/80.PNG">
- <img src="img/81.PNG">

- Change Password : thay đổi mật khẩu
- Login History : xem các lịch sử đăng nhập
- DNS Management : quản lý các bản ghi, ta có thể chỉnh sửa xóa hay thêm mới các bản ghi.
- <img src="img/82.PNG">
- Support Center : trung tâm hỗ trợ, gửi ticket cho nhà quản trị.
- <img src="img/83.PNG">
-  Installed Perl Modules: xem các mô-đun đã cài đặt
- Site Summary / Statistics / Logs thống kê các logs
-  FTP Management : quản lý tài khoản ftp
- Subdomain Management quản lý các sub, tạo các sub
- <img src="img/84.PNG">
- <img src="img/85.PNG">
- MySql Management : quản lý mysql
- <img src="img/88.PNG">
- <img src="img/86.PNG">
- <img src="img/87.PNG">
- Sau đó ta đăng nhập vào trang quản trị, tại đây ta có thể thực hiện các lệnh , truy vấn sql ,....
- <img src="img/89.PNG">
- Password Protected Directories : mật khẩu bảo vệ thư mục
- <img src="img/90.PNG">
- <img src="img/91.PNG">
- chọn protect để thiết lập mật khẩu, điền các thông tin như lời nhắc, cập nhập người dùng , đặt mật khẩu và nhập lại.
- <img src="img/92.PNG">

- File Manager: quản lý các file, ta có thể thao tác trực tiếp các file bằng giao diện
- <img src="img/93.PNG">

### E-mail Management 
- Quản lý các vấn đề về mail
- <img src="img/94.PNG">

- E-mail Accounts : quản lý tài khoản mail
- <img src="img/95.PNG">
- ta tạo tài khoản mail mới
- <img src="img/98.PNG">
- <img src="img/97.PNG">
- ta vào web mail để kiểm tra dịch vụ, đăng nhập tài khoản vừa tạo
- <img src="img/99.PNG">
- <img src="img/100.PNG">
- <img src="img/101.PNG">
- Autoresponders: chức năng trả lời tự động
- <img src="img/102.PNG">
- <img src="img/103.PNG">
- SPAM filters: các thiết lập để để chống spam










































 

















































