# I Công nghệ ảo hóa
- 1. KVM
- KVM ( Kernel Virtualization Machine) máy ảo dựa trên hạt nhân. Sử dụng môi trường máy tính ảo không yêu cầu phần cứng bổ sung để thiết lập. Thay vào đó nó sử dụng tài nguyên từ hệ thống máy tính hiện có bao gồm phần cứng đang lưu trữ nó.
- Sử dụng KVM với không gian người dùng cho phép người dùng thiết lập môi trường ảo cho nhiều mục đích khác nhau, gồm kiểm thử phần mềm và các không gian làm việc của người khác.
2. Yêu cầu hệ thống của KVM 
- Việc sử dụng KVM trên 1 hệ thống máy vi tính cụ thể yêu cầu bộ xử lý phải có phần mở rộng được ảo hóa phần cứng. KVM hỗ trợ 1 số loại bộ xử lý : x86, S/390, PowerPC và IA-64
- Môi trường KVM sử dụng 1 BIOS cụ thể là SeaBIOS và có khả năng mô phỏng các thành phần phần cứng như card màn hình, card âm thanh, card mạng, RAM và CPU. Việc quản lý các môi trường này có thể được thực hiện thông qua việc sử dụng một số công cụ quản lý đồ họa, bao gồm Witsbits, ConVirt, OpenNode, SolusVM và Virtualbricks.
3. Đặc điểm :
- Công  nghệ này có cách hoạt động như người quản lý giúp chia sẻ các nguồn tài nguyên ổ đĩa, network , CPU 1 cách công bằng. Công nghệ này nguồn mở còn được tích hợp trong Linux:
 + Với công nghệ này bạn có thể chuyển Linux thành ảo hóa để máy chủ chạy trên nhiều môi trưởng ảo bị cô lập là máy khách hoặc máy ảo VM.
 + KVM là một phần của mã Linux và được hưởng lời từ các tính năng, khi đó KVM sẽ được hưởng lời từ mọi tính năng, Khả năng sửa lỗi và tiến bộ cập nhập mới của linux mà khồn cần kỹ thuật bổ sung.
 + Ảo hóa KVM không có tài nguyên dùng chung, bởi chúng đã được mặc định sẵn để chia sẻ. Do vậy mà RAM của mỗi KVM được định sẵn cho từng gói VPS, để có thể tận dụng triệt để 100% và không bị chia sẻ. Điều này sẽ giúp cho chúng hoạt động ổn định hơn, ngoài ra không bị ảnh hưởng bởi các VPS khác chung hệ thống. Tương tự với các tài nguyên ở ổ cứng được định săn phân chia như RAM.
 
 - 4. Cách hoạt động :
 + KVM cung cấp một số thành phần cấp hệ điều hành , chẳng hạn như trình quản lý bộ nhớ, bộ lập lịch xử lý , ngăn xếp đầu vào/ đầu ra(I/0), trình điều khiển thiết bị, trình quản lý bảo mật, ngăn xếp mạng để có thể chạy ảo hóa.
 + Mọi ảo hóa sẽ được triển khai như 1 quy trình linux thông thường được lên lịch sẵn bởi bộ lập lịch linux tiêu chuẩn, với phần cứng ảo chuyên dùng như card mạng , bộ điều hợp đồ họa, CPU, bộ nhớ và đĩa.



