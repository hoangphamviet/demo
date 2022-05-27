# I. Tìm hiểu về NAT
1.NAT là gì ?
NAT (Network Address Translation) là . Đây là kỹ thuật để chuyển đổi từ địa chỉ IP này sang địa chỉ IP khác. 
NAT được sử dụng phổ biến trong các mạng dùng địa chỉ cục bộ để truy cập đến mạng công cộng (tức là Internet). Để nối kết 2 mạng này với nhau, router biên đóng vai trò là vị trí thực hiện NAT.
- 2.Nhiệm vụ ?
- NAT có nhiệm vụ truyền gói tin từ lớp mạng này sang lớp mạng khác trong cùng một hệ thống. NAT sẽ thực hiện thay đổi địa chỉ IP bên trong gói tin. Sau đó chuyển đi qua router và các thiết bị mạng.
- 3.Ưu và nhược điểm ?
+ Tiết kiệm địa chỉ IPv4 : Lượng người dùng truy cập internet ngày càng tăng cao. Điều này dẫn đến nguy cơ thiếu hụt địa chỉ IPv4. Kỹ thuật NAT sẽ giúp giảm thiểu số lượng địa chỉ IP cần sử dụng.
+ Giúp che giấu IP bên trong mạng LAN.
+ NAT có thể chia sẻ kết nối internet cho nhiều máy tính, thiết bị di động khác nhau trong mạng LAN chỉ với 1 địa chỉ IP public duy nhất.
+ NAT giúp nhà quản trị mạng lọc được các gói tin đến và xét duyệt quyền truy cập của IP public đến 1 port bất kỳ.
- Nhược điểm:
+ Khi dùng kỹ thuật NAT, CPU sẽ phải kiểm tra và tốn thời gian để thay đổi địa chỉ IP. Điều này làm tăng độ trễ trong quá trình switching. Làm ảnh hưởng đến tốc độ đường truyền của mạng internet.
+ NAT có khả năng che giấu địa chỉ IP trong mạng LAN nên kỹ thuật viên sẽ gặp khó khăn khi cần kiểm tra nguồn gốc IP hoặc truy tìm dấu vết của gói tin.
+ NAT giấu địa chỉ IP nên sẽ khiến cho 1 vài ứng dụng cần sử dụng IP không thể hoạt động được.
- Phân loại NAT:
+ Hiện nay có 3 loại NAT phổ biến mà bạn cần biết đó là: Static NAT, Dynamic NAT và NAT Overload.
+ Dynamic NAT: Đuợc dùng để ánh xạ một địa chỉ IP này sang một địa chỉ khác một cách tự động, thông thường là ánh xạ từ một địa chỉ cục bộ sang một địa chỉ được đăng ký. Bất kỳ một địa chỉ IP nào nằm trong dải địa chỉ IP public đã định trước đều có thể được gán một thiết bị trong mạng
+ NAT overload: Là kỹ thuật sử dụng nhiều địa chỉ IP private ra ngoài sử dụng 1 IP public, nó đc ứng dụng trong trg hợp kết nối người dùng ra ngoài internet
+ NAT static: Là 1 kỹ thuật ánh xạ 1:1 1 địa chỉ IP private ra ngoài bằng 1 địa chỉ public theo 1 giao thức và 1 port cố định. Ứng dụng trong trường hợp cho phép NAT các máy chủ ra ngoài Internet.
