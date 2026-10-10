# Project Overview — Phần mềm quản lý và thu phí chung cư BlueMoon

| Mục | Giá trị |
| --- | --- |
| Phiên bản tài liệu | 0.1 — bản tổng hợp theo tài liệu hiện có, các vấn đề chưa chốt được liệt kê cuối tài liệu |
| Ngày cập nhật | 2026-10-10 |
| Tên dự án | Xây dựng phần mềm quản lý và thu phí ở chung cư BlueMoon |
| Nhóm thực hiện | Nguyễn Doãn Dũng, Nguyễn Hoàng Đức , Nguyễn Văn Tuấn Hưng, Phạm Công Nam Khánh, Nguyễn Quang Minh — theo `Product_Backlog.xlsx`, sheet `Workload_Summary` |
| Bối cảnh học tập | Bài tập lớn Công nghệ phần mềm; bộ đề `20261 - Chu de BTL.pdf`. Số nhóm và mã học phần chưa được xác nhận bằng tài liệu hiện có trong dự án. |
| Khách hàng / người dùng chính | Ban quản trị chung cư BlueMoon |
| Nhà tài trợ | Chưa xác định trong đề bài hiện có |
| Giai đoạn hiện tại | Phân tích yêu cầu, xây dựng Epic / User Story và lập kế hoạch Sprint; chưa có mã nguồn ứng dụng trong thư mục dự án tại ngày cập nhật |
| Nền tảng mục tiêu | xây dựng phần mềm DESKTOP |
| Phạm vi phiên bản | Baseline và kế hoạch Sprint hiện tập trung vào v1.0; v2.0 là phiên bản mở rộng được đề bài nêu, chưa có User Story hoặc Sprint riêng trong các bảng hiện tại |

> **Quy ước nguồn dữ liệu.** **[Đề bài]** là nội dung đối chiếu với PDF trong dự án; **[Dự án]** là nội dung đang được ghi trong các tài liệu Markdown và Excel; **[Giả lập]** là nhu cầu stakeholder được nhóm mô phỏng; **[Giả định / Đề xuất]** là cách diễn giải hoặc quyết định còn cần xác nhận. Các nhãn có thể đi cùng nhau khi một yêu cầu vừa có căn cứ trong đề bài, vừa được chi tiết hóa qua dữ liệu giả lập.
>
> Theo `Raw_Requirements.xlsx`, sheet `Interview_Summary`, dữ liệu phỏng vấn là **Simulated Interview / Role-play**; chưa có phỏng vấn, khảo sát hoặc quan sát thực tế. Các mã `SIM-INT-...` và `SIM-SCEN-...` là tham chiếu nội bộ. Tài liệu này không xác nhận stakeholder thực tế đã phê duyệt yêu cầu hoặc kế hoạch.
>
> Bản mẫu `F:\01_Project_Overview.md` do người dùng cung cấp được dùng để tham khảo bố cục. Thông tin riêng của bản mẫu như số nhóm, nhân vật trong Project Charter, nhà tài trợ, ngân sách và lịch thực hiện cần có căn cứ riêng trước khi áp dụng cho dự án này.

## 1. Tên dự án

**Xây dựng phần mềm quản lý và thu phí ở chung cư BlueMoon**, gọi tắt là **BlueMoon**.

- **BlueMoon v1.0:** quản lý tài khoản, hộ gia đình, nhân khẩu, khoản thu, ghi nhận thu phí, tra cứu và thống kê; các yêu cầu chất lượng được chi tiết hóa trong tài liệu dự án.
- **BlueMoon v2.0:** phát triển tiếp v1.0, bổ sung quản lý phương tiện, phí gửi xe và thu hộ điện, nước, internet. [Đề bài, trang 3]

### 1.1. Hiện trạng hồ sơ dự án

| Nhóm tài liệu | Nội dung hiện có | Nguồn |
| --- | --- | --- |
| Đề bài | Bối cảnh, chức năng v1.0 / v2.0, nền tảng và các luồng nghiệp vụ | [20261 - Chu de BTL.pdf](../Documents/20261%20-%20Chu%20de%20BTL.pdf), 3 trang |
| Thu thập yêu cầu | 35 Wish, 35 RAW gồm 27 FR và 8 NFR; 4 cuộc phỏng vấn giả lập và 5 câu hỏi tình huống bổ sung | [Raw_Requirements.xlsx](../output_dataprocessing/Raw_Requirements.xlsx) |
| Phân tích yêu cầu | 7 Epic, 50 User Story gồm 41 story baseline và 9 story ứng viên chờ xác nhận | [Epic_UserStory.xlsx](../output_dataprocessing/Epic_UserStory.xlsx) |
| Backlog và kế hoạch | Product Backlog, Traceability, PO Refinement, 3 Sprint và phân công dự kiến | [Product_Backlog.xlsx](../output_dataprocessing/Product_Backlog.xlsx) |
| Tài liệu tổng hợp | Tóm tắt đề bài và tổng quan dữ liệu phỏng vấn giả lập | [bao-cao-yeu-cau-btl.md](bao-cao-yeu-cau-btl.md), [interview_overview.md](interview_overview.md) |

Các số lượng trên được đếm theo mã định danh. Tám bản ghi trong sheet `NFR` mô tả chi tiết cùng tám NFR đã có trong RAW, không làm tăng tổng số yêu cầu lên 43. Hồ sơ hiện có thể hiện công việc phân tích và lập kế hoạch; chưa có bằng chứng ứng dụng đã được xây dựng hoặc nghiệm thu.

## 2. Bối cảnh

[Đề bài, trang 1] Chung cư BlueMoon tọa lạc tại ngã tư Văn Phú, khởi công năm 2021 và hoàn thành năm 2023. Chung cư được xây dựng trên diện tích 450 m², gồm 30 tầng: tầng 1 làm kiot, 4 tầng đế, 24 tầng nhà ở và 1 tầng penthouse.

[Đề bài, trang 1–2] Ban quản trị do cư dân bầu ra thực hiện quản lý và thu phí. Hằng tháng, Ban quản trị lập danh sách các khoản cần đóng của từng hộ và gửi thông báo thu tiền. Việc thu phí đang được quản lý thủ công, có Excel hỗ trợ nhưng hiệu quả chưa cao.

Các khoản thu của v1.0:

| Khoản thu | Tính chất | Căn cứ tính / thu |
| --- | --- | --- |
| Phí dịch vụ chung cư | Bắt buộc, thu hằng tháng | Tính theo diện tích căn hộ; đề nêu khoảng 2.500–16.500 đồng/m²/tháng, chưa chọn đơn giá cụ thể cho BlueMoon |
| Phí quản lý chung cư | Bắt buộc, thu hằng tháng | Tính theo diện tích căn hộ; đề nêu mức từ 7.000 đồng/m², cần xác định đơn giá áp dụng |
| Các khoản đóng góp cho quỹ vì người nghèo, biển đảo, từ thiện… | Tự nguyện, thu theo từng đợt | Ban quản trị phối hợp với chính quyền địa phương và tổ dân phố; số tiền đóng góp theo tinh thần tự nguyện |

[Đề bài, trang 2–3] Hệ thống còn quản lý thông tin hộ gia đình và nhân khẩu, gồm các biến động, tạm trú và tạm vắng, để Ban quản trị cung cấp thông tin cho cơ quan chức năng khi được yêu cầu.

## 3. Vấn đề hiện tại

Vấn đề được đề bài xác nhận là **hiệu quả quản lý thu phí thủ công chưa cao**. Các vấn đề chi tiết dưới đây được tổng hợp từ dữ liệu giả lập trong dự án và chưa được kiểm chứng với người dùng thực tế.

| # | Vấn đề [Giả lập] | Hệ quả nghiệp vụ | Tham chiếu RAW |
| --- | --- | --- | --- |
| 1 | Thông tin hộ, nhân khẩu và lịch sử cư trú cần được tập trung | Tốn thời gian tra cứu, cập nhật và tổng hợp thông tin cho cơ quan chức năng | `RAW-003`–`RAW-009` |
| 2 | Tính phí theo diện tích và đơn giá bằng tay | Dễ sai số tiền, khó giải thích cách tính cho từng hộ | `RAW-010`–`RAW-011` |
| 3 | Ghi nhận nộp tiền, nộp thiếu hoặc nộp gộp khó đối chiếu | Khó xác định hộ đã đóng, còn thiếu bao nhiêu và khoản tiền được phân bổ vào kỳ nào | `RAW-013`, `RAW-018`, `RAW-020` |
| 4 | Biên lai và xử lý giao dịch ghi nhầm thiếu một quy trình thống nhất | Chứng từ chậm, khó truy lại người sửa và lý do sửa | `RAW-014`–`RAW-015`, `RAW-025` |
| 5 | Thống kê thu phí và dân cư phải tổng hợp thủ công | Chậm nắm hiện trạng khoản thu, đợt đóng góp và dân cư theo thời điểm | `RAW-019`–`RAW-021` |
| 6 | Quyền truy cập, bảo vệ dữ liệu và sao lưu cần được làm rõ | Có nguy cơ xem hoặc sửa dữ liệu ngoài trách nhiệm, mất dữ liệu khi xảy ra sự cố | `RAW-022`–`RAW-026` |

Các tình huống miễn/giảm phí, công nợ khi đổi chủ, chuyển khoản chưa xác định, kết sổ và lưu trùng phiếu thu thuộc nhóm bổ sung `RAW-031`–`RAW-035`; trạng thái phạm vi được trình bày tại mục 8.2.

## 4. Mục tiêu hệ thống

### 4.1. Mục tiêu sản phẩm

1. Tập trung dữ liệu hộ gia đình, nhân khẩu, khoản thu và lịch sử nộp tiền trong một hệ thống. [Đề bài / Dự án]
2. Hỗ trợ luồng **tạo khoản thu → xác định khoản phải đóng theo hộ và kỳ / đợt → ghi nhận thu phí → tra cứu, thống kê**. [Đề bài / Dự án]
3. Tính phí bắt buộc theo diện tích và đơn giá áp dụng; phân biệt với đóng góp tự nguyện. [Đề bài / Dự án]
4. Giúp Ban quản trị tra cứu thông tin cư trú và cung cấp dữ liệu khi cơ quan chức năng yêu cầu. [Đề bài]
5. Bảo vệ truy cập và dữ liệu; hỗ trợ truy vết, sao lưu và khôi phục theo tiêu chí được xác nhận. [Dự án / Giả lập]
6. Phát triển v2.0 trên nền v1.0, bổ sung phí gửi xe và các khoản thu hộ theo đề bài. [Đề bài / Dự án]

### 4.2. Tiêu chí kết quả ở mức tổng quan

Các tiêu chí dưới đây là diễn giải để kiểm tra sản phẩm, cần đối chiếu Acceptance Criteria của từng story khi triển khai:

- Người dùng được cấp quyền có thể đăng nhập, quản lý thông tin tài khoản và đổi mật khẩu; chức năng quản lý yêu cầu đăng nhập.
- Có thể quản lý hộ, diện tích căn hộ, nhân khẩu, biến động cư trú, tạm trú và tạm vắng.
- Dữ liệu khoản thu và nộp tiền được liên kết với đúng hộ, khoản thu và kỳ / đợt; tra cứu, thống kê phản ánh các giao dịch đã ghi nhận.
- Hộ chưa đóng góp tự nguyện không bị coi là đang nợ phí bắt buộc.
- Ứng dụng desktop Java đọc lại được dữ liệu đã lưu trên MySQL sau khi khởi động lại.
- Khi bổ sung v2.0, chức năng và dữ liệu v1.0 tiếp tục sử dụng được.

Các chỉ tiêu như thời gian phản hồi, số thao tác hay ngưỡng khóa đăng nhập hiện là đề xuất trong tài liệu dự án, chưa phải tiêu chí đã được stakeholder thực tế phê duyệt.

## 5. Đối tượng sử dụng

[Đề bài / Dự án] Người dùng trực tiếp của v1.0 là **nhân sự Ban quản trị**. Tài liệu dự án đang mô tả các vai trò sau:

| Vai trò được mô tả | Công việc dự kiến | Tình trạng phân quyền |
| --- | --- | --- |
| Quản trị hệ thống | Cấp, vô hiệu hóa tài khoản; đặt lại mật khẩu; gán quyền; thực hiện các thao tác quản trị được cho phép | Có trong `US-05`, `US-41`; ma trận quyền cần được xác nhận |
| Thành viên Ban quản trị | Quản lý hộ, nhân khẩu, khoản thu; xem dữ liệu và thống kê theo trách nhiệm | Được dùng làm vai trò trong User Story; quyền cụ thể cần đối chiếu với ma trận chung |
| Thủ quỹ / người thu phí | Tra cứu hộ và khoản thu, ghi nhận nộp tiền, in hoặc xuất biên lai | `US-05` dự kiến hạn chế sửa hộ, nhân khẩu, khoản thu, đơn giá và tài khoản |

Các tên vai trò trên chưa tạo thành một mô hình ba vai trò đã chốt. Acceptance Criteria của `US-05` hiện nêu gán vai trò Quản trị hệ thống hoặc Thủ quỹ, trong khi nhiều story dùng vai trò Thành viên Ban quản trị; cần thống nhất cách ánh xạ các vai trò này.

Cư dân, chủ hộ và cơ quan chức năng là stakeholder. Baseline v1.0 hiện không có tài khoản tự phục vụ cho các nhóm này; nhu cầu của họ được xử lý thông qua Ban quản trị. [Dự án, `WISH-24`, `WISH-25`, tham chiếu `AS-02`]

## 6. Stakeholder

Các mối quan tâm chi tiết trong bảng là nội dung tổng hợp phục vụ phân tích; phần được lấy từ phỏng vấn là **giả lập**.

| Stakeholder | Vai trò đối với dự án | Mối quan tâm chính | Tương tác | Nguồn |
| --- | --- | --- | --- | --- |
| Ban quản trị BlueMoon | Khách hàng, người dùng chính | Quản lý đúng hộ, nhân khẩu, khoản thu; nắm hiện trạng thu phí | Trực tiếp | Đề bài; `SIM-INT-BQT` |
| Thủ quỹ / người thu phí | Người vận hành nghiệp vụ thu tiền | Tính phí rõ ràng, ghi nhận chính xác, tra cứu nhanh, có chứng từ | Trực tiếp | Giả lập; `SIM-INT-TQ` |
| Hộ gia đình, cư dân, chủ sở hữu | Bên đóng phí và đối tượng được quản lý thông tin | Minh bạch khoản thu; đúng tính tự nguyện; thông tin cư trú và dữ liệu cá nhân được bảo vệ | Qua Ban quản trị trong v1.0 | Đề bài; giả lập `SIM-INT-CD` |
| Cơ quan chức năng | Bên yêu cầu thông tin hộ và nhân khẩu | Danh sách và lịch sử cư trú chính xác theo phạm vi yêu cầu | Nhận thông tin qua Ban quản trị | Đề bài; giả lập `SIM-INT-CQ` |
| Chính quyền địa phương, tổ dân phố | Bên phối hợp thu đóng góp | Theo dõi các đợt đóng góp tự nguyện | Gián tiếp | Đề bài |
| Nhà cung cấp điện, nước, internet | Nguồn thông báo khoản thu hộ ở v2.0 | Khoản thu theo đúng thông báo dịch vụ | Qua Ban quản trị; chưa có yêu cầu tích hợp trực tiếp | Đề bài, v2.0 |
| Nhóm thực hiện | Phân tích, lập kế hoạch và xây dựng sản phẩm | Phạm vi rõ ràng, yêu cầu truy vết được, có tiêu chí kiểm tra | Xây dựng dự án | Dự án |
| Giảng viên / người đánh giá bài tập lớn | Hướng dẫn, đánh giá | Sản phẩm và hồ sơ đáp ứng yêu cầu môn học | Gián tiếp | Bối cảnh bài tập lớn; chưa có hướng dẫn đánh giá riêng trong thư mục hiện tại |

## 7. Phạm vi v1.0

### 7.1. Baseline theo Epic hiện có

[Dự án] `Epic_UserStory.xlsx` tổ chức baseline thành **7 Epic**. Tra cứu và thống kê được gộp trong một Epic; an toàn dữ liệu và chất lượng nền tảng được tổ chức thành Epic riêng. Chi tiết Feature, User Story và Acceptance Criteria nằm trong các bảng Excel.

| Epic | Phạm vi baseline | User Story baseline | RAW nguồn |
| --- | --- | --- | --- |
| `EPIC-01` — Tài khoản và truy cập | Đăng nhập, đổi mật khẩu, cập nhật thông tin tài khoản, bảo vệ đăng nhập, phân quyền và cấp tài khoản | `US-01`–`US-05`, `US-41` | `RAW-001`, `RAW-002`, `RAW-022`, `RAW-023` |
| `EPIC-02` — Hộ gia đình | Thêm, xem, sửa thông tin hộ, diện tích, chủ hộ; giữ lịch sử đổi chủ hoặc ngừng cư trú | `US-06`–`US-09` | `RAW-003`–`RAW-005` |
| `EPIC-03` — Nhân khẩu | Hồ sơ thành viên, biến động cư trú, tạm trú / tạm vắng, xuất hoặc in danh sách | `US-10`–`US-15` | `RAW-006`–`RAW-009` |
| `EPIC-04` — Khoản thu | Định nghĩa khoản thu, quản lý đơn giá và kỳ / đợt, lập khoản phải thu, diễn giải cách tính, đóng góp tự nguyện | `US-16`–`US-21` | `RAW-010`–`RAW-012` |
| `EPIC-05` — Thu phí | Ghi nhận thanh toán, nộp một phần hoặc gộp nhiều khoản, biên lai, sửa / hủy giao dịch kèm lý do | `US-22`–`US-26` | `RAW-013`–`RAW-015` |
| `EPIC-06` — Tra cứu và thống kê | Tìm hộ / nhân khẩu; xem lịch sử, tình trạng nộp, công nợ; thống kê thu phí, đóng góp và dân cư | `US-27`–`US-34` | `RAW-016`–`RAW-021` |
| `EPIC-07` — An toàn dữ liệu và chất lượng | Bảo vệ dữ liệu cá nhân, nhật ký thao tác, sao lưu / khôi phục, hiệu năng, giao diện dễ dùng | `US-35`–`US-40` | `RAW-024`–`RAW-028` |

Tổng baseline là **41 story**. Các chi tiết như biên lai, nộp một phần, nộp gộp, audit log và sao lưu được tài liệu dự án bổ sung từ dữ liệu giả lập; đề PDF không đặc tả đầy đủ các hành vi này.

### 7.2. Luồng nghiệp vụ và quy tắc chính

PDF trang 3 liệt kê bốn luồng: **đăng ký tài khoản, tạo khoản thu, thu phí, thống kê các khoản đóng góp**. Baseline hiện diễn giải việc cấp tài khoản thành thao tác của quản trị viên (`US-41`); quan hệ với luồng đăng ký của đề bài cần được làm rõ.

Luồng vận hành dự kiến:

**Đăng nhập → quản lý dữ liệu hộ / nhân khẩu → tạo khoản thu và kỳ / đợt → lập khoản phải thu → ghi nhận nộp tiền → tra cứu và thống kê.**

- Phí dịch vụ và phí quản lý là bắt buộc, thu theo tháng và tính theo diện tích. Đơn giá áp dụng cần được xác định; các khoảng giá trong đề không tự trở thành đơn giá cố định. [Đề bài / Dự án]
- Các khoản đóng góp thu theo đợt, tự nguyện; không cộng khoản chưa đóng góp vào công nợ phí bắt buộc. [Đề bài / Dự án]
- Baseline dự kiến lưu đơn giá áp dụng và lịch sử thay đổi; cách tính lại khi sửa diện tích hoặc khoản thu đã phát hành còn cần xác nhận. [Dự án / Giả lập]
- Nộp một phần, nộp gộp, sửa / hủy thanh toán và biên lai được chi tiết hóa trong `US-22`–`US-26`; ưu tiên và việc xếp Sprint không giống nhau cho mọi story. [Dự án]
- Ghi nhận hình thức chuyển khoản trong phiếu thu không đồng nghĩa với tích hợp ngân hàng hoặc xử lý thanh toán trực tuyến. [Dự án]

### 7.3. Yêu cầu chất lượng đang được theo dõi

| Nhóm | NFR / RAW | Phạm vi và điểm cần xác nhận |
| --- | --- | --- |
| Xác thực an toàn | `NFR-001` / `RAW-022` | Băm mật khẩu, giới hạn đăng nhập sai; ngưỡng và thời gian khóa chưa chốt |
| Phân quyền | `NFR-002` / `RAW-023` | Giới hạn thao tác theo trách nhiệm; cần xác nhận ma trận vai trò – chức năng |
| Quyền riêng tư | `NFR-003` / `RAW-024` | Che số giấy tờ, giới hạn quyền xem đầy đủ và xuất dữ liệu; cần xác định trường dữ liệu và thẩm quyền |
| Truy vết | `NFR-004` / `RAW-025` | Ghi người, thời điểm, thao tác và dữ liệu trước / sau; thời gian giữ log chưa chốt |
| Độ tin cậy | `NFR-005` / `RAW-026` | Sao lưu và khôi phục; tần suất hằng ngày là giả định |
| Hiệu năng | `NFR-006` / `RAW-027` | Mục tiêu tối đa 3 giây với vài trăm hộ, vài nghìn nhân khẩu, 2–3 người dùng đồng thời là giả định cần xác nhận |
| Khả năng sử dụng | `NFR-007` / `RAW-028` | Giao diện tiếng Việt, tiền VND dễ đọc, lỗi rõ ràng; khoảng 5 thao tác chính cho một lần thu là đề xuất |
| Toàn vẹn khi lưu lặp | `NFR-008` / `RAW-035` | Có ứng viên `US-50` về tránh trùng phiếu thu khi thử lại; chưa thuộc baseline hoặc kế hoạch Sprint |

### 7.4. Phạm vi đã xếp lịch trong kế hoạch Sprint

[Dự án] Ba Sprint hiện có là **kế hoạch dự kiến**, chưa chốt ngày bắt đầu và thời lượng. Story Points và số giờ là ước lượng ban đầu của nhóm, cần rà soát trong Sprint Planning.

| Sprint | Trọng tâm | Story baseline | Story Points | Task | Giờ dự kiến |
| --- | --- | ---: | ---: | ---: | ---: |
| Sprint 1 | Nền tảng Java / MySQL, tài khoản, hộ gia đình và nhân khẩu | 11 | 34 | 55 | 202 |
| Sprint 2 | Khoản thu, lập khoản phải thu, ghi nhận thu tiền, biên lai và cấp tài khoản | 10 | 37 | 46 | 174 |
| Sprint 3 | Tra cứu, thống kê, bảo vệ dữ liệu, sao lưu và ổn định sản phẩm | 10 | 35 | 49 | 195 |
| **Tổng đã xếp lịch** | | **31** | **106** | **150** | **571** |

Nguồn: `Product_Backlog.xlsx`, các sheet `Product_Backlog`, `Sprint_1`–`Sprint_3` và `Workload_Summary`. Cả 150 task hiện có trạng thái `Todo`; việc được xếp Sprint không chứng minh đã triển khai.

**10 story baseline chưa xếp Sprint** là `US-04`, `US-09`, `US-13`, `US-15`, `US-18`, `US-24`, `US-30`, `US-34`, `US-36`, `US-37`. Chúng vẫn nằm trong Product Backlog. Cần rà soát nhóm này trước khi tuyên bố đã hoàn thành toàn bộ baseline v1.0.

**9 ứng viên `US-42`–`US-50`** có trạng thái `Candidate / PO Review`, `Planned Sprint = Unplanned`, không được tính trong 31 story, 150 task hoặc 571 giờ trên. Tổng 50 story hiện có được phân thành **31 đã xếp Sprint + 10 baseline chưa xếp Sprint + 9 ứng viên**.

## 8. Ngoài phạm vi v1.0 và hướng phát triển

### 8.1. Phiên bản v2.0 theo đề bài

V2.0 là phiên bản mở rộng được PDF nêu và được bản tóm tắt yêu cầu của dự án đặt trong mục tiêu sản phẩm. Hai RAW roadmap hiện chưa có User Story hoặc Sprint, nên cần bổ sung kế hoạch khi chuyển sang v2.0.

| Hạng mục | Nội dung | Tham chiếu |
| --- | --- | --- |
| Quản lý phương tiện và phí gửi xe | Gắn phương tiện với hộ, phân biệt xe máy / ô tô, thu phí hằng tháng; xe máy 70.000 đồng/xe/tháng | Đề bài trang 3; `RAW-029` |
| Phí gửi ô tô | PDF ghi “1.200.000 nghìn đồng/xe/một tháng”; đơn vị có dấu hiệu nhầm và cần xác nhận trước khi chốt giá | Đề bài trang 3; `RAW-029` |
| Thu hộ điện, nước, internet | Quản lý khoản thu hằng tháng theo thông báo của từng nhà cung cấp; đề chưa yêu cầu tự tính từ chỉ số tiêu thụ | Đề bài trang 3; `RAW-030` |

Các hạng mục này nằm ngoài baseline và các Sprint v1.0 hiện có. Chưa có căn cứ yêu cầu kết nối API với nhà cung cấp dịch vụ.

### 8.2. Yêu cầu bổ sung chờ xác nhận phạm vi

[Dự án / Giả lập] Năm RAW tình huống bổ sung đã được phát triển thành **9 story ứng viên**, có Acceptance Criteria dự thảo và được đưa vào sheet `PO_Refinement`. Chúng chưa được phê duyệt vào baseline hoặc cam kết Sprint.

| Chủ đề | RAW | Story ứng viên | Quyết định cần có |
| --- | --- | --- | --- |
| Miễn / giảm phí có căn cứ | `RAW-031` | `US-42`, `US-43` | Loại phí, mức giảm, thẩm quyền, thời hạn và cách xử lý khoản đã phát hành |
| Công nợ khi đổi chủ | `RAW-032` | `US-44`, `US-45` | Mốc bàn giao, căn cứ và bên chịu trách nhiệm khoản nợ cũ |
| Chuyển khoản chưa xác định | `RAW-033` | `US-46`, `US-47` | Chứng từ, người đối soát, quy tắc xác minh và ghép giao dịch |
| Bảng kê và kết sổ | `RAW-034` | `US-48`, `US-49` | Định nghĩa ca / ngày, đối chiếu, người xác nhận và xử lý chênh lệch |
| Tránh trùng phiếu thu khi lưu lại | `RAW-035` / `NFR-008` | `US-50` | Định danh một lần nộp, hành vi thử lại, tính toàn vẹn và tiêu chí kiểm thử |

Nhãn Must / Should của ứng viên thể hiện ưu tiên dự thảo, không tự động đưa story vào Sprint. Việc mở rộng phạm vi cần thống nhất quy tắc, Acceptance Criteria, phụ thuộc và ước lượng.

### 8.3. Các hạng mục chưa có trong baseline v1.0

- Cổng hoặc ứng dụng cho cư dân tự tra cứu trên điện thoại (`WISH-24`).
- Gửi nhắc phí tự động qua SMS, email hoặc kênh điện tử (`WISH-25`).
- Thanh toán trực tuyến, kết nối API ngân hàng / ví điện tử.
- Ứng dụng web hoặc di động; nền tảng mục tiêu hiện là desktop.
- Tích hợp trực tiếp với hệ thống cơ quan chức năng.
- Dịch vụ nhập hộ hoặc chuyển đổi toàn bộ dữ liệu cũ cho Ban quản trị; việc nhập dữ liệu do Ban quản trị thực hiện đang là giả định.

Việc tự đăng ký tài khoản được để ở câu hỏi mở Q-01 vì đề bài và baseline hiện có cách diễn giải khác nhau.

## 9. Các giả định

Các tham chiếu `AS-xx` dưới đây được giữ theo ghi chú Excel. Thư mục hiện tại chưa có tài liệu riêng chứa đầy đủ danh mục giả định, nên bảng chỉ diễn giải những nội dung đã thấy trong nguồn dự án.

| Chủ đề | Giả định đang sử dụng | Căn cứ / trạng thái |
| --- | --- | --- |
| Nguồn stakeholder | Nhóm mô phỏng vai trò và tình huống dựa trên đề bài; không coi đây là kết quả phỏng vấn thực tế | `Interview_Summary`; [interview_overview.md](interview_overview.md) |
| Người dùng | V1.0 phục vụ nhân sự Ban quản trị; cư dân không có tài khoản tự phục vụ | `WISH-24`, `WISH-25`; tham chiếu `AS-02` |
| Cấp tài khoản | Quản trị viên cấp tài khoản qua `US-41`; tài khoản quản trị ban đầu được nạp sẵn để khởi tạo / demo | `RAW-001`, `US-41`; `AS-03`, `OQ-01`; cần thống nhất với luồng đăng ký của đề |
| Quyền hạn | Phân tách trách nhiệm quản trị và thu phí; ma trận quyền chưa được chốt đầy đủ | `RAW-023`, `US-05`; `AS-04`, `OQ-04` |
| Thông báo thu tiền | V1.0 lập dữ liệu phải thu và hỗ trợ nhắc thủ công; kênh gửi thông báo được xử lý ngoài hệ thống theo giả định hiện tại | `AS-07`, `RAW-020`; cần xác nhận hình thức in / xuất thông báo |
| Dữ liệu ban đầu | Ban quản trị nhập dữ liệu hộ, nhân khẩu và khoản thu; nhập dữ liệu cũ hộ khách hàng chưa thuộc phạm vi | `RAW-003`, `WISH-02`; `AS-08`, `OQ-12` |
| Dữ liệu trình diễn | Dùng dữ liệu mẫu giả trong demo và kiểm thử | `NFR-003`; `AS-10` |
| Lịch sử dữ liệu | Giữ dữ liệu cũ khi đổi chủ, ngừng cư trú hoặc vô hiệu hóa tài khoản; không xóa cứng theo giả định | `RAW-005`, `US-41`; `AS-17` |
| Ngưỡng chất lượng | Quy mô dữ liệu, 3 giây phản hồi, số lần đăng nhập sai, số thao tác và lịch sao lưu là giá trị đề xuất | `RAW-022`, `RAW-026`–`RAW-028`; `AS-13`, `OQ-10` |
| Miễn / giảm phí | Chưa thuộc baseline; việc bổ sung đang được xem xét qua ứng viên | `AS-14`, `OQ-02`; `RAW-031`, `US-42`, `US-43` |

## 10. Các ràng buộc

| Loại | Ràng buộc / giới hạn hiện có | Nguồn |
| --- | --- | --- |
| Công nghệ | Nền tảng mục tiêu là ứng dụng desktop Java và MySQL server lưu dữ liệu tập trung | Đề bài trang 3 |
| Chức năng | V1.0 quản lý thu phí và hộ dân; v2.0 bổ sung gửi xe và thu hộ dịch vụ | Đề bài trang 2–3 |
| Truy cập | Chức năng quản lý hộ dân yêu cầu Ban quản trị đăng nhập thành công | Đề bài trang 3; baseline mở rộng kiểm soát truy cập cho các màn hình quản lý |
| Nghiệp vụ | Phí dịch vụ / quản lý bắt buộc theo tháng; đóng góp tự nguyện theo đợt; phí tính theo diện tích cần đơn giá áp dụng | Đề bài trang 1 |
| Quy trình hiện tại | Kế hoạch sử dụng Epic, Feature, User Story, Acceptance Criteria, MoSCoW, Story Points và 3 Sprint; không có căn cứ từ PDF này để coi mọi chi tiết quy trình là yêu cầu bắt buộc của môn học | Các bảng Excel của dự án |
| Truy vết | Duy trì liên hệ nguồn giả lập → Wish / RAW → Epic → Feature → User Story → Acceptance Criteria → Backlog / Sprint khi có kế hoạch | `Raw_Requirements.xlsx`, `Epic_UserStory.xlsx`, `Product_Backlog.xlsx` |
| Tiến độ | Ngày bắt đầu và thời lượng Sprint chưa chốt; 10 baseline story và 9 ứng viên chưa xếp Sprint; v2.0 chưa có kế hoạch chi tiết | `Product_Backlog.xlsx` |
| Ngân sách và hạn nộp | Chưa có ngân sách, hạn nộp hoặc lịch triển khai chính thức trong bộ tài liệu hiện có | PDF và các tài liệu hiện tại |
| Môi trường triển khai | Chưa chốt hệ điều hành, phiên bản Java / MySQL, thư viện giao diện hoặc cách đóng gói | Chưa có cấu hình hoặc mã nguồn ứng dụng |
| Bằng chứng | Các đường dẫn biên bản phỏng vấn và báo cáo Pain Points được Excel dẫn chiếu chưa có trong dự án; không thể xác minh transcript hoặc nội dung từng PP từ các đường dẫn đó | `Interview_Summary`; [interview_overview.md](interview_overview.md) |

## Câu hỏi mở

Các câu hỏi dưới đây phục vụ rà soát tiếp theo; không ngăn việc sử dụng bản tổng quan làm tài liệu tham chiếu hiện trạng.

| ID | Nội dung cần làm rõ | Ảnh hưởng / tham chiếu |
| --- | --- | --- |
| Q-01 | Luồng “Đăng kí tài khoản” trong đề được thực hiện bằng quản trị viên cấp tài khoản hay cần một luồng đăng ký khác? | `RAW-001`, `US-41`, `AS-03`, `OQ-01`; phạm vi tài khoản |
| Q-02 | Thành viên Ban quản trị là vai trò độc lập hay được ánh xạ vào vai trò quản trị? Ai được sửa dữ liệu, sửa / hủy phiếu thu, xem / xuất dữ liệu cá nhân và sao lưu? | `US-05`, `NFR-002`, `AS-04`, `OQ-04`; ma trận quyền |
| Q-03 | Đơn giá dịch vụ / quản lý áp dụng là bao nhiêu; kiot có chính sách riêng không; sửa diện tích hoặc đổi giá ảnh hưởng khoản đã phát hành thế nào? | `RAW-004`, `RAW-011`, `OQ-03`, `OQ-14`; tính phí và lịch sử |
| Q-04 | V1.0 cần mẫu biên lai, danh sách gửi cơ quan chức năng và thông báo thu tiền nào; có in / xuất thông báo trong ứng dụng không? | `RAW-009`, `RAW-014`, `AS-07`, `OQ-06`, `OQ-07`; chứng từ và cung cấp thông tin |
| Q-05 | Cần bổ sung Sprint nào hoặc điều chỉnh phạm vi nào cho 10 story baseline chưa được xếp lịch? | Sheet `Product_Backlog`; khoảng cách giữa baseline 41 story và kế hoạch 31 story |
| Q-06 | Những ứng viên nào trong `US-42`–`US-50` được duyệt, cho phiên bản nào và với tiêu chí nào? | Sheet `PO_Refinement`; mở rộng phạm vi, phụ thuộc và ước lượng |
| Q-07 | Ngưỡng bảo mật, thời gian lưu log, lịch sao lưu, hiệu năng và tiêu chí dễ dùng sẽ được chốt ở mức nào? | `NFR-001`, `NFR-004`–`NFR-007`; tiêu chí kiểm thử và nghiệm thu |
| Q-08 | Đơn vị chính xác của phí ô tô là gì và khi nào lập kế hoạch chi tiết v2.0? | Đề bài trang 3; `RAW-029`, `RAW-030` |
| Q-09 | Số nhóm, mã học phần, lịch Sprint, hạn nộp, môi trường chạy và đầu ra đánh giá chính thức là gì? | Thông tin cần bổ sung từ nhóm hoặc hướng dẫn môn học |

## Nguồn và lưu ý đồng bộ tài liệu

1. [20261 - Chu de BTL.pdf](../Documents/20261%20-%20Chu%20de%20BTL.pdf): trang 1 cho bối cảnh và loại phí; trang 2–3 cho v1.0; trang 3 cho v2.0, nền tảng và luồng nghiệp vụ.
2. [Raw_Requirements.xlsx](../output_dataprocessing/Raw_Requirements.xlsx): các sheet `Client_Wish_List`, `Raw_Requirements`, `NFR`, `Interview_Summary`.
3. [Epic_UserStory.xlsx](../output_dataprocessing/Epic_UserStory.xlsx): các sheet `Epic-Focused User Story Map`, `Epics`, `Features`, `RAW_Review`.
4. [Product_Backlog.xlsx](../output_dataprocessing/Product_Backlog.xlsx): các sheet `Product_Backlog`, `Traceability`, `PO_Refinement`, `Sprint_1`–`Sprint_3`, `Workload_Summary`, `Legend`.
5. [bao-cao-yeu-cau-btl.md](bao-cao-yeu-cau-btl.md) và [interview_overview.md](interview_overview.md): các tài liệu tổng hợp sẵn có.
6. Bản mẫu `F:\01_Project_Overview.md`: tham khảo cấu trúc; các tài liệu `references/…`, `deliverables/…` và `02_Agile_Scrum_Plan.md` được bản mẫu nhắc tới chưa có trong thư mục dự án hiện tại.

**Mốc đồng bộ cần chú ý:** `interview_overview.md`, mục 3.4, và ghi chú của một số RAW bổ sung còn ghi “chưa chuyển thành User Story” hoặc “chưa xuất hiện trong các file 05/06”. Hai bảng `Epic_UserStory.xlsx` và `Product_Backlog.xlsx` hiện đã có `US-42`–`US-50`. Bản tổng quan này ghi nhận trạng thái chi tiết hơn là **đã có story ứng viên và AC dự thảo, chưa được phê duyệt vào baseline hoặc Sprint**. Các nguồn cũ cần được cập nhật ở một lần đồng bộ riêng.

Các tên file nguồn cũ như `05_Epic_UserStory.xlsx` và `05_Epic_UserStory_35.xlsx` trong ghi chú Backlog được giữ trong bảng gốc; đường dẫn tài liệu trong bản tổng quan này trỏ tới các file thực sự có trong dự án. Các mã `OQ`, `AS`, `C` và `PP` là tham chiếu nguồn, chưa có đủ tài liệu định nghĩa riêng để xác minh toàn bộ danh mục.
