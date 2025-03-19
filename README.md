# Network Basic

- [x]  Mô hình OSI, TCP/IP
- [x]  Switching
- [x]  Routing
- [x]  Các giao thức trong mạng Internet
- [x]  NAT
- [x]  Firewall
- [x]  Cài đặt hệ điều hành Ubuntu 20.04 trên VMware
- [x]  Tìm hiểu network trong VMware
- [x]  Cấu hình ip tĩnh trong ubuntu 20.04
- [ ]  

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

- Hiện nay có 14 giao thức mạng phổ biển
    - **Internet Protocol Suite (TCP/IP)**
        - Bộ giao thức cơ bản của Internet.
        - Gồm nhiều giao thức, trong đó TCP và IP là chính.
    - **Protocol Stack**
        - Tập hợp các lớp giao thức hoạt động cùng nhau để kết nối mạng.
    - **TCP (Transmission Control Protocol)**
        - Cung cấp kết nối dữ liệu đáng tin cậy.
        - Gửi dữ liệu theo thứ tự, kiểm tra lỗi.
        - Ứng dụng: Web, email, truyền file.
    - **IP (Internet Protocol)**
        - Định tuyến và chuyển tiếp dữ liệu qua mạng.
        - Giúp kết nối các thiết bị trên Internet.
    - **HTTP (Hypertext Transfer Protocol)**
        - Giao thức truyền tải dữ liệu cho World Wide Web.
        - Cổng: 80 (HTTP) và 443 (HTTPS – bảo mật).
    - **FTP (File Transfer Protocol)**
        - Dùng để truyền file giữa các máy tính.
        - Cổng: 20/21.
    - **SSH (Secured Shell)**
        - Quản lý thiết bị mạng qua dòng lệnh một cách an toàn.
        - Thay thế Telnet do bảo mật cao hơn.
        - Cổng: 22.
    - **Telnet**
        - Quản lý thiết bị mạng qua dòng lệnh.
        - Không bảo mật.
        - Cổng: 23.
    - **SMTP (Simple Mail Transfer Protocol)**
        - Chuyển email giữa các mail server và từ người dùng đến hệ thống mail.
        - Cổng: 25; SMTPS bảo mật qua cổng 465 (không tiêu chuẩn).
    - **DNS (Domain Name System)**
        - Chuyển đổi tên miền thành địa chỉ IP.
        - Cổng: 53.
    - **POP3 (Post Office Protocol version 3)**
        - Lấy mail từ máy chủ và xóa sau khi tải về.
        - Cổng: 110; bảo mật qua cổng 995.
    - **IMAP (Internet Message Access Protocol)**
        - Lấy mail từ máy chủ mà không xóa dữ liệu.
        - Cổng: 143; bảo mật qua cổng 993.
    - **SNMP (Simple Network Management Protocol)**
        - Quản lý, giám sát và cấu hình thiết bị mạng.
        - Hỗ trợ thông báo (trap) khi có sự kiện.
        - Cổng: 161/162.
    - **HTTPS (HTTP over SSL/TLS)**
        - Phiên bản bảo mật của HTTP, sử dụng SSL/TLS.
        - Cổng: 443.
- Active Recall
    - Hãy giải thích vai trò của TCP trong Internet Protocol Suite và vì sao nó được coi là giao thức cốt lõi để truyền dữ liệu đáng tin cậy?
    - So sánh chức năng của TCP và IP trong việc đảm bảo truyền tải dữ liệu qua mạng Internet.
    - HTTP và HTTPS khác nhau như thế nào về mặt bảo mật, và cổng mặc định của chúng là gì?
    - Khi nhận email, bạn sẽ gặp gì khi sử dụng POP3 so với IMAP?
    - Tại sao SSH lại được ưu tiên sử dụng hơn Telnet trong quản lý thiết bị mạng, và cổng mặc định của SSH là gì?

# NAT

- NAT là “mạng ảo”
    - Trong môi trường máy ảo sử dụng mạng NAT, mỗi máy ảo được cấp một địa chỉ IP riêng (ex: 10.0.0.99) do người dùng chỉnh sửa.
- Chuyển đổi IP khi truyền ra ngoài Internet
    - Khi máy ảo giao tiếp với bên ngoài, địa chỉ IP nội bộ sẽ được chuyển thành địa chỉ IP của mạng vật lý (WIFI) để truyền dữ liệu lên Internet.
- Cấu hình NAT trong máy ảo
    - Cấu hình mạng NAT sẽ có một gateway cố định (.2) và DHCP là địa chỉ cấp phát từ 1 đến 254.
- Lợi ích
    - NAT không chỉ giúp ẩn địa chỉ IP nội bộ, nó còn tạo thêm lớp bảo mật, mà còn có phép tùy chỉnh cấu hình mạng theo yêu cầu của người dùng.
- Active Recall
    - NAT là “mạng ảo” nghĩa là gì trong môi trường máy ảo?
    - Khi máy ảo giao tiếp ra ngoài Internet, địa chỉ IP nội bộ của nó được chuyển đổi thành địa chỉ nào?
    - Trong cấu hình NAT của máy ảo, gateway cố định thường được đặt ở địa chỉ nào?
    - DHCP trong cấu hình NAT cấp phát địa chỉ từ bao nhiêu đến bao nhiêu?
    - Những lợi ích chính của NAT là gì?

# Firewall

- Firewall - Tường lửa
    - Kiểm soát luồng thong tin giữa các mạng.
- Chức năng
    - Phát hiện, ngăn chặn truy cập trái phép.
- Mục đích
    - Đảm bảo an toàn thông tin và bảo vệ hệ thống.
- Active Recall
    - Firewall có chức năng gì trong hệ thống mạng?
    - Firewall giúp kiểm soát luồng thông tin giữa những gì?
    - Tại sao firewall quan trọng đối với an toàn thông tin?
    - Firewall có thể phát hiện và ngăn chặn điều gì?
    - Mục tiêu chính của firewall trong network basic là gì?

# Cài đặt hệ điều hành Ubuntu 20.04 trên VMware

- Bước 1
    - Cài đặt phiên bản server. [Tải Ubuntu Server tại đây](https://ubuntu.com/download/server)
    
    ![image.png](image.png)
    
- Bước 2
    - Mở VMware, chọn **Create a New Virtual Machine** để khởi tạo máy ảo Ubuntu.
    
    ![image.png](image%201.png)
    
    - Nhấn **Next** để tiếp tục.
    - Chọn file cấu hình vừa tải
        
        ![image.png](image%202.png)
        
    - Chọn file cấu hình xong tiếp tục nhấn “next”.
- Bước 3
    - Khởi động máy ảo và bắt đầu cài đặt Ubuntu Server.
        
        ![image.png](image%203.png)
        
    - Click chuột vào mũi tên rồi nhấn “enter”.
        
        ![image.png](image%204.png)
        
    - Tiếp theo là cài đặt ngôn ngữ, nhấn “enter” để tiếp tục
        
        ![Screenshot 2025-03-17 222537.png](1e904468-2f89-48fc-8557-7a19ad89ade7.png)
        
    - Bỏ qua quá trình cập nhật cài đặt
        
        ![Screenshot 2025-03-17 222546.png](Screenshot_2025-03-17_222546.png)
        
    - sử dụng mũi tên xuống nhấn **Continue without updating** (Tiếp tục mà không cần cập nhật). rồi “enter”.
    - Chọn bố cục phím
        
        ![Screenshot 2025-03-17 222559.png](Screenshot_2025-03-17_222559.png)
        
    - Cấu hình giao diện mạng.
        
        ![Screenshot 2025-03-17 222608.png](Screenshot_2025-03-17_222608.png)
        
    - Cài **Định cấu hình chi tiết proxy để kết nối với Internet.** Chọn **Done** rồi nhấn **Enter.**
        
        ![image.png](image%205.png)
        
    - **Định cấu hình Ubuntu Archive Mirror.** Chọn **Done** rồi nhấn **Enter.**
        
        ![image.png](image%206.png)
        
    - **Chọn cấu hình lưu trữ.** Chọn **Done** rồi nhấn **Ente**
        
        ![image.png](image%207.png)
        
    - **Định cấu hình hồ sơ của bạn**
        
        ![image.png](image%208.png)
        
    - **Điền các thông tin để đăng nhập server. Sau đó** Chọn **Done** rồi nhấn **Enter.**
        
        ![Screenshot 2025-03-17 222855.png](Screenshot_2025-03-17_222855.png)
        
    - **Nhấn “Reboot” để hoàn tất cả đặt để máy tự động chạy.**
- Bước 4
    - Đăng nhập
        
        ![image.png](image%209.png)
        
    - Sau khi đăng nhập thì cập nhật hệ thống.
    
    ```bash
    sudo apt update && sudo apt upgrade
    ```
    

# Tìm hiểu network trong VMware

- Bridged
    - Máy ảo dùng chung mạng với máy thật.
    - Có địa chỉ IP trong cùng subnet với máy thật.
- Host - Only
    - Máy ảo chỉ có thể giao tiếp với máy thật và các máy ảo khác trong cùng host.
    - Không có kết nối Internet.
    - Đây là mạng chỉ dùng trong nội bộ.
- NAT
    - Máy ảo kết nối mạng qua máy thật.
    - Máy ảo không trực tiếp nhận từ IP ngoài, mà dùng Ip riêng (do mình đặt).
    - Không bị phát hiện khi truy cập mạng.
- Custom Network (hay dùng VMmet8)
    - Cho phép cấu hình nâng cao với VMware Virtual Network Editor.
    - Có thể tạo mạng riêng theo yêu cầu, thêm DHCP, NAT, hoặc điều chỉnh subnet.
- Active Recall
    - **Bridged Network hoạt động như thế nào và tại sao máy ảo có thể nhận IP trong cùng subnet với máy thật?**
    - **Sự khác biệt chính giữa Host-Only và NAT là gì?**
    - **Tại sao máy ảo sử dụng NAT không bị phát hiện khi truy cập mạng?**
    - **Custom Network trong VMware cho phép điều chỉnh những yếu tố nào?**
    - **Khi nào nên sử dụng Host-Only thay vì Bridged hoặc NAT?**

# Cấu hình IP tĩnh trong ubuntu 20.04

- Bước 1: Xem cấu hình mạng hiện tại
    
    ```bash
    ip a
    ```
    
    ![image.png](image%2010.png)
    
    - Hiện tại card mạng là `ens33`
- Bước 2:  Chỉnh sửa file cấu hình mạng
    - Xem tên file cấu hình
        
        ```bash
        ls /etc/netplan/
        ```
        
    - Hiện tại, file có tên dạng `50-cloud-init.yaml`
    - Mở file cấu hình Netplan để chỉnh sửa
    
    ```bash
    sudo nano /etc/netplan/50-cloud-init.yaml
    ```
    
    ```bash
    network:
        ethernets:
            ens33: 
    	          dhcp4: false
    	          addresses:
    	            - 10.0.0.86/24
    	          gateway4: 10.0.0.2
    	          nameservers:
    	            addresses:
    	             - 8.8.8.8
    	             - 8.8.4.4
    	  version: 2  
    ```
    
    - Sau khi chỉnh sửa file trong `nano`, nhấn: **`Ctrl + X` → `Y` → `Enter`**
- Bước 3: Áp dụng thay đổi và kiểm tra lại IP
    
    ```bash
    sudo netplan apply
    ip a
    ```
    
- Bước 4: `ping 8.8.8.8` để kiểm tra mạng có hoạt động không.
    
    ![image.png](image%2011.png)
