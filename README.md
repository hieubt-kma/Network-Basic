# Network Basic

- [x]  Mô hình OSI, TCP/IP
- [x]  Switching
- [x]  Routing
- [x]  Các giao thức trong mạng Internet
- [ ]  NAT
- [ ]  Firewall

# Mô hình OSI, TCP/IP

- OSI (Open Systems Interconnection)
    - là chia quá trình giao tiếp mạng thành 7 tầng để giúp các thiết bị khác nhau có thể giao tiếp với nhau dễ dàng. Nó giống như dây chuyền sản xuất, mỗi tầng làm nhiệm vụ riêng và chỉ làm với tầng bên trên hoặc bên dưới khi có sự cố.
    - Mục đích: Giúp chuẩn hóa các thiết bị giao tiếp, Dễ dàng phát hiện và sửa lỗi khi có sự cố
    - Các Tầng và chức năng:
    
    | Tầng | Chức năng | ví dụ |
    | --- | --- | --- |
    | 7. Application - Ứng dụng | Cung cấp giao diện cho người dùng và các ứng dụng. | Web (HTTP), Email (SMTP), tải file (FTP). |
    | 6. Presentation - Trình diễn | Mã hóa, giải mã, nén dữ liệu. | Chuyển đổi file .txt, .jpg; SSL/TLS bảo mật dữ liệu. |
    | 5. Session - Phiên | Quản l;ý kết nối giữa các thiết bị. |  Mở nhiều tab web cùng lúc những không bị trùng dữ liệu. |
    | 4. Transport - Giao vận | Đảm bảo dữ liệu được gửi đúng thứ tự và đầy đủ | TCP (chuyển file an toàn), UDP (stream video nhanh). |
    | 3. Network - Mạng | Định tuyến dữ liệu qua các mạng khác nhau. | Địa chỉ IP; Router tìm đường đi cho dữ liệu. |
    | 2. Data Link - Liên kết dữ liệu | Điều khiển truyền dữ liệu giữa các thiết bị trên cùng mạng vật lý. | Địa chỉ MAC; kết nối Wifi; Ethernet. |
    | 1. Physical - Vật lý | Chuyển dữ thành tín hiệu điện/ quang để truyền đi. | Cáp mạng; sóng Wifi, Bluetooth. |
    
- TCP/IP (Transmission Control Protocol/Internet Protocol)
    - là bộ giao thức cốt lõi của Internet. Nó chia quá trình giao tiếp thành 4 tầng - từ tầng ứng dụng đến tầng vật lý, nhằm định tuyến và truyền tải dữ liệu trên mạng.
    - Mục đích: Đảm bảo dữ liệu được truyền tải qua mạng một cách hiệu quả và tin cậy.
    - Các tầng và chức năng:
    
    | Tầng | Chức năng |
    | --- | --- |
    | 4. Application - Ứng dụng | Bao gồm các giao thức như HTTP, SMTP, FTP… (có thể tích hợp thêm các chức năng của tầng trình diễn và tầng phiên của OSI). |
    | 3. Transport - Giao vận | Đảm bảo kết nối tin cậy (TCP) hoặc không kết nối (UDP). |
    | 2. Internet  | Định tuyến dữ liệu giữa các mạng (IP, ICMP). |
    | 1. Network Accesss - Truy cập mạng | Xử lý việc truyền dữ liệu trên các phương tiện vật lý (Ethernet, Wi-Fi). |
- **Active Recall**
    1. **Mô hình OSI gồm bao nhiêu tầng và nhiệm vụ chính của từng tầng là gì?**
    2. **Sự khác biệt cơ bản giữa mô hình OSI và TCP/IP là gì?**
    3. **Giải thích vai trò của tầng giao vận trong cả hai mô hình.**
    4. **Trong ví dụ gửi email, mỗi tầng xử lý dữ liệu như thế nào?**
    5. **Tại sao TCP/IP lại được ưu tiên sử dụng trong thực tế so với mô hình OSI?**

# Switching

- Khái niệm
    
    **Switching** là quá trình chuyển dữ liệu giữa các thiết bị trong mạng. Nó giúp kết nối và truyền dữ liệu hiệu quả.
    
- Các loại switching chính
    - **Circuit Switching**: Tạo đường truyền cố định trước khi gửi dữ liệu (như gọi điện thoại cố định).
    - **Packet Switching**: Cắt dữ liệu thành gói nhỏ, gửi qua nhiều đường khác nhau (như Internet).
    - **Message Switching**: Dữ liệu được gửi dưới dạng thông điệp đầy đủ, mỗi điểm trung gian lưu trữ toàn bộ thông điệp trước khi chuyển tiếp (giống gửi thư qua bưu điện, nhưng có lưu trữ tạm thời ở trạm trung gian)
- **Active Recall**
    - **Switching là gì?**
    - **Có bao nhiêu loại switching chính?**
    - **Circuit Switching hoạt động như thế nào?**
    - **Packet Switching khác gì so với Circuit Switching?**
    - **Message Switching hoạt động ra sao?**

# Routing

- Khái niệm
    
    **Routing** là quá trình lựa chọn đường đi tối ưu để chuyển các gói dữ liệu từ nguồn đến đích, trong một mạng hoặc giữa các mạng.
    
- Chức năng
    - **Định tuyến (Path Selection):** Xác định đường đi tốt nhất.
    - **Chuyển tiếp gói (Packet Forwarding):** Chuyển các gói dữ liệu qua các nút trung gian.
    - **Quản lý bảng định tuyến:** Duy trì và cập nhật thông tin các tuyến đường.
- Active Recall
    - **Routing là gì và mục tiêu của quá trình routing là gì?**
    - **Chức năng "Định tuyến (Path Selection)" trong routing thực hiện nhiệm vụ gì?**
    - **"Chuyển tiếp gói (Packet Forwarding)" có vai trò gì trong quá trình truyền dữ liệu?**
    - **Tại sao việc quản lý bảng định tuyến lại quan trọng đối với quá trình routing?**
    - **Các chức năng định tuyến, chuyển tiếp gói và quản lý bảng định tuyến phối hợp như thế nào để đảm bảo dữ liệu được chuyển từ nguồn đến đích?**

# Các giao thức mạng trong internet

- Application Layer
    - **HTTP/HTTPS** – Giao thức truyền tải siêu văn bản (HyperText Transfer Protocol)
    - **FTP/SFTP** – Giao thức truyền tập tin (File Transfer Protocol)
    - **SMTP/POP3/IMAP** – Giao thức email
    - **DNS** – Hệ thống phân giải tên miền
    - SSH - Kết nối an toàn từ xa
- Transport Layer
    - **TCP** – Giao thức điều khiển truyền vận (Transmission Control Protocol)
    - **UDP** – Giao thức gói dữ liệu không kết nối (User Datagram Protocol)
- Network Layer
    - **IP (IPv4/IPv6)** – Giao thức định tuyến địa chỉ trên Internet
    - **ICMP** – Giao thức chẩn đoán mạng (ping, traceroute)
    - **ARP** – Giao thức phân giải địa chỉ MAC
- Data link Layer
    - **Ethernet** – Giao thức phổ biến trong LAN
    - **PPP** – Giao thức kết nối điểm-điểm (Point-to-Point Protocol)
    - **Wi-Fi (802.11)** – Kết nối không dây
- Active Recall
    - **HTTP và HTTPS khác nhau như thế nào? Tại sao HTTPS lại bảo mật hơn?**
    - **So sánh TCP và UDP: Chúng khác nhau ra sao về cách truyền dữ liệu và ứng dụng thực tế?**
    - **DNS hoạt động như thế nào trong việc phân giải tên miền thành địa chỉ IP?**
    - **ICMP được sử dụng trong những công cụ nào để chẩn đoán mạng?**
    - **Ethernet, PPP và Wi-Fi (802.11) có vai trò gì trong lớp Liên kết Dữ liệu?**
