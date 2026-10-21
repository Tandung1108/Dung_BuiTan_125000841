NHẬT KÝ PROMPT ENGINEERING (VIBE CODING LOG)

Họ và tên: Bùi Tấn Dũng

MSSV: 125000841

Tên đề tài Website: Website Bán Đồ Công Nghệ CyberTech Store

Công cụ AI đã sử dụng: Gemini (Google AI)

1. Yêu cầu ban đầu (System/Initial Prompt)

"Hãy đóng vai là một lập trình viên Front-End xuất sắc. Tạo cho tôi một trang web bán đồ công nghệ hiện đại tên CyberTech Store theo phong cách Cyberpunk/Neon Futuristic. Website phải tuân thủ chuẩn Semantic HTML5 (header, nav, main, section, article, footer), sử dụng CSS riêng biệt với CSS Variables (:root), Flexbox/Grid responsive. Tích hợp CDN Animate.css và AOS (Animate On Scroll) cho các hiệu ứng xuất hiện cuộn trang sinh động."

2. Quá trình tinh chỉnh & Giải quyết sự cố (Iteration Iterations)

Lần 1: Dựng khung Semantic HTML & Hệ thống CSS Variable

Prompt đã dùng:

"Hãy tạo cấu trúc HTML5 chuẩn Semantic không dùng nhiều div vô nghĩa, phân chia rõ header (chứa logo, nav, search, cart), main (chứa hero, categories, products, deals, newsletter) và footer. Tạo file style.css khai báo hệ thống CSS Variables cho bảng màu Cyberpunk (Cyan, Electric Blue, Neon Pink, Dark BG)."

Kết quả AI tạo ra: Code phân chia thẻ khá chuẩn. Tuy nhiên, AI ban đầu sử dụng các thẻ <div> bọc danh mục sản phẩm thay vì <article>.

Nhận xét & Tinh chỉnh của SV: Yêu cầu AI sửa lại toàn bộ các thẻ sản phẩm và danh mục thành <article> chuẩn ngữ nghĩa SEO & Accessibility.

Lần 2: Tích hợp thư viện Animate.css, AOS & Hiệu ứng Custom CSS

Prompt đã dùng:

"Thêm các thuộc tính data-aos (fade-up, zoom-in, flip-up) vào các section và thẻ sản phẩm. Áp dụng các class Animate.css (animate__pulse, animate__zoomIn) cho logo và Hero Title. Đồng thời bổ sung CSS Glassmorphism, Neon Glow hiệu ứng khi hover card."

Thách thức gặp phải: Ban đầu thư viện AOS không hoạt động do quên thêm đoạn script khởi tạo AOS.init().

Cách sửa prompt (Debug prompt):

"Đoạn code AOS không tự kích hoạt khi cuộn trang. Hãy thêm đoạn Script khởi tạo AOS.init() ở cuối file HTML trước khi đóng thẻ body."

Lần 3: Tinh chỉnh Responsive & Tràn ảnh trên thiết bị di động

Prompt đã dùng:

"Hình ảnh trong section Hero và Sản phẩm bị tràn viền khi màn hình co lại dưới 768px. Hãy sửa lại Media Query trong style.css bằng thuộc tính max-width: 100%, height: auto và dàn lại layout 1 cột cho Mobile."

Kết quả nhận được: Layout chuyển mượt mà về dạng Single-Column trên giao diện thiết bị di động, hình ảnh co giãn fluid tỉ lệ hoàn hảo.

3. Đánh giá cá nhân về quá trình Vibe Coding

AI đã giúp tiết kiệm thời gian ở phần nào nhất?
AI giúp tiết kiệm hơn 70% thời gian viết CSS boilerplate, tra cứu cú pháp animation/effects phức tạp (như Glassmorphism hay Neon Glow shadow) và dựng nhanh cấu trúc Semantic HTML5.

Bài học rút ra khi đặt câu hỏi (Prompt) cho AI trong thiết kế web:

Cần chỉ định rõ ràng kiến trúc mã nguồn (HTML/CSS tách biệt, dùng Semantic tags thay vì div).

Prompt càng cụ thể về Style Guide (CSS Variables, màu sắc, phông chữ) thì kết quả tạo ra càng chuẩn thẩm mỹ.

Cần làm rõ cấu trúc CDN và kịch bản khởi tạo JS để tránh các lỗi animation không hoạt động.