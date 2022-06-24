# I Backup vs restore là gì ?
### Backup là gì ?

-  Backup dữ liệu là hành động sao chép , lưu lại toàn bộ nội dung và các dữ liệu quan trong của 1 web , máy tính , máy chủ  và lưu trữ nội dung dữ liệu đó ở một hoặc nhiều thiết bị có chức năng lưu trữ khác để làm dữ liệu dự phòng. 
### Restore là gì
- Data backup là việc tạo ra các bản sao của dữ liệu gốc, cất giữ ở một nơi an toàn và lấy  ra sử dụng (restore) khi hệ thống gặp sự cố.

# II Backup và restore trên DirectAdmin

### Backup
- Ta truy cập vào DirectAdmin với quyền admin.
- <img src="img/1.PNG">
- Tại Admin Tools ta chọn chức năng Admin Backup/Transfer.
- <img src="img/2.png">
- Sau đó ta chọn Schedule để tiến hành các thao tác cho việc backup.
- <img src="img/3.PNG">
- Ta tích chọn các user muốn backup rồi chọn next step.
- <img src="img/4.PNG">
- Bước này ta chọn thời gian
- Mặc định ta để now để backup ngay lập tức.
- <img src="img/5.PNG">
- Hoặc ta chọn cron schedule để lựa chọn thời gian. vd minute: số phút để tiến hành backup, hour h mỗi ngày , day of month ngày trong tháng ,....
- <img src="img/6.PNG">
- Tại vd này ta tiến hành backup ngay lập tức.
- <img src="img/7.PNG">
- Tại bước này ta dùng lưu ta có 2 tùy chọn lưu trực tiếp trên local hoặc 1 tài khoản ftp.
- <img src="img/8.PNG">
- <img src="img/9.PNG">
- Tại bước này ta chọn những dữ liệu để sao lưu mặc định sẽ chọn all data , trong trường hợp ta chỉ muốn lấy dữ liệu tùy chọn ta chọn selected data.

- Sau khi chọn xong ta chon schedule để hệ thống tiến hành backup , sau khi xong ta nhận được 1 tin nhắn thông báo.
- <img src="img/10.PNG">

### Restore

- Tại Admin Tools ta vẫn chọn chức năng Admin Backup/Transfer và chọn restore.

- <img src="img/11.PNG">

- Ta chọn đường dẫn đến file backup nằm ở đâu mặc định nó sẽ ở /home/admin/admin_backups
- <img src="img/13.PNG">
- Tiếp theo tại chọn ip 
- <img src="img/12.PNG">
- Chọn user cần khôi phục, rồi chọn Restore.
- <img src="img/14.PNG">
- <img src="img/15.PNG">


# II Backup và restore trên Plesk
### Backup 
- Tại giao diện chính ta chọn Tool & Settings 
- <img src="img/16.PNG">
- Tại công cụ Tools & Resources ta chọn backup manager 
- <img src="img/17.PNG">
- Chọn back up để tiến hành các thao tác back up
- <img src="img/18.PNG">
- Chọn các tùy chỉnh phù hợp với yêu cầu vd như ta muốn back up tin nhắn mail hoặc các file , cơ sở dữ liệu
- mặc định nó lưu trữ tại C:\Program Files (x86)\Plesk\Backup\ sau khi tùy chỉnh xong ta chọn ok
- <img src="img/19.PNG">

- Sau đó ta sẽ đợi quá tình sao lưu
- <img src="img/20.PNG">
- Khi hoàn tất ta có thể tải file back up về máy
- <img src="img/21.PNG">
- Tại tùy chọn tiếp hành plesk khuyến nghị sử dụng mật khẩu để mã hóa mk của người dùng . tại vd này ta sẽ không dùng mk tích 
- <img src="img/23.PNG">
- Sau khi tải xuống ta kiểm tra file tải về chưa vậy là hoàn tất
- <img src="img/24.PNG">
### Restore 

- Chọn trực tiếp vào bản backup ta cần restore.
- <img src="img/25.PNG">
- <img src="img/26.PNG">
- Ta chọn All objects để restore tất cả sau đó chọn restore 
- <img src="img/27.PNG">




























