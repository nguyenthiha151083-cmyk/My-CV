# Nhật ký thay đổi AI

Ghi lại tại đây mỗi khi có thay đổi lớn được thực hiện với sự hỗ trợ của AI, chẳng hạn như bổ sung chức năng, sửa lỗi quan trọng hoặc thay đổi cấu trúc dự án. Không cần ghi các chỉnh sửa nhỏ về định dạng hay câu chữ.

## Mẫu ghi

### YYYY-MM-DD — Tên thay đổi

- **Thay đổi:** Mô tả ngắn gọn nội dung đã thực hiện.
- **Lý do:** Vì sao cần thay đổi.
- **Phạm vi ảnh hưởng:** Tính năng, tệp hoặc khu vực bị ảnh hưởng.

### 2026-11-05 — Bổ sung báo cáo kiểm thử trước bàn giao

- **Thay đổi:** Tạo báo cáo kiểm thử theo 6 nhóm tiêu chí, kèm trạng thái, minh chứng rà soát và đề xuất trước bàn giao.
- **Lý do:** Ghi nhận mức độ sẵn sàng của website CV và các nội dung cần xác minh trước nghiệm thu.
- **Phạm vi ảnh hưởng:** Tài liệu `docs/test_report.md`; không thay đổi mã nguồn hoặc chức năng website.

### 2026-11-05 — Bổ sung minh chứng kiểm thử responsive

- **Thay đổi:** Chụp và lưu ảnh giao diện tại các viewport mobile (390×844), tablet (768×1024) và desktop (1440×1000); cập nhật liên kết minh chứng trong báo cáo kiểm thử.
- **Lý do:** Cung cấp bằng chứng trực quan cho đánh giá bố cục responsive.
- **Phạm vi ảnh hưởng:** `docs/screenshots/` và `docs/test_report.md`; không thay đổi mã nguồn hoặc chức năng website.