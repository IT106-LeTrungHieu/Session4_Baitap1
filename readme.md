# Bước 1. Tìm lỗi

| Mã US   | Đánh giá & Nhận xét                                                                                                                                                                                                                                                                                                               |
| :------ | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **US1** | **Đạt:** Vai trò rõ, một việc, có lợi ích, thử được bằng cách chọn loại món rồi xem kết quả.                                                                                                                                                                                                                                      |
| **US2** | **Vi phạm Testable:** Tiêu chí "đẹp" và "dễ dùng" mang tính cảm quan cá nhân không thể đo lường. Tester không biết phải dựa vào tiêu chí nào để bấm Done/Pass.                                                                                                                                                                    |
| **US3** | **Vi phạm Valuable:** Không mang lại giá trị cho khách hàng. Khách hàng không quan tâm công nghệ hay code có dễ bảo trì hay không, họ quan tâm giao diện dễ sử dụng.                                                                                                                                                              |
| **US4** | **Vi phạm đồng thời 3 tiêu chí của INVEST:** (1) **Small:** Nhồi nhét quá nhiều tính năng, khó hoàn thành trong Sprint 2–4 tuần; (2) **Independent:** Dồn nhiều tính năng khiến kiểm thử bị phụ thuộc chéo (lỗi gửi email thì xem báo cáo cũng kẹt); (3) **Estimable:** Quá cồng kềnh nên khó ước lượng và chấm điểm Story Point. |

# Bước 2. Sửa lỗi

## a) US2: Là một khách hàng, tôi muốn một giao diện đặt món ăn với hình ảnh trực quan, nút bấm thêm vào giỏ dễ nhìn dễ ấn để tôi có thể đặt món một cách dễ dàng

## b) Viết lại US4

### Epic: Hệ thống quản trị & Báo cáo kinh doanh

### Feature: Báo cáo & phân tích doanh thu đa chiều

### Story:

- 4.1: Là một admin, tôi muốn xem biểu đồ doanh thu lọc theo ngày/tuần/tháng, để nắm bắt tình hình kinh doanh tổng quan
- 4.2: Là một admin, tôi muốn lọc báo cáo doanh thu theo từng khu vực và nhà hàng, để đánh giá hiệu quả từng điểm bán.
- 4.3: Là một admin, tôi muốn xuất dữ liệu báo cáo ra file Excel, để lưu trữ và xử lý số liệu ngoại tuyến.
- 4.4: Là một admin, tôi muốn hệ thống tự động gửi email báo cáo định kỳ hàng tuần cho ban giám đốc, để ban lãnh đạo cập nhật tiến độ mà không cần đăng nhập hệ thống

# Bước 3. Xếp lại Product Backlog

## a) Sắp xếp thứ tự ưu tiên cho các User Story

Danh sách User Story cần sắp xếp:

- **US1:** Lọc nhà hàng theo loại món
- **US2 (Đã sửa):** Giao diện đặt món trực quan, dễ thao tác
- **US4.1 (Tách từ US4):** Xem báo cáo doanh thu theo thời gian, khu vực, nhà hàng
- **US4.2 (Tách từ US4):** Xuất báo cáo Excel và tự động gửi email

---

### Bảng phân loại độ ưu tiên trên Product Backlog:

| Thứ tự |      Mã Story      | Nội dung User Story                                                                                                                                                                                       |     Độ ưu tiên      | Lý do sắp xếp                                                                                                                                                       |
| :----: | :----------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **1**  | **US2** _(Đã sửa)_ | Là một khách hàng, tôi muốn giao diện đặt món hiển thị hình ảnh món ăn trực quan và nút 'Thêm vào giỏ' to rõ ràng, để tôi có thể thao tác hoàn tất đặt món trong vòng dưới 3 lần chạm (hoặc dưới 1 phút). |  **Cao nhất (P1)**  | **Luồng giá trị cốt lõi (Core Value Stream):** Khách hàng phải có giao diện đặt món thuận tiện trước thì hệ thống mới phát sinh đơn hàng và dòng tiền doanh thu.    |
| **2**  |      **US1**       | Là một khách hàng, tôi muốn lọc nhà hàng theo loại món, để nhanh tìm được món muốn ăn.                                                                                                                    |    **Cao (P2)**     | **Tính năng hỗ trợ trải nghiệm người dùng (UX):** Giúp người dùng tìm kiếm món nhanh hơn sau khi luồng đặt món cơ bản đã vận hành tốt.                              |
| **3**  |     **US4.1**      | Là một admin, tôi muốn xem báo cáo doanh thu lọc theo thời gian (ngày/tuần/tháng), theo khu vực và nhà hàng, để nắm bắt tình hình kinh doanh trực quan.                                                   | **Trung bình (P3)** | **Nghiệp vụ quản trị:** Khi hệ thống đã có đơn hàng từ US1 và US2, Admin cần theo dõi số liệu doanh thu trực quan trên hệ thống.                                    |
| **4**  |     **US4.2**      | Là một admin, tôi muốn xuất dữ liệu báo cáo ra file Excel và lên lịch tự động gửi email cho ban giám đốc, để lưu trữ và báo cáo ngoại tuyến tiện lợi.                                                     | **Thấp nhất (P4)**  | **Tính năng nâng cao / Tự động hóa:** Admin vẫn có thể xem số liệu trực tiếp ở US4.1 trước, việc kết xuất file hay gửi mail tự động chưa cấp thiết ở giai đoạn đầu. |

---

## b) Mức độ chi tiết theo DEEP & Hoạt động trong buổi Backlog Refinement

### 1. Mức độ chi tiết của Story đứng đầu (US2) theo tiêu chí DEEP:

Theo nguyên tắc **D (Detailed appropriately)** trong DEEP:

- Story nằm trên đỉnh Product Backlog (chuẩn bị đưa vào Sprint tiếp theo) phải đạt trạng thái **Definition of Ready (DoR)**.
- **Mức độ chi tiết cần đạt được:**
  - **Kích thước nhỏ (Small):** Đã được phân rã đủ nhỏ để hoàn thành trọn vẹn trong một chu kỳ Sprint.
  - **Tiêu chí chấp nhận rõ ràng (Acceptance Criteria - AC):** Phải có các tiêu chí đo lường cụ thể (ví dụ: kích thước tối thiểu nút bấm, hình ảnh tải dưới 1.5s, luồng thêm món không quá 3 bước chạm).
  - **Thiết kế đi kèm:** Đã có Wireframe/UI Prototype (Figma) chi tiết để Dev Team hiểu rõ bố cục và trải nghiệm thao tác.

---

### 2. Các hoạt động cần thực hiện trong buổi Backlog Refinement trước khi đưa vào Sprint:

Trong buổi Refinement (diễn ra giữa Product Owner và Dev Team), nhóm cần thực hiện 4 công việc:

1. **Làm rõ yêu cầu & Tháo gỡ mơ hồ:**
   - Product Owner giải thích chi tiết mục đích nghiệp vụ của US2.
   - Dev Team trao đổi, đặt câu hỏi về mặt kỹ thuật, trải nghiệm người dùng để xóa bỏ điểm chưa rõ ràng.
2. **Thống nhất Tiêu chí Chấp nhận (Acceptance Criteria - AC):**
   - Đội ngũ Dev và Tester cùng PO chốt danh sách các kịch bản kiểm thử (test cases) cụ thể mà tính năng phải vượt qua.
3. **Ước lượng kích thước (Estimating):**
   - Toàn bộ Dev Team tiến hành đánh giá độ phức tạp và chấm điểm Story Points (thông qua phương pháp Planning Poker).
4. **Rà soát Definition of Ready (DoR):**
   - Kiểm tra xem Story đã thỏa mãn đầy đủ các điều kiện tiên quyết (DoR) để chính thức sẵn sàng đưa vào buổi họp **Sprint Planning** hay chưa.ước 3.
