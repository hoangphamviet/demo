# I Xác thực SSL

## Khái niệm
- Xác thực qua tên miền là phương pháp nhanh nhất xác thực SSL và có sẵn cho doanh nghiệp và các khách hàng cá nhân.
## Các phương pháp xác thực SSL 
-  Phương pháp truyền thống qua DCV - Email. Ta sẽ nhận được 1 email xác thực tương ứng với email đăng ký SSL. Các email sẽ chứ 1 mã xác nhận duy nhất và một liên kết. Nhấp vào liên kết và nhập mã để xác nhận việc sở hữu tên miền.
- Phương pháp thay thế DCV HTTP-based DCV, HTTPS-based DCV (Xác thực qua file ). Nhà cung cấp sẽ gửi cho quý khách nội dung của file xác thực kèm đường dẫn để quý khách khởi tạo file theo đường dẫn được cung cấp trên server quý khách.
- DNS CNAME-based ( Xác thực qua DNS). Nhà cung cấp sẽ gửi cho quý khách nội dung 1 bản ghi để quý khách xác thực SSL qua hệ thống DNS domain.

## Các bước xác thực 
 
### Xác thực qua email tên miền:
- Bước 1 : Khách hàng cần đảm bảo email admin@domain.com (với domain.com là tên miền cần cài đặt SSL) có thể nhận email gửi đến. 
- Bước 2 : Sau đó khách hàng sẽ nhận 1 mail xác thực gửi đến admin@domain.com. Ta sẽ click vào liên kết trong mail và xác nhận.
- Bước 3 : Sau khi xác thực khách sẽ nhận được các file cài đặt SSL sau khi SSL đã được xác thực.
### Xác thực qua DNS và upload file
-  Xác thực DNS ta cần tạo 1 bản ghi dùng để xác thực theo yêu cầu nơi cấp SSL.
- Xác thực qua upload file:
ta truy cập vào dịch vụ  SSL tại trang quản lý dịch vụ , ta tìm đến chỗ dowload file để xác thực và tải file xác thực lên.