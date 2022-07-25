# Tìm hiểu về zabbix
## Zabbix là gì?
- Zabbix là một phần mềm mã nguồn mở được công bố lần đầu 2001, có chức năng giám sát các dịch vụ mạng và  tài nguyên công nghệ khác như máy chủ, phần cứng,.. một cách nhanh chóng, hiệu quả. Kết quả phân tích, thống kê số liệu được thể hiện một cách trực quan; các thông báo về vấn đề tiềm ẩn được cập nhật chính xác và kịp thời. 
## Các công việc mà Zabbix thực hiện 
- Giám sát phần cứng: Zabbix thực hiện giám sát các vấn đề như nhiệt độ máy chủ, công tắc bộ định tuyến, ... thông qua SNMP ( Simple Network Management Protocol là tập hợp các giao thức có chức năng kiểm tra hoạt động và hỗ trợ vận hành từ xa cho các thiết bị mạng như router, switch hay server.)
- Giám sát hệ thống: Là việc theo dõi các số liệu về dung lượng, tốc độ của hạ tầng như CPU, Ram, ổ cứng,... nhằm đảm bảo tài nguyên của bạn luôn đủ để sử dụng. Tránh trường hợp gây mất ổn định, hoặc khởi động lại hệ thống.

- Giám sát mạng: thường sử dụng với các công ty sử dụng giải pháp mạng điện toán đám mây. 

- Giám sát bảo mật: Bao gồm tường lửa, phần mềm chống DDOS, mật khẩu, sao lưu, phục hồi và các hệ thống bảo mật được các nhà cung cấp cài đặt sẵn trên các giải pháp mạng. Báo cáo quá trình hoạt động của các công cụ này, sự ghé thăm của mã độc, những đường link chứa nhiều mã độc truy cập vào trang,...
- Giám sát web: chức năng này có thể được phát triển cao hơn với nhu cầu kiểm soát của người dùng. Nó đưa ra các số liệu về thời gian tải trang, tốc độ load, thời gian phản hồi,... 
- Theo dõi nhật ký: là quá trình thu thập, lưu trữ, truy vấn dữ liệu. Bạn có thể theo dõi Nginx thông qua nhật ký 500x, lỗi PHP,... Ngoài ra, bạn có thể phát triển chức năng này bằng cách sử dụng mã nguồn mở ELKstack để đạt được .logstash, ,elasticsearch (lưu trữ + tìm kiếm), kibana (hiển thị) 

## Đánh giá 
### Ưu điểm 
Đây là một công cụ mã nguồn mở, dễ phát triển và mở rộng theo ý người dùng. Chi phí đầu tư ban đầu thấp

- Thực hiện chức năng giám sát toàn diện trên các thiết bị phần cứng và dịch vụ mạng 

- Hỗ trợ tốt các máy chủ đặt trên hệ điều hành Linux

- Giao diện thân thiện và đẹp mắt

- Phân quyền user linh động và dễ thực hiện 

- Thông báo các sự cố nhanh chóng qua email hoặc app

- Các chức năng theo dõi thống kê được thực hiện chủ động, dễ thiết lập và sửa đổi

- Sở hữu tài nguyên công cụ lớn với nhiều plugin hỗ trợ cho các dịch vụ hệ thống khác nhau

- Có tính năng chứng thực người dùng 

- Kết quả được trả về dưới dạng biểu đồ trực quan, dễ phân tích và đánh giá. 

### Ưu điểm
Nhược điểm 
- Zabbix không hỗ trợ giao diện web mobile 

- Thiết kế template/alerting rule của hệ thống được người dùng đánh giá là không mấy thân thiện vì đôi khi nó yêu cầu cao về kiến thức code của người dùng.

- Sẽ gặp tình trạng mất ổn định và các vấn đề hiệu suất về PHP và Database khi sử dụng hệ thống mạng lớn hơn 1000+ node.


