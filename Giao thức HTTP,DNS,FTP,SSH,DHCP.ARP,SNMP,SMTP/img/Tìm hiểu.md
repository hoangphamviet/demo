# I.Giao thức HTTP
## 1.1 Giao thức HTTP
- HTTP (HyperText Transfer Protocol) là giao thức truyền tải siêu văn bản được sử dụng trong www dùng để truyền tải dữ liệu giữa Web server đến các trình duyệt Web và ngược lại
## 1.1.2 Cấu trúc của HTTP
- Cấu trúc của HTTP bao gồm 2 đối tượng là Client và Server. Có thể coi HTTP như giao thức gửi các yêu cầu và phản hồi giữa Client - Server. Tại giao thức này, mọi thiết bị tìm kiếm hay trình duyệt web sẽ đóng vai trò như máy khách, còn máy chủ web có vai trò như Server. 

- Client: Client (máy khách) gửi yêu cầu cụ thể đến Server theo mẫu phương thức yêu cầu -> Các phiên bản giao thức cùng với URI gửi thông báo MIME (gồm thông tin máy khách, nội dung của đối tượng, bộ chỉnh sửa) đến server qua kết nối TCP/IP.
- Server: Server nhận được yêu cầu -> Phản hồi lại bằng một dòng trạng thái qua thông báo MIME có chứa thông tin máy chủ, thông tin về nội dung của đối tượng và thực thể của đa phương tiện.
## 1.1.3 cách thức hoạt động: 
- HTTP hoạt động theo mô hình Client (máy khách) khởi tạo yêu cầu (tạo kết nối TCP tới cổng 80 hoặc 1 cổng khác trên server )-> server nhận yêu cầu -> gửi lại trạng thái đến cho client kèm theo thông điệp (thông điệp ở đây là thông điệp yêu cầu, báo lỗi hay thông tin khác ) . Sau khi phiên giao dịch hoàn thành Việc truy cập website được tiến hành dựa trên các giao tiếp giữa 2 đối tượng trên.
- HTTP tiến hành hoạt động giao tiếp giữa server và máy khách thông qua một loạt các tin nhắn. 3 kiểu tin nhắn được dùng nhiều nhất trong quá trình hoạt động của HTTP là GET, POST, HEAD.
 - HTTP GET: Loại tin nhắn chỉ bao gồm một đường dẫn gửi đến server. Nó thường chỉ tiếp nhận dữ liệu mà gần như không có những tác dụng khác. Máy chủ sẽ xử lý dữ liệu của URL và gửi phản hồi về cho trình duyệt. Thao tác này được sử dụng khi Client cần lấy toàn bộ nội dung URL.
- HTTP POST: Tin nhắn này dùng để đặt các tham số dữ liệu vào phần thân của thông báo yêu cầu. Nó được dùng khi cần upload tệp tin hay submit form web, chủ đề,...
- HTTP HEAD: Có cách thức hoạt động tương tự như tin nhắn GET, điểm khác biệt duy nhất là máy chủ sẽ phản hồi thông tin về header. 
- Khi bạn truy cập một trang web qua giao thức HTTP, trình duyệt sẽ thực hiện các phiên kết nối đến server của trang web đó thông qua địa chỉ IP do hệ thống phân giải tên miền DNS cung cấp. Máy chủ sau khi nhận lệnh, sẽ trả về lệnh tương ứng giúp hiển thị website, bao gồm các nội dung như: văn bản, ảnh, video, âm thanh,…

## 1.2 Giao thức DNS
- DNS( Domain Name System) là hệ thống phân giải tên miền. DNS cho phép thiết lập ứng giữa địa chỉ IP và tên miền trên Internet.
- Quá trình phân giải DNS bao gồm chuyển đổi tên máy chủ (chẳng hạn như www.example.com) thành địa chỉ IP thân thiện với máy tính (chẳng hạn như 192.168.1.1). Một địa chỉ IP được cung cấp cho mỗi thiết bị trên Internet và địa chỉ đó là cần thiết để tìm thiết bị Internet phù hợp.
## 1.3 Giao thức FTP 
FTP (File Transfer Protocol) là một giao thức truyển tải tập tin trong mạng thông qua giao thức TCP/IP . Với giao thức này các máy client trong mạng có thể truy cập đến máy chủ FTP để gửi hoặc lấy dữ liệu.
Các hình thức hoạt động dựa trên 2 tiến trình cơ bản là kiểm soát kết nối và kết nối dữ liệu.
- Control connection(kiểm soát kết nối ) Khi phiên làm việc bắt đầu thì trong suốt quá trình diễn ra công việc thì tiến trình này sẽ kiểm soát kết nối và chỉ thực hiện nhiệm vụ các thông tin điều khiển đi qua trong suốt quá trình truyền dữ liệu. 
- Data connection(kết nối dữ liệu) đây là tiến trình nhắm thực hiện các kết nối chứ không còn kiểm soát nữa. Nó sẽ kết nối các dữ liệu khi dữ liệu được gửi từ server tới client và ngược lại .Tiến trình thực hiện xuyên suốt quá trình đến khi việc truyền dữ liệu hoàn tất thì nó cung ngừng lại .
## 1.4 Giao thức SSH 
- SSH là một giao thức mạng cung cấp cho người dùng cách truy cập an toàn vào một máy tính qua một mạng không được bảo mật. 
- Cách thức hoạt động của SSH theo 3 bước:
B1 : Định danh host xác định định danh của hệ thống tham gia phiên làm việc SSH (khởi tạo kết nối )
B2 : Mã hóa dữ liệu thiết lập kênh làm việc mã hóa. Sau khi client xác được định danh của server kết nối bảo mật đối xứng được hình thành giữa 2 bên.
B3: Chứng thực và giải mã xác thực người sử dụng có quyền đăng nhập hệ thống.Kết nối này sẽ sử dụng server xác thực client.
## 1.5 Giao thức DHCP 
- DHCP là giao thức được sử dụng để cấu hình địa chỉ ip cho thiết bị máy tính. Mỗi thiết bị của người dùng đều cần phải có ít nhất 1 địa chỉ IP để tham gia vào mạng - để kết nối tới các dịch vụ khác. Nó cung cấp cho máy tính địa chỉ ip ; subnet mask; default gateway. Và nó thường được cấp phát bởi DHPC server được tích hợp sẵn trên router.
- Cách thực hoạt động của DHCP  : khi có một thiết bị cần truy cập mạng nó sẽ gửi yêu cầu từ một router và được router gán cho một địa chỉ IP khả dụng.Router hoạt động như một máy chủ DHCP đối với các mô hình mạng nhỏ hoặc hộ gia đình. Đối với các mạng lớn hơn một router không thể quản lý số lượng lớn các thiết bị nên sẽ có một máy chủ chuyên dụng để cấp IP.
## 1.6 Giao thức ARP 
- ARP (Address Resolution Protocol) là giao thức mạng được dùng để tìm ra địa chỉ phần cứng (địa chỉ MAC) của thiết bị từ một địa chỉ IP nguồn. Nó được sử dụng khi một thiết bị giao tiếp với các thiết bị khác dựa trên nền tảng local network.
## 1.7 Giao thức SNMP
Giao thức SNMP là một trong những giao thức mạng  để quản lý và giám sát các phần tử mạng. Hầu hết các thiết bị mạng được cung cấp đi kèm với SNMP agent. Các agent này phải được kích hoạt và cấu hình để giao tiếp với các công cụ giám sát mạng hoặc hệ thống quản lý mạng (NMS).
## 1.8 Giao thức SMTP
 - SMTP (Simple Mail Transfer Protocol) là giao thức truyền tải thư tín đơn giản hóa. Và giao thức này thực hiện nhiệm vụ chính là gửi mail còn việc nhận mail hay truy xuất dữ liệu mail server sẽ có giao thức IMAP hay POP3 đảm nhiệm.
 - SMTP Server (server dùng để gửi mail) là một dịch vụ cho phép gửi email với số lượng lớn, tốc độ nhanh mà không bị giới hạn như các hòm mail miễn phí của Gmail hoặc mail đi kèm hosting. Nói cách khác các máy chỉ chủ giúp bạn thao tác gửi thư người ta thường gọi là SMTP server chúng thực hiện gửi thư qua giao thức TCP hoặc IP.

 - Giao thức SMTP hoạt động :
 - Khi doanh nghiệp gửi một email nào đó, hệ thống SMTP sẽ tự động dựa vào tên địa chỉ email đó và chuyển thông báo tới cho máy chủ SMTP. Sau khi SMTP server nhận được tín hiệu, tín hiệu sẽ được trao đổi giữa máy chủ SMTP và máy chủ DNS để tìm ra tên miền gốc tại Hostname trong máy chủ SMTP.

- Máy chủ thực hiện bước kiểm tra liệu thông tin người dùng với thông tin email có trùng khớp hay không, nếu trùng khớp thì doanh nghiệp sẽ nhận hay gửi dữ liệu có dung lượng lớn thông qua email và nhận các thư điện tử bằng phần mềm.

- Nhằm đề phòng trường hợp máy chủ SMTP và máy chủ DNS có thể không trao đổi với nhau, những tín hiệu không được phản hồi ấy sẽ gửi tới server trung gian. Server trung gian vẫn nhận được tín hiệu gốc và bắt đầu truyền qua nhiều máy chủ khác cho tới khi gửi tới Server gốc. Hệ thống phụ sẽ chạy hết công suất cùng thời gian tối đa trước khi tín hiệu bị thông báo là hết hạn và không sử dụng được nữa.

- Hầu hết Email client (outlook, thunderbird, app trên điện thoại, webmail...) đều sử dụng giao thức SMTP để gửi và nhận thư. 

