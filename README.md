# GROUP 7: XÂY DỰNG GIAO DIỆN ỨNG DỤNG AUDIO BOOK
## https://www.figma.com/design/Bs7SqlTbnSeO8yCWAe1D8j/KTMP_GROUP_7?node-id=0-1&t=BshrU64vkGtStRRx-1
## Giới Thiệu Dự Án
- Ứng dụng Audio Book là một giao diện người dùng thân thiện, hiện đại giúp người dùng dễ dàng tìm kiếm những loại sách, chọn những cuốn sách tri thức hấp dẫn, có thể nghe thời gian rảnh, khi chuẩn bị đi ngủ và kể cả khi bạn đang làm việc. Giúp bạn giảm áp lực trong công việc học tập và làm việc hiệu quả
- Dự án này tập trung vào thiết kế giao diện người dùng (UI/UX) trên Figma nhằm mô phỏng trải nghiệm nghe kể chuyện như các ứng dụng phổ biến hiện nay.
## Giới thiệu thành viên:


| Thành viên nhóm       | Mã sinh viên | Email                           | Đóng góp |
|-----------------------|--------------|---------------------------------|----------|
| Bùi Thanh Tuân        | 23010569     | 23010569@st.phenikaa-uni.edu.vn | 100%     |
| Đặng Đắc Tú           | 23010619     | 23010619@st.phenikaa-uni.edu.vn | 100%     |
| Đỗ Tiến Hải           | 23010615     | 23010615@st.phenikaa-uni.edu.vn | 100%     |

## 1. Bảng phân chia công việc chi tiết theo tuần:
| Thành viên            | Tuần 1 (Phân tích yêu cầu)                                              | Tuần 2 (Thiết kế Use‑case & Flow)                                           | Tuần 3 (Thiết kế hướng đối tượng)                                                  | Tuần 4 (UI Flow & Prototype)                                   | Tuần 5 (Hoàn thiện & Đánh giá)                                                   |
|-----------------------|---------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------|
| **Bùi Thanh Tuân** | - Thu thập yêu cầu<br>- Xác định actors & chức năng chính                 | - Phân tích chức năng theo actor<br>- Vẽ Use‑case diagram<br>- Mô tả chi tiết từng use‑case | - Xác định class chính và thuộc tính<br>- Thiết kế quan hệ giữa các class (UML)     | - Liên kết màn hình, thiết lập điều hướng (Prototype)         | - Tổng hợp phản hồi<br>- Chạy test UI flow<br>- Ghi nhận và sửa lỗi trong prototype |
| **Đặng Đắc Tú**  | - Nghiên cứu người dùng & kịch bản thực tế                                | - Chọn flow diagram (Sequence hoặc Activity)<br>- Vẽ sơ đồ flow              | - Viết đặc tả phương thức các class (method signatures)                             | - Bố trí layout chính, style guide trên Figma                | - Đánh giá ưu/nhược điểm<br>- Ghi nhận lỗi<br>- Đề xuất cải tiến tính năng            |
| **Đỗ Tiến Hải**  | - Tham khảo ứng dụng tương tự<br>- Soạn thảo đề bài toán                   | - Chuẩn hóa sơ đồ Use‑case                                                    | - Chuẩn hóa sơ đồ Class                                                              | - Vẽ UI flow diagram (Wireflow)                              | - Viết phần đánh giá<br>- Báo cáo kết quả                                            |
## 2. Phân tích yêu cầu:
### 2.1. Đặt vấn đề bài toán
Trong bối cảnh nhu cầu học tập và giải trí thông qua hình thức **nghe sách nói (audio book)** ngày càng phổ biến, việc phát triển một ứng dụng nghe sách trực tuyến tiện lợi, dễ sử dụng và thân thiện với người dùng là rất cần thiết.

Hệ thống của nhóm chúng tôi cho phép người dùng:
- Đăng ký / Đăng nhập tài khoản
- Duyệt danh sách sách nói theo thể loại, tác giả, độ phổ biến
- Nghe thử hoặc nghe toàn bộ sách nói
- Đánh dấu sách yêu thích, thêm vào danh sách cá nhân
- Tùy chỉnh tốc độ phát, chế độ nghe nền
- Quản lý nội dung sách nói (dành cho Admin)

Mục tiêu của hệ thống:
- Tối ưu trải nghiệm người dùng
- Mang lại phương thức tiếp cận tri thức hiện đại
- Đảm bảo tính ổn định, bảo mật và dễ mở rộng.

### 2.2. Tác nhân, người dùng
| Tác nhân                    | Mô tả                                                                 |
|-----------------------------|------------------------------------------------------------------------|
| **Người dùng (User)**       | Đăng ký/Đăng nhập, duyệt sách nói, nghe sách, quản lý danh sách yêu thích |
| **Quản trị viên (Admin)**   | Quản lý nội dung sách nói, thể loại, tác giả, tài khoản người dùng      |

### 2.3. Chức năng & Phân tích chức năng (theo tác nhân)

- **Người dùng (User)**  
1. Đăng ký / Đăng nhập  
2. Duyệt danh sách sách nói theo thể loại, từ khóa  
3. Xem thông tin chi tiết sách nói (tên, tác giả, mô tả, độ dài, số chương, ảnh bìa, đánh giá)  
4. Nghe thử / nghe toàn bộ nội dung sách  
5. Thêm sách vào danh sách yêu thích  
6. Tùy chỉnh tốc độ phát, chế độ nghe nền  
7. Quản lý danh sách cá nhân (xóa hoặc thêm sách)  

- **Quản trị viên (Admin)**  
1. Quản lý nội dung sách nói: Thêm/sửa/xóa sách  
2. Quản lý thể loại, tác giả  
3. Quản lý tài khoản người dùng  
4. Theo dõi thống kê lượt nghe / lượt yêu thích  
5. Kiểm duyệt nội dung sách nói

## 3. Đặc tả và thiết kế
### 3.1. Use case + Mô tả

#### 3.1.1 Mô tả
1. **UC1: Đăng ký / Đăng nhập**  
   - **Actor:** User  
   - **Mô tả:** Cho phép người dùng tạo tài khoản mới hoặc đăng nhập để truy cập các tính năng của hệ thống.

2. **UC2: Duyệt sách nói**  
   - **Actor:** User  
   - **Mô tả:** Xem danh sách sách nói, tìm kiếm theo thể loại, tên sách hoặc tác giả.

3. **UC3: Nghe sách nói**  
   - **Actor:** User  
   - **Mô tả:** Phát nội dung sách nói, có thể điều chỉnh tốc độ, tua nhanh/chậm, nghe nền.

4. **UC4: Quản lý danh sách yêu thích**  
   - **Actor:** User  
   - **Mô tả:** Thêm hoặc xóa sách khỏi danh sách cá nhân để dễ dàng truy cập lại sau.

5. **UC5: Quản lý nội dung sách nói**  
   - **Actor:** Admin  
   - **Mô tả:** Thực hiện CRUD nội dung sách nói, thể loại, tác giả.

6. **UC6: Quản lý người dùng & thống kê**  
   - **Actor:** Admin  
   - **Mô tả:** Quản lý tài khoản người dùng, xem thống kê lượt nghe, lượt yêu thích, báo cáo.
   
### 3.1.2. Sơ đồ diagram Use-case User:
