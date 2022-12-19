# Security Operation

## Mục lục

- [Module 1: Understand Data Security](#1)
- [Module 2: Understand System Hardening](#2)
- [Module 3: Understand Best Practice Security Policies](#3)
- [Module 4: Understand Security Awareness Training](#4)

<a name="1"></a>
## Module 1: Understand Data Security

### Data Handling
Data life cycle

- Create
- Store
- Use
- Share
- Archive
- Destroy

### Data Handling Practices

Classification:
Labeling
    Highly restricted
    Moderately restricted
    Low sensitivity
    Unrestricted public data
Retention

## Logging and Monitoring Security Event
Ghi nhật ký là hình thức thiết bị chính cố gắng thu thập các tín hiệu do các sự kiện tạo ra. Sự kiện là bất kỳ hành động nào diễn ra trong môi trường hệ thống và gây ra thay đổi có thể đo lường hoặc quan sát được trong một hoặc nhiều thành phần hoặc tài nguyên trong hệ thống. Ghi nhật ký áp đặt một chi phí tính toán nhưng là vô giá khi xác định trách nhiệm giải trình. Thiết kế phù hợp của môi trường ghi nhật ký và đánh giá nhật ký thường xuyên vẫn là những phương pháp hay nhất bất kể loại hệ thống máy tính nào

Các khung kiểm soát chính nhấn mạnh tầm quan trọng của các hoạt động ghi nhật ký của tổ chức. Thông tin có thể liên quan đến việc được ghi lại và xem xét bao gồm (nhưng không giới hạn ở):
    - user IDs
    - system activities
    - dates/times of key events (e.g., logon and logoff)
    - device and location identity
    - successful and rejected system and resource access attempts
    - system configuration changes and system protection activation and deactivation events 

## Data Security Event Example

Hệ thống security phải có plan ngay từ đầu. Chúng không thể là một thứ gì đó có thể cắm thêm vào mà phải có ngay từ đầu.

## Event Logging Best Practices

- Ingress monitoring: monitoring of incoming network traffic. Devices and tools:
    - Firewalls
    - Gateways
    - Remote authentication servers
    - IDS/IPS tools
    - SIEM solutions
    - Anti-malware solutions

- Egress monitoring: monitoring of outgoing network traffic. data loss prevention (DLP). Including:
    - Email (content and attachments)
    - Copy to portable media
    - File Transfer Protocol (FTP)
    - Posting to web pages/websites
    - Applications/application programming interfaces (APIs) 

## Encryption Overview
- Confidentiality
- Integrity: hash function and digital signatures

cryptography:
- ciphertext >< Plaintext
- Encryption
- hash functions
- digital signatures

encryption system
decryption

Symmetric Encryption
Asymmetric Encryption

Hashing
- message digest

<a name="2"></a>
# Module 2: Understand System Hardening

### Configuration Management Overview
Quản lý cấu hình là một quy trình và nguyên tắc được sử dụng để đảm bảo rằng những thay đổi duy nhất được thực hiện đối với hệ thống là những thay đổi đã được cấp phép và xác thực

- Identification: Nhận dạng cơ sở của một hệ thống và tất cả các thành phần, giao diện và tài liệu của nó

- Baseline: Đường cơ sở bảo mật là mức bảo vệ tối thiểu có thể được sử dụng làm điểm tham chiếu. Đường cơ sở cung cấp một cách để đảm bảo rằng các bản cập nhật cho công nghệ và kiến trúc phải tuân theo mức yêu cầu bảo mật tối thiểu được hiểu và chấp nhận được.

- Change Control: Một quy trình cập nhật để yêu cầu thay đổi đường cơ sở, bằng cách thực hiện các thay đổi đối với một hoặc nhiều thành phần trong đường cơ sở đó. Một quá trình xem xét và phê duyệt cho tất cả các thay đổi. Điều này bao gồm các bản cập nhật và bản vá lỗi

- Verification and Audit: Quy trình xác thực và hồi quy, có thể bao gồm thử nghiệm và phân tích, để xác minh rằng không có nội dung nào trong hệ thống bị hỏng do tập hợp các thay đổi mới được áp dụng. Một quy trình kiểm toán có thể xác thực rằng đường cơ sở hiện đang được sử dụng khớp với tổng của đường cơ sở ban đầu cộng với tất cả các thay đổi đã được phê duyệt áp dụng theo trình tự.

- Inventory:
Tạo một bản kiểm kê, danh mục hoặc sổ đăng ký tất cả các tài sản thông tin mà tổ chức biết (cho dù chúng đã tồn tại hay có danh sách mong muốn hoặc cần tạo hoặc mua chúng) là bước đầu tiên trong bất kỳ quy trình quản lý tài sản nào. Nó yêu cầu chúng tôi định vị và xác định tất cả các tài sản quan tâm, bao gồm (và đặc biệt) các tài sản thông tin:

Bạn không thể bảo vệ những gì bạn không biết bạn có.

Việc giữ khoảng không quảng cáo đó, tình trạng và tình trạng của nó đối với các bản cập nhật và bản vá, nhất quán và hiện tại, ngày này qua ngày khác, càng trở nên khó khăn hơn. Trên thực tế, khá khó khăn để xác định mọi máy chủ vật lý và điểm cuối, chứ đừng nói đến việc thu thập dữ liệu từ tất cả chúng.

- Baseline: Ví dụ, một sản phẩm phần mềm thương mại có thể có hàng nghìn mô-đun, quy trình, tham số và tệp khởi tạo riêng lẻ hoặc các thành phần khác. Nếu thiếu bất kỳ một trong số chúng, hệ thống không thể hoạt động bình thường. Đường cơ sở là tổng kiểm kê tất cả các thành phần, phần cứng, phần mềm, dữ liệu, kiểm soát quản trị, tài liệu và hướng dẫn người dùng của hệ thống.

Khi các biện pháp kiểm soát được áp dụng để giảm thiểu rủi ro, các đường cơ sở có thể được tham chiếu. Tất cả các so sánh và phát triển tiếp theo đều được đo lường dựa trên các đường cơ sở.

Khi bảo vệ tài sản, đường cơ sở có thể đặc biệt hữu ích trong việc đạt được mức bảo vệ tối thiểu của những tài sản đó dựa trên giá trị. Hãy nhớ rằng, nếu tài sản đã được phân loại dựa trên giá trị và các đường cơ sở có ý nghĩa đã được thiết lập cho từng cấp độ phân loại, thì chúng tôi có thể tuân theo các cấp độ tối thiểu được yêu cầu. Nói cách khác, nếu các phân loại như cao, trung bình và thấp đang được sử dụng, thì các đường cơ sở có thể được phát triển cho từng phân loại của chúng tôi và cung cấp mức bảo mật tối thiểu cần thiết cho từng phân loại.

- Updates: Các hoạt động sửa chữa, bảo trì và cập nhật thường xuyên được yêu cầu ở hầu hết các cấp độ của các thành phần hệ thống, từ cơ sở hạ tầng cơ bản của kiến trúc CNTT trở lên thông qua các hệ điều hành, nền tảng ứng dụng, mạng và giao diện người dùng. Những sửa đổi như vậy phải được kiểm tra chấp nhận để xác minh rằng chức năng mới được cài đặt (hoặc sửa chữa) hoạt động như yêu cầu. Chúng cũng phải được kiểm tra hồi quy để xác minh rằng các sửa đổi không đưa ra các hành vi sai hoặc không mong muốn khác trong hệ thống. Thử nghiệm đánh giá và đánh giá bảo mật đang diễn ra sẽ đánh giá xem cùng một hệ thống đã vượt qua thử nghiệm chấp nhận có còn an toàn hay không.

- patches: Bản vá lỗi là bản cập nhật, nâng cấp hoặc sửa đổi đối với một hệ thống hoặc thành phần. Những bản vá này có thể cần thiết để giải quyết lỗ hổng hoặc để cải thiện chức năng.


<a name="3"></a>
# Module 3: Understand Best Practice Security Policies

## Common Security Policies
Tất cả các chính sách phải hỗ trợ mọi nghĩa vụ pháp lý và hợp đồng của tổ chức. Đôi khi, việc đảm bảo chính sách bao gồm tất cả các yêu cầu trong khi vẫn đủ đơn giản để người dùng hiểu là một thách thức.

Data Handling Policy:
    Định nghĩa các quy định sử dụng data, Sử dụng dữ liệu phù hợp: Khía cạnh này của chính sách xác định liệu dữ liệu có được sử dụng trong công ty hay không, chỉ bị hạn chế sử dụng bởi một số vai trò nhất định hoặc có thể được công khai cho bất kỳ ai bên ngoài tổ chức. Ngoài ra, một số dữ liệu có liên quan đến các định nghĩa sử dụng hợp pháp. Chính sách của tổ chức phải nêu rõ mọi hạn chế như vậy hoặc tham khảo các định nghĩa pháp lý theo yêu cầu. Phân loại dữ liệu phù hợp cũng giúp tổ chức tuân thủ các luật và quy định thích hợp. Ví dụ: phân loại dữ liệu thẻ tín dụng là bí mật có thể giúp đảm bảo tuân thủ PCI DSS. Một trong những yêu cầu của tiêu chuẩn này là mã hóa thông tin thẻ tín dụng. Chủ sở hữu dữ liệu đã xác định chính xác khía cạnh mã hóa trong chính sách phân loại dữ liệu của tổ chức của họ sẽ yêu cầu dữ liệu được mã hóa theo các thông số kỹ thuật được xác định trong tiêu chuẩn này.

Password policy:
    Mọi tổ chức nên có chính sách mật khẩu để xác định kỳ vọng của hệ thống và người dùng. Chính sách mật khẩu phải mô tả cam kết của lãnh đạo cấp cao trong việc đảm bảo quyền truy cập an toàn vào dữ liệu, phác thảo bất kỳ tiêu chuẩn nào mà tổ chức đã chọn để xây dựng mật khẩu và xác định người được chỉ định thực thi và xác thực chính sách.

acceptable use policy (AUP):
    Chính sách sử dụng được chấp nhận (AUP) xác định việc sử dụng mạng và hệ thống máy tính của tổ chức được chấp nhận và có thể giúp bảo vệ tổ chức khỏi hành động pháp lý. Nó phải nêu chi tiết cách sử dụng phù hợp và được phê duyệt đối với tài sản của tổ chức, bao gồm môi trường CNTT, thiết bị và dữ liệu. Mỗi nhân viên (hoặc bất kỳ ai có quyền truy cập vào tài sản của tổ chức) phải ký vào một bản sao của AUP, tốt nhất là trước sự chứng kiến của một nhân viên khác của tổ chức và cả hai bên nên giữ một bản sao của AUP đã ký.
    Policy aspects commonly included in AUPs: 
        - Data access
        - System access
        - Data disclosure
        - Passwords
        - Data retention
        - Internet usage
        - Company device usage

bring your own device (BYOD):
    Tổ chức có thể cho phép người lao động mua thiết bị do họ lựa chọn và sử dụng thiết bị thuộc sở hữu cá nhân cho mục đích kinh doanh (và cá nhân). Điều này đôi khi được gọi là mang theo thiết bị của riêng bạn (BYOD). Một lựa chọn khác là trình bày cho nhân viên làm việc từ xa hoặc nhân viên danh sách các thiết bị đã được phê duyệt và yêu cầu nhân viên chọn một trong các sản phẩm trong danh sách đáng tin cậy.
    Để nhân viên chọn thiết bị mà họ cảm thấy thoải mái nhất có thể tốt cho tinh thần của nhân viên, nhưng nó đặt ra những thách thức bổ sung cho chuyên gia bảo mật vì điều đó có nghĩa là tổ chức mất quyền kiểm soát đối với tiêu chuẩn hóa và quyền riêng tư. Nếu nhân viên được phép sử dụng điện thoại và máy tính xách tay của họ cho cả mục đích sử dụng cá nhân và công việc, thì điều này có thể gây ra thách thức nếu chẳng hạn như thiết bị phải được kiểm tra để kiểm tra pháp y. Có thể khó đảm bảo rằng thiết bị được định cấu hình an toàn và không có bất kỳ cửa hậu hoặc lỗ hổng bảo mật nào khác có thể được sử dụng để truy cập dữ liệu hoặc hệ thống của tổ chức.
    Tất cả nhân viên phải đọc và đồng ý tuân thủ chính sách này trước khi được phép truy cập vào hệ thống, mạng và/hoặc dữ liệu. Nếu và khi lực lượng lao động phát triển, thì các vấn đề với BYOD cũng vậy. Chắc chắn, các công cụ thích hợp sẽ cần thiết để quản lý việc sử dụng và bảo mật xung quanh các thiết bị và cách sử dụng BYOD. Tổ chức cần thiết lập những kỳ vọng rõ ràng của người dùng và đặt ra các quy tắc kinh doanh phù hợp.

Privacy Policy
    Thông thường, nhân viên có quyền truy cập vào thông tin nhận dạng cá nhân (PII) (còn được gọi là thông tin sức khỏe được bảo vệ điện tử [ePHI] trong ngành y tế). Điều bắt buộc là tổ chức phải ghi lại rằng nhân viên hiểu và thừa nhận các chính sách và thủ tục của tổ chức để xử lý loại thông tin đó và được biết về hậu quả pháp lý của việc xử lý dữ liệu nhạy cảm đó. Loại tài liệu này tương tự như AUP nhưng dành riêng cho dữ liệu liên quan đến quyền riêng tư.

    Chính sách quyền riêng tư của tổ chức phải quy định thông tin nào được coi là PII/ePHI, quy trình và cơ chế xử lý thích hợp được tổ chức sử dụng, cách người dùng được kỳ vọng sẽ thực hiện theo chính sách và quy trình đã nêu, mọi cơ chế thực thi và biện pháp trừng phạt đối với việc không tuân thủ tuân thủ cũng như tham chiếu đến các quy định và pháp luật hiện hành mà tổ chức phải tuân theo. Điều này có thể bao gồm các luật quốc gia và quốc tế, chẳng hạn như GDPR ở EU và Đạo luật tài liệu điện tử và bảo vệ thông tin cá nhân (PIPEDA) ở Canada; luật cho các ngành cụ thể ở một số quốc gia như HIPAA và Đạo luật Gramm–Leach–Bliley (GLBA); hoặc luật pháp địa phương nơi tổ chức hoạt động.

    Tổ chức cũng nên tạo một tài liệu công khai giải thích cách thông tin cá nhân được sử dụng, cả bên trong và bên ngoài. Ví dụ: nhà cung cấp dịch vụ y tế có thể phải cung cấp cho bệnh nhân bản mô tả về cách nhà cung cấp sẽ bảo vệ thông tin của họ (hoặc tham chiếu đến nơi họ có thể tìm thấy bản mô tả này, chẳng hạn như trang web của nhà cung cấp).

Change Management Policy:
    Quản lý thay đổi là kỷ luật chuyển đổi từ trạng thái hiện tại sang trạng thái tương lai. Nó bao gồm ba hoạt động chính: quyết định thay đổi, thực hiện thay đổi và xác nhận rằng thay đổi đã được thực hiện đúng. Quản lý thay đổi tập trung vào việc đưa ra quyết định thay đổi và dẫn đến sự chấp thuận cho các nhóm hỗ trợ hệ thống, nhà phát triển và người dùng cuối để bắt đầu thực hiện các thay đổi theo chỉ đạo.

    Trong suốt vòng đời của hệ thống, những thay đổi được thực hiện đối với hệ thống, các thành phần riêng lẻ và môi trường hoạt động của nó đều có khả năng tạo ra các lỗ hổng mới và do đó làm suy yếu tính bảo mật của doanh nghiệp. Quản lý thay đổi yêu cầu một quy trình để thực hiện các thay đổi cần thiết để chúng không ảnh hưởng xấu đến hoạt động kinh doanh.

## Common Security Policies Deeper Dive

Các chính sách sẽ được thiết lập theo nhu cầu của tổ chức cũng như tầm nhìn và sứ mệnh của nó. Mỗi chính sách này nên có hình phạt hoặc hậu quả kèm theo trong trường hợp không tuân thủ. Lần đầu tiên có thể là một cảnh báo; tiếp theo có thể là buộc phải nghỉ việc hoặc đình chỉ không lương, và một vi phạm nghiêm trọng thậm chí có thể dẫn đến việc nhân viên bị chấm dứt hợp đồng. Tất cả những điều này cần được phác thảo rõ ràng trong quá trình giới thiệu, đặc biệt đối với nhân viên bảo mật thông tin. Cần làm rõ ai chịu trách nhiệm thực thi các chính sách này và nhân viên phải ký vào chúng và có tài liệu chứng minh rằng họ đã làm như vậy. Quá trình này thậm chí có thể bao gồm một số câu hỏi trong cuộc khảo sát hoặc bài kiểm tra để xác nhận rằng nhân viên thực sự hiểu chính sách. Các chính sách này là một phần của tư thế bảo mật cơ bản của bất kỳ tổ chức nào. Mọi quy trình xử lý dữ liệu hoặc bảo mật phải được hỗ trợ bởi các chính sách phù hợp.

## Change Management Components

Documentation:
    Tất cả các phương pháp quản lý thay đổi chính đều giải quyết một tập hợp chung các hoạt động cốt lõi bắt đầu bằng yêu cầu thay đổi (RFC) và chuyển qua các giai đoạn phát triển và thử nghiệm khác nhau cho đến khi thay đổi được phát hành cho người dùng cuối. Từ bước đầu tiên đến bước cuối cùng, mỗi bước phải tuân theo một số hình thức quản lý và ra quyết định chính thức; mỗi bước tạo ra các mục kế toán hoặc nhật ký để ghi lại kết quả của nó.

Approval:
    Các quy trình này thường bao gồm: Đánh giá tính đầy đủ của RFC, Chỉ định quy trình ủy quyền thay đổi phù hợp dựa trên rủi ro và thực tiễn của tổ chức, Đánh giá của các bên liên quan, xác định và phân bổ nguồn lực, Phê duyệt hoặc từ chối phù hợp và Tài liệu phê duyệt hoặc từ chối

Rollback:
    Tùy thuộc vào bản chất của sự thay đổi, có thể cần hoàn thành nhiều hoạt động khác nhau. Chúng thường bao gồm: Lập kế hoạch thay đổi, Thử nghiệm thay đổi, Xác minh quy trình khôi phục, Thực hiện thay đổi, Đánh giá thay đổi để vận hành đúng và hiệu quả và Ghi lại thay đổi trong môi trường sản xuất. Thẩm quyền khôi phục thường sẽ được xác định trong kế hoạch khôi phục, có thể ngay lập tức hoặc được lên lịch như một thay đổi tiếp theo nếu việc giám sát thay đổi cho thấy hiệu suất không phù hợp.

<a name="4"></a>
## Module 4: Understand Security Awareness Training

### Purpose
Mục đích của đào tạo nâng cao nhận thức là để đảm bảo mọi người biết những gì được mong đợi ở họ, dựa trên trách nhiệm và trách nhiệm giải trình, đồng thời tìm hiểu xem có bất kỳ sự bất cẩn hoặc tự mãn nào có thể gây rủi ro cho tổ chức hay không. Chúng ta sẽ có thể sắp xếp các mục tiêu bảo mật thông tin phù hợp với sứ mệnh và tầm nhìn của tổ chức, đồng thời hiểu rõ hơn về môi trường là gì.

## What is Security Awareness Training?

- Education:
    Mục tiêu tổng thể của giáo dục là giúp người học nâng cao hiểu biết của họ về những ý tưởng này và khả năng liên hệ chúng với kinh nghiệm của chính họ và áp dụng việc học đó theo những cách hữu ích

- Training:
    Tập trung vào việc xây dựng sự thành thạo trong một nhóm kỹ năng hoặc hành động cụ thể, bao gồm mài giũa nhận thức và phán đoán cần thiết để đưa ra quyết định về việc sử dụng kỹ năng nào, khi nào sử dụng và cách áp dụng. Đào tạo có thể tập trung vào các kỹ năng cấp thấp, toàn bộ nhiệm vụ hoặc quy trình công việc phức tạp bao gồm nhiều nhiệm vụ.

- Awareness: 
    Đây là những hoạt động thu hút và thu hút sự chú ý của người học bằng cách giúp họ làm quen với các khía cạnh của một vấn đề, mối quan tâm, vấn đề hoặc nhu cầu.

