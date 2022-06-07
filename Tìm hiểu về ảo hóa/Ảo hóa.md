# I Ảo hóa là gì?
- Ảo hóa là công nghệ cho phép khai thác triệt để khả năng hoạt động của các phần cứng trong hệ thống máy chủ  bằng cách chạy đồng thời nhiều OS trên cùng lớp vật lý.
- Cùng chia sẻ tài nguyên phần cứng và được quản lý bởi lớp ảo hóa
- Lớp ảo hóa nằm giữa một tầng trung gian giữa phần cứng và phần mềm hệ điều hành (OS) giúp quản lý, phân phát tài nguyên phần cứng cho lớp OS ảo hoạt động ở trên.
- 2. Các thành phần của 1 hệ thống ảo hóa
+ Tài nguyên vật lý chính : Máy chủ vật lý, CPU, RAM , ổ đĩa cứng , card mạng ,..
Nhiệm vụ là chia tài nguyên cấp cho các máy ảo.
+ Phần mềm ảo hóa : cung cấp truy cập cho mỗi máy chủ đến tài nguyên của máy vật lý, lập kế hoạch và phân chia tài nguyên vật lý cho các máy chủ ảo 
+ Hệ điều hành khác : được cài đặt trên một máy chủ ảo, tháo tác như hệ điều hành bình thường.
+ Máy ảo : nó hoạt động như một máy chủ vật lý thông thường với tài nguyên riêng, giao diện riêng , hệ điều hành riêng.
- 3. Cách thức hoạt động
- Ảo hóa được xây dựng dựa trên giải pháp chia 1 máy vật lý thành nhiều máy con . Giải pháp này cho phép tạo tách rời các máy ảo và điều phối truy cập của các máy ảo đến tài nguyên phần cứng và cấp pháp tài nguyên tự động theo nhu cầu.Cấu trúc này giúp cần bằng khả năng điện toán mang lại:
+ Nhiều ứng dụng chạy trên cùng một server, mỗi máy ảo được lập trình trên máy chủ, do đó nhiều ứng dụng và các hệ điều hành có thể chạy cùng lúc chạy trên một host.
+ Tối đa hóa công suất sử dụng và tối thiểu hóa server: Mỗi máy chủ vật lý được sử dụng với đầy đủ công suất , cho phép giảm đáng kể chi phí nhờ sử dụng tối đa server.
+ Cấp phát tài nguyên và ứng dụng nhanh chóng , dễ dàng . Máy ảo được triển khái từ 1 file chứa đầy đủ phần mềm với cơ chế là copy điều này mang lại sự đơn giản, nhanh chóng và linh hoạt chưa từng có cho việc quản lý và cung cấp hạ tầng. 
- 4. Mục tiêu
+ Availability : giúp các ứng dụng hoạt động liên tục bằng các giảm thiểu ( bỏ qua ) thời gian chết khi phần cứng gặp sự cố , khi nâng cấp hoặc di chuyển .
+ Scalability : khả năng tùy biên, thu hẹp hay mở rộng mô hình server dễ dàng mà không làm gián đoạn ứng dụng.
+ Optimization : sử dụng triệt để nguồn tài nguyên phần cứng và tránh lãng phí bằng cách giảm số lượng thiết bị vật lý cần thiếu( giảm số lượng server, switch ,...)
+ Management : Khả năng quản lý tập trung , giúp việc quản lý trở nên dễ dàng hơn.
- 5. Ưu điểm và nhược điểm
 - Ưu điểm:
 + Tiết kiệm năng lượng tiêu thụ, giảm chi phí duy trì server
 + Giảm số lượng thiết bị vật lý cần thiết (giảm số lượng server, switch,cáp,...)
 + Tận dụng tối đa nguồn tài nguyên , tránh lãng phí
 + Quản lý tập trung , liên tục , nâng cao hiệu quả làm việc của quản trị viên
 + Khả năng mở rộng dễ dàng.
 - Nhược điểm: 
 + Thông thường , mỗi máy ảo chỉ sử dụng 1 file VMDK (file này có thể được chia nhỏ tùy theo cách cài đặt) để lưu lại toàn bộ dữ liệu trong máy ảo và 1 số file nhở khác để lưu lại cấu hình máy ảo. Do đó , nếu 1 trong những tập kia bị lỗi hoặc bị mất mà chưa được backup thì có thể xem như máy ảo bị hư không thể phục hồi
 + Ngoài ra nếu máy chủ có cấu hình phần cứng thấp nhưng lại có 1 máy ảo sử dụng quá nhiều tài nguyên hoặc chạy quá nhiều máy ảo sẽ làm chậm toàn bộ hệ thống bao gồm các máy ảo và các ứng dụng chạy trên máy ảo. Đồng thời 1 hoặc 1 vài máy chủ phải đảm nhận nhiều máy ảo chạt trên nó nên khi máy chủ gặp trục trặc thì các máy ảo cũng gặp sự cố theo
 + Ở góc độ bảo mật , nếu hacker nắm quyền điều khiển 1 máy chủ vật lý thì hacker có thể kiểm soát tất cả các máy ảo trong nó.
 # II . Các mức độ ảo hóa
 - Ảo hóa mạng 
 + Là phương pháp kết hợp các tài nguyên có sẵn trong mạng bằng cách chia băng thông khả dụng thành các kênh, mỗi kênh độc lập với các kênh khác và có thể gán hoặc chỉ định lại cho 1 máy chủ hoặc thiết bị cụ thể trong thời giản thực.
 - Ảo hóa bộ nhớ
 + Là tập hợp bộ nhớ vật lý từ nhiều thiết bị lưu trữ mạng thành một thiết bị duy nhất được quản lý từ bảng điều khiển trung tâm. Ảo hóa lưu trữ thường được sử dụng trong các mạng khư vực lưu trữ.
 - Ảo hóa máy chủ 
 + Là việc che giấu tài nguyên máy chủ- gồm số lượng và danh tính của từng máy chủ vật lý, bộ xử lý và hệ điều hành- khỏi người dùng máy chủ. Mục đích là giúp người dùng không phải hiểu và quản lý các chi tiết phức tạp của tài nguyên máy chủ trong khi tăng cường chia sẻ và sử dụng tài nguyên cũng như khả năng mở rộng sau này.
 - Ảo hóa dữ liệu
 + Là trừu tượng hóa các chi tiết kỹ thuật truyền thống của dữ liệu và quản lý dữ liệu chẳng hạn như vị trí hiệu suất hoặc định dạng có lợi cho quyền truy cập rộng hơn và khả năng phục hòi cao hơn gắn liền với nhu cầu kinh doanh.
 - Ảo hóa máy tính bàn 
 + Là ảo hóa tải máy trạm thay vì máy chủ. Điều này cho phép người dùng truy cập máy tính để bản từ xa, thường sử dụng 1 thin client  tại bàn làm việc. Vì máy  trạm về cơ bản đang chạy trong 1 máy chủ trung tâm dữ liệu ,nên việc truy cập vào nó có thể an toàn hơn và di động hơn.
 - Ảo hóa ứng dụng
 + Là trừu tượng hóa lớp ứng dụng khỏi hệ điều hành. Bằng cách này,ứng dụng có thể chạy ở dạng đóng gói mà không bị phụ thuộc vào hệ điều hành bên dưới. Điều này có thể cho phép 1 ứng dụng windows chạt trên linux và ngược lại , ngoài việc tăng thêm mức dộ cô lập.
 
