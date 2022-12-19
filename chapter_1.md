# Chapter 1: Security principle

Nguyên tắc cơ bản của security

## Mục lục
- [Module 1: Understand the Security Concepts of Information Assurance](#1)
- [Module 2: Understand the Risk Management Process](#2)
- [Module 3: Security Controls](#3)
- [Module 4: Understand Governance Elements and Processes](#4)

----

<a name="1"></a>
## module 1: Understand the Security Concepts of Information Assurance
    
- Concept CIA:
    - Confidentiality: Confidentiality relates to permitting authorized access to information, while at the same time protecting information from improper disclosure.
    - Integrity: Integrity is the property of information whereby it is recorded, used and maintained in a way that ensures its completeness, accuracy, internal consistency and usefulness for a stated purpose.
    - Availability: Availability means that systems and data are accessible at the time users need them.

- Deep concepts:
    - Confidentiality: The National Institute of Standards and Technology, known as NIST, in its Special Publication 800-66 defines confidentiality as the characteristic of data or information when it is not made available or disclosed to unauthorized persons or processes.
        
    Confidentiality is a difficult balance to achieve when many system users are guests or customers, and it is not known if they are accessing the system from a compromised machine or vulnerable mobile application. So, the security professional’s obligation is to regulate access—protect the data that needs protection, yet permit access to authorized individuals.

    Confidentiality là tính bảo mật thông tin, nó là khó có thể đạt được tính chất này vì khi hệ thống có nhiều user, chúng ta khó có thể kiểm soát được. Ví dụ, một user họ có quyền truy các thông tin của họ, nhưng vì họ dùng các ứng dụng có lỗ hổng, hacker có thể truy cập thông tin của họ, như vậy đứng từ phía nhà cung cấp dịch vụ không đảm bảo được tính bảo mật thông tin

    - Personally Identifiable Information (PII): (1) any information that can be used to distinguish or trace an individual’s identity, such as name, Social Security number, date and place of birth, mother’s maiden name, or biometric records; and (2) any other information that is linked or linkable to an individual, such as medical, educational, financial and employment information.  NIST SP800-122.
        
    protected health information (PHI): Information regarding health status, the provision of healthcare or payment for healthcare as defined in HIPAA (Health Insurance Portability and Accountability Act)
        
    Other terms related to confidentiality are protected health information (PHI) , which is information regarding one’s health status, and classified or sensitive information, which includes trade secrets, research, business plans and intellectual property.

    - sensitivity: 

    - Data Integrity: tính toàn vẹn dữ liệu là đảm bảo dữ liệu không bị thay đổi trong quá trình lưu trữ, truyền, dữ liệu phải được nhất quán, nghĩa là phải đảm bảo các bản sao giống hệt nhau.
        
    System integrity: 
    Integrity vs criticality

- Authentication:
    method: 
    - Something you know, 
    - Something you have, 
    - Something you are

- Methods of Authentication:
    - single-factor authentication (SFA): sử dụng 1 trong 3 method
    - multi-factor authentication (MFA): ít nhất 2 loại trong 3 method trên
    - best practive: least 2 in 3
    
- Non-repudiation: chống thoái thác có nghĩa là phòng chống một người thực hiện 1 hành vi sau đó phủ nhận
    Privacy

<a name="2"></a>
## Module 2: Understand the Risk Management Process

Mức độ an ninh mạng cần thiết phụ thuộc vào mức độ rủi ro mà thực thể sẵn sàng chấp nhận; đó là những hậu quả tiềm ẩn của những gì đang diễn ra trong môi trường của chúng ta. Sau khi đánh giá rủi ro này, chúng tôi sẽ triển khai các biện pháp kiểm soát bảo mật để giảm thiểu rủi ro xuống mức mà chúng tôi thấy có thể chấp nhận được.
Rủi ro có thể đến từ các cuộc tấn công mạng, chẳng hạn như phần mềm độc hại, kỹ thuật xã hội hoặc tấn công từ chối dịch vụ hoặc từ các tình huống khác ảnh hưởng đến môi trường của chúng ta, chẳng hạn như hỏa hoạn, tội phạm bạo lực hoặc thiên tai. Với các công nghệ quản lý rủi ro được thiết kế tốt, chúng ta có thể nhận ra
các lỗ hổng và mối đe dọa, đồng thời tính toán khả năng xảy ra và tác động tiềm tàng của từng mối đe dọa

- Risk Management Terminology: 

    - Anything of value that is owned by an organization. Assets include both tangible items such as information systems and physical property and intangible assets such as intellectual property. An asset is something in need of protection
    - Weakness in an information system, system security procedures, internal controls or implementation that could be exploited by a threat source. NIST SP 800-30 Rev 1. A vulnerability is a gap or weakness in those protection efforts.
    - Any circumstance or event with the potential to adversely impact organizational operations (including mission, functions, image or reputation), organizational assets, individuals, other organizations or the nation through an information system via unauthorized access, destruction, disclosure, modification of information and/or denial of service. NIST SP 800-30 Rev 1. A threat is something or someone that aims to exploit a vulnerability to thwart protection efforts.
Risk is the intersection of these terms. Let's look at them more closely.

- threat actors:
    Insiders
    Outside
    Formal entities that are nonpolitical (such as business competitors and cybercriminals).Các thực thể chính thức phi chính trị (chẳng hạn như đối thủ kinh doanh và tội phạm mạng).
    Formal entities that are political (such as terrorists, nation-states, and hacktivists). Các thực thể chính thức mang tính chính trị (chẳng hạn như những kẻ khủng bố, các quốc gia dân tộc và những người theo chủ nghĩa hack).

    Intelligence or information gatherers (could be any of the above).Người thu thập thông tin hoặc tình báo (có thể là bất kỳ người nào ở trên).
    Công nghệ (chẳng hạn như bot chạy tự do và trí tuệ nhân tạo , có thể là một phần của bất kỳ điều nào ở trên).

- Vulnerabilities:
    xác định xác xuất xảy ra => xem hậu quả nếu xảy ra

- Risk Identification: nhận biết các mỗi đe doạ
    Là một chuyên gia bảo mật, bạn có khả năng hỗ trợ đánh giá rủi ro ở cấp độ hệ thống, tập trung vào quy trình, kiểm soát, giám sát hoặc các hoạt động ứng phó và phục hồi sự cố

Risk Assessment: thẩm định rủi ro, có bản báo cáo đánh giá rủi roi, đưa cho ban quản lý phê duyệt

Risk Treatment: xử lý rủi ro
    - Risk avoidance: Né tránh rủi ro là quyết định cố gắng loại bỏ hoàn toàn rủi ro, khi rủi ro được đánh giá là quá lớn
    - Risk acceptance: Chấp nhận rủi ro là không thực hiện hành động nào để giảm khả năng xảy ra rủi ro. Ban quản lý có thể lựa chọn thực hiện chức năng kinh doanh có liên quan đến rủi ro mà không cần thực hiện thêm bất kỳ hành động nào từ phía tổ chức, vì tác động hoặc khả năng xảy ra là không đáng kể hoặc vì lợi ích là quá đủ để bù đắp rủi ro đó
    - Risk transference: Chuyển giao rủi ro là thực tiễn chuyển rủi ro cho một bên khác, bên này sẽ chấp nhận tác động tài chính của thiệt hại do rủi ro được thực hiện để đổi lấy khoản thanh toán. Thông thường, đây là một hợp đồng bảo hiểm.
    - Risk mitigation: Giảm thiểu rủi ro là loại hình quản lý rủi ro phổ biến nhất và bao gồm thực hiện các hành động để ngăn chặn hoặc giảm thiểu khả năng xảy ra sự kiện rủi ro hoặc tác động của nó. Giảm thiểu có thể liên quan đến các biện pháp khắc phục hoặc kiểm soát, chẳng hạn như kiểm soát an ninh, thiết lập chính sách, thủ tục và tiêu chuẩn để giảm thiểu rủi ro bất lợi. Rủi ro không phải lúc nào cũng được giảm thiểu, nhưng các biện pháp giảm thiểu như các biện pháp an toàn phải luôn được thực hiện.

Risk Priorities: qualitative risk analysis and/or quantitative risk analysis

<a name="3"></a>
## Module 3: Security Controls
Physical Controls
Technical Controls
Administrative Controls

<a name="4"></a>
## Module 4: Understand Governance Elements and Processes
Regulations and Laws
Standards:
    International Organization for Standardization (ISO)
    National Institute of Standards and Technology (NIST)
    Internet Engineering Task Force (IETF)
    Institute of Electrical and Electronics Engineers (IEEE)
Policies
Procedures