# Tìm hiểu giao diện quản trị
## Giao diện  Dashboard
### - Tại giao diện này hiển thị các thông tin:
- Kerio News : Giới thiệu về các chức năng mới trong phiên bản hiện tại
- System : Hiển thị thông tin phiên bản kerio-connect, hệ điều hành, hostname
- System status: hiển thị trạng thái của hệ thống 
- License Details: Giấy phép 
- Kerio Antivirus : Hiển thị trạng thái của Kerio Antivirus
- System Health: Hiển thị RAM, CPU, Disk của hệ thống dưới dạng biểu đồ (%, time)
- Disk Storage Info: Hiển thị dung lượng Disk tổng và dung lượng Disk đang được sử dụng
<img src="img/1.PNG">
<img src="img/2.png">
<img src="img/3.PNG">

## Giao diện Message Queue

<img src="img/4.png">

- Messages in Queue: Hiển thị các thư đang được chờ trên hàng đợi để được gửi ra bên ngoài
- Message Queue Processing: Tiến trình xếp hàng thư

## Traffic Chart

<img src="img/5.PNG">

- Tracffic Chart cho phép hiển thị các thông tin Connection hoặc các Message trong một khoảng thời gian (có thể tùy chỉnh tối đa 30 ngày).

##  Statistics

- Hiển thị các thông số của hệ thống 

<img src="img/6.PNG">

##  Active Connections

-  Hiển thị các Connection và các Session đang hoạt động.

<img src="img/7.PNG">
<img src="img/8.PNG">

## Opened Folders
- Hiển thị các thư mục đã mở

<img src="img/9.PNG">

# Configuration

<img src="img/11.PNG">

- Tại đây ta cấu hình của hệ thống

## Services

<img src="img/12.PNG">

- Ta thấy được các trạng thái dịch vụ của hệ thống , các cổng ,....
##  Domains

- Hiển thị các domain đã được tạo. 
<img src="img/13.PNG">
- Tại đây có thể tạo, sửa, xóa domain và thiết lập các tùy chọn cho domain đó bằng cách click chuột phải rồi tùy chọn các tùy chỉnh
<img src="img/14.PNG">
 
 ## SMTP server
- Máy chủ SMTP xác định ai có thể gửi thư đi qua Kerio Connect và họ có thể thực hiện những hành động nào.
-Để thiết lập gửi tin nhắn từ bên ngoài server Kerio Connect ta làm như sau
- Trong giao diện Configuration chọn SMTP server -> Relay Control
-Nhấp vào option Allow relay only for:
-Để chỉ định một nhóm địa chỉ IP mà từ đó người dùng có thể gửi đi, chọn Users from IP address group và thiết lập như mong muốn
- Để cho phép người dùng đã xác thực gửi thư đi, chọn User authenticated through SMTP for outgoing mail
-Để cho phép người dùng đã xác thực trước đó qua POP3 gửi thư đi từ cùng một địa chỉ IP, chọn Users previously authenticated through POP3 from the same IP address
- Nhấp vào Apply để lưu thiết lập
## Instant Messaging

- Dịch vụ trò chuyện tức thời trên Kerio-connect

<img src="img/15.PNG">

##  Archiving and Backup
- Kerio-connect hỗ trợ Full Backup và nó cũng hỗ trợ Differential Backup, lưu các tệp đã được thêm vào hoặc thay đổi kể từ lần sao lưu đầy đủ nhất
- Ta có thể lên lịch sao lưu như sau:
- Trong giao diện quản trị, vào Configuration -> Archiving and Backup -> Backup
- Chọn Enable message store and configuration recovery backup
- Chọn Add
- Nhập mô ta cho bản sao lưu trong Description
- Chọn thời gian và loại sao lưu và nhấp vào ok
- <img src="img/16.PNG">
- Ta có thể tùy chỉnh kích thước bản lưu tối đa
- Ta chọn chuột phải vào bản backup muốn thay đổi sau đó chọn advanced
- <img src="img/17.PNG">
- <img src="img/18.PNG">
- Target backup directory, chỉ định thư mục nơi lưu trữ tất cả các bản sao lưu
- Notification, nhập địa chỉ email để nhận thông báo về các bản sao lưu
. Cuối cùng nhấn vào Apply để lưu các tùy chọn
- <img src="img/19.PNG">

- Khôi phục dữ liệu Current status nhấp vào Start Now để tạo một bản sao lưu đầy đủ (chọn đường dẫn lưu bản sao lưu /mnt/backup)
- <img src="img/19.PNG">
- <img src="img/20.PNG">
- Thông báo như trong hình là thành công
- Tiếp theo đó ta restore
-  Stop Kerio Connect
- Vào thư mục cài đặt Kerio Connect 
- cd /opt/kerio/mailserver
- Chạy lệnh
- ./kmsrecover /opt/kerio/mailserver/store/
- <img src="img/21.PNG">
## Delivery
- Trong Kerio-connect, ta có thể lên lịch để
- Tải xuống thư từ máy chủ POP3 từ xa
- Nhận thông báo bằng lệnh ETRN đến các máy chủ đã xác định
- Gửi tin nhắn từ hàng đợi tin nhắn
- Cấu hình Scheduling, để add scheduling ta làm như sau:
- Trong giao diện quản trị chọn Configuration -> Delivery -> Scheduling
- Chọn Add
- Chỉ định Time condition
- Để giới hạn việc lập lịch trong một phạm vi thời gian cụ thể, hãy chọn Valid only at time và chọn một phạm vi thời gian
- Chỉ định Action. Có thể lên lịch cho bất kỳ hoạt động nào sau đây
- Gửi tin nhắn từ hàng đợi tin nhắn
- Tải xuống tin nhắn qua POP3
- Gửi lệnh ETRN
- Bấm ok
- <img src="img/22.PNG">

- <img src="img/23.PNG">

##  SSL Certificates
- SSL hỗ trợ việc cài đặt chứng chỉ SSL miễn phí Let's Encrypt cho mail.domain. Tại đây ta có thể tạo mới và xóa chứng chỉ.
## Advanced Options
- Tại đây ta có thể thiết lập các tùy chọn nâng cao hơn phù hợp với nhu cầu 
 ## Security
-  Kerio-connect cung cấp chức năng yêu cầu xác thực Require secure authentication. Người dùng phải xác thực an toàn khi họ truy cập Kerio-connect
- Có thể chọn bất cứ phương thức xác thực nào sau đây
- CRAM-MD5: Xác thực mật khẩu bằng cách sử dụng thông báo MD5
- DIGEST-MD5: Xác thực mật khẩu sử dụng thông báo MD5
- LOGIN
- PLAIN
- Nếu mật khẩu của người dùng được lưu ở định dạng SHA, chọn LOGIN hoặc PLAIN. Nếu chọn nhiều phương pháp, Kerio sẽ thực hiện phương pháp khả dụng đầu tiên

- <img src="img/24.PNG">

## Administration Settings
- Trong Kerio-connect, có thể kích hoạt một tài khoản quản trị viên đặc biệt. Tài khoản này được tích hợp sẵn để truy cập giao diện quản trị.
- Để kích hoạt giao diện quản trị ta làm như sau:
- Đi tới phần Configuration -> Administration Settings
- Chọn Enable built-in administrator account
- Nhập password cho tài khoản. Tên tài khoản mặc định là Admin và không thể thay đổi
- <img src="img/25.PNG">






















