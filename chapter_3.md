# Chapter 3: Access Control Concepts

# Module 1: Understand Access Control Concepts

### What is Security Control?

Các quy tắc để kiểm soát truy cập vào các tài nguyên, liệu người này có được truy cập để xem, sửa hay không v.v

Controls Overview (3 conceptions)

- Subjects: là các đối tượng thực hiện yêu cầu truy cập vào tài nguyên, như vậy các subject có thể là end user, các chương trình, các tiến trình con v.v. Các subject đi kèm với các hành động. Cái gì làm gì với tài nguyên trong hệ thống.
    A subject:
        - Is a user, a process, a procedure, a client (or a server), a program, a device such as an endpoint, workstation, smartphone or removable storage device with onboard firmware.
        - Is active: It initiates a request for access to resources or services.
        - Requests a service from an object.
        - Should have a level of clearance (permissions) that relates to its ability to successfully access services or resources: Nên có các mức quyền liên quan đến khả năng truy cập vào dịch vụ hoặc tài nguyên

- Objects: là đối tượng mà Subject truy cập vào. là các đối tượng bị tác động và cần được bảo vệ, kiểm soát truy cập vào objects. Các object có chủ sở hữu, chủ sỡ hữu có quyền xác định ai, cái gì có quyền truy cập vào object của họ.
    An object:
        - Is a building, a computer, a file, a database, a printer or scanner, a server, a communications resource, a block of memory, an input/output port, a person, a software task, thread or process.
        - Is anything that provides service to a user.
        - Is passive
        - Responds to a request
        - May have a classification.

- Rules: các quy tắc xác định Subjects có quyền thực hiện request đối với Objects hay không. Ví dụ điển hình là các quy tắc của firewall. Bộ quy tắc gọi là *Access controll list*

### Controls Assessments

Giảm rủi ro phụ thuộc vào mức độ hiệu quả của control. Thực hiện control phải áp dụng có tình huống hiện tại và thích hợp với môi trường thay đổi. thường phải qua các bài lab mô phỏng các tình huống có thể xảy ra.

Ví dụ. Chúng ta tái sử dụng một toà nhà để lưu trữ, bảo về các tài liệu về thông tin xác thực của người dùng. Trước đó, ở đây dùng 5 cửa cho việc ra vào. Giờ đây, chúng ta phải thiết lập cơ chế kiểm soát truy cập đảm bảo an toàn cho tài liệu trước khi đưa chúng vào lưu trữ. Giải pháp lắp đặt máy quét sinh trắc học cho 2 cửa, các cửa còn lại được vệ tuyết đối, ko thể vào được hoặc xây tường bịt kín luôn. Có thể cả 5 cửa dùng máy quét sinh trắc học nhưng việc làm đó là không cần thiết và quá tốn kém. Chi phí đầu tư cho bảo vệ phải tương xứng với giá trị của đối tượng cần bảo vệ.

### Defense in Depth

Các giải pháp được nêu như là đi vào toà nhà, phòng máy chủ, truy cập vào network, app, v.v những biện pháp này là thể hiện của giải pháp Phòng chống phân tầng, hay là phòng chống nhiều lớp.

Chiến lược Defense in Depth là sự kết hợp con người, công nghệ, quy trình để thiết lập các rào cản nhiều tầng cho việc truy cập vào tài nguyên hệ thống. Triển khai chiến lược bảo vệ nhiều lớp nhằm đạt được mục tiêu an ninh nhưng không phải là đảm bảo rằng data không bị xâm phạm.

### Principle of Least Privilege

Chỉ cấp quyền tối thiểu, đủ để họ thực hiện công việc ở vị trí của họ

Tự lấy vài ví dụ

### Privileged Access Management

Privileged Accounts: những account có đặc quyền để thực hiện các việc quản lý của họ, ví dụ như các system admin, các nhà quản lý

Các đặc quyền dành cho toàn bộ hệ thống.
Một số vai trò có đặc quyền:
- system admin
- Help desk
- Security analyst.

Có thể chia các đặc quyền nhỏ hơn ở mức từng ứng dụng, cho phép họ quản lý data, members, ...

These few examples indicate that organizations often need to delegate the capability to manage and protect information assets to various managerial, supervisory, support or leadership people, with differing levels of authority and responsibility. This delegation, of course, should be contingent upon trustworthiness, since misuse or abuse of these privileges could lead to harm for the organization and its stakeholders. Một vài ví dụ này chỉ ra rằng các tổ chức thường cần ủy quyền khả năng quản lý và bảo vệ tài sản thông tin cho nhiều người quản lý, giám sát, hỗ trợ hoặc lãnh đạo khác nhau, với các cấp độ quyền hạn và trách nhiệm khác nhau. Tất nhiên, việc ủy quyền này phải phụ thuộc vào độ tin cậy, vì việc sử dụng sai hoặc lạm dụng các đặc quyền này có thể dẫn đến tổn hại cho tổ chức và các bên liên quan.

Các biện pháp điển hình được sử dụng để kiểm duyệt khả năng rủi ro gia tăng do sử dụng sai mục đích hoặc lạm dụng tài khoản đặc quyền bao gồm:
    - Cần phải ghi lại log nhiều hơn, chi tiết hơn. Vì họ có quyền đặt biệt, cần phát hiện ra các hành vi lạm quyền để ngăn chặn. Có thể được dùng để 
    - Kiểm soát nghiêm ngặt hơn user bình thường. Với user thường, chúng ta đã phải sử dụng các biện pháp xác thực Multiple Factory Authentication, đối với các user đặc quyền, chúng ta phải yêu cầu thêm các bước xác thực phức tạp hơn
    - Cần phải xác thực độ tin cậy sâu hơn
    - Kiểm toán nhiều hơn

### Segregation of Duties 

Nguyên tắc cốt lỗi của authorizaiton là chia nhỏ các nhiệm vụ, không một ai có thể kiểm soát toàn bộ các bước rủi ro. Ví dụ, một nhân viên cần gửi một hoá đơn thanh toán đến nhà cung cấp (hoặc là yêu cầu hoàn trả tiền) thì hoá đơn đó phải được phê duyệt bởi người quản lý. Ở đây đã chia việc xử lý hoá đơn đã chia ra cho 2 người là nhân viên và người quản lý. Ví dụ khác trong hệ thống thông tin, việc thay đổi cấu hình phải được cấp quản lý, bộ phận công nghệ xét duyệt trước khi thực hiện.

Việc chia nhỏ các tác vụ như thế này nhằm ngăn ngừa gian lận, hoặc phát hiện ra lỗi trước khi thực hiện. Giảm thiểu những rủi ro. Ví dụ về việc thực hiện gửi hoá đơn, cùng một nhân viên có thể có quyền gửi hoá đơn đi, nhưng lại không có quyền phê duyệt nó, trong khi đó người này có thể phê duyệt hoá đơn khác nhưng lại ko có quyền gửi đi. Và tất nhiên nhân viên đó có thể làm việc cùng với bộ phận tiếp nhận hoá đơn để bỏ qua bước chia nhỏ công việc nhằm gian lận, ở đây gọi là thông đồng.

Ví dụ khác về triển khai chia nhỏ công việc là trong Bank, khoá kho bạc là sự kết hợp của nhiều ổ khoá, mỗi nhân viên sẽ được nắm giữ một phần chìa khoá có thể mở, không một ai có toàn bộ chìa khoá. Việc mở khoá phải kết hợp tất cả nhân viên giữ chìa khoá của kho bạc.

Quy tắc hai người là một chiến lược bảo mật yêu cầu tối thiểu hai người cùng ở trong một khu vực, khiến một người không thể ở trong khu vực đó một mình. Nhiều hệ thống kiểm soát truy cập ngăn chủ thẻ cá nhân vào khu vực an ninh cao đã chọn trừ khi có ít nhất một người khác đi cùng. Việc sử dụng quy tắc hai người có thể giúp giảm thiểu các mối đe dọa nội bộ đối với các khu vực quan trọng bằng cách yêu cầu ít nhất hai cá nhân phải có mặt bất cứ lúc nào. Nó cũng được sử dụng để đảm bảo an toàn tính mạng trong khu vực an ninh; nếu một người gặp trường hợp khẩn cấp về y tế, sẽ có mặt hỗ trợ.

### Authorized Versus Unauthorized Personnel

Các chủ thể được phép truy cập vào các đối tượng sau khi chúng đã được xác thực. Hãy nhớ từ các phần trước rằng xác thực đang xác nhận danh tính của chủ thể. Khi một chủ thể đã được xác thực, hệ thống sẽ kiểm tra ủy quyền của chủ thể đó để xem liệu chủ thể đó có được phép hoàn thành hành động mà nó đang thực hiện hay không. Điều này thường được thực hiện thông qua một ma trận bảo mật được truy cập bởi hệ thống kiểm soát quyền truy cập, dựa trên các mức được phê duyệt trước. Ví dụ: khi một người xuất trình huy hiệu ID đến cửa trung tâm dữ liệu, hệ thống sẽ kiểm tra số ID, so sánh số đó với ma trận bảo mật trong hệ thống và mở khóa cửa nếu ID đó được ủy quyền. Nếu ID không được ủy quyền để mở khóa cửa, nó sẽ vẫn bị khóa. Trong một ví dụ khác, người dùng cố gắng xóa một tệp. Hệ thống tệp kiểm tra các quyền để xem liệu người dùng có được phép xóa tệp hay không. Nếu người dùng được ủy quyền, tệp sẽ bị xóa. Nếu người dùng không được cấp quyền, thông báo lỗi sẽ hiển thị và tệp không bị ảnh hưởng.

### How Users Are Provisioned

- A new employee
- Change of position
- Separation of employment

Cách người dùng được cấp phép
Các tình huống khác yêu cầu cung cấp tài khoản người dùng mới hoặc thay đổi đặc quyền bao gồm:

Nhân viên mới—Khi một nhân viên mới được tuyển dụng, người quản lý tuyển dụng sẽ gửi yêu cầu tới người quản trị bảo mật để tạo ID người dùng mới. Yêu cầu này cho phép tạo ID mới và cung cấp hướng dẫn về các cấp truy cập phù hợp. Chính sách của công ty có thể yêu cầu ủy quyền bổ sung đối với các quyền nâng cao.
Thay đổi vị trí—Khi một nhân viên đã được thăng chức, các quyền và quyền truy cập của họ có thể thay đổi như được xác định bởi vai trò mới, điều này sẽ quy định bất kỳ đặc quyền và cập nhật bổ sung nào đối với quyền truy cập. Đồng thời, mọi quyền truy cập không còn cần thiết trong công việc mới sẽ bị xóa.
Tách việc—Khi nhân viên rời công ty, tùy thuộc vào chính sách và thủ tục của công ty, tài khoản của họ phải bị vô hiệu hóa sau ngày và giờ chấm dứt. Bạn nên vô hiệu hóa các tài khoản trong một khoảng thời gian trước khi xóa chúng để duy trì tính toàn vẹn của bất kỳ tệp hoặc dấu vết kiểm tra nào mà người dùng có thể sở hữu. Vì tài khoản sẽ không còn được sử dụng nữa nên nó sẽ bị xóa khỏi mọi vai trò bảo mật hoặc hồ sơ truy cập bổ sung. Điều này bảo vệ công ty, vì vậy nhân viên bị cách ly không thể truy cập vào dữ liệu của công ty sau khi chia tay và nó cũng bảo vệ họ vì tài khoản của họ không thể bị người khác sử dụng để truy cập dữ liệu.
LƯU Ý: Khi tuyển dụng hoặc thay đổi vai trò, cách tốt nhất là không sao chép hồ sơ người dùng cho người dùng mới, vì điều này thúc đẩy “sự leo thang quyền hoặc đặc quyền”. Ví dụ: nếu một nhân viên được cấp thêm quyền truy cập để hoàn thành một nhiệm vụ và quyền truy cập đó không bị xóa khi hoàn thành nhiệm vụ, sau đó hồ sơ của người dùng đó được sao chép để tạo ID người dùng mới, thì ID mới sẽ được tạo với nhiều quyền hơn so với hiện tại. cần thiết để hoàn thành chức năng của họ. Bạn nên thiết lập vai trò tiêu chuẩn và người dùng mới được tạo dựa trên các tiêu chuẩn đó chứ không phải người dùng thực.

# Module 2: Understand Physical Access Controls

Kiểm soát truy cập vật lý là các mục bạn có thể chạm vào. Chúng bao gồm các cơ chế vật lý được triển khai để ngăn chặn, giám sát hoặc phát hiện sự tiếp xúc trực tiếp với các hệ thống hoặc khu vực trong cơ sở. Ví dụ về các biện pháp kiểm soát truy cập vật lý bao gồm nhân viên bảo vệ, hàng rào, thiết bị phát hiện chuyển động, cửa/cổng khóa, cửa sổ bịt kín, đèn chiếu sáng, bảo vệ dây cáp, khóa máy tính xách tay, phù hiệu, thẻ quẹt, chó bảo vệ, máy ảnh, bẫy/cửa xoay và báo động.

Kiểm soát truy cập vật lý là cần thiết để bảo vệ tài sản của một công ty, bao gồm cả tài sản quan trọng nhất của nó, con người. Khi xem xét các biện pháp kiểm soát truy cập vật lý, bảo mật của nhân viên luôn được đặt lên hàng đầu, tiếp theo là bảo mật các tài sản vật chất khác.

### Why Have Physical Security Controls?
Các biện pháp kiểm soát truy cập vật lý bao gồm hàng rào, rào chắn, cửa quay, ổ khóa và các tính năng khác ngăn chặn những cá nhân không được phép vào địa điểm thực tế, chẳng hạn như nơi làm việc. Điều này không chỉ để bảo vệ tài sản vật chất như máy tính khỏi bị đánh cắp mà còn để bảo vệ sức khỏe và sự an toàn của nhân viên bên trong.

### Types of Physical Access Controls

Nhiều loại cơ chế kiểm soát truy cập vật lý có thể được triển khai trong một môi trường để kiểm soát, giám sát và quản lý quyền truy cập vào một cơ sở. Những phạm vi từ ngăn chặn để cơ chế phát hiện. Mỗi khu vực yêu cầu các cơ chế kiểm soát, giám sát và ngăn chặn truy cập vật lý duy nhất và tập trung. Các phần sau đây thảo luận về nhiều cơ chế như vậy có thể được sử dụng để kiểm soát quyền truy cập vào các khu vực khác nhau của trang web, bao gồm cả vành đai và an ninh nội bộ.

#### Badge Systems and Gate Entry

Kiểm soát an ninh vật lý đối với giao thông của con người thường được thực hiện bằng các công nghệ như cửa quay, bẫy và khóa cửa được điều khiển từ xa hoặc hệ thống. Để hệ thống xác định nhân viên được ủy quyền, hệ thống kiểm soát truy cập cần phải có một số dạng trạm đăng ký được sử dụng để chỉ định và kích hoạt thiết bị kiểm soát truy cập. Thông thường, một huy hiệu được sản xuất và cấp với số nhận dạng của nhân viên, với trạm đăng ký cung cấp cho nhân viên các khu vực cụ thể có thể truy cập được. Trong môi trường bảo mật cao, việc đăng ký cũng có thể bao gồm các đặc điểm sinh trắc học. Nói chung, hệ thống kiểm soát truy cập so sánh huy hiệu của một cá nhân với cơ sở dữ liệu đã được xác minh. Nếu được xác thực, hệ thống kiểm soát truy cập sẽ gửi tín hiệu đầu ra cho phép nhân viên được ủy quyền đi qua cổng hoặc cửa đến khu vực được kiểm soát. Các hệ thống này thường được tích hợp với hệ thống ghi nhật ký của tổ chức để ghi lại hoạt động truy cập (được ủy quyền và trái phép)

Một loạt các loại thẻ cho phép hệ thống được sử dụng trong nhiều môi trường khác nhau. Những thẻ này bao gồm:
    - Bar code
    - Magnetic stripe
    - Proximity
    - Smart
    - Hybrid

#### Environmental Design

Ngăn chặn tội phạm thông qua thiết kế môi trường (CPTED) tiếp cận thách thức tạo ra không gian làm việc an toàn hơn thông qua các yếu tố thiết kế thụ động. Điều này có khả năng ứng dụng tuyệt vời cho cộng đồng bảo mật thông tin khi các chuyên gia bảo mật thiết kế, vận hành và đánh giá môi trường bảo mật của tổ chức. Các thông lệ khác, chẳng hạn như các tiêu chuẩn về xây dựng tòa nhà và trung tâm dữ liệu, cũng ảnh hưởng đến cách chúng tôi triển khai các biện pháp kiểm soát đối với môi trường vật lý của mình. Các chuyên gia bảo mật nên làm quen với các khái niệm này để họ có thể ủng hộ thành công các không gian vật lý hiệu quả và chức năng, nơi thông tin sẽ được tạo, xử lý và lưu trữ.

CPTED cung cấp hướng giải quyết các thách thức của tội phạm bằng các phương pháp tổ chức (con người), cơ học (công nghệ và phần cứng) và thiết kế tự nhiên (kiến trúc và dòng chảy lưu thông). Bằng cách điều hướng dòng người, sử dụng các kỹ thuật thụ động để báo hiệu ai nên và không nên ở trong một không gian và cung cấp khả năng hiển thị cho các không gian ẩn khác, khả năng ai đó sẽ phạm tội trong khu vực đó sẽ giảm đi.

#### Biometrics

Để xác thực danh tính của người dùng, sinh trắc học sử dụng các đặc điểm duy nhất cho cá nhân đang tìm kiếm quyền truy cập. Một giải pháp xác thực sinh trắc học bao gồm hai quy trình:
    - Enrollment - Đăng ký—trong quá trình đăng ký, mã sinh trắc học đã đăng ký của người dùng được lưu trữ trong hệ thống hoặc trên thẻ thông minh do người dùng lưu giữ
    - Verification - Xác minh—trong quá trình xác minh, người dùng trình bày dữ liệu sinh trắc học của họ cho hệ thống để dữ liệu sinh trắc học có thể được so sánh với mã sinh trắc học được lưu trữ.

Mặc dù dữ liệu sinh trắc học có thể không bí mật, nhưng đó là thông tin nhận dạng cá nhân và giao thức không được tiết lộ dữ liệu đó nếu không có sự đồng ý của người dùng. Sinh trắc học có hai dạng chính là sinh lý và hành vi.

Các hệ thống sinh lý đo lường các đặc điểm của một người như dấu vân tay, quét mống mắt (phần có màu xung quanh bên ngoài đồng tử trong mắt), quét võng mạc (mô hình mạch máu ở phía sau mắt), quét lòng bàn tay và tĩnh mạch. quét tìm dòng chảy của máu qua các tĩnh mạch trong lòng bàn tay. Một số thiết bị sinh trắc học kết hợp các quy trình với nhau—chẳng hạn như kiểm tra xung và nhiệt độ trên máy quét dấu vân tay—để phát hiện hàng giả.

Các hệ thống hành vi đo lường cách một người hành động bằng cách đo giọng nói, động lực chữ ký và động lực gõ phím. Khi một người nhập, hệ thống động lực gõ phím đo lường hành vi như tốc độ trễ (thời gian một người nhấn giữ phím) và tốc độ truyền (tốc độ một người di chuyển giữa các phím).

Các hệ thống sinh trắc học được coi là có độ chính xác cao, nhưng việc triển khai và bảo trì chúng có thể tốn kém do chi phí mua thiết bị và đăng ký tất cả người dùng. Người dùng cũng có thể không thoải mái với việc sử dụng sinh trắc học, coi chúng là xâm phạm quyền riêng tư hoặc có nguy cơ tiết lộ thông tin y tế (vì quét võng mạc có thể tiết lộ các tình trạng y tế). Một nhược điểm nữa là thách thức vệ sinh thiết bị.

### Monitoring

Việc sử dụng các biện pháp kiểm soát truy cập vật lý và giám sát nhân viên và thiết bị ra vào cũng như kiểm tra/ghi nhật ký (auditing/logging) tất cả các sự kiện vật lý là những yếu tố chính trong việc duy trì an ninh tổng thể của tổ chức.

- Cameras: Camera thường được tích hợp vào chương trình bảo mật tổng thể và được giám sát tập trung. Camera cung cấp một phương pháp giám sát và theo dõi linh hoạt. Chúng có thể ngăn chặn hoạt động tội phạm, có thể phát hiện các hoạt động nếu được kết hợp với các cảm biến khác và nếu được ghi lại, có thể cung cấp bằng chứng sau hoạt động. Chúng thường được sử dụng ở những nơi khó tiếp cận hoặc cần có hồ sơ pháp y. Trong khi camera cung cấp một công cụ để giám sát chu vi bên ngoài của các cơ sở, các công nghệ khác tăng cường khả năng phát hiện của chúng. Một loạt các công nghệ cảm biến chuyển động có thể có hiệu quả ở các vị trí bên ngoài. Chúng bao gồm tia hồng ngoại, lò vi sóng và tia laser được đào tạo trên các máy thu được điều chỉnh. Các cảm biến khác có thể được tích hợp vào cửa ra vào, cổng và cửa quay, đồng thời cáp nhạy cảm với lực căng và các cảm biến rung khác có thể phát hiện nếu ai đó cố gắng mở rộng hàng rào. Việc tích hợp đúng cách các cảm biến bên ngoài hoặc bên ngoài sẽ cảnh báo cho tổ chức về bất kỳ kẻ xâm nhập nào đang cố gắng giành quyền truy cập qua không gian mở hoặc cố gắng vi phạm hàng rào.

- Logs: 
    Trong phần này, chúng tôi đang tập trung vào việc sử dụng nhật ký vật lý, chẳng hạn như bảng đăng nhập do nhân viên bảo vệ duy trì hoặc thậm chí nhật ký được tạo bởi hệ thống điện tử quản lý truy cập vật lý. Các hệ thống điện tử ghi lại nhật ký hệ thống và bảo mật trong phần mềm sẽ được đề cập trong phần khác. 
    
    Nhật ký là bản ghi các sự kiện đã xảy ra. Nhật ký bảo mật vật lý là điều cần thiết để hỗ trợ các yêu cầu kinh doanh. Họ nên nắm bắt và lưu giữ thông tin miễn là cần thiết vì lý do pháp lý hoặc kinh doanh. Vì nhật ký có thể cần thiết để chứng minh việc tuân thủ các quy định và hỗ trợ điều tra pháp y nên nhật ký phải được bảo vệ khỏi sự thao túng. Nhật ký cũng có thể chứa dữ liệu nhạy cảm về khách hàng hoặc người dùng và cần được bảo vệ để không bị tiết lộ trái phép. 
    
    Tổ chức nên có chính sách xem xét nhật ký thường xuyên như một phần của chương trình bảo mật của tổ chức. Là một phần của quy trình nhật ký của tổ chức, các nguyên tắc lưu giữ nhật ký phải được thiết lập và tuân theo. Nếu chính sách của tổ chức chỉ lưu giữ các tệp nhật ký tiêu chuẩn trong sáu tháng, thì đó là tất cả những gì tổ chức nên có

    Nhật ký bất thường là bất cứ điều gì khác thường. Việc xác định các điểm bất thường trong nhật ký thường là bước đầu tiên trong việc xác định các vấn đề liên quan đến bảo mật, cả trong quá trình kiểm tra và giám sát định kỳ. Một số điểm bất thường sẽ rất rõ ràng: ví dụ: khoảng trống về dấu ngày/giờ hoặc khóa tài khoản. Những người khác sẽ khó bị phát hiện hơn, chẳng hạn như ai đó đang cố ghi dữ liệu vào một thư mục được bảo vệ. Mặc dù có vẻ như việc ghi nhật ký mọi thứ để bạn không bỏ lỡ bất kỳ dữ liệu quan trọng nào là cách tiếp cận tốt nhất, nhưng hầu hết các tổ chức sẽ sớm chìm trong lượng dữ liệu thu thập được.

    Các yêu cầu pháp lý và kinh doanh đối với việc lưu giữ nhật ký sẽ khác nhau giữa các nền kinh tế, quốc gia và ngành. Một số doanh nghiệp sẽ không có yêu cầu lưu giữ dữ liệu. Những người khác được ủy thác bởi bản chất kinh doanh của họ hoặc bởi các đối tác kinh doanh để tuân thủ dữ liệu lưu giữ nhất định. Ví dụ: Tiêu chuẩn bảo mật dữ liệu ngành thẻ thanh toán (PCI DSS) yêu cầu các doanh nghiệp lưu giữ dữ liệu nhật ký trong một năm để hỗ trợ PCI. Một số quy định của liên bang cũng bao gồm các yêu cầu về lưu giữ dữ liệu.

    Nếu một doanh nghiệp không có yêu cầu kinh doanh hoặc pháp lý để giữ lại dữ liệu nhật ký, thì tổ chức nên giữ nó trong bao lâu? Những người đầu tiên hỏi nên là bộ phận pháp lý. Hầu hết các bộ phận pháp lý đều có hướng dẫn rất cụ thể về việc lưu giữ dữ liệu và những hướng dẫn đó có thể thúc đẩy chính sách lưu giữ nhật ký.

- Security Guards:
    Nhân viên bảo vệ là một kiểm soát an ninh vật lý hiệu quả. Bất kể hình thức kiểm soát truy cập vật lý nào được sử dụng, nhân viên bảo vệ hoặc hệ thống giám sát khác sẽ không khuyến khích một người giả dạng người khác hoặc theo sát gót người khác để có quyền truy cập. Điều này giúp ngăn chặn hành vi trộm cắp và lạm dụng thiết bị hoặc thông tin.

- Alarm Systems:
    Hệ thống báo động thường được tìm thấy trên cửa ra vào và cửa sổ trong nhà và tòa nhà văn phòng. Ở dạng đơn giản nhất, chúng được thiết kế để cảnh báo cho nhân viên thích hợp khi cửa ra vào hoặc cửa sổ bị mở bất ngờ. 
    
    Ví dụ: một nhân viên có thể nhập mã và/hoặc vuốt huy hiệu để mở cửa và hành động đó sẽ không kích hoạt báo động. Ngoài ra, nếu chính cánh cửa đó bị mở bằng vũ lực mà không có người nhập đúng mã hoặc sử dụng huy hiệu được ủy quyền, báo động sẽ được kích hoạt. 
    
    Một hệ thống báo động khác là báo cháy, có thể được kích hoạt bằng nhiệt hoặc khói ở bộ cảm biến và có khả năng sẽ phát ra âm thanh cảnh báo để bảo vệ tính mạng con người ở khu vực lân cận. Nó có thể cũng sẽ liên lạc với nhân viên phản ứng địa phương cũng như sở cứu hỏa gần nhất. 
    
    Cuối cùng, một loại hệ thống báo động phổ biến khác có dạng nút hoảng loạn. Sau khi được kích hoạt, nút báo động sẽ báo cho cảnh sát hoặc nhân viên an ninh thích hợp.

# Module 3: Understand Logical Access Controls

What are Logical Access Controls?
Trong khi kiểm soát truy cập vật lý là các phương pháp hoặc cơ chế hữu hình hạn chế ai đó truy cập vào một khu vực hoặc tài sản, thì kiểm soát truy cập logic là các phương pháp điện tử hạn chế ai đó truy cập vào hệ thống và đôi khi thậm chí vào các khu vực hoặc tài sản hữu hình. Các loại điều khiển truy cập logic bao gồm:
    - Passwords
    - Biometrics (implemented on a system, such as a smartphone or laptop)
    - Badge/token readers connected to a system

Những loại công cụ điện tử này giới hạn những người có thể có quyền truy cập hợp lý vào một nội dung, ngay cả khi người đó đã có quyền truy cập thực tế.

### Discretionary Access Control (DAC)

Kiểm soát truy cập tùy ý (DAC) là một loại chính sách kiểm soát truy cập cụ thể được thi hành đối với tất cả các chủ thể và đối tượng trong một hệ thống thông tin. Trong DAC, chính sách chỉ định rằng một chủ thể đã được cấp quyền truy cập thông tin có thể thực hiện một hoặc nhiều thao tác sau:

- Pass the information to other subjects or objects - Truyền thông tin cho các đối tượng hoặc đối tượng khác
- Grant its privileges to other subjects - Cấp đặc quyền của nó cho các đối tượng khác
- Change security attributes on subjects, objects, information systems or system components - Thay đổi thuộc tính bảo mật đối với chủ thể, đối tượng, hệ thống thông tin hoặc thành phần hệ thống
- Choose the security attributes to be associated with newly created or revised objects; and/or - Chọn các thuộc tính bảo mật được liên kết với các đối tượng mới được tạo hoặc sửa đổi; và/hoặc
- Change the rules governing access control; mandatory access controls restrict this capability - Thay đổi các quy tắc quản lý kiểm soát truy cập; kiểm soát truy cập bắt buộc hạn chế khả năng này

Hầu hết các hệ thống thông tin trên thế giới đều là hệ thống DAC. Trong hệ thống DAC, người dùng có quyền truy cập vào tệp thường có thể chia sẻ tệp đó hoặc chuyển tệp đó cho người khác. Điều này cấp cho người dùng mức truy cập gần như giống với chủ sở hữu ban đầu của tệp. Các hệ thống kiểm soát truy cập dựa trên quy tắc (Rule-based) thường là một dạng DAC.

#### DAC Example
Các hệ thống kiểm soát truy cập tùy ý cho phép người dùng thiết lập hoặc thay đổi các quyền này đối với các tệp mà họ tạo hoặc có quyền sở hữu.
Ví dụ, Steve và Aidan là hai người dùng (đối tượng) trong môi trường UNIX hoạt động với DAC tại chỗ. Thông thường, các hệ thống sẽ tạo và duy trì một bảng ánh xạ chủ thể tới đối tượng, như minh họa trong hình. Tại mỗi giao điểm là tập hợp các quyền mà một chủ thể nhất định có đối với một đối tượng cụ thể. Nhiều hệ điều hành, chẳng hạn như Windows và toàn bộ cây gia đình Unix (bao gồm cả Linux) và iOS, sử dụng loại cấu trúc dữ liệu này để đưa ra quyết định nhanh chóng, chính xác về việc cho phép hoặc từ chối yêu cầu truy cập. Lưu ý rằng dữ liệu này có thể được xem dưới dạng hàng hoặc cột

Phương pháp này dựa trên quyết định của chủ sở hữu đối tượng kiểm soát truy cập để xác định các quyền cụ thể của chủ thể kiểm soát truy cập. Do đó, bảo mật của đối tượng theo nghĩa đen tùy thuộc vào quyết định của chủ sở hữu đối tượng. DAC không có khả năng mở rộng cho lắm; chúng dựa trên các quyết định kiểm soát truy cập do từng chủ sở hữu đối tượng đưa ra và có thể khó tìm ra nguồn gốc của các vấn đề kiểm soát truy cập khi xảy ra sự cố.

#### DAC in the Workplace

Hầu hết các hệ thống thông tin là hệ thống DAC. Trong hệ thống DAC, người dùng có quyền truy cập vào tệp có thể chia sẻ tệp đó hoặc chuyển tệp đó cho người khác. Chủ sở hữu nội dung có toàn quyền quyết định cấp hoặc thu hồi quyền truy cập cho người dùng hay không. Để truy cập vào các tệp máy tính, đây có thể là tệp được chia sẻ hoặc bảo vệ bằng mật khẩu. Ví dụ: nếu bạn tạo một tệp trong nền tảng chia sẻ tệp trực tuyến, bạn có thể hạn chế những người nhìn thấy tệp đó. Đó là tùy thuộc vào quyết định của bạn. Hoặc nó có thể là thứ gì đó công nghệ thấp và tạm thời, chẳng hạn như huy hiệu của khách được cung cấp theo quyết định của nhân viên tại bàn an ninh.

### Mandatory Access Control (MAC)

Chính sách kiểm soát truy cập bắt buộc (MAC) là chính sách được thực thi thống nhất trên tất cả các chủ thể và đối tượng trong ranh giới của một hệ thống thông tin. Nói một cách đơn giản nhất, điều này có nghĩa là chỉ những quản trị viên bảo mật được chỉ định đúng, với tư cách là chủ thể đáng tin cậy, mới có thể sửa đổi bất kỳ quy tắc bảo mật nào được thiết lập cho chủ thể và đối tượng trong hệ thống. Điều này cũng có nghĩa là đối với tất cả các chủ thể do tổ chức xác định (nghĩa là, được biết đến với hệ thống kiểm soát truy cập và quản lý danh tính tích hợp), tổ chức chỉ định một tập hợp con của tổng số đặc quyền cho một tập hợp con các đối tượng, sao cho chủ thể bị hạn chế thực hiện bất kỳ những điều sau đây:
    - Passing the information to unauthorized subjects or objects 
    - Granting its privileges to other subjects 
    - Changing one or more security attributes on subjects, objects, the information system or system components 
    - Choosing the security attributes to be associated with newly created or modified objects 
    - Changing the rules governing access control 

Mặc dù MAC nghe rất giống với DAC nhưng sự khác biệt chính là ai có thể kiểm soát quyền truy cập. Với Kiểm soát truy cập bắt buộc, quản trị viên bảo mật bắt buộc phải gán quyền hoặc quyền truy cập; với Kiểm soát truy cập tùy ý, tùy thuộc vào chủ sở hữu đối tượng.

MAC in the Workplace
Quyền kiểm soát quyền truy cập bắt buộc cũng do chủ sở hữu tài sản xác định, nhưng trên cơ sở toàn diện hơn, ít có sự ra quyết định của cá nhân về việc ai có quyền truy cập.

Ví dụ: tại một số cơ quan chính phủ, nhân viên phải có một số loại giấy phép an ninh nhất định để được tiếp cận các khu vực nhất định. Nói chung, mức truy cập này được thiết lập theo chính sách của chính phủ chứ không phải do một cá nhân cấp phép dựa trên đánh giá của riêng họ.

Thường thì điều này đi kèm với sự phân chia nhiệm vụ, trong đó phạm vi công việc của bạn bị hạn chế và bạn không có quyền truy cập để xem thông tin không liên quan đến mình; người khác xử lý thông tin đó. Việc phân chia nhiệm vụ này cũng được hỗ trợ bởi kiểm soát truy cập dựa trên vai trò, như chúng ta sẽ thảo luận tiếp theo.

### Role-Based Access Control (RBAC)

Kiểm soát truy cập dựa trên vai trò (RBAC), như tên gợi ý, thiết lập quyền của người dùng dựa trên vai trò. Mỗi vai trò đại diện cho người dùng có quyền tương tự hoặc giống hệt nhau.
RBAC in the Workplace
Kiểm soát truy cập dựa trên vai trò cung cấp cho mỗi nhân viên các đặc quyền dựa trên vai trò của họ trong tổ chức. Ví dụ, chỉ nhân viên Nhân sự mới có quyền truy cập vào hồ sơ nhân sự; chỉ Tài chính mới có quyền truy cập vào tài khoản ngân hàng; mỗi người quản lý có quyền truy cập vào các báo cáo trực tiếp của riêng họ và bộ phận riêng của họ. Quản trị viên hệ thống cấp rất cao có thể có quyền truy cập vào mọi thứ; nhân viên mới sẽ có quyền truy cập rất hạn chế, mức tối thiểu cần thiết để thực hiện công việc của họ.

Giám sát các quyền dựa trên vai trò này là rất quan trọng, bởi vì nếu bạn mở rộng quyền của một người vì một lý do cụ thể—chẳng hạn như quyền của một nhân viên cấp dưới có thể được mở rộng để họ có thể tạm thời đóng vai trò là người quản lý bộ phận—nhưng bạn quên thay đổi lại quyền của họ khi người quản lý mới được thuê, thì người tiếp theo đến ở cấp cơ sở đó có thể kế thừa những quyền đó khi họ không thích hợp để có chúng. Điều này được gọi là creep đặc quyền hoặc creep quyền. Chúng ta đã thảo luận điều này trước đây khi nói về việc cấp phép cho người dùng mới.

Có nhiều vai trò với các tổ hợp quyền khác nhau có thể yêu cầu giám sát chặt chẽ để đảm bảo mọi người đều có quyền truy cập mà họ cần để thực hiện công việc của mình và không có gì khác. Trong thế giới nơi công việc luôn thay đổi, điều này đôi khi có thể là một thách thức để theo dõi, đặc biệt là với các quyền và vai trò cực kỳ chi tiết. Khi tuyển dụng hoặc thay đổi vai trò, cách tốt nhất là không sao chép hồ sơ người dùng cho người dùng mới. Bạn nên thiết lập vai trò tiêu chuẩn và người dùng mới được tạo dựa trên các tiêu chuẩn đó chứ không phải người dùng thực. Bằng cách đó, nhân viên mới bắt đầu với các vai trò và quyền thích hợp.