# BlueMoon — Quản lý và thu phí chung cư

Bài tập lớn môn **Công nghệ phần mềm**, xây dựng phần mềm cho **Ban quản trị chung cư BlueMoon** để tập trung dữ liệu hộ dân, quản lý khoản thu và theo dõi việc nộp tiền, giảm thao tác thủ công và sai sót khi đối chiếu.

**Nền tảng mục tiêu:** ứng dụng desktop bằng **Java**, lưu dữ liệu tập trung trên **MySQL server**.

**Trạng thái hiện tại:** phân tích yêu cầu và lập kế hoạch phát triển; project gồm tài liệu Markdown, Excel và đề bài PDF, chưa có mã nguồn ứng dụng hoặc hướng dẫn cài đặt/chạy.

## Phạm vi chức năng

### v1.0 — Quản lý hộ dân và thu phí

- **Tài khoản và truy cập:** đăng nhập, đổi mật khẩu, cập nhật thông tin cá nhân, cấp tài khoản và phân quyền cho nhân sự Ban quản trị.
- **Hộ gia đình:** quản lý căn hộ, diện tích, chủ hộ, thông tin liên hệ và lịch sử thay đổi.
- **Nhân khẩu:** quản lý thành viên từng hộ, biến động cư trú, tạm trú/tạm vắng; xuất hoặc in danh sách.
- **Khoản thu:** quản lý loại phí, đơn giá, kỳ/đợt thu; tính khoản phải đóng theo diện tích căn hộ.
- **Thu phí:** ghi nhận nộp tiền, nộp một phần hoặc gộp nhiều khoản; in/xuất biên lai, sửa hoặc hủy giao dịch kèm lý do.
- **Tra cứu và thống kê:** tìm hộ/nhân khẩu, xem lịch sử thanh toán và công nợ, thống kê thu phí, đóng góp và dân cư.
- **An toàn dữ liệu và chất lượng:** bảo vệ dữ liệu cá nhân, ghi nhật ký thao tác, sao lưu/khôi phục, hiệu năng và giao diện tiếng Việt dễ dùng.

**Quy tắc chính:** phí dịch vụ và phí quản lý là khoản bắt buộc, thu hằng tháng theo diện tích và đơn giá áp dụng; đóng góp tự nguyện thu theo đợt, không tính khoản chưa đóng góp vào công nợ bắt buộc.

### v2.0 — Mở rộng theo đề bài

Bổ sung quản lý phương tiện, phí gửi xe và thu hộ điện, nước, internet theo thông báo của nhà cung cấp; kế thừa chức năng và dữ liệu v1.0. Phiên bản này chưa có User Story hoặc kế hoạch Sprint riêng.

## Hồ sơ yêu cầu và kế hoạch

- **Đầu vào:** 4 cuộc phỏng vấn giả lập và 5 câu hỏi tình huống; 35 mong muốn (Wish), 35 yêu cầu RAW gồm 27 yêu cầu chức năng (FR) và 8 yêu cầu phi chức năng (NFR). Đây là dữ liệu mô phỏng từ đề bài, chưa được xác nhận qua phỏng vấn thực tế.
- **Phân tích:** 7 Epic, 50 User Story kèm tiêu chí chấp nhận; gồm 41 story thuộc phạm vi cơ sở v1.0 (baseline) và 9 ứng viên chờ duyệt. Các ứng viên đề cập miễn/giảm phí, công nợ khi đổi chủ, đối soát chuyển khoản, kết sổ và chống lưu trùng phiếu thu.
- **Truy vết:** nguồn yêu cầu → Wish/RAW → Epic/Feature → User Story → tiêu chí chấp nhận → Backlog/Sprint; backlog có ưu tiên MoSCoW, Story Points và phụ thuộc.

| Sprint dự kiến | Trọng tâm | User Story | Task |
| --- | --- | ---: | ---: |
| 1 | Nền tảng Java/MySQL, tài khoản, hộ gia đình và nhân khẩu | 11 | 55 |
| 2 | Khoản thu, thu phí, biên lai và cấp tài khoản | 10 | 46 |
| 3 | Tra cứu, thống kê, bảo vệ dữ liệu, sao lưu và ổn định sản phẩm | 10 | 49 |

Ba Sprint đã xếp **31 story và 150 task**; còn **10 story baseline chưa xếp Sprint**, cùng **9 ứng viên chưa được cam kết**. Ngày bắt đầu và thời lượng Sprint chưa chốt; các task hiện ở trạng thái `Todo`.

## Tài liệu trong project

| Tài liệu | Nội dung |
| --- | --- |
| [Đề bài BTL](Documents/20261%20-%20Chu%20de%20BTL.pdf) | Bối cảnh, yêu cầu v1.0/v2.0, nền tảng và luồng nghiệp vụ |
| [Tổng quan dự án](.docs/project_overview.md) | Mục tiêu, stakeholder, phạm vi, giả định, ràng buộc và câu hỏi mở |
| [Tóm tắt yêu cầu đề bài](.docs/bao-cao-yeu-cau-btl.md) | Chức năng và tiêu chí hoàn thành từng phiên bản |
| [Tổng quan phỏng vấn giả lập](.docs/interview_overview.md) | Phương pháp thu thập, nguồn dữ liệu và tổng hợp yêu cầu |
| [Raw Requirements](data_output/Raw_Requirements.xlsx) | Wish List, RAW, NFR và tổng hợp phỏng vấn |
| [Epic & User Story](data_output/Epic_UserStory.xlsx) | Story Map, Epic, Feature, tiêu chí chấp nhận và rà soát RAW |
| [Product Backlog](data_output/Product_Backlog.xlsx) | Backlog, truy vết, ứng viên chờ duyệt, Sprint và phân công dự kiến |

Đọc **Tổng quan dự án** để nắm phạm vi, sau đó dùng ba bảng Excel để xem chi tiết và theo dõi công việc. Quy trình cấp/đăng ký tài khoản, ma trận quyền, đơn giá phí và một số tiêu chí chất lượng còn cần xác nhận; xem câu hỏi mở trong tài liệu tổng quan.
