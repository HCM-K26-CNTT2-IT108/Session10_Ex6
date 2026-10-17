# Bài 6 Sự cố tài liệu dự án trên GitHub

## Phần 1 Phân tích

Nam đã chọn định dạng không phù hợp cho tài liệu dự án cần đọc trực tiếp trên GitHub và theo dõi bằng Git.

- **Sai lầm 1:** Xem tệp Word như văn bản nguồn thông thường. DOCX là tài liệu Rich Text dạng gói nhị phân có cấu trúc; nội dung, định dạng và tài nguyên được lưu trong nhiều phần. Git thường không thể hiển thị khác biệt theo từng câu chữ như với tệp văn bản.
- **Sai lầm 2:** Cho rằng sửa dấu phẩy chỉ tạo thay đổi nhỏ trong Git. Khi DOCX được lưu lại, Word có thể cập nhật nhiều phần bên trong gói; Git có thể xem cả tệp như một khối nhị phân, khiến diff kém hữu ích và việc hòa nhập thay đổi khó hơn.
- **Sai lầm 3:** Dùng định dạng ưu tiên trình bày để lưu tài liệu cần xem nhanh trên web. GitHub render Markdown trực tiếp, còn DOCX thường phải tải xuống hoặc mở bằng ứng dụng tương thích.

Markdown là **Plain Text**: nhẹ, mở được bằng trình soạn thảo văn bản, render trực tiếp trên GitHub và cho Git so sánh thay đổi theo từng dòng. Nếu một byte bị hỏng, DOCX có thể không mở được vì cấu trúc gói bị ảnh hưởng; Markdown thường vẫn đọc được và hư hại chỉ tác động đến ký tự hoặc dòng liên quan. Tuy vậy, Markdown không miễn nhiễm với lỗi dữ liệu: nên dùng Git, sao lưu và lưu tệp bằng UTF-8.

## Phần 2 Giới thiệu GreenTech bằng Markdown

> Đề bài không cung cấp nội dung Word gốc, vì vậy phần dưới đây là đoạn giới thiệu mẫu để minh họa chuyển đổi sang Markdown.

# GreenTech

**GreenTech** là dự án của nhóm sinh viên PTIT hướng đến ứng dụng công nghệ để hỗ trợ nông nghiệp bền vững. Hệ thống kết hợp cảm biến và bộ điều khiển để theo dõi điều kiện canh tác, giúp người trồng đưa ra quyết định tưới tiêu phù hợp và sử dụng tài nguyên hiệu quả hơn.

## Mục tiêu

- Theo dõi các điều kiện quan trọng tại khu vực trồng.
- Hỗ trợ tưới đúng lúc dựa trên dữ liệu cảm biến.
- Cung cấp thông tin dễ hiểu để người vận hành kiểm tra hệ thống.

## Công nghệ dự kiến

| Thành phần | Vai trò |
|---|---|
| Cảm biến | Thu thập dữ liệu môi trường và đất |
| Bộ điều khiển | Xử lý dữ liệu và điều khiển thiết bị |
| Máy bơm | Cấp nước theo quyết định của hệ thống |

*GreenTech hướng đến một quy trình canh tác tiết kiệm và dễ theo dõi.*
