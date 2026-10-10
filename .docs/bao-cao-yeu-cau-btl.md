# Báo cáo ngắn gọn yêu cầu bài tập lớn — BlueMoon

Nguồn: [20261 - Chu de BTL.pdf](../Documents/20261%20-%20Chu%20de%20BTL.pdf), 3 trang. Tài liệu này tóm tắt phạm vi sản phẩm để Codex dùng làm mục tiêu triển khai và đối chiếu khi hoàn thành dự án.

## 1. Mục tiêu cuối cùng

Xây dựng phần mềm cho **Ban quản trị chung cư BlueMoon** quản lý các khoản thu, việc nộp tiền của từng hộ và thông tin hộ dân. Sản phẩm phải là **ứng dụng desktop sử dụng Java**, lưu dữ liệu tập trung trên **MySQL server** (trang 3).

Hoàn thành lần lượt **version 1 (v1.0)** và **version 2 (v2.0)**; v2 kế thừa đầy đủ chức năng và dữ liệu của v1.

## 2. Version 1 — Quản lý thu phí và hộ dân

Phạm vi theo trang 1–3 của đề:

| Mã | Chức năng phải làm | Kết quả cần có |
| --- | --- | --- |
| V1-01 | Tài khoản Ban quản trị | Có luồng đăng ký tài khoản và đăng nhập; chức năng quản lý hộ dân chỉ truy cập được sau khi đăng nhập thành công. |
| V1-02 | Thông tin cá nhân | Quản lý thông tin cá nhân của người dùng và thay đổi mật khẩu đăng nhập. |
| V1-03 | Quản lý khoản thu | Quản lý thông tin phí dịch vụ, phí quản lý và các đợt đóng góp tự nguyện; có luồng tạo khoản thu. |
| V1-04 | Thu phí theo hộ gia đình | Quản lý các khoản cần đóng và ghi nhận tiền từng hộ đã nộp theo khoản thu, tháng hoặc đợt tương ứng. |
| V1-05 | Tra cứu, tìm kiếm | Tra cứu thông tin khoản thu và việc nộp tiền của hộ gia đình. |
| V1-06 | Thống kê cơ bản | Thống kê các khoản đóng góp và hiện trạng thu tiền để Ban quản trị theo dõi. |
| V1-07 | Quản lý hộ khẩu | Quản lý thông tin cơ bản và chi tiết hộ gia đình, danh sách nhân khẩu trong hộ. |
| V1-08 | Quản lý nhân khẩu | Quản lý thông tin cư dân, biến đổi nhân khẩu, tạm trú và tạm vắng; tra cứu được để cung cấp cho cơ quan chức năng khi có yêu cầu. |

**Quy tắc nghiệp vụ cần giữ:**

- Phí dịch vụ và phí quản lý là **bắt buộc, thu hằng tháng**, tính theo diện tích căn hộ. Cần có thông tin diện tích để xác định tiền phải nộp.
- Phí dịch vụ được đề mô tả trong khoảng **2.500–16.500 đồng/m²/tháng**; đề chưa chọn đơn giá cụ thể cho BlueMoon.
- Phí quản lý BlueMoon được mô tả ở mức **từ 7.000 đồng/m²**; bối cảnh là thu hằng tháng. Cần xác định đơn giá áp dụng trước khi chốt tính phí.
- Đóng góp cho các quỹ là **tự nguyện, thu theo từng đợt**, không coi hộ chưa đóng là đang nợ phí bắt buộc.
- Nghiệp vụ hằng tháng có lập danh sách khoản phải đóng theo hộ và thông báo thu tiền. Đề chưa quy định thông báo qua email, SMS hay kênh điện tử nào.

**Tiêu chí hoàn thành v1 — diễn giải để kiểm tra sản phẩm:**

- [ ] Đăng ký/đăng nhập, quản lý thông tin cá nhân và đổi mật khẩu hoạt động; truy cập quản lý hộ dân yêu cầu đăng nhập.
- [ ] Quản lý được hộ gia đình, thành viên, biến đổi nhân khẩu, tạm trú và tạm vắng.
- [ ] Tạo khoản thu → xác định khoản phải đóng theo hộ/tháng/đợt → ghi nhận thu tiền → tra cứu và thống kê được dữ liệu vừa tạo.
- [ ] Phân biệt đúng phí bắt buộc với đóng góp tự nguyện; tính phí theo diện tích và đơn giá đã xác định.
- [ ] Ứng dụng desktop Java lưu và đọc lại được dữ liệu trên MySQL sau khi khởi động lại.

## 3. Version 2 — Bổ sung gửi xe và các khoản thu hộ

Phạm vi bổ sung theo trang 3 của đề:

| Mã | Chức năng phải làm | Quy tắc nghiệp vụ |
| --- | --- | --- |
| V2-01 | Quản lý phương tiện đăng ký của hộ | Lưu phương tiện gắn với hộ gia đình và phân biệt xe máy, ô tô để tính phí. |
| V2-02 | Thu phí gửi xe | Thu hằng tháng theo phương tiện đăng ký; xe máy **70.000 đồng/xe/tháng**; phí ô tô cần xác nhận đơn vị ở mục 4. |
| V2-03 | Thu hộ điện, nước, internet | Ghi nhận và quản lý thu tiền hằng tháng theo thông báo của công ty cung cấp dịch vụ tương ứng. Đề không yêu cầu tự tính tiền từ chỉ số tiêu thụ. |

**Tiêu chí hoàn thành v2 — diễn giải để kiểm tra sản phẩm:**

- [ ] Toàn bộ chức năng và dữ liệu v1 tiếp tục sử dụng được.
- [ ] Đăng ký phương tiện cho hộ → tính phí gửi xe theo tháng → ghi nhận thu tiền → tra cứu và thống kê được.
- [ ] Nhập khoản điện/nước/internet theo thông báo dịch vụ cho hộ và tháng tương ứng → ghi nhận thu hộ → tra cứu và thống kê được.

## 4. Điểm đề chưa xác định rõ

- **Phí ô tô:** PDF ghi “1.200.000 nghìn đồng/xe/một tháng”. Có dấu hiệu nhầm đơn vị; giá trị có thể được hiểu là **1.200.000 đồng/xe/tháng**, nhưng đây là suy đoán. Phải xác nhận trước khi chốt đơn giá; không tự sửa thành yêu cầu chính thức.
- **Tài khoản:** đề vừa nói dùng tài khoản đã cung cấp, vừa liệt kê luồng đăng ký. Cần làm rõ ai được đăng ký và cách cấp tài khoản; đề chưa yêu cầu nhiều vai trò người dùng.
- Đề chưa quy định chi tiết trường dữ liệu hộ dân, cách xử lý nộp thiếu/nộp nhiều lần, mẫu thống kê hoặc cách gửi thông báo. Cần xác định khi thiết kế nghiệp vụ.

## 5. Hướng dẫn cho Codex khi triển khai

Các điểm dưới đây là **gợi ý triển khai**, không phải yêu cầu bổ sung của đề:

- Dùng các mã V1-xx/V2-xx để liên kết công việc với mục tiêu; hoàn tất và kiểm tra v1 trước khi bổ sung v2.
- Thiết kế dữ liệu liên kết hộ gia đình, căn hộ/diện tích, nhân khẩu, khoản thu, kỳ/đợt thu và lần nộp tiền; v2 bổ sung phương tiện và khoản thu hộ.
- Cho phép cấu hình đơn giá; ghi lại đơn giá áp dụng của từng kỳ để thay đổi giá không làm sai các khoản thu trước đó.
- Đối chiếu checklist sau mỗi phiên bản. Khi có yêu cầu mới hoặc giải đáp điểm chưa rõ, cập nhật tài liệu và ghi rõ nguồn thay đổi.

**Giới hạn bản tóm tắt:** PDF nêu yêu cầu sản phẩm và bốn luồng nghiệp vụ: đăng ký tài khoản, tạo khoản thu, thu phí, thống kê đóng góp. PDF không nêu hạn nộp, thang điểm hoặc danh sách hồ sơ phải nộp; cần đối chiếu hướng dẫn môn học nếu có.
