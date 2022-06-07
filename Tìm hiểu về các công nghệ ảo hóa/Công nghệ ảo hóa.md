
# I Công nghệ ảo hóa  KVM
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

- 5. Tính năng công nghệ ảo hóa
- Tính năng bảo mật:
+ Khi công nghệ KVM kết hợp với Linux sẽ giúp tăng khả năng bảo mật SELinux ( xây dựng ranh giới bảo mật quanh máy ảo ),sVirt( đẩy mạnh khả năng của SELinux, tăng khả năng bảo mật kiểm soát truy cập bắt buộc MAC dùng cho máy ảo khách, chống lỗi ghi nhãn thủ công, cách ly VM)
- Lưu trữ:
+ KVM cho phép người dùng được sử dụng các bộ lưu trữ được Linux hỗ trợ như: bộ lưu trữ gắn mạng NAS, địa cục bộ,...Khi đó, bạn cũng có thể chia sẻ tệp để hình ảnh ảo hóa bởi nhiều máy chủ.
- Hỡ trợ phần cứng:
+ Công nghệ KVM cũng có thể sử dụng được nhiều nền tảng phần cứng được linux hỗ trợ
- Quản lý bộ nhớ:
+ KVM được sở hữu các chức năng quản lý bộ nhớ của linux, chũng giúp hỗ trợ truy cập bộ nhớ không đồng nhất, hợp nhất kernel cùng tran. Khi đó bộ nhớ ảo hóa KVM có khả năng hoán đổi có hiệu suất tốt, được chia sẻ hoặc sao lưu nởi một tệp đĩa.
- Di chuyển công nghệ ảo hóa KVM trực tiếp:
+ KVM sẽ cho phép bạn di chuyển ảo hóa trực tiếp – nghĩa là di chuyển một chương trình ảo hóa đang chạy mà không gây ra sự gián đoạn giữa các máy chủ vật lý. Lúc này, KVM vẫn được bật, mọi kết nối mạng và ứng dụng vẫn hoạt động bình thường. Đồng thời trong quá trình di chuyển nó không quên thực hiện cả các thao tác lưu trữ.
- Hiệu suất, khả năng mở rộng:
+ Do KVM sở hữu các ưu điểm của linux, đồng thời có khả năng mở rộng giúp phù hợp để đáp ứng nhu cầu khi máy khách và yêu cầu truy cập tăng lên nhiều lần. Công nghệ KVM cho phép khối lượng công việc ứng dụng yêu cầu khắt khe nhất được ảo hóa và là cơ sở cho nhiều thiết lập ảo hóa doanh nghiệp, điển hình như trung tâm dữ liệu, máy chủ ảo vps, công nghệ đám mây riêng.
- Độ trễ thấp hơn
+ Do linux có các phần cho phép mở rộng thời gian thực tế các ứng dụng dựa trên KVM chạy trong một chế độ trễ thấp hơn với mức độ ưu tiên tốt hơn. Đồng thời chúng tiến hành phân chia các quá trình yêu cầu 1 khoảng thời gian dài tính toán thành các khoảng nhỏ hơn, rồi sau đó lên lịch để xử lý tương ứng.
-  Quản lý với KVM
+ Thông qua KVM cho phép quản lý thủ công chương trình ảo hóa sau khi được kích hoạt từ máy trạm mà không cần thông qua công cụ quản lý. Chức năng thường được sử dụng để quản trị tài nguyên, tăng khả năng phân tích dữ liệu hợp lý các hoạt động.

- 6. Ưu và nhược điểm:
- Ưu điểm:
+ Khả năng linh hoạt: Mặc dù máy chủ gốc được cài đặt Linux , nhưng KVM hỗ trợ máy chủ ảo có thể chạy cả linux,windows. Khi được sử dụng kết hợp với QEMU,KVM có thể chạy MacOSX. KVM cũng hồ trợ cả x86 và x86-64 system.
+ Có tính độc quyền cao: Cấu hình từng gói VPS KVM sẽ chỉ được một người sở hữu và toàn quyền sử dụng tài nguyên đó(bao gồm CPU,RAM,DISK SPACE,...)mà không hề bị chia sẻ hay ảnh hưởng bởi các VPS khác hoạt động trên cùng hệ thống.
+ Độ bảo mật chắc chắn : Nhờ tích hợp các đặc điểm bảo mật của linux như SELinux với các cơ chế bảo mật nhiều lớp, KVM bảo vệ các máy ảo tối đa và cách ly hoàn toàn , tránh bị xâm hại.
+ Giúp tiết kiệm chi phí, độ mở rộng cao: do được phát triển trên nền tảng mã nguồn mở hoàn toàn miễn phí và được hỗ trợ từ cộng đồng và nhà sản xuất thiết bị, KVM ngày càng lớn mạnh và trờ thành một lựa chọn hàng đầu cho doanh nghiệp có chi phí thấp nhưng hiệu quả sử dụng đem lại cao.
- Nhược điểm: 
+ Cần yêu cầu cao về máy chủ: Do là công nghệ ảo hóa hoàn toàn phần cứng, KVM yêu cầu cấu hình server vật lý cao.
+ KVM chỉ có sẵn trong các hệ thống Linux
+ Cần nhiều thời gian để nghiên cứu và học tập để có thể đưa vào sử dụng.
+ Do tập trung hóa phần cứng nên rủi ro tăng cao trong trường hợp hệ thống bị lỗi.
# II VMware
- 1. Vmware server là gì?
+ VMware Server là 1 sản phầm ảo hóa miễn phí dành cho máy chủ windows và linux có hỗ trợ cấp doanh nghiệp.
+ Mợt virtual machine như 1 một máy chủ và là phần mềm. Virtual machine chạy các hệ điều hành và ứng dụng giống như một máy chủ vật lý. Tuy nhiên, máy ảo cung cấp nhiều lợi ích hơn cho người dùng so với máy chủ vật lý.
+ Máy ảo: 
 + Là phần cứng độc lập và chạy trên bất kỳ máy chủ vật lý x86 nào. 
 + Có thể truy cập tất cả các tài nguyên phần cứng máy chủ vật lý như CPU , bộ nhớ, đĩa , mạng và thiết bị ngoại vi.
 + Được lưu dưới dạng tệp và có thể được cấp phép và di chuyển nhanh chóng.
 + Hoàn toàn bị cô lập và an toàn.
 + Có thể chạy đồng thời và an toàn trên cùng một máy chủ vật lý.
 + là thiết bị di động vì vậy toàn bộ hệ thống cùng 1 máy chủ vật lý.
 + là thiết bị di động , vì vậy toàn bộ hệ thống bao gồm  virtual hardware, operating systems và các ứng dụng được cấu hình đầy đủ có thể dễ dàng di chuyển từ một máy chủ vật lý này đến một máy chủ khác, ngay cả khi đang hoạt động.
 + Có thể được xây dựng và phân phối dưới dạng các thiết bị ảo plug-and-play chứa toàn bộ phần cứng ảo, , operating system và các ứng dụng phần mềm được cấu hình đầy đủ.
 - 2. cơ chế hoạt động
 + VMware server cài đặt và chạy như một ứng dụng on top của hệ điều hành windows hoặc linux. Virtualiation layer sẽ phần vùng máy chủ vật lý sao cho nhiều máy ảo có thể chạy đồng thời trên một máy chủ đơn.
 + Tài nguyên máy tính của máy chủ vật lý là một nhóm tài nguyên thống nhất có thể được phân bổ cho virtual machines theo các được kiểm soát.
 + VMware Server tách riêng từng máy ảo khỏi máy chủ của nó và các máy ảo khác, để máy này không bị ảnh hưởng nếu có máy khác bị treo. Dữ liệu không bị rò ri trên máy ảo và ứng dụng chỉ có thể giao tiếp thông qua các kết nối mạng được cấu hình.  VMware Server đóng gói môi trường máy ảo như một tập hợp các tệp, giúp dễ sao lưu, di chuyển và sao chép.
 - 3. Tính năng:
 + Chạy trên mọi phần cứng x86 tiêu chuẩn.
 + Hỗ trợ 64-bit guset operating systems, bao gồm windows, linux, và solaris.
 + Hỗ trợ VMware VirtualCenter để quản lý hiệu quả cơ sở hạ tầng từ bảng điều khiển quản lý trung tâm.
 + Hỗ trợ thử nghiệm cho two-processor Virtual SMP.
 + Hỗ trợ thử nghiệm cho công nghệ ảo háo Intel®.
 + Chạy trên nhiều máy chủ Windows hoặc linux bao gồm pre-built virtual appliances.
 + Cài đặt như 1 ứng dụng, nhanh chóng và dễ dang. 
 + Tạo máy ảo nhanh chóng.
 + Hỗ trợ cho bất kỳ định dạng máy ảo VMware hoặc Microsoft nào và Symantec LiveState Recovery images.
 + Nâng cấp dễ dàng lên vmware
 + Giám sát và quản lý máy ảo với 1 giao diện điều khiển từ xa trực quan, thân thiện với người dùng.

 # - III Openstack

 - 1. Khái niệm
 + Openstack là nền tảng mã nguồn mở miễn phí được phát triển trên nền tảng công nghệ điện toán đám mây. Thông qua nền tảng điện toán đám mây, các máy ảo và các tài nguyên khác cung cấp cho người dùng dưới dạng Infrastructure-as-a-Service (IaaS).
 - 2. các thành phần
 -  Compute Infrastructure
 + Bao gồm nhiều loại nova như: nova compute, nova network,nova schedule, nova api và nova volume. 
 + No- Schedule có nhiệm vụ lọc ra các thông tin cụ thể từ số lượng thông tin khổng lồ để cung cấp một cách kịp thời. No-compute với nhiệm vụ chạy các máy ảo, No-network thực hiện việc cấu hình lại các mạng ảo cho máy ảo. Cuối cùng là No-Volume sẽ tiếp nhận công việc xử lý, tạo xoá thêm hoặc bớt các volume vào instance. 
 - Storage Infrastructure (Swift)  
 + Bao gồm Proxy node và Storage nodes. Ban đầu các proxy nodes sẽ tiếp nhận các yêu cầu xử lý và gửi về cho storage nodes , tiếp theo chính là sao lưu các mục yêu cầu dưới 1 accout, khu lưu trữ (container) hoặc vùng đối tượng(các object).
 + Thông tin thêm các container sẽ thuộc sở hữu của 1 account (không giới hạn số lượng) và các objiect sẽ là các tập con bên trong container. Do đó, điều bắt buộc chính là phải có ít nhất 1 container bên trong account để tiến hành các thao tác update. Swift sẽ thực hiện các công việc như ghi chép lại các thông tin dữ liệu.
  - Imaging service (Glance)
  + Chức năng của phần này là xử lý những file ảnh của máy chủ ảo. Ngoài ra, chúng ta còn thực hiện được 1 số công việc quản trị khác như cập nhật thêm các tính năng vitural disk images, cài đặt các chế độ quyền riêng tư cho các hình ảnh, dễ dàng tùy biến việc chỉnh sửa hoặc xóa ảnh.
  - 3 Lợi ích
  + Compute: quản lý và cung cấp máy ảo cho phép người điều khiển bằng lệnh.
  + Glance : quản lý các image ảo.
  + Object Storage: quản lý các kho lưu trữ ảo chứa các thông tin, dữ liệu.
  +  Identity Server: quản lý chương trình xác thực dành cho user và projects.
  + Open Network: quản lý network cho các máy ảo.
  + Open dashboard: cung cấp giao diện đồ họa cho người dùng. 






 


