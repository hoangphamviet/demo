# I Những lệnh liên quan đến hệ thống
- exit : thoát khỏi cửa số dòng lệnh.
- logout: tương tự exit
- reboot : khởi động lại hệ thống
- halt : tắt máy
# II Lệnh thao tác trên thư mục ,tập tin
- ls : lấy danh sách các file và thư mục trong thư mục hiện hành
+ <img src="img/1.PNG">
- pwd : xuất đường dẫn của thư mục làm việc
+ <img src="img/2.PNG">
- cd: thay đổi thư mục làm việc đến một thư mục mới
- mkdir + tên thư mục : tạo thư mục mới
+ <img src="img/3.PNG">
- rmdir : xóa thư mục
+ rmdir + tên thư mục : xóa thư mục rông
+ rm -r + tên thư mục : xóa thư mục chứa các thư mục con và tập tin (có xác nhận cho từng đối tượng)
+ rm -rf + tên thư mục: xóa thư mục chứa các thư mục con và tập tin (không cần xác nhận)
- cp : copy một hay nhiều tập tin đến thư mục mới
- mv : đổi tên hoặc di chuyển tập tin , thư mục
- touch + tên tập tin : tạo 1 tập tin
- nano + tên tập tin : khởi động trình soạn thảo văn bản nano
+ <img src="img/5.PNG">
+ <img src="img/6.PNG">
+
- cat + tên tập tin: xem nội dung của 1 tập tin
+ <img src="img/7.PNG">
- rm : xóa tập tin
+ rm + tên tập tin: xóa 1 tập tin
+ rm + tên tập tin1 + tên tập tin2 : xóa nhiều tập tin
+ rm /a/b/tên tập tin : xóa theo đường dẫn
+ rm -i : xóa có xác nhận
+ rm -f : xóa không xác nhận

# III Lệnh khi làm việc trên terminal
- clear : xóa trắng cửa số dòng lệnh
- date : xem ngày giờ hệ thống
+ <img src="img/8.PNG">
- cal : xem lịch hệ thống 
+ <img src="img/9.PNG">
# III Lệnh quản lý hệ thống
- rpm: kiểm tra gói đã cài đặt hay chưa, hoặc cài đặt một gói, hoặc sử dụng để gỡ bỏ một gói.
+ <img src="img/10.PNG">
- ps : kiểm tra hệ thống tiến trình đang chạy
+ <img src="img/11.PNG">
+ PID : id của tiến trình
+ TTY : thông tin terminal mà người dùng đăng nhập
+ TIME : lượng CPU tình bằng phút giây mà tiến trình đó chạy
+ CMD : câu lệnh để thực hiện process đó
- cat /proc/cpuinfo: kiểm tra thông tin CPU
+ <img src="img/15.PNG">
- cat /proc/meminfo: kiểm tra thông tin về RAM đang sử dụng
+ <img src="img/16.PNG">
- free -m: kiểm tra dung lượng RAM còn trống
+ <img src="img/17.PNG">
- df: kiểm tra dung lượng đĩa cứng,các phân vùng ổ đĩa
+ <img src="img/19.PNG">
- du -sh: kiểm tra dung lượng thư mục hiện tại
+ <img src="img/18.PNG">

# IV các lệnh về quản lý user 
- useradd : tạo một người dùng mới
- passwd : cập nhập mật khẩu với user vừa tạo
+ <img src="img/13.PNG">
- cat /etc/passwd : xem danh sách user
+ <img src="img/14.PNG">
+ Mỗi hàng sẽ có 7 phần được ngăn cách nhau bởi dấu hai chấm
+ Tên tài khoản.
+ Mật khẩu đã được mã hóa (x có nghĩa là mật khẩu được lưu trong file /etc/shadow).
+ Số ID người dùng 
+ Số ID nhóm của người dùng 
+ Tên đầy đủ của người dùng 
+ Thư mục chính của người dùng.
+ Shell đăng nhập (mặc định là /bin/bash).
- userdel : xóa người dùng đã tạo
- groupadd : tạo một nhóm người dùng mới
- groupdel : xóa nhóm người dùng
-gpasswd : thay đổi mật khẩu cho người dùng

## V Lệnh giải nén và nén
- Các option dùng với lệnh tar
+ -c: tạo file a.tar
+ -x: giải nén file a.tar
+ -v: hiển thị quá trình giải nén và nén dữ liệu ra màn hình
+ -f: chỉ định nén thành file
+ -t: xem dữ liệu trong file nén
+ -j :tạo file nén với bzip2 file.tar.bz2
+ -z: tạo file nén với gzip  file.tar.gz
+ -r: ghđm một file và thư mục và file nén đã tồn tại
+ --willcards : tìm và xuất file bất kỳ trong file nén
- Tạo file nén 
+  tar -cvf filename.tar file1 file2 folder1 folder2
(filename là file nén tar được tạo ra file , folder được nén vào file nén tar)

- giải nén file
 tar -xvf filename.tar
- xem nội dung file
+ tar -tvf filename.tar
- thêm mới, cập nhập nội dung vào file lưu trữ
+  tar -rvf filename.tar add_file1 add_file2
- xóa dữ liệu file
+ tar -f filename.tar --delete file1 file2





 







 







