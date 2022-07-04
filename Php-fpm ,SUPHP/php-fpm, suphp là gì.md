# Tìm hiểu về PHP-FPM  ?
## PHP-FPM là gì ?
- PHP-FPM là một chương trình có tính năng phiên dịch PHP khi chạy web cho server. PHP-FPM được phát triển dựa trên việc mở rộng CGI. Nó có khả năng tối ưu quá trình xử lý thông tin của web server và hỗ trợ xử lý thông tin nhanh nhất từ các web khác nhau, trong cùng 1 khoảng thời gian.PHP-FPM có tốc độ xử lý PHP script nhanh, tăng lượng truy cập và khả năng tối ưu hóa cho những web có kích thước lớn.

## CGI là gì ?
- CGI (Common Gateway Interface) là một phần mềm lập trình có chức năng kết nối giữa máy chủ và chương trình , dựa trên các định danh đặc tả thông tin.
- Nó có nhiệm vụ xây dựng chương trình từ các trang web. Sau khi nhận dữ liệu từ các trang web dưới dạng HTML, phần mềm này sẽ truyền dữ liệu đó qua cổng thông tin Internet đến máy tính của người dùng.
## FastCGI là gì ? 
- Là một giao thực phát triển mở rộng từ CGI. Nó có tác dụng để web server tối ưu trong việc xử lý. Đồng thời giúp máy chủ có thể xử lý nhiều yêu cầu từ trang web trong cùng 1 lúc.
## Ưu điểm và nhược điểm
### Ưu điểm:
- Tính bảo mật, ổn định và hiệu suất mà PHP-FPM mang lại cao hơn nhiều so với CGI 
- Được sử dụng rộng rãi nhất là khi khai thác tài nguyên CPU để chạy chương trình (tốn ít tài nguyên CPU).
- Giúp tăng tốc độ tải trang web và việc truy cập của người dùng nhanh chóng dễ dàng hơn. Lưu lượng truy cập cũng tăng lên đáng kể.
### Nhược điểm:
- Tiêu tốn dung lượng bộ Ram.
# Tìm hiểu về SuPHP 
## SuPHP là gì ?
- SuPHP cũng chạy PHP như CGI module. SuPHP khác với CGI vì PHP scripts được gọi từ web Server sẽ được chạy dưới quyền của user sở hữu PHP scripts đó. SuPHP thông thường là một handler mặc định và được khuyến cáo bởi cPanel để chạy PHP. Với suPHP bạn sẽ có thể thấy user nào đang chạy đoạn PHP script.

## Ưu điểm và nhược điểm
### Ưu điểm:
- Khi ban sử dụng công cụ upload file lên web bạn , các file sẽ được phân dúng quyền hạn của user đó. Upload và một vài tính năng khác của WordPress không hoạt động nếu không sử dụng SuPHP hoặc FastCGI.
- SuPHP cũng cung cấp một lợi thế bảo mật hơn là DSO hay CGI. Tất cả những PHP Scripts không thuộc một user cụ thể nào đó sẽ không thể  thực thi được. Hoặc user này sẽ không thể nào thực thi được các PHP Scripts của user khác. Khi một tài khoản nào đó bị đánh cắp, các scripts cũng không thể nào lây lan sang các tài khoản khác được.
- Nhược điểm :
- Sử dụng CPU cao.
- Bạn không thể sử dụng Opcode Cache (như xCache) với suPHP.
- Khi sử dụng suPHP nếu CPU load cao bạn có thể chuyển lại dùng DSO hoặc FastCGI.