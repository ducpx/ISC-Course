# Chapter 2: Incident Response, Business Continuity and Disaster Recovery Concepts

# Module 1: Understand Incident Response

### Incident Terminology
    Breach
    Event
    Exploit
    Incident
    Intrusion
    Threat
    Vulnerability
    Zero day

    có 1 cuộc tấn công vào hệ thống, 
    Breach: chúng ta xác định đó là một sự vi phạm, hành động trái quy định
    Event: có những sự kiện gì mà chúng ta phát hiện ra cuộc tấn công, có nhiều sự kiến cố truy cập bất thường, quá nhiều request đến từ 1 source ...

    => sau cuộc tấn công, chúng ta cần xác định các lỗ hổng của hệ thống: reflection, bao gồm có những sự cố gì dẫn đến lỗ hổng, ví dụ cấu hình sai, trong logic xử lý dẫn đến data có thể bị lead ra ngoài, xác định nguồn xâm nhập từ đâu (fosensic)

### The Goal of Incident Response
    adverse events
    crisis management, incident management: incident management được làm như thế nào, làm sao để tạo ra incident management, các bước chuẩn bị, thực hiện, đánh giá như thế nào, cần chuẩn bị gì, có những gì để làm việc này được tốt
    các event trong hệ thống thường đều vô hại, nhưng sẽ có những event xảy ra bất thường gây bất lợi cho hệ thống, được xem là những incident. Cần phải có incident response plan. Làm thế nào lập plan, dựa vào kinh nghiệm, lý thuyết, những bài toán thực tế đã có, phân tích rủi ro, dựa vào policy của tổ chứ
    Khi lập kế hoạch, chính sách hoạt động của cty, trong đó sẽ có phần chính sách tiếp tục kinh doanh khi có sự cố, trong này lại phải định nghĩa các bước để xác định những bất lợi trong kinh doanh, đánh giá rủi ro, quản lý các rủi ro, các thủ tục khi xảy ra một sự cố, đó gọi là incident response plan

*tối về đọc podcast*

### Components of the Incident Response Plan
Khi soạn thảo các chính sách xử lý sự cố cần tham chiếu đến kế hoạch xử lý sự cố, từ kế hoạch cần làm gì, đạt mục tiệu mà chúng ta sẽ định nghĩa các chính sách để yêu cầu nhân viên tuân thủ.

Lập kế hoạch xử lý sự cố dựa trên sứ mệnh, chiến lược, nhiệm vụ doanh nghiệp,
Lập thủ tục mô tả các bước thực hiện, cách sử dụng kỹ thuật, công cụ hỗ trợ, danh sách kiểm tra để xử lý sự cố. Hay gọi là bước lập các quy trình, khi có sự cố nào, tương ứng với loại sự cố thì cứ theo quy trình để làm, do đó yêu cầu người làm phải nắm rõ, chắc quy trình, thực hiện chính xác, đúng thứ tự, yêu cầu chặt chẽ

Đi vào cụ thể các thành phần của kế hoạch xử lý sự cố như sau:

- Chuẩn bị: đánh giá hệ thống, xác định các rủi ro, chuẩn bị các kịch bản ...
- Phát hiện và phân tích: xây dựng hệ thống để phát hiện (hệ thống làm bằng cách gì có thể phát hiện?), phân tích hành vi xảy ra trong sự cố
- Ngăn chặn, loại bỏ, khôi phục: bước xử lý sự cố, cần phải phân tích liên tục, phát hiện các sự cố mới, 2 bước này sẽ thực hiện qua lại với nhau cho đến khi khắc phục được sự cố, khôi phục lại hệ thống
- các hoạt động sau sự cố: rút ra bài học gì, cần củng cố, sửa đổi thủ tục quy trình xử lý sự cố không v.v => lặp lại quy trình

Các bước cụ thể trong từng bước:

Preparation
    Develop a policy approved by management.
    Identify critical data and systems, single points of failure.
    Train staff on incident response.
    Implement an incident response team. (covered in subsequent topic)
    Practice Incident Identification. (First Response)
    Identify Roles and Responsibilities.
    Plan the coordination of communication between stakeholders.
    Consider the possibility that a primary method of communication may not be available.

Detection and Analysis
    Monitor all possible attack vectors.
    Analyze incident using known data and threat intelligence.
    Prioritize incident response.
    Standardize incident documentation.

Containment
    Gather evidence.
    Choose an appropriate containment strategy.
    Identify the attacker.
    Isolate the attack.

Post-Incident Activity
    Identify evidence that may need to be retained.
    Document lessons learned.
    Retrospective
        Preparation
        Detection and Analysis
        Containment, Eradication and Recovery
        Post-incident Activity

### Incident Response Team

SOC
Determine the amount and scope of damage caused by the incident.
Determine whether any confidential information was compromised during the incident.
Implement any necessary recovery procedures to restore security and recover from incident-related damage.
Supervise the implementation of any additional security measures necessary to improve security and prevent recurrence of the incident.

# Module 2: Understand Business Continuity (BC)

### The Importance of Business Continuity

### Components of a Business Continuity Plan

- có danh sách các thành viên và cách liên hệ
- có các thủ tục và danh sách các việc thực hiện ngay tức thời
- hệ thống thông báo, call tree để cảnh báo cho nhân viên rằng BCP đang được ban hành
- hướng dẫn quản lý như thế nào, bao gồm chỉ định quyền cho các nhà quản lý
- khi nào/như thế nào ban hành plan
- có số liên lạc với các thành viên quan trọng

Cho bài toán cần lên kế hoạch để khôi phục lại công việc kinh doanh sau khi xảy ra một cuộc tấn công:
- Lập ra các thủ tục cần thiết cho từng thành phần khi có xảy ra với từng phần
- có danh sách những người sẽ tham gia thực hiện
- cấp quyền hạn cho họ, để họ có thể thực hiện trong hệ thống
- có hệ thống thông báo cho họ sẵn sàng khi có sự cố
- hướng dẫn làm như thế nào và khi nào thì thực hiện
- phải có thông tin liên hệ để khi xảy ra ới cái là có mặt ngay

### Business Continuity in Action

Business Impact Analysis (BIA)

# Module 3: Understand Disaster Recovery (DR)

Khôi phục hệ thống thông tin và truyền thông trong quá trình có sự cố xảy ra gây gián đoạn hệ thống và trong quá trình khôi phục cho đến khi hệ thống hoạt động bình thường.
Việc khôi phục hệ thống thông tin có thể độc lập với khôi phục kinh doanh, tuy nhiên hệ thống thông tin là quan trọng cho hệ thống kinh doanh

Khác nhau giữa Businees Continuity với Disaster Recovery là

- Disaster Recovery là khôi phục lại hoàn toàn hoạt động của hệ thống thông tin
- Business Continuity là khôi phục các chức năng và dịch quan trọng để phục vụ khách hàng.

### Disaster Recovery in the Real World

ví dụ cần có phương án backup, thông thường nguyên nhân xảy ra sự cố đã tồn tại trong hệ thống trước đó, sau một thời gian mới xảy. Đối với các phương án backup, có thể sẽ phải khôi phục lại từ những bản backup rất xa.
các hệ thống phức tạp cũng kết hợp nhiều phương án khác nhau cho từng bộ phận

### Components of a Disaster Recovery Plan

- có một plan tổng quan cho management
- từng phòng ban có plan cụ thể, chi tiết
- hướng dẫn cho người chịu trách nhiệm kỹ thuật thực hiện và duy trì các hệ thống backup quan trọng
- cung cấp đầy đủ plan cho các thành viên
- có danh sách đầu việc cho từng người:
    - các thành viên quan trọng sẽ có danh sách việc cụ thể để hướng dẫn họ biết làm gì trong tình huống phức tạp
    - có các hưỡng dẫn để họ thiết lập và chạy hệ thống web thay thế
    - giúp cho quản lý có nhìn tổng quan, giúp họ có thể trao đổi các vấn đề, giúp các thành viên trao đổi tốt hơn mà không cần thông tin từ các thành viên đang tham gia xử lý sự cố

