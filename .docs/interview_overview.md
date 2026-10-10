# Tổng quan phỏng vấn thu thập yêu cầu — BlueMoon

**Nguồn:** [Raw_Requirements.xlsx](../output_dataprocessing/Raw_Requirements.xlsx), gồm các sheet `Interview_Summary`, `Client_Wish_List`, `Raw_Requirements` và `NFR`. Tài liệu tổng hợp dữ liệu giả lập đã có; không ghi nhận kết quả phỏng vấn thực tế hoặc bổ sung nội dung hỏi đáp.

## 1. Tổng quan phỏng vấn

Hoạt động thu thập yêu cầu (Requirement Elicitation) nhằm nhận diện khó khăn, mong muốn và ràng buộc của các nhóm liên quan trong bài toán quản lý thu phí và hộ dân BlueMoon. Kết quả cung cấp đầu vào có khả năng truy vết cho việc phân tích phạm vi, Epic, User Story và Product Backlog.

**Phương pháp được ghi nhận là Simulated Interview / Role-play:** nhóm thực hiện đóng vai các stakeholder dựa trên bối cảnh đề bài BlueMoon, kết hợp phân tích tài liệu và các câu hỏi tình huống bổ sung. Theo ghi chú tại `Interview_Summary!A9:A14`, toàn bộ đầu vào là giả lập; **không có phỏng vấn, khảo sát hoặc quan sát thực tế**. Các tham chiếu `SIM-INT-...`, `SIM-SCEN-01-...`, `PS-01`, `PS-02` và `DA-02` là mã nguồn nội bộ được Excel nêu; không phải bằng chứng thu thập từ người tham gia thực tế. `DA-02` được ghi nhận gắn với giả định.

Phạm vi đối chiếu gồm `Interview_Summary!A1:H6`, `Client_Wish_List!A2:G36`, `Raw_Requirements!A2:I36` và `NFR!A2:G9`. Các biên bản và báo cáo Pain Points được Excel dẫn chiếu chưa có trong dự án tại thời điểm lập tài liệu; vì vậy, số câu hỏi được trình bày theo sheet tổng hợp, chưa được kiểm chứng bằng transcript.

## 2. Các chủ thể được phỏng vấn

### 2.1. Bốn cuộc phỏng vấn giả lập

Mục đích trong bảng được tổng hợp từ các Wish và RAW liên quan; stakeholder là vai trò giả lập, không phải danh sách người tham gia thực tế.

| Interview ID | Stakeholder | Số câu hỏi | Mục đích phỏng vấn | Đường dẫn biên bản được ghi trong Excel |
| --- | --- | ---: | --- | --- |
| `SIM-INT-BQT` | Đại diện Ban quản trị (BQT), cấp quyết định | 12 | Làm rõ quản lý hộ, nhân khẩu, khoản thu, thống kê, quyền truy cập, truy vết và sao lưu; nhận diện nhu cầu v2.0. | `docs/interviews/01_Ban_Quan_Tri_Interview.md` |
| `SIM-INT-TQ` | Thủ quỹ / người thu phí (TQ) | 12 | Làm rõ tính phí, ghi nhận nộp tiền, biên lai, xử lý sai sót, công nợ, tra cứu và thao tác thu phí. | `docs/interviews/02_Thu_Quy_Interview.md` |
| `SIM-INT-CD` | Chủ hộ / cư dân (CD) | 12 | Làm rõ tính minh bạch của chứng từ, đóng góp tự nguyện, cập nhật cư trú, quyền riêng tư và nhu cầu tự tra cứu, nhận nhắc phí. | `docs/interviews/03_Cu_Dan_Interview.md` |
| `SIM-INT-CQ` | Đại diện cơ quan chức năng (CQ), vai trò chung | 12 | Làm rõ cung cấp danh sách hộ, nhân khẩu, lịch sử cư trú và báo cáo theo thời điểm, theo đợt đóng góp. | `docs/interviews/04_Co_Quan_Chuc_Nang_Interview.md` |

Cả bốn đường dẫn trên **chưa tìm thấy trong dự án**. Chúng được giữ nguyên để truy vết nguồn, không được xem là biên bản đã đọc hoặc đã xác minh.

### 2.2. Câu hỏi tình huống bổ sung

`SIM-SCEN-01` gồm **5 câu hỏi tình huống giả lập** liên quan BQT, TQ và CD, được tham chiếu bằng `SIM-SCEN-01-01` đến `SIM-SCEN-01-05`. Nội dung chỉ có trong các sheet `Client_Wish_List` và `Raw_Requirements`; Excel ghi rõ **không có biên bản riêng**, chưa xác nhận và không gán PP ID.

Như vậy, dữ liệu gồm **4 cuộc phỏng vấn × 12 = 48 câu hỏi**, cộng **5 câu hỏi tình huống**, tổng cộng **53 câu hỏi theo Excel**. `SIM-SCEN-01` không phải cuộc phỏng vấn thứ năm.

## 3. Tổng hợp kết quả

### 3.1. Vấn đề và mong muốn theo stakeholder

Các vấn đề dưới đây được tổng hợp từ `Statement`, `Raw Requirement` và `Rationale`. PP ID chỉ thể hiện liên hệ với nhóm stakeholder theo `Interview_Summary`; **không ánh xạ từng mô tả vấn đề sang một PP ID cụ thể**, vì tài liệu định nghĩa PP tại `docs/04_Interview_Report.md` chưa có trong dự án.

| Nhóm | Vấn đề chính được phản ánh trong dữ liệu giả lập | Mong muốn chính và Wish ID | PP ID theo sheet tổng hợp |
| --- | --- | --- | --- |
| BQT | Dữ liệu hộ và nhân khẩu cần tập trung; tổng hợp thu phí còn thủ công; thay đổi dữ liệu thiếu dấu vết; lo mất dữ liệu và quyền truy cập chưa rõ. | Quản lý hộ, nhân khẩu, khoản thu, thống kê, tài khoản, phân quyền, truy vết và sao lưu: `WISH-01`–`WISH-08`. Gửi xe và thu hộ dịch vụ ở v2.0: `WISH-09`, `WISH-10`. | `PP-01`, `PP-02`, `PP-03`, `PP-05`, `PP-07` |
| TQ | Tính phí thủ công dễ sai; ghi sổ rồi nhập lại Excel; khó xử lý nộp thiếu, nộp gộp và giao dịch nhầm; biên lai viết tay chậm; tra cứu, đối chiếu mất thời gian. | Tự tính phí, ghi nhận một lần, theo dõi công nợ, in biên lai, xử lý sai sót, tìm kiếm nhanh và ít thao tác: `WISH-11`–`WISH-19`. | `PP-02`, `PP-03`, `PP-04`, `PP-05`, `PP-06` |
| CD | Chứng từ cần rõ cách tính; lo bị nhắc nợ với khoản tự nguyện, thông tin cư trú sai và lộ dữ liệu cá nhân; có nhu cầu tự tra cứu, nhận nhắc phí. | Chứng từ minh bạch, đóng góp đúng tính tự nguyện, cập nhật cư trú và bảo vệ thông tin: `WISH-20`–`WISH-23`. Tra cứu trên điện thoại và nhắc phí: `WISH-24`, `WISH-25`, ngoài v1.0. | `PP-03`, `PP-06`, `PP-08`, `PP-09`, `PP-10` |
| CQ | Danh sách phải gom thủ công; cần dữ liệu cư trú có thời hạn, lịch sử có ngày và số liệu thống kê theo thời điểm. | Cung cấp, tra cứu danh sách; lưu tình trạng và biến động cư trú; báo cáo dân cư, đóng góp: `WISH-26`–`WISH-30`. | `PP-07`, `PP-09` |

Liên hệ Wish–RAW được trình bày ở các bảng tiếp theo. Một RAW có thể phục vụ nhiều stakeholder; không cộng số RAW của từng cuộc phỏng vấn để tính tổng yêu cầu duy nhất.

### 3.2. Các nhóm yêu cầu chức năng (FR)

Bảng dưới tổng hợp **23 FR có nguồn từ bốn cuộc phỏng vấn**. Wish ID được đối chiếu theo cột `Related RAW`; một Wish có thể xuất hiện ở nhiều nhóm.

| Nhóm FR | Nội dung chính | RAW ID | Wish ID liên quan | Phạm vi ghi nhận |
| --- | --- | --- | --- | --- |
| Tài khoản và truy cập | Đăng nhập bằng tài khoản được cấp; đổi mật khẩu, cập nhật thông tin cá nhân. | `RAW-001`–`RAW-002` | `WISH-01` | v1.0 |
| Quản lý hộ gia đình | Lưu tập trung, tránh trùng căn hộ; xem, sửa thông tin; đổi chủ hoặc ngừng cư trú vẫn giữ lịch sử. | `RAW-003`–`RAW-005` | `WISH-02` | v1.0 |
| Quản lý nhân khẩu | Quản lý thành viên, biến động theo thời gian, tạm trú/tạm vắng; xuất hoặc in danh sách khi có yêu cầu. | `RAW-006`–`RAW-009` | `WISH-03`, `WISH-22`, `WISH-26`–`WISH-28` | v1.0 |
| Quản lý khoản thu | Quản lý khoản thu, đơn giá; tính phí theo diện tích; phân biệt đóng góp tự nguyện với phí bắt buộc. | `RAW-010`–`RAW-012` | `WISH-04`, `WISH-11`, `WISH-20`, `WISH-21`, `WISH-30` | v1.0 |
| Thu phí | Ghi nhận nộp tiền, nộp một phần hoặc gộp; in/xuất biên lai; xử lý giao dịch ghi nhầm. | `RAW-013`–`RAW-015` | `WISH-06`, `WISH-12`–`WISH-15`, `WISH-20` | v1.0 |
| Tra cứu và thống kê | Tìm hộ, nhân khẩu; tra cứu lịch sử và công nợ; thống kê thu, hộ còn thiếu và dân cư theo thời điểm. | `RAW-016`–`RAW-021` | `WISH-05`, `WISH-13`, `WISH-16`–`WISH-18`, `WISH-21`, `WISH-26`, `WISH-29`, `WISH-30` | v1.0 |
| Mở rộng v2.0 | Quản lý phí gửi xe; thu hộ điện, nước, internet theo thông báo của nhà cung cấp. | `RAW-029`–`RAW-030` | `WISH-09`, `WISH-10` | Roadmap v2.0; Won't-have v1.0 |

`WISH-24` và `WISH-25` được lưu để theo dõi nhu cầu ngoài v1.0, **không có RAW tương ứng trong cột `Related RAW`**. Theo Excel, nhu cầu của cư dân trong v1.0 được thực hiện qua BQT; danh sách `RAW-020` hỗ trợ nhắc thủ công, không đồng nghĩa với chức năng gửi nhắc tự động.

### 3.3. Các nhóm yêu cầu phi chức năng (NFR)

Giữ nguyên cách phân loại FR/NFR trong Excel, bao gồm phân quyền và truy vết. Bảy NFR đầu có nguồn phỏng vấn giả lập; NFR cuối có nguồn tình huống bổ sung.

| NFR ID / RAW ID | Nhóm và nội dung chính | Wish ID liên quan | Giới hạn hoặc điểm cần xác nhận |
| --- | --- | --- | --- |
| `NFR-001` / `RAW-022` | Bảo mật: băm mật khẩu, giới hạn đăng nhập sai liên tiếp. | `WISH-01` | Ngưỡng số lần sai là giả định, cần xác nhận. |
| `NFR-002` / `RAW-023` | Phân quyền: phân biệt quản trị và người thu phí, giới hạn thao tác theo trách nhiệm. | `WISH-08`, `WISH-23` | Mức phân quyền chưa chốt: `OQ-04`, `AS-04`, `C-01`. |
| `NFR-003` / `RAW-024` | Quyền riêng tư: che bớt số giấy tờ; giới hạn xem đầy đủ và xuất dữ liệu. | `WISH-23` | Dữ liệu giấy tờ, thẩm quyền cần xác nhận: `OQ-08`, `C-03`; demo dùng dữ liệu mẫu theo `AS-10`. |
| `NFR-004` / `RAW-025` | Truy vết: ghi người, thời điểm, thao tác, dữ liệu trước/sau và lần xuất dữ liệu; không sửa/xóa log qua giao diện. | `WISH-06`, `WISH-15` | Thời gian lưu log chưa rõ: `OQ-11`. |
| `NFR-005` / `RAW-026` | Độ tin cậy: sao lưu và khôi phục tự động hoặc bằng một thao tác. | `WISH-07` | Tần suất mặc định hằng ngày là giả định. |
| `NFR-006` / `RAW-027` | Hiệu năng: tìm kiếm, hiển thị danh sách tối đa 3 giây với vài trăm hộ, vài nghìn nhân khẩu, 2–3 người dùng đồng thời. | `WISH-19` | Các ngưỡng và quy mô là giả định: `AS-13`, `OQ-10`. |
| `NFR-007` / `RAW-028` | Khả năng sử dụng: giao diện tiếng Việt, tiền VND dễ đọc, lỗi rõ ràng, khoảng 5 thao tác chính cho một lần thu. | `WISH-19` | Số thao tác là giả định, chưa phải tiêu chí nghiệm thu đã thống nhất. |
| `NFR-008` / `RAW-035` | Toàn vẹn dữ liệu: tránh tạo hai phiếu thu khi lưu lặp hoặc bị gián đoạn; lần thử lại cho biết kết quả đã ghi nhận. | `WISH-35` | Nhu cầu bổ sung chưa xác nhận; cần xác định giao dịch duy nhất và tiêu chí kiểm thử. |

### 3.4. Các yêu cầu từ tình huống bổ sung chưa xác nhận

| Tham chiếu tình huống | Wish ID | RAW ID / loại | Nội dung cần làm rõ trước khi đặc tả |
| --- | --- | --- | --- |
| `SIM-SCEN-01-01` | `WISH-31` | `RAW-031` / FR | Miễn, giảm phí: khoản được giảm, mức giảm, thẩm quyền, thời hạn và xử lý khoản phải thu đã phát hành. |
| `SIM-SCEN-01-02` | `WISH-32` | `RAW-032` / FR | Công nợ khi đổi chủ: trách nhiệm chủ cũ/chủ mới, ngày hiệu lực và thỏa thuận riêng; liên quan `RAW-005`, `RAW-018`. |
| `SIM-SCEN-01-03` | `WISH-33` | `RAW-033` / FR | Chuyển khoản chưa xác định: người đối soát, bằng chứng và nguyên tắc ghép giao dịch; chưa mặc định tích hợp API ngân hàng. |
| `SIM-SCEN-01-04` | `WISH-34` | `RAW-034` / FR | Kết sổ: định nghĩa ca/ngày, phân tách tiền mặt/chuyển khoản, xác nhận chênh lệch và hoàn tiền; liên quan `RAW-013`, `RAW-019`. |
| `SIM-SCEN-01-05` | `WISH-35` | `RAW-035` / NFR; `NFR-008` | Tránh ghi nhận trùng: cách nhận diện một lần nộp, hành vi thử lại và tiêu chí kiểm thử. |

Cả năm Wish có `Scope = Chưa chốt`, không có PP ID. Ghi chú Excel cho biết nhóm bổ sung chưa được bên liên quan xác nhận và chưa xuất hiện trong các file 05/06; không xem chúng là User Story, DoD hoặc cam kết phát triển đã hoàn tất.

### 3.5. Các vấn đề còn mở và giả định

Các mã dưới đây được giữ theo tham chiếu trong Excel. Chưa có tài liệu riêng để kiểm chứng đầy đủ danh mục `OQ`, `AS` và `C`; bảng chỉ nêu nội dung được các ô dữ liệu mô tả.

| Chủ đề | Nội dung chưa rõ hoặc giả định cần xác nhận | Mã truy vết |
| --- | --- | --- |
| Tài khoản và quyền hạn | Giả định dùng tài khoản cấp sẵn, không tự đăng ký; cần chốt quy trình cấp tài khoản, tài khoản dùng chung và quyền từng vai trò. | `RAW-001`, `RAW-023`; `AS-03`, `AS-04`, `OQ-01`, `OQ-04`, `C-01` |
| Chính sách phí và điều chỉnh | Chưa chốt miễn/giảm, cách tính cho kiot, phạt chậm nộp/nộp trước và tính lại khi sửa diện tích hoặc giao dịch. Phí ô tô ở v2.0 cần xác nhận. | `RAW-004`, `RAW-011`, `RAW-013`, `RAW-015`, `RAW-029`, `RAW-031`; `AS-14`, `OQ-02`, `OQ-03`, `OQ-05`, `OQ-14`, `C-02` |
| Chứng từ và cung cấp dữ liệu | Chưa chốt mẫu biên lai, thông báo thu, mẫu danh sách và trường dữ liệu gửi CQ; thông báo và đóng dấu được đặt ngoài hệ thống theo giả định. | `RAW-009`, `RAW-011`, `RAW-014`; `OQ-06`, `OQ-07`, `AS-07`, `AS-16` |
| Nhân khẩu và dữ liệu cá nhân | Cần xác nhận trường dữ liệu, việc lưu số giấy tờ, loại biến động và quyền xem/xuất. Không xóa cứng dữ liệu cũ là giả định được ghi nhận. | `RAW-005`–`RAW-008`, `RAW-024`; `AS-17`, `AS-18`, `OQ-08`, `OQ-13`, `C-03` |
| Dữ liệu ban đầu và hình thức nộp | Dữ liệu cũ do BQT nhập là giả định; hỗ trợ nhập dữ liệu cũ ngoài phạm vi. Hình thức nộp chỉ để ghi nhận, chưa chốt chi tiết xử lý thanh toán. | `WISH-02`, `RAW-003`, `RAW-013`; `AS-08`, `AS-12`, `OQ-09`, `OQ-12`, `C-08` |
| Chỉ tiêu chất lượng | Cần chốt ngưỡng đăng nhập sai, tần suất sao lưu, thời gian lưu log, quy mô, thời gian phản hồi và số thao tác. | `RAW-022`, `RAW-025`–`RAW-028`; `NFR-001`, `NFR-004`–`NFR-007`; `AS-13`, `OQ-10`, `OQ-11` |
| Ranh giới phạm vi | Cư dân tự tra cứu trên điện thoại và nhắc phí tự động ngoài v1.0; đóng góp tự nguyện không được coi là nợ; thống kê hiện chỉ ở mức cơ bản, chưa gồm biểu đồ. | `WISH-24`, `WISH-25`, `RAW-012`, `RAW-019`, `RAW-020`; `AS-02`, `AS-07`, `AS-19`, `C-04`–`C-07` |

Các mục Must/Should/Won't-have trong `Notes` là **ưu tiên MoSCoW sơ bộ**. Nhãn v1.0 và roadmap mô tả phạm vi ghi trong dữ liệu giả lập, không chứng minh đã được stakeholder thực tế phê duyệt.

## 4. Kết quả đầu ra của quá trình thu thập yêu cầu

### 4.1. Số lượng và phạm vi

Đếm theo mã định danh duy nhất; không tính dòng tiêu đề hoặc ghi chú.

| Nguồn đầu vào | Wish | Raw Requirements | FR trong RAW | NFR trong RAW / sheet NFR |
| --- | ---: | ---: | ---: | ---: |
| Bốn cuộc phỏng vấn giả lập: `WISH-01`–`WISH-30`, `RAW-001`–`RAW-030` | 30 | 30 | 23 | 7 |
| Tình huống bổ sung: `WISH-31`–`WISH-35`, `RAW-031`–`RAW-035` | 5 | 5 | 4 | 1 |
| **Tổng cộng** | **35** | **35** | **27** | **8** |

Sheet `NFR` có **8 bản ghi**, gồm `NFR-001`–`NFR-007` liên kết `RAW-022`–`RAW-028`, và `NFR-008` liên kết `RAW-035`. Đây là phần mô tả chi tiết của **cùng 8 NFR trong RAW**, không cộng thêm vào tổng 35 yêu cầu.

- **Wish theo phạm vi:** 26 thuộc v1.0; 2 thuộc roadmap v2.0 (`WISH-09`, `WISH-10`); 2 ngoài v1.0 và không có RAW tương ứng (`WISH-24`, `WISH-25`); 5 chưa chốt (`WISH-31`–`WISH-35`). Tổng: **26 + 2 + 2 + 5 = 35**.
- **RAW theo phạm vi ghi nhận:** v1.0 có 28 yêu cầu, gồm 21 FR và 7 NFR; roadmap v2.0 có 2 FR; tình huống chưa chốt có 4 FR và 1 NFR. Tổng: **28 + 2 + 5 = 35**; **27 FR + 8 NFR = 35**.

### 4.2. Chuyển đầu vào phỏng vấn thành Wish và RAW

`Client_Wish_List` lưu mong muốn theo stakeholder, câu phát biểu, mã nguồn phỏng vấn, RAW liên quan, phạm vi và ghi chú. `Raw_Requirements` diễn đạt nhu cầu thành yêu cầu ban đầu, bổ sung loại FR/NFR, lý do, bằng chứng, artefact đích dự kiến và vấn đề cần xác nhận. Sheet `NFR` mô tả chi tiết các yêu cầu chất lượng đã phân loại trong RAW.

Ví dụ, `SIM-INT-TQ-Q03` và `SIM-INT-TQ-Q10` được ghi làm nguồn cho `WISH-11` về tính phí theo diện tích, liên kết `RAW-011`. Ngược lại, `RAW-011` đồng thời liên kết `WISH-04` và `WISH-20`; `WISH-20` liên kết cả `RAW-011` và `RAW-014`. Vì vậy, **Wish–RAW là quan hệ nhiều–nhiều**; hai danh mục cùng có 35 bản ghi không có nghĩa là ánh xạ một–một.

### 4.3. Vai trò trong phân tích và xây dựng backlog

| Bước tiếp theo | Vai trò của dữ liệu thu thập |
| --- | --- |
| Phân tích Epic | Nhóm nhu cầu theo `Target Artefact`: tài khoản và truy cập, hộ gia đình, nhân khẩu, khoản thu, thu phí, tra cứu và thống kê; giữ riêng mở rộng v2.0. Đây là định hướng Epic dự kiến trong Excel. |
| Phân tích User Story | Dùng stakeholder, mong muốn và RAW để xác định mục tiêu, quy tắc nghiệp vụ, tiêu chí chấp nhận và phụ thuộc; xác nhận các vấn đề còn mở trước khi chốt đặc tả. Các yêu cầu tình huống bổ sung cần được làm rõ trước khi chuyển thành User Story hoặc DoD. |
| Xây dựng Product Backlog | Duy trì liên kết nguồn phỏng vấn → Wish → RAW → artefact; phân biệt v1.0, roadmap, ngoài phạm vi và chưa chốt; rà soát lại ưu tiên sơ bộ. NFR có thể được xử lý qua NFR, Technical Story hoặc DoD theo `Target Artefact`, sau khi xác nhận tiêu chí. |

**Kiểm tra tính nhất quán:** các danh mục Wish, RAW và NFR không có mã trùng; tham chiếu Wish/RAW của cả bốn cuộc phỏng vấn và nhóm tình huống trong `Interview_Summary` khớp các cột nguồn ở sheet chi tiết; mọi `Related RAW` có mã đều tồn tại; tám NFR đều liên kết RAW được phân loại NFR. Giới hạn còn lại là thiếu biên bản và tài liệu định nghĩa PP, nên chưa thể kiểm chứng nội dung hỏi đáp hoặc diễn giải riêng từng PP ID.
