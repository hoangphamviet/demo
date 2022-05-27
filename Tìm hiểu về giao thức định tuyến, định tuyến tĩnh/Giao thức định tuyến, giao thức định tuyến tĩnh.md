# I Các giao thức định tuyến 
 ## 1.1 Khái niệm 
 - Định tuyến là quá trình xác định đường đi tốt nhất trên một mạng máy tính để gói tin tới được đích theo một số thủ tục nhất định nào đó thông qua các nút trung gian là các bộ định tuyến router. Thông tin về những con đường này có thể được cập nhật tự động từ các router khác hoặc là do người quản trị mạng chỉ định cho router. Sau khi Router nhận gói tin, thì Router sẽ gỡ bỏ phần header lớp 2 để tìm địa chỉ đích thuộc lớp 3. Sau khi đọc xong địa chỉ đích lớp 3 nó tìm kiếm trong Routing Table cho mạng chứa địa chỉ đích.
 Bảng định tuyến của mỗi giao thức định tuyến khác nhau, nhưng có thể gồm những thông tin sau:
+ Địa chỉ đích của mạng, mạng con hoặc hệ thống.
+ Địa chỉ IP của router chặng kế tiếp phải đến.
+ Giao tiếp vật lí phải sử dụng để đi đến Router kế tiếp.
+ Subnet mask của địa chỉ đích.
+ Khoảng cách đến đích (ví dụ: số lượng chặng để đến đích).
+ Thời gian (tính theo giây) từ khi Router cập nhật lần cuối.
+ Giao thức định tuyến là ngôn ngữ giao tiếp giữa các router. Một giao thức định tuyến cho phép các router chia sẻ thông tin về các network, router sử dụng các thông tin này để xây dựng và duy trì bảng định tuyến.
- Phân loại các loại định tuyến:
+ Định tuyến tĩnh: Việc xây dựng bảng định tuyến của router được thực hiện bằng tay bởi người quản trị.
+ Định tuyến động: Việc xây dựng và duy trì trạng thái của bảng định tuyến được thực hiện tự động bởi router.
- 2 Định tuyến tĩnh : 
- Định tuyến tĩnh là quá trình router thực hiện chuyển gói dữ liệu tới địa chỉ mạng đích dựa vào địa chỉ IP đích của gói dữ liệu. Để chuyển được gói dữ liệu đến đúng đích thì router phải học thông tin về đường đi tới các mạng khác. Thông tin về đường đi tới các mạng khác sẽ được người quản trị cấu hình cho router. Khi cấu trúc mạng thay đổi, người quản trị mạng phải tự thay đổi bảng định tuyến của router.
- Kỹ thuật định tuyến tĩnh đơn giản, dễ thực hiện, ít hao tốn tài nguyên mạng và CPU xử lý trên router (do không phải trao đổi thông tin định tuyến và không phải tính toán định tuyến). Tuy nhiên kỹ thuật này không hội tụ với các thay đổi diễn ra trên mạng và không thích hợp với những mạng có quy mô lớn (khi đó số lượng route quá lớn, không thể khai báo bằng tay được).
- Ưu điểm:
+ Sử dụng ít bandwidth hơn định tuyến động.
+ Không tiêu tốn tài nguyên để tính toán và phân tích gói tin định tuyến.
- Nhược điểm:
+ Không có khả năng tự động cập nhật đường đi.
+ Phải cấu hình thủ công khi mạng có sự thay đổi.
+ Phù hợp với mạng nhỏ, rất khó triển khai trên mạng lớn.
- Một số tình huống bắt buộc dùng định tuyến tĩnh:
+ Đường truyền có băng thông thấp
+ Người quản trị mạng cần kiểm soát các kết nối.
+ Kết nối dùng định tuyến tĩnh là đường dự phòng cho đường kết nối dùng giao thức định tuyến động.
+ Chỉ có một đường duy nhất đi ra mạng bên ngoài (mạng stub).
+ Router có ít tài nguyên và không thể chạy một giao thức định tuyến động.
+ Người quản trị mạng cần kiểm soát bảng định tuyến và cho phép các giao thức classful và classless.

 