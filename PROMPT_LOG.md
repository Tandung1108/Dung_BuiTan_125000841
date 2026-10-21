# NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

- **Họ và tên:** Bùi Tấn Dũng
- **MSSV:** 125000841
- **Tên đề tài Website:** Website Bán Đồ Công Nghệ CyberTech (CyberTech Store)
- **Công cụ AI đã sử dụng:** Gemini (Google AI)

---

## 1. Yêu cầu ban đầu (System/Initial Prompt)

> *"là một lập trình viên hãy tạo cho tôi một trang web bán đồ công nghệ xịn xò viết code theo tất cả các yêu cầu đã cho YÊU CẦU KỸ THUẬT VÀ KHUNG TỐI THIỂU CỦA WEBSITE..."*

---

## 2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

### Lần 1: Dựng khung Semantic HTML5 & CSS Variables
- **Prompt đã dùng:**
  > *"Hãy tạo cấu trúc HTML5 chuẩn Semantic và file CSS riêng biệt cho trang web bán đồ công nghệ CyberTech gồm: Header, Hero Section, Categories, Products, Deals và Footer. Sử dụng CSS Variables trong `:root` và layout Flexbox/Grid."*
- **Kết quả AI tạo ra:** 
  AI đã khởi tạo thành công cấu trúc web đẹp mắt với phong cách Cyberpunk, sử dụng chuẩn các thẻ ngữ nghĩa `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>` và hệ thống biến màu sắc trong `:root`.
- **Nhận xét & Tinh chỉnh của SV:** 
  Giao diện sinh ra đẹp nhưng AI có chèn thêm một số đoạn mã JavaScript (CDN `aos.js`, `AOS.init()`, và `onsubmit="event.preventDefault();"`).

---

### Lần 2: Yêu cầu loại bỏ 100% JavaScript nhưng vẫn giữ nguyên giao diện xịn xò
- **Prompt đã dùng:**
  > *"ní ơi làm lại code html và css không có js nha ní nhưng vẫn phải đáp ứng đủ tiêu chí và yêu cầu tôi đưa ban đầu nha"*
- **Kết quả AI tạo ra:**
  AI đã chuyển đổi mã nguồn thành 100% HTML5 & CSS3 thuần (Zero JS):
  1. Loại bỏ toàn bộ thẻ `<script>`, file `.js` bên ngoài và các sự kiện inline JS.
  2. Thay thế Menu Mobile bằng kỹ thuật **Pure CSS Checkbox Hack** (`<input type="checkbox">` + `:checked`).
  3. Thay thế thư viện AOS bằng **Hiệu ứng cuộn trang thuần CSS (`animation-timeline: view()`)** và các `@keyframes` mượt mà.
  4. Giữ nguyên cấu trúc Semantic HTML5, CSS Variables và Animate.css.
- **Nhận xét & Tinh chỉnh của SV:**
  Trang web hoạt động cực kỳ mượt mà, phản hồi tốt trên di động, đúng quy định cấm dùng JS của bài thi.

---

### Lần 3: Tích hợp Form Mua Hàng Nhập Thông Tin Thật (100% Pure CSS & Formspree)
- **Prompt đã dùng:**
  > *"ní ơi thêm code vào html và css để chạy trên web và có thể mua hàng nhập thông tin thật sự"*
- **Kết quả AI tạo ra:**
  1. Bổ sung các nút **"Mua Ngay"** trên từng thẻ sản phẩm và giỏ hàng.
  2. Xây dựng **Cửa sổ Pop-up (Checkout Modal)** nhập thông tin mua hàng gồm: Chọn sản phẩm, Họ tên, Số điện thoại, Email, Địa chỉ, Phương thức thanh toán và Ghi chú.
  3. Áp dụng kỹ thuật **Pure CSS `:target` Hack** để đóng/mở Pop-up mượt mà mà **KHÔNG DÙNG JAVASCRIPT**.
  4. Tích hợp endpoint `Formspree` (`action="https://formspree.io/f/..."`) giúp Form thu thập và gửi dữ liệu đặt hàng thật 100% về Email của chủ shop.
- **Nhận xét & Tinh chỉnh của SV:**
  Website vừa đáp ứng hoàn hảo yêu cầu kỹ thuật không JS của bài thi, vừa có tính thực tế cao khi có thể đặt hàng thật.

---

## 3. Đánh giá cá nhân về quá trình Vibe Coding

- **AI đã giúp bạn tiết kiệm thời gian ở phần nào nhất?**
  AI giúp tiết kiệm hơn 80% thời gian trong việc dựng khung HTML Semantic chuẩn, viết hệ thống CSS Variables phức tạp, phối màu Dark Mode Cyberpunk / Glassmorphism và xử lý Responsive Media Queries cho đa dạng kích thước màn hình.

- **Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web?**
  1. **Đặt câu hỏi rõ ràng và có ràng buộc (Constraints):** Khi cần cấm dùng JS, phải nhắc AI rõ ràng để AI chuyển sang các giải pháp sáng tạo bằng CSS thuần (như Checkbox Hack, CSS `:target`, CSS Scroll Animations).
  2. **Tư duy tinh chỉnh từng bước (Iteration):** Không nên bắt AI làm tất cả trong 1 bước, mà nên đi từ dựng khung, phối màu CSS, sau đó bổ sung tính năng mua hàng thật và tinh chỉnh theo đúng tiêu chí chấm điểm.