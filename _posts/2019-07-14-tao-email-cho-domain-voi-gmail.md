---
layout: default
date: 2019-07-14
title: Tạo email tên miền riêng miễn phí với Gmail
---

Gmail là dịch vụ mail miễn phí cực phổ biến mà đa số mọi người dùng, với dung lượng miễn phí cực lớn dao động từ **15GB** đến **17GB** <sub><sup>thời invite giới thiệu được tặng thêm 2GB</sup></sub>.

Cùng vô số các tính năng hỗn hợp khác nhau phục vụ lưu trữ, lịch cá nhân, văn bản, dữ liệu... vân vân..

## Vì sao tôi chọn Gmail chứ không phải dịch vụ miễn phí nào khác?

Thường mặc định bạn sẽ buộc phải nghĩ đến dịch vụ email cho tên miền miễn phí với một số nhà cung cấp lớn cho phép dùng miễn phí như Zoho Mail, Migadu, hay Yandex.Mail for domain nhưng đều có giới hạn nhất định của nó và đôi khi là phiền phức vì sự cố mà sẽ được liệt kê các thông số ở cuối bài, chú ý tham khảo để đưa ra quyết định cuối cùng.

## Hướng dẫn Tạo email tên miền riêng miễn phí với Gmail

Bản thân <mark>tiep.me</mark> sử dụng dịch vụ Gmail của Google để tăng sức mạnh cho giao tiếp email tên miền tùy chỉnh của mình. Gmail cung cấp một tính năng độc đáo thông qua đó tôi có thể thêm nhiều địa chỉ tên miền tùy chỉnh ngay trong tài khoản Gmail của mình. 

Trong khi soạn email, tôi có thể dễ dàng chọn các địa chỉ email tùy chỉnh cần thiết từ menu thả xuống. Rất đơn giản và được tích hợp cùng với email cũ của mình dùng chính trước khi có tên miền, vì vậy không phải chuyển qua chuyển lại hay phải báo cáo với mọi người về sự thay đổi.

Một quá trình đơn giản có thể được hoàn thành trong vòng chưa đầy 5 phút. Đây là cách để làm. 

**Bước 1:** Chuyển đến dịch vụ chuyển tiếp email [**ImprovMX**](https://improvmx.com).

**Bước 2:** Sao chép các bản ghi MX sau và thêm chúng vào bản ghi máy chủ DNS của tên miền của bạn.

<sub><sub>xem mẫu của tiep.me</sub></sub>

![Mẫu mx record của tiep.me](https://data.tiep.me/assets/img/images/og-images/gmail/dns_mx.png)

**Host** | **Value** | **Priority**
--- | --- | ---
@ | mx1.improvmx.com | 10
@ | mx2.improvmx.com | 20

**Bước 3:** Thêm tên miền và địa chỉ Gmail nơi bạn muốn sử dụng địa chỉ. Sau đó, nhấp vào nút xác minh. Một thiết lập mẫu được hiển thị dưới đây.

![Form nhập tên miền và email bạn dùng gmail](https://data.tiep.me/assets/img/images/og-images/gmail/add_domain.png)

**Bước 4:** bạn phải tạo **Google 2-Step Verification** hay còn được biết đến với tiếng việt là [**Xác minh 2 bước**](https://myaccount.google.com/security). Bạn phải cung cấp số điện thoại đang dùng smartphone để tiến hành tạo xác minh 2 bước cho **Gmail** của mình. Sau khi hoàn thành hãy quay trở lại trang [**tài khoản Google - phân mục Bảo mật này**](https://myaccount.google.com/security) để chọn vào mục [**Mật khẩu ứng dụng hay tiếng anh là App Passwords**](https://myaccount.google.com/apppasswords?utm_source=google-account&utm_medium=web) nhớ tích chọn **Thư** và ô kế bên là **Mac** nhé. Sau khi nó hiện ra cái mật khẩu loằng ngoằng chia đoạn ấy thì copy hết chỗ pass mới tạo đó để chuyển sang bước tiếp theo.

![Xác minh 2 bước phải được bật](https://data.tiep.me/assets/img/images/og-images/gmail/xacminh2buoc.png)

*xác minh 2 bước phải được bật*

![Tạo mật khẩu ứng dụng](https://data.tiep.me/assets/img/images/og-images/gmail/apppassword.png)

*Tạo mật khẩu ứng dụng*



**Bước 5:** Bây giờ, hãy mở hộp thư đến Gmail của bạn và đi đến tùy chọn ' **Cài đặt** → **Tài khoản và Nhập** → **Gửi thư bằng địa chỉ:** → **Thêm địa chỉ email khác** '. Tại đây bạn có thể cấu hình bao nhiêu địa chỉ email tên miền tùy chỉnh mà bạn muốn. Một thiết lập làm việc mẫu được hiển thị dưới đây.
<sub><sub>Lưu ý quan trọng là bạn phải bỏ tích ở **Xử lý như bí danh**</sub></sub>

![thêm mail tên miền vào gmail](https://data.tiep.me/assets/img/images/og-images/gmail/gmail1.png)

*thêm mail tên miền vào gmail*

![Gõ mật khẩu ứng dụng vào cấu hình smtp](https://data.tiep.me/assets/img/images/og-images/gmail/gmail2.png)

*Nhập các thông số ta có được từ **bước 4***

**Yêu cầu** | **nhập** | **ghi chú**
--- | --- | ---
Máy chủ SMTP | smtp.gmail.com | cổng **587**
Tên người dùng | gmail của bạn@gmail.com | dùng @gmail của bạn làm user
Mật khẩu | dán mật khẩu ứng dụng bạn lấy được từ **bước 4** | đây là dòng mật khẩu ứng dụng bạn tạo ở bước 4, không phải mật khẩu gmail của bạn vẫn hay đăng nhập đâu :v
Kết nối an toán sử dụng TLS | **được khuyến nghị** | mặc định
tiếp theo | **Thêm tài khoản** | và làm theo hướng dẫn của Gmail sau đó nhé.

[**ImprovMX**](https://improvmx.com). dịch vụ bắt tất cả các địa chỉ email được gửi đến tên miền của bạn và chuyển chúng vào tài khoản Gmail của bạn. đảm bảo bạn có thể dễ dàng gửi email đến đối tượng mục tiêu của mình bằng các địa chỉ miền tùy chỉnh được định cấu hình của mình.

Sau khi vào mục **Soạn thư** bạn sẽ thấy địa chỉ cá nhân cho tên miền của bạn được hiển thị, kể từ lúc đó bạn sẽ **nhận** và **gửi** thư từ địa chỉ email tên miền của mình trực tiếp bằng **Gmail** mà không cần đến các dịch vụ cung cấp mail cho tên miền rườm rà phiền phức và hay có sự cố khác đi.

Đời sẽ đơn giản hơn.s



## Một số dịch vụ Mail for domain miễn phí khác

> [Zoho Mail](https://www.zoho.com/mail/) for domain. Đây là một trong những dịch vụ email phổ biến và được sử dụng rộng rãi nhất mà bạn có thể dễ dàng sử dụng với tên miền tùy chỉnh của trang web. Gói miễn phí đủ tốt cho hầu hết người dùng và hoàn toàn không có bất kỳ quảng cáo phiền phức nào. Quá trình thiết lập cũng khá dễ dàng cho một giáo dân. Sau đây là một số tính năng ấn tượng của dịch vụ lưu trữ email này. 

> Tối đa 25 địa chỉ email - Gói miễn phí cho phép bạn định cấu hình hơn 2 chục địa chỉ email tên miền tùy chỉnh, quá đủ cho một người dùng trung bình.

> Tối đa 5 GB dung lượng trên mỗi hộp thư đến - Với dung lượng lưu trữ phù hợp cho mỗi địa chỉ email, bạn có thể lưu hàng ngàn email mà không cần phải xóa chúng để giải phóng dung lượng cho những địa chỉ mới hơn.

> Điện thoại di động, máy tính để bàn và máy khách web - Người dùng có thể sử dụng giao diện web để truy cập nhanh email của họ ngay cả trên các máy tính dùng chung. Tương tự, các ứng dụng di động cho phép bạn giao tiếp dễ dàng thông qua điện thoại thông minh của bạn.

> Bảng điều khiển mạnh mẽ - Bảng điều khiển quản trị bao gồm vô số tùy chọn để định cấu hình chính sách, quy tắc và bộ lọc để dễ dàng quản lý cả người dùng và luồng lưu lượng email.

___

> [Migadu](https://www.migadu.com/en/index.html) : Dịch vụ lưu trữ email đơn giản này cung cấp một gói miễn phí linh hoạt có thể được sử dụng để cung cấp năng lượng cho giao tiếp email tên miền tùy chỉnh của bạn. Nếu bạn đang chạy trang web của mình trên máy chủ Digital Ocean, dịch vụ này cho phép bạn dễ dàng định cấu hình các bản ghi tên miền email chỉ bằng một cú nhấp chuột. Các tính năng sau đây là một phần của dịch vụ lưu trữ email đơn giản và thân thiện với người dùng này cho một miền tùy chỉnh.

> Hộp thư không giới hạn - Không có giới hạn về số lượng địa chỉ bạn có thể tạo cho tên miền của mình, quá đủ cho một gói miễn phí.

> Dung lượng hộp thư đến 1GB - Với dung lượng lưu trữ lớn đó, bạn có thể dễ dàng lưu hàng ngàn văn bản và email HTML phong phú.

> Giao diện web đơn giản - Giao diện web nhanh như chớp mặc dù bạn có thể định cấu hình ứng dụng email yêu thích của mình ngay trên màn hình.

> Dễ dàng thiết lập - Toàn bộ thiết lập rất đơn giản và bao gồm một vài bước thiết lập hồ sơ lưu trữ cho email.

___

> [Yandex.Mail for Domain](https://connect.yandex.com) Đây là một dịch vụ lưu trữ email phổ biến khác có sẵn cho các miền tùy chỉnh. Nó có một giao diện tối thiểu và hoạt động như sự quyến rũ mà không gặp rắc rối. Nếu bạn đang tìm kiếm một dịch vụ lưu trữ email đáng tin cậy cho tên miền của trang web của bạn, thì dịch vụ lưu trữ này là một trong những ứng cử viên tốt nhất cho cùng. Các tính năng sau được bao gồm trong tài khoản email tên miền tùy chỉnh của bạn khi sử dụng dịch vụ này.

> 1000 hộp thư - Bây giờ đó là một con số lớn khi nói đến việc tạo nhiều địa chỉ email bằng một tên miền tùy chỉnh.

> Dung lượng hộp thư đến không giới hạn - Nếu bạn đang chơi công bằng và không lạm dụng đặc quyền, bạn có thể dễ dàng yên tâm về không gian hộp thư đến không giới hạn.

> Giao diện web theo chủ đề - Giao diện web thanh lịch có thể được tùy chỉnh bằng các chủ đề khác nhau phù hợp với sở thích của riêng bạn.

> Hỗ trợ IMAP / POP3 - Điều này cho phép bạn dễ dàng định cấu hình hầu hết mọi ứng dụng email để truy cập email tên miền tùy chỉnh của mình trong một ứng dụng bên ngoài.

