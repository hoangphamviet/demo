# I DNS là gì
- 1. Khái niệm
- DNS (Domain Name System) là hệ thống phân giải tên miền. Là một hệ thống chuyển đổi các tên miền website đang sử dụng, ở dạng www.tenmien.com sáng 1 địa chỉ ip dạng số tương ứng tên miền đó và ngược lại.
- 2. Các thức hoạt động của DNS
- Khi người dùng muốn truy cập vào website , sẽ cần sử dụng tên miền để kết nối. Sau đó máy chủ tên miền sẽ tiếp nhận yêu cầu và thực hiện việc tra cứu địa chỉ IP tương ứng với tên miền trong cơ sở dữ liệu.
- Sau khi đã tìm được địa chỉ IP tương ứng với tên miền mà người dùng yêu cầu, hệ thống DNS sẽ tự động chuyển đổi và kết nối dữ liệu với web được lưu trữ theo địa chỉ IP đó.
- Còn nếu không tìm được, tền miền sẽ được chuyển đến máy chủ tên miền ở mức cao hơn đó là mức ROOT. Tại đây thì quá trình tìm kiếm IP tương ứng sẽ tiếp diễn và nếu vẫn không tìm được địa chỉ tương ứng thì người dùng sẽ nhận được báo lỗi.
- DNS có quy trình thông qua nhiều giai đoạn và cơ chế nhiệm vụ khác nhau. Những quy trình này là cơ chế phân giải địa chỉ, vận hành bộ nhờ đệm của máy chủ tên miền, phân giải DNS, lưu trữ dữ liệu caching, tra cứu ngược, tra cứu client,...
- 3. Các loại DNS server và vai trò
- Root Name servers:
+ là server quan trọng nhất trong hệ thống cấp bậc của DNS. Root Name servers là một thư viện để định hướng tìm kiếm giúp bạn.
- DNS Recursor
+ giữ trách nhiệm liên lạc với các server khác để phản hồi đến trình duyệt người dùng.
- TLD Nameserver
+ khi ta truy câp 1 trang google bình thường, phần mở rộng sẽ thấy ".com" nó chính là 1 trong các Top-level Domain. Đây là nhà quản lý toàn bộ hệ thống thông tin của một phần mở rộng tên miền chung.
+ theo trình tự ,TLD name server sẽ phản hồi từ DNS resolver, sau đó nó cho 1 Authoritative DNS Server – hay nơi chứa chính thức nguồn dữ liệu của tên miền đó.
- Authoritative Nameserver
+ Khi DNS resolver tìm thấy Authoritative Nameserver , đó là lúc mà việc phần giải tên miền diễn ra.
+  Authoritative Name Server có chứa thông tin cho biết tên miền đang gắn với địa chỉ nào. Nó sẽ cung cấp cho Recursive Resolver địa chỉ IP cần thiết tìm thấy trong danh mục những bản ghi của nó.
# II DNS record là gì ?
- 1. DNS record là bản ghi nằm trong DNS servers cung cấp thông tin về cơ sở dữ liệu DNS, cho biết các tên miền, địa chỉ IP gắn với tên miền và cách xử lý các yêu cầu với tên miền đó …
- 2. Thông tin trong mỗi bản ghi DNS ?
- Mỗi bản ghi DNS chứa 4 trường chính :
+ Type : Loại bản ghi DNS xác định phần domain mà mỗi bản ghi sẽ thay đổi. Các loại bản ghi quan trọng nhất để giúp bạn thiết lập và vận hành được đề cập bên dưới.
+ Name : Trường này cho phép thêm tiền tố vào tên miền chính . Nếu đang thêm bản ghi cho một domain phụ, vd: shop.example.com,  sẽ nhập "shop" vào trường này.
+ Data : Trường dữ liệu chứa thông tin khác nhau tùy thuộc vòa loại bản ghi đang tạo.
+ TTL (Time to Live) : là thời gian tính bằng giây để mọi thay đổi đối với bản ghi DNS có hiệu lực. Với TTL là 3600 = 1 giờ, tất cả thay đổi đối với bản ghi này sẽ cập nhập giá trị mới, trường hợp nếu sau 1 giờ các máy chủ phân giải tên miền không còn thấy bản ghi này nữa thì chính thức nó bị xóa.
- 3. Các loại bản ghi
 - A record
 + A được hiểu là "Adress", và đây là loại record phổ biến nhất, được dùng để trỏ 1 địa chỉ IP đến 1 tên miền.
+ A record chỉ dùng cho ipv4, còn với ipv6 phải dùng AAAA record.
+ Hầu hết các web chỉ có một bản ghi A, nhưng 1 số trang web sẽ có 1 vài bản ghi A không giống nhau. Điều này có nghĩa là 1 tên miền có thể được trỏ đến nhiều địa chỉ IP khác nhau....

- AAAA record 
+ Tương tự như A record nhưng nó lưu trữ địa chỉ ipv6 của tên miền.
