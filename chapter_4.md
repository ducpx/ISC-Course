# Chapter 4: Network Security

## Mục lục

- [Module 1: Understand Computer Networking](#1)
- [Module 2: Understand Network (Cyber) Threats and Attacks](#2)
- [Module 3: Understand Network Security Infrastructure](#3)

<a name="1"></a>
## Module 1: Understand Computer Networking

### What is Networking
Mạng đơn giản là hai hoặc nhiều máy tính được liên kết với nhau để chia sẻ dữ liệu, thông tin hoặc tài nguyên.

Để thiết lập đúng cách truyền thông dữ liệu an toàn, điều quan trọng là phải khám phá tất cả các công nghệ liên quan đến truyền thông máy tính. Từ phần cứng và phần mềm đến các giao thức và mã hóa, v.v., có nhiều chi tiết, tiêu chuẩn và quy trình cần làm quen.

Types of Networks
    - Mạng cục bộ (LAN) - Mạng cục bộ (LAN) là mạng thường bao trùm một tầng hoặc tòa nhà. Đây thường là một khu vực địa lý hạn chế.
    - Mạng diện rộng (WAN) - Mạng diện rộng (WAN) là thuật ngữ thường được gán cho các kết nối đường dài giữa các mạng ở xa về mặt địa lý.

Network Devices:
    - Hub:
        được sử dụng để kết nối nhiều thiết bị trong một mạng. Chúng ít có khả năng được nhìn thấy trong mạng doanh nghiệp hoặc công ty hơn là trong mạng gia đình. Hub là thiết bị có dây và không thông minh như switches or routers.
    - Switches:
        Thay vì sử dụng hub, bạn có thể cân nhắc sử dụng switches hay còn được gọi là bộ tập trung thông minh. Switches là thiết bị có dây biết địa chỉ của các thiết bị được kết nối với chúng và định tuyến lưu lượng truy cập đến cổng/thiết bị đó thay vì truyền lại cho tất cả các thiết bị.

        Mang lại hiệu quả cao hơn cho việc phân phối lưu lượng và cải thiện thông lượng tổng thể của dữ liệu, Switches thông minh hơn hub, nhưng không thông minh bằng Router. Switch cũng có thể tạo các miền quảng bá riêng biệt khi được sử dụng để tạo VLAN, điều này sẽ được thảo luận sau.

    - Router:
        được sử dụng để kiểm soát luồng lưu lượng trên mạng và thường được sử dụng để kết nối các mạng tương tự và kiểm soát luồng lưu lượng giữa chúng. Router có thể có dây hoặc không dây và có thể kết nối nhiều thiết bị chuyển mạch. Thông minh hơn so với các trung tâm và thiết bị chuyển mạch, Router xác định "tuyến đường" hiệu quả nhất để lưu lượng truy cập qua mạng.

    - Firewall:
        là công cụ cần thiết trong việc quản lý, kiểm soát lưu lượng mạng và bảo vệ mạng. Firewall là một thiết bị mạng được sử dụng để lọc lưu lượng. Nó thường được triển khai giữa mạng riêng và internet, nhưng nó cũng có thể được triển khai giữa các phòng ban (mạng phân đoạn) trong một tổ chức (mạng tổng thể). Tường lửa lọc lưu lượng dựa trên một bộ quy tắc đã xác định, còn được gọi là bộ lọc hoặc danh sách kiểm soát truy cập.

    - Server: 
        Máy chủ là máy tính cung cấp thông tin cho các máy tính khác trên mạng. Một số máy chủ phổ biến là máy chủ web, máy chủ email, máy chủ in, máy chủ cơ sở dữ liệu và máy chủ tệp. Tất cả những thứ này, theo thiết kế, được nối mạng và truy cập theo một cách nào đó bởi một máy khách. Máy chủ thường được bảo mật khác với máy trạm để bảo vệ thông tin mà chúng chứa.

    - Endpoint: 
        Điểm cuối là điểm kết thúc của một liên kết truyền thông mạng. Một đầu thường ở máy chủ nơi tài nguyên cư trú và đầu kia thường là máy khách đưa ra yêu cầu sử dụng tài nguyên mạng. Điểm cuối có thể là một máy chủ khác, máy trạm để bàn, máy tính xách tay, máy tính bảng, điện thoại di động hoặc bất kỳ thiết bị người dùng cuối nào khác.

Other Networking Terms:
    - Ethernet: 
        Ethernet (IEEE 802.3) là một tiêu chuẩn xác định các kết nối có dây của các thiết bị nối mạng. Tiêu chuẩn này xác định cách dữ liệu được định dạng qua dây để đảm bảo các thiết bị khác nhau có thể giao tiếp qua cùng một loại cáp.

    - Device Address:
        - Media Access Control (MAC) Address
        - Internet Protocol (IP) Address

## Networking Models

Nhiều mô hình, kiến trúc và tiêu chuẩn khác nhau tồn tại cung cấp các cách để kết nối các hệ thống phần cứng và phần mềm khác nhau với nhau nhằm mục đích chia sẻ thông tin, điều phối các hoạt động của chúng và hoàn thành các nhiệm vụ chung hoặc chia sẻ.

Máy tính và mạng xuất hiện từ sự tích hợp của các thiết bị truyền thông, thiết bị lưu trữ, thiết bị xử lý, thiết bị bảo mật, thiết bị đầu vào, thiết bị đầu ra, hệ điều hành, phần mềm, dịch vụ, dữ liệu và con người.

Việc biến các nhu cầu bảo mật của tổ chức thành các hệ thống mạng an toàn, đáng tin cậy và hiệu quả cần bắt đầu từ một tiền đề đơn giản. Mục đích của tất cả các giao tiếp là trao đổi thông tin và ý tưởng giữa mọi người và các tổ chức để họ có thể hoàn thành công việc.

Those simple goals can be re-expressed in network (and security) terms such as:
    - Cung cấp thông tin liên lạc được quản lý, đáng tin cậy hosts (and users)
    - Isolate functions in layers: Cô lập các chức năng trong các lớp
    - Use packets as the basis of communication: Sử dụng các gói làm cơ sở giao tiếp
    - Standardize routing, addressing and control: Chuẩn hóa định tuyến, đánh địa chỉ và điều khiển
    - Allow layers beyond internetworking to add functionality: Cho phép các lớp ngoài kết nối mạng thêm chức năng
    - Be vendor-agnostic, scalable and resilient: Không phụ thuộc vào nhà cung cấp, có khả năng mở rộng và linh hoạt

Ở dạng cơ bản nhất, một mô hình mạng có ít nhất hai lớp:
    - Upper Layer: 
        Lớp trên, còn được gọi là máy chủ hoặc lớp ứng dụng, chịu trách nhiệm quản lý tính toàn vẹn của kết nối và kiểm soát phiên cũng như thiết lập, duy trì và chấm dứt các phiên liên lạc giữa hai máy tính. Nó cũng chịu trách nhiệm chuyển đổi dữ liệu nhận được từ Lớp ứng dụng sang định dạng mà bất kỳ hệ thống nào cũng có thể hiểu được. Và cuối cùng, nó cho phép các ứng dụng giao tiếp và xác định xem đối tác giao tiếp từ xa có khả dụng và có thể truy cập hay không.
    - Lower layer:
        Lớp bên dưới thường được gọi là lớp phương tiện hoặc lớp vận chuyển và chịu trách nhiệm nhận các bit từ phương tiện kết nối vật lý và chuyển đổi chúng thành một khung. Các khung được nhóm thành các kích thước tiêu chuẩn hóa. Hãy nghĩ về các khung như một cái xô và các bit như nước. Nếu các thùng có kích thước tương tự nhau và nước được chứa trong các thùng, thì dữ liệu có thể được vận chuyển một cách có kiểm soát. Dữ liệu định tuyến được thêm vào các khung dữ liệu để tạo các gói. Nói cách khác, một địa chỉ đích được thêm vào thùng. Khi chúng tôi đã sắp xếp các nhóm và sẵn sàng hoạt động, lớp máy chủ sẽ tiếp quản.

## Open Systems Interconnection (OSI) Model

Mô hình OSI được phát triển để thiết lập một cách chung để mô tả cấu trúc giao tiếp cho các hệ thống máy tính được kết nối với nhau. Mô hình OSI phục vụ như một khung trừu tượng, hoặc mô hình lý thuyết, về cách các giao thức sẽ hoạt động trong một thế giới lý tưởng, trên phần cứng lý tưởng. Do đó, mô hình OSI đã trở thành một tham chiếu khái niệm phổ biến được sử dụng để hiểu giao tiếp của các thành phần phân cấp khác nhau từ giao diện phần mềm đến phần cứng vật lý.

Mô hình OSI chia các tác vụ mạng thành bảy lớp riêng biệt. Mỗi lớp chịu trách nhiệm thực hiện các nhiệm vụ hoặc hoạt động cụ thể với mục tiêu hỗ trợ trao đổi dữ liệu (hay nói cách khác là giao tiếp mạng) giữa hai máy tính. Các lớp được tham chiếu thay thế cho nhau bằng tên hoặc số lớp. Ví dụ, Lớp 3 còn được gọi là Lớp Mạng. Các lớp được sắp xếp cụ thể để chỉ ra cách thông tin chảy qua các cấp độ giao tiếp khác nhau. Mỗi lớp giao tiếp trực tiếp với lớp bên trên và lớp bên dưới nó. Ví dụ: Lớp 3 giao tiếp với cả hai lớp Liên kết dữ liệu (2) và Vận chuyển (4).

## Transmission Control Protocol/Internet Protocol (TCP/IP)

Application Layer:          Defines the protocols for the transport layer.  
Transport Layer:            Permits data to move among devices.  
Internet Layer:             Creates/inserts packets.  
Network Interface Layer:    How data moves through the network.  

Bộ giao thức được sử dụng rộng rãi nhất là TCP/IP, nhưng nó không chỉ là một giao thức duy nhất; đúng hơn, nó là một chồng giao thức bao gồm hàng chục giao thức riêng lẻ. TCP/IP là một giao thức độc lập với nền tảng dựa trên các tiêu chuẩn mở. Tuy nhiên, đây vừa là ưu điểm vừa là nhược điểm. TCP/IP có thể được tìm thấy trong mọi hệ điều hành hiện có, nhưng nó tiêu tốn một lượng tài nguyên đáng kể và tương đối dễ bị xâm nhập vì nó được thiết kế để dễ sử dụng hơn là để bảo mật.

## Internet Protocol (IPv4 and IPv6)

## What is WiFi?

Mạng không dây là một phương pháp phổ biến để kết nối các hệ thống công ty và gia đình vì dễ triển khai và chi phí tương đối thấp. Nó đã làm cho mạng trở nên linh hoạt hơn bao giờ hết. Máy trạm và hệ thống di động không còn bị ràng buộc vào cáp mà có thể chuyển vùng tự do trong phạm vi tín hiệu của các điểm truy cập không dây đã triển khai. Tuy nhiên, với sự tự do này có thêm lỗ hổng.

Phạm vi Wi-Fi thường đủ rộng cho hầu hết các gia đình hoặc văn phòng nhỏ và các bộ mở rộng phạm vi có thể được đặt một cách chiến lược để mở rộng tín hiệu cho các khuôn viên hoặc nhà lớn hơn. Theo thời gian, chuẩn Wi-Fi đã phát triển, với mỗi phiên bản cập nhật nhanh hơn phiên bản trước.

Trong mạng LAN, các tác nhân đe dọa cần xâm nhập vào không gian vật lý hoặc vùng lân cận của chính phương tiện vật lý đó. Đối với mạng có dây, điều này có thể được thực hiện bằng cách đặt các vòi nghe lén vào cáp, cắm thiết bị USB hoặc sử dụng các công cụ khác yêu cầu quyền truy cập vật lý vào mạng. Ngược lại, sự xâm nhập của phương tiện không dây có thể xảy ra ở khoảng cách xa.

## Security of the Network 


TCP/IP’s vulnerabilities are numerous. Improperly implemented TCP/IP stacks in various operating systems are vulnerable to various DoS/DDoS attacks, fragment attacks, oversized packet attacks, spoofing attacks, and man-in-the-middle attacks. Có rất nhiều lỗ hổng của TCP/IP. Ngăn xếp TCP/IP được triển khai không đúng cách trong các hệ điều hành khác nhau dễ bị tấn công DoS/DDoS, tấn công phân mảnh, tấn công gói quá khổ, tấn công giả mạo và tấn công trung gian.

TCP/IP (cũng như hầu hết các giao thức) cũng có thể bị tấn công thụ động thông qua giám sát hoặc đánh hơi. Giám sát mạng, hoặc đánh hơi, là hành động theo dõi các mẫu lưu lượng truy cập để lấy thông tin về mạng.

## Ports and Protocols (Applications/Services)

- physical ports
- logical ports:
    - ports (0–1023): These ports are related to the common protocols that are at the core of the Transport Control Protocol/Internet Protocol (TCP/IP) model, Domain Name Service (DNS), Simple Mail Transfer Protocol (SMTP), etc.
    - Registered ports (1024–49151): These ports are often associated with proprietary applications from vendors and developers.
    - Dynamic or private ports (49152–65535): Whenever a service is requested that is associated with well-known or registered ports, those services will respond with a dynamic port that is used for that session and then released.

## Secure Ports

Một số giao thức mạng truyền thông tin ở dạng văn bản rõ ràng, nghĩa là nó không được mã hóa và không nên được sử dụng. Thông tin văn bản rõ ràng có thể bị mạng đánh hơi. Chiến thuật này sử dụng phần mềm để kiểm tra các gói dữ liệu khi chúng di chuyển trên mạng và trích xuất văn bản như tên người dùng và mật khẩu. Đánh hơi mạng cũng có thể tiết lộ nội dung của tài liệu và các tệp khác nếu chúng được gửi qua các giao thức không an toàn. Bảng bên dưới hiển thị một số giao thức không an toàn cùng với các giao thức thay thế an toàn được khuyến nghị.

<a name="2"></a>
# Module 2: Understand Network (Cyber) Threats and Attacks

## Types of Threats

- Spoofing: Một cuộc tấn công với mục tiêu giành quyền truy cập vào hệ thống mục tiêu thông qua việc sử dụng danh tính giả mạo. Giả mạo có thể được sử dụng đối với địa chỉ IP, địa chỉ MAC, tên người dùng, tên hệ thống, SSID mạng không dây, địa chỉ email và nhiều loại nhận dạng logic khác

- Phishing: Một cuộc tấn công cố gắng chuyển hướng sai người dùng hợp pháp đến các trang web độc hại thông qua việc lạm dụng URL hoặc siêu liên kết trong email có thể được coi là lừa đảo.

- Dos/DDos: Tấn công từ chối dịch vụ (DoS) là một cuộc tấn công tiêu thụ tài nguyên mạng với mục tiêu chính là ngăn chặn hoạt động hợp pháp trên hệ thống nạn nhân. Các cuộc tấn công liên quan đến nhiều hệ thống nạn nhân thứ cấp không nghi ngờ được gọi là các cuộc tấn công từ chối dịch vụ (DDoS) phân tán.

- Virus: Vi-rút máy tính có lẽ là dạng mã độc sớm nhất gây tai họa cho các quản trị viên bảo mật. Giống như virus sinh học, virus máy tính có hai chức năng chính là lan truyền và phá hủy. Vi-rút là một đoạn mã tự sao chép và lây lan mà không có sự đồng ý của người dùng, nhưng thường là với sự hỗ trợ của họ (người dùng phải nhấp vào liên kết hoặc mở tệp).

- Worm gây rủi ro đáng kể cho an ninh mạng. Chúng chứa tiềm năng phá hoại giống như các đối tượng mã độc khác với một khuynh hướng bổ sung—chúng tự lan truyền mà không cần bất kỳ sự can thiệp nào của con người.

- Trojan: Được đặt tên theo câu chuyện cổ xưa về con ngựa thành Troy, Trojan là một chương trình phần mềm có vẻ nhân từ nhưng lại chứa một nội dung độc hại, ẩn sau hậu trường có khả năng tàn phá hệ thống hoặc mạng. Ví dụ: ransomware thường sử dụng Trojan để lây nhiễm máy mục tiêu, sau đó sử dụng công nghệ mã hóa để mã hóa tài liệu, bảng tính và các tệp khác được lưu trữ trên hệ thống bằng khóa chỉ người tạo phần mềm độc hại biết.

- Trong một cuộc tấn công trên đường dẫn, kẻ tấn công tự đặt mình vào giữa hai thiết bị, thường là giữa trình duyệt web và máy chủ web, để chặn hoặc sửa đổi thông tin dành cho một hoặc cả hai điểm cuối. Các cuộc tấn công trên đường dẫn còn được gọi là các cuộc tấn công trung gian (MITM).

- A side-channel - Tấn công kênh bên là một cuộc tấn công thụ động, không xâm lấn để quan sát hoạt động của thiết bị. Các phương pháp bao gồm giám sát năng lượng, định thời gian và tấn công phân tích lỗi.

- Advanced persistent threat - Mối đe dọa liên tục nâng cao (APT) đề cập đến các mối đe dọa thể hiện mức độ phức tạp về kỹ thuật và hoạt động cao bất thường kéo dài hàng tháng hoặc thậm chí hàng năm. Các cuộc tấn công APT thường được thực hiện bởi các nhóm kẻ tấn công có tổ chức cao.

- Các mối đe dọa nội bộ là các mối đe dọa phát sinh từ các cá nhân được tổ chức tin cậy. Đây có thể là những nhân viên bất mãn hoặc nhân viên tham gia vào hoạt động gián điệp. Các mối đe dọa nội bộ không phải lúc nào cũng sẵn sàng tham gia. Một người dùng đáng tin cậy trở thành nạn nhân của một vụ lừa đảo có thể là một mối đe dọa nội gián không mong muốn.

- Một chương trình được chèn vào hệ thống, thường là bí mật, với mục đích xâm phạm tính bảo mật, tính toàn vẹn hoặc tính khả dụng của dữ liệu, ứng dụng hoặc hệ điều hành của nạn nhân hoặc gây phiền nhiễu hoặc làm gián đoạn nạn nhân.

- Phần mềm độc hại được sử dụng với mục đích tạo điều kiện cho một cuộc tấn công đòi tiền chuộc. Các cuộc tấn công ransomware thường sử dụng mật mã để “khóa” các tệp trên máy tính bị ảnh hưởng và yêu cầu thanh toán phí chuộc để đổi lấy mã “mở khóa”

## Identify Threats and Tools Used to Prevent Them
steps:
    - If a system doesn’t need a service or protocol, it should not be running
    - Firewalls

## Intrusion Detection System (IDS)

Xâm nhập xảy ra khi kẻ tấn công có thể bỏ qua hoặc cản trở các cơ chế bảo mật và giành quyền truy cập vào tài nguyên của tổ chức. Phát hiện xâm nhập là một hình thức giám sát cụ thể theo dõi thông tin được ghi lại và các sự kiện theo thời gian thực để phát hiện hoạt động bất thường cho thấy sự cố hoặc xâm nhập tiềm ẩn. Hệ thống phát hiện xâm nhập (IDS) tự động kiểm tra nhật ký và các sự kiện hệ thống theo thời gian thực để phát hiện các nỗ lực xâm nhập và lỗi hệ thống. IDS được dự định là một phần của kế hoạch bảo mật chuyên sâu về phòng thủ. Nó sẽ hoạt động và bổ sung cho các cơ chế bảo mật khác như tường lửa, nhưng nó không thay thế chúng.

IDS có thể nhận ra các cuộc tấn công đến từ các kết nối bên ngoài, chẳng hạn như cuộc tấn công từ internet và các cuộc tấn công lan truyền nội bộ, chẳng hạn như sâu độc hại. Khi họ phát hiện ra một sự kiện đáng ngờ, họ sẽ phản hồi bằng cách gửi cảnh báo hoặc tăng cảnh báo. Mục tiêu chính của IDS là cung cấp phương tiện để phản ứng kịp thời và chính xác đối với các cuộc xâm nhập.

Phát hiện và ngăn chặn xâm nhập đề cập đến các khả năng là một phần của việc cô lập và bảo vệ một miền hoặc vùng an toàn hơn hoặc đáng tin cậy hơn khỏi một miền hoặc vùng kém tin cậy hơn hoặc kém an toàn hơn. Ví dụ, đây là những chức năng tự nhiên mà tường lửa mong đợi.

IDS types are commonly classified as host-based and network-based. A host-based IDS (HIDS) monitors a single computer or host. A network-based IDS (NIDS) monitors a network by observing network traffic patterns. 

- Host-based:
    HIDS giám sát hoạt động trên một máy tính, bao gồm các cuộc gọi xử lý và thông tin được ghi lại trong nhật ký tường lửa dựa trên hệ thống, ứng dụng, bảo mật và máy chủ. Nó thường có thể kiểm tra các sự kiện chi tiết hơn so với NIDS có thể và nó có thể xác định chính xác các tệp cụ thể bị xâm phạm trong một cuộc tấn công. Nó cũng có thể theo dõi các quy trình được sử dụng bởi kẻ tấn công. Một lợi ích của HIDS so với NIDS là HIDS có thể phát hiện sự bất thường trên hệ thống máy chủ mà NIDS không thể phát hiện được. Ví dụ, một HIDS có thể phát hiện sự lây nhiễm khi kẻ xâm nhập đã xâm nhập vào hệ thống và đang điều khiển nó từ xa. HIDS quản lý tốn kém hơn NIDS vì chúng yêu cầu sự chú ý của quản trị viên trên từng hệ thống, trong khi NIDS thường hỗ trợ quản trị tập trung. HIDS không thể phát hiện các cuộc tấn công mạng trên các hệ thống khác.

- Network-based:
    NIDS giám sát và đánh giá hoạt động mạng để phát hiện các cuộc tấn công hoặc sự kiện bất thường. Nó không thể giám sát nội dung của lưu lượng được mã hóa nhưng có thể giám sát các chi tiết gói tin khác. Một NIDS duy nhất có thể giám sát một mạng lớn bằng cách sử dụng các cảm biến từ xa để thu thập dữ liệu tại các vị trí mạng chính gửi dữ liệu đến bảng điều khiển quản lý trung tâm. Các cảm biến này có thể giám sát lưu lượng truy cập tại bộ định tuyến, tường lửa, bộ chuyển mạch mạng hỗ trợ phản chiếu cổng và các loại vòi mạng khác. NIDS có rất ít ảnh hưởng tiêu cực đến hiệu suất mạng tổng thể và khi nó được triển khai trên một hệ thống có mục đích duy nhất, nó không ảnh hưởng xấu đến hiệu suất trên bất kỳ máy tính nào khác. NIDS thường có thể phát hiện sự bắt đầu của một cuộc tấn công hoặc các cuộc tấn công đang diễn ra, nhưng không phải lúc nào chúng cũng có thể cung cấp thông tin về sự thành công của một cuộc tấn công. Họ sẽ không biết liệu một cuộc tấn công có ảnh hưởng đến các hệ thống, tài khoản người dùng, tệp hoặc ứng dụng cụ thể hay không.

- Security Information and Event Management (SIEM)
    Quản lý bảo mật liên quan đến việc sử dụng các công cụ thu thập thông tin về môi trường CNTT từ nhiều nguồn khác nhau để kiểm tra tốt hơn tính bảo mật tổng thể của tổ chức và hợp lý hóa các nỗ lực bảo mật. Những công cụ này thường được gọi là giải pháp quản lý sự kiện và thông tin bảo mật (hoặc S-I-E-M, phát âm là “SIM”). Ý tưởng chung của giải pháp SIEM là thu thập dữ liệu nhật ký từ nhiều nguồn khác nhau trong toàn doanh nghiệp để hiểu rõ hơn về các vấn đề bảo mật tiềm ẩn và phân bổ tài nguyên phù hợp.

## Preventing Threats

- Keep systems and applications up to date
- Remove or disable unneeded services and protocols
- Use intrusion detection and prevention systems
- Use up-to-date anti-malware software
- Use firewalls. 

- Antivirus
- Scans
    Quét cổng và lỗ hổng thường xuyên là một cách hay để đánh giá hiệu quả của các biện pháp kiểm soát bảo mật được sử dụng trong một tổ chức. Chúng có thể tiết lộ các khu vực mà các bản vá lỗi hoặc cài đặt bảo mật không đủ, nơi các lỗ hổng bảo mật mới đã phát triển hoặc bị lộ và nơi các chính sách bảo mật không hiệu quả hoặc không được tuân thủ. Những kẻ tấn công có thể khai thác bất kỳ lỗ hổng nào trong số này.
- Firewalls
- Intrusion Prevention System (IPS)

<a name="3"></a>
## Module 3: Understand Network Security Infrastructure

### On-Premises Data Centers

- Data Center/Closets:
    Cơ sở hạ tầng đi dây của cơ sở là không thể thiếu đối với độ tin cậy và bảo mật của hệ thống thông tin tổng thể. Bảo vệ quyền truy cập vào lớp vật lý của mạng là rất quan trọng trong việc giảm thiểu thiệt hại có chủ ý hoặc không chủ ý. Việc bảo vệ đúng cách trang web vật lý phải giải quyết các loại thách thức bảo mật này. Trung tâm dữ liệu và tủ nối dây có thể bao gồm:
        - Điện thoại, mạng, kết nối đặc biệt
        - ISP hoặc thiết bị của nhà cung cấp viễn thông
        - May chủ
        - Các bộ phận đi dây và/hoặc công tắc

- Heating, Ventilation and Air Conditioning (HVAC) / Environmental
- Fire Suppression
- Power

### Redundancy

Khái niệm dự phòng là thiết kế các hệ thống với các thành phần trùng lặp để nếu xảy ra lỗi, sẽ có một bản sao lưu. Điều này cũng có thể áp dụng cho trung tâm dữ liệu. Đánh giá rủi ro liên quan đến trung tâm dữ liệu phải xác định khi nào cần có nhiều lối vào dịch vụ tiện ích riêng biệt cho các kênh và/hoặc cơ chế liên lạc dự phòng.

### Memorandum of Understanding (MOU)/Memorandum of Agreement (MOA) Biên bản ghi nhớ, biên bản thoả thuận

Một số tổ chức đang tìm cách giảm thiểu thời gian ngừng hoạt động và nâng cao khả năng BC (Kinh doanh liên tục) và DR (Khôi phục sau thảm họa) sẽ tạo ra các thỏa thuận với các tổ chức tương tự khác. Họ đồng ý rằng nếu một trong các bên gặp trường hợp khẩn cấp và không thể hoạt động trong cơ sở của mình, thì bên kia sẽ chia sẻ tài nguyên của mình và để họ hoạt động trong cơ sở của họ để duy trì các chức năng quan trọng. Các thỏa thuận này thậm chí thường bao gồm cả các đối thủ cạnh tranh, bởi vì cơ sở vật chất và nguồn lực của họ đáp ứng nhu cầu của ngành cụ thể của họ.

- joint operating agreements, JOA - MOU - MOA

### Cloud

Cloud Characteristics
- chi phí tính trên thời gian sử dụng
- không mất chi phí chủ sở hữu, giá trị ko bị hao theo thời gian
- giảm chi phí tiêu thụ điện làm mát,...
- giúp doanh nghiệp mở rộng nhanh chóng.

### Service Models

- Software as a Service (SaaS) 
- Platform as a Service (PaaS)  
- Infrastructure as a Service (IaaS).

### Deployment Models

- public, 
- private, 
- hybrid 
- community

### Managed Service Provider (MSP)

là một công ty quản lý tài sản công nghệ thông tin cho một công ty khác. Các doanh nghiệp vừa và nhỏ thường thuê ngoài một phần hoặc tất cả các chức năng công nghệ thông tin của họ cho một MSP để quản lý các hoạt động hàng ngày hoặc cung cấp kiến ​​thức chuyên môn trong các lĩnh vực mà công ty không có. Các tổ chức cũng có thể sử dụng MSP để cung cấp các dịch vụ vá lỗi và giám sát mạng và bảo mật. Ngày nay, nhiều MSP cung cấp các dịch vụ dựa trên đám mây, tăng cường các giải pháp SaaS với các hoạt động ứng phó và điều tra sự cố tích cực. Một ví dụ như vậy là dịch vụ phát hiện và phản hồi được quản lý (MDR), trong đó nhà cung cấp giám sát tường lửa và các công cụ bảo mật khác để cung cấp kiến ​​thức chuyên môn trong việc xử lý các sự kiện.

Một số triển khai MSP phổ biến khác là:
    - Augment in-house staff for projects: tăng nhân viên nội bộ cho dự án
    - Utilize expertise for implementation of a product or service: Sử dụng chuyên môn để thực hiện một sản phẩm hoặc dịch vụ
    - Provide payroll services: Cung cấp dịch vụ tính lương
    - Provide Help Desk service management: Cung cấp quản lý dịch vụ Help Desk
    - Monitor and respond to security incidents: Giám sát và ứng phó với các sự cố an ninh
    - Manage all in-house IT infrastructure: Quản lý toàn bộ cơ sở hạ tầng CNTT nội bộ

### Service-Level Agreement (SLA)

Thoả thuận giữa nhà cung cấp và khách hàng

Mục đích của SLA là ghi lại các tham số cụ thể, mức dịch vụ tối thiểu và biện pháp khắc phục cho mọi lỗi không đáp ứng các yêu cầu đã chỉ định. Nó cũng phải xác nhận quyền sở hữu dữ liệu và chỉ định chi tiết trả lại và hủy dữ liệu. Các điểm SLA quan trọng khác cần xem xét bao gồm những điểm sau:
    - Cloud system infrastructure details and security standards
    - Customer right to audit legal and regulatory compliance by the CSP         
    - Rights and costs associated with continuing and discontinuing service use
    - Service availability
    - Service performance
    - Data security and privacy
    - Disaster recovery processes
    - Data location
    - Data access
    - Data portability
    - Problem identification and resolution expectations
    - Change management processes
    - Dispute mediation processes
    - Exit strategy 

## Network Design

Network segmentation:
    Phân đoạn mạng liên quan đến việc kiểm soát lưu lượng giữa các thiết bị được nối mạng. Phân đoạn mạng vật lý hoặc hoàn chỉnh xảy ra khi một mạng bị cô lập khỏi tất cả các giao tiếp bên ngoài, vì vậy các giao dịch chỉ có thể xảy ra giữa các thiết bị trong mạng được phân đoạn.

A DMZ:
    DMZ là một vùng mạng được thiết kế để khách truy cập bên ngoài truy cập nhưng vẫn bị cô lập khỏi mạng riêng của tổ chức. DMZ thường là máy chủ của web công cộng, email, tệp và các máy chủ tài nguyên khác

VLAN:
    Vlan được tạo bởi các thiết bị chuyển mạch để phân đoạn mạng một cách hợp lý mà không làm thay đổi cấu trúc liên kết vật lý của nó.

VPN:
    Mạng riêng ảo (VPN) là một đường hầm giao tiếp cung cấp khả năng truyền điểm tới điểm của cả xác thực và lưu lượng dữ liệu qua một mạng không đáng tin cậy

Defense in depth:
    Bảo vệ chuyên sâu sử dụng nhiều loại kiểm soát truy cập theo nghĩa đen hoặc lớp lý thuyết để giúp một tổ chức tránh được lập trường bảo mật nguyên khối

Network access control (NAC):
    là một khái niệm kiểm soát quyền truy cập vào một môi trường thông qua việc tuân thủ và thực hiện nghiêm ngặt chính sách bảo mật.

## Defense in Depth

Bảo vệ theo chiều sâu sử dụng cách tiếp cận theo lớp khi thiết kế tư thế bảo mật của một tổ chức. 

Bảo vệ theo chiều sâu cung cấp nhiều điểm khởi đầu hơn để xem xét tất cả các loại kiểm soát—hành chính, công nghệ và vật lý—giúp trao quyền cho người trong cuộc và người điều hành hợp tác cùng nhau để bảo vệ tổ chức của họ và hệ thống của tổ chức.

- Data: 
- Application
- Host
- internal network
- Perimeter
- Physical
- Policies, procedures and awareness

## Zero Trust

Không tin tưởng: có nghĩa là khi thực hiện các yêu cầu truy cập đều phải được xác minh danh tính. Thông thường việc định danh chỉ thực hiện ở những khu vực không tin cậy, mặc định được phép truy cập từ khu vực tin cậy, do đó hacker có thể truy cập bất cứ tài nguyên nào sau khi thành công truy cập vào được khu vực an toàn. Do đó cần thực hiện xác minh danh tính mỗi khi thực hiện truy cập cho dù đang ở trong vùng tin tưởng.

## Network Access Control (NAC)

## Network Segmentation (Demilitarized Zone (DMZ))
Phân đoạn mạng cũng là một cách hiệu quả để đạt được sự bảo vệ theo chiều sâu cho các ứng dụng phân tán hoặc nhiều tầng. Ví dụ, việc sử dụng khu phi quân sự (DMZ) là một thông lệ phổ biến trong kiến trúc bảo mật. Với DMZ, các hệ thống máy chủ có thể truy cập thông qua tường lửa được tách biệt về mặt vật lý với mạng nội bộ bằng các công tắc bảo mật hoặc bằng cách sử dụng tường lửa bổ sung để kiểm soát lưu lượng giữa máy chủ web và mạng nội bộ. Ngày nay, DMZ ứng dụng (hoặc mạng bán tin cậy) thường được sử dụng để giới hạn quyền truy cập vào máy chủ ứng dụng đối với những mạng hoặc hệ thống có nhu cầu kết nối hợp pháp.

## Segmentation for Embedded Systems and IoT
Các hệ thống nhúng và các thiết bị hỗ trợ mạng giao tiếp với internet được coi là thiết bị IoT và cần đặc biệt chú ý để đảm bảo rằng giao tiếp không được sử dụng theo cách độc hại. Bởi vì một hệ thống nhúng thường kiểm soát một cơ chế trong thế giới vật chất, vi phạm an ninh có thể gây hại cho người và tài sản. Vì nhiều thiết bị này có nhiều tuyến truy cập, chẳng hạn như ethernet, không dây, Bluetooth, v.v., cần đặc biệt chú ý để cách ly chúng khỏi các thiết bị khác trên mạng. Bạn có thể áp đặt phân đoạn mạng logic với các công tắc sử dụng Vlan hoặc thông qua các phương tiện kiểm soát lưu lượng khác, bao gồm địa chỉ MAC, địa chỉ IP, cổng vật lý, giao thức hoặc lọc ứng dụng, định tuyến, và quản lý kiểm soát truy cập. Phân đoạn mạng có thể được sử dụng để cô lập môi trường IoT. 

## Microsegmentation

## Virtual Local Area Network (VLAN)

## Virtual Private Network (VPN)
