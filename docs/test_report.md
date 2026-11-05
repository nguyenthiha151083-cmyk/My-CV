# BÁO CÁO KIỂM THỬ TRƯỚC BÀN GIAO

## 1. Thông tin chung

| Thông tin | Chi tiết |
|---|---|
| **Tên dự án** | Website CV/Portfolio cá nhân — Đoàn Bá Trường |
| **Phiên bản** | v1.0.0 |
| **Ngày kiểm thử/đánh giá** | 05/11/2026 |
| **Người thực hiện/đánh giá** | Chưa cung cấp |
| **Phạm vi** | Đối chiếu mã nguồn, nội dung và tài liệu bàn giao theo 6 nhóm tiêu chí bên dưới |
| **Phương pháp** | Rà soát tĩnh repository và chụp ảnh giao diện tại các viewport responsive bằng trình duyệt; chưa kiểm thử trên thiết bị vật lý hoặc môi trường triển khai |

> **Lưu ý:** Trạng thái trong báo cáo phản ánh bằng chứng có thể xác nhận từ mã nguồn và tài liệu hiện có. Các nội dung chưa chạy thử được ghi rõ là cần kiểm chứng; không xem việc rà soát tĩnh là thay thế cho kiểm thử trên môi trường thực tế.

### Quy ước trạng thái

- **Đạt:** Có bằng chứng phù hợp trong phạm vi đã rà soát.
- **Chưa đạt:** Có lỗi hoặc nội dung chưa đáp ứng, cần xử lý trước khi nghiệm thu.
- **Cần cải thiện:** Có cơ sở triển khai nhưng cần bổ sung, xác minh hoặc nâng chất lượng trước khi kết luận.

## 2. Bảng tổng quan trạng thái

| # | Nhóm tiêu chí | Trạng thái | Tóm tắt |
|---:|---|---|---|
| 1 | Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng | **Cần cải thiện** | Các phần nội dung chính hiện diện; một số liên kết chưa có đích thực tế và cần xác nhận ranh giới giữa nội dung giới thiệu với chức năng thật. |
| 2 | Giao diện, trải nghiệm người dùng và khả năng tương thích | **Cần cải thiện** | Đã chụp giao diện ở ba viewport responsive; vẫn cần kiểm tra tương phản màu và xác minh trên thiết bị/trình duyệt thực tế. |
| 3 | Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản | **Cần cải thiện** | Website tĩnh, cấu trúc chạy đơn giản; chưa có bằng chứng chạy thử, đo hiệu năng hoặc kiểm tra xử lý lỗi tài nguyên. |
| 4 | Bảo mật, quản lý cấu hình và dữ liệu | **Cần cải thiện** | Không thấy luồng backend hoặc dữ liệu người dùng trong phạm vi rà soát; cần xác minh cấu hình bảo mật ở máy chủ và việc công khai thông tin liên hệ. |
| 5 | Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao | **Cần cải thiện** | Cấu trúc đơn giản và có README; cây thư mục trong README chưa phản ánh đầy đủ `docs/`, và một số nội dung dự án cần nhất quán hơn. |
| 6 | Khả năng triển khai, kiểm thử và cung cấp minh chứng | **Cần cải thiện** | Đã có ảnh minh chứng responsive; chưa có biên bản kiểm thử đầy đủ, kết quả triển khai hoặc minh chứng ở môi trường production. |

## 3. Nội dung chi tiết theo nhóm tiêu chí

### 3.1. Tính đúng đắn và mức độ đáp ứng yêu cầu chức năng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có các khu vực Giới thiệu, Kỹ năng, Dự án và Liên hệ | **Đạt** | Các section tương ứng có trong [`index.html`](../index.html); thanh điều hướng trỏ đến các ID này. |
| Điều hướng nội bộ đến đúng khu vực | **Cần cải thiện** | Các liên kết `#about`, `#skills`, `#projects`, `#contact` và `#top` khớp với ID trong HTML theo rà soát mã nguồn; cần xác minh thao tác thực tế trên trình duyệt và bàn phím. |
| Thẻ dự án cung cấp liên kết xem chi tiết hoạt động | **Chưa đạt** | Các liên kết “Xem chi tiết” trong [`index.html`](../index.html) dùng `href="#"`, chưa đưa người dùng đến nội dung dự án. |
| Thông tin liên hệ mở đúng phương thức liên hệ | **Chưa đạt** | Email dùng `mailto:`; Facebook và số điện thoại hiện dùng `href="#"`. Nên dùng URL Facebook và `tel:` tương ứng hoặc trình bày như văn bản không tương tác. |
| Nội dung giới thiệu dự án phản ánh đúng chức năng có thể sử dụng | **Cần cải thiện** | README xác định Todo List và Weather Dashboard chỉ là nội dung giới thiệu, không phải ứng dụng đang chạy. Cần duy trì cách diễn đạt này nhất quán trên trang để tránh hiểu nhầm về ứng dụng tương tác/API. |
| Tài nguyên hình ảnh được tham chiếu trong trang có trong repository | **Đạt** | Các ảnh `meomeo.jpg`, `meo.jpg`, `hhh.jpg`, `doremon.jpg` có trong `assets/img/` và đường dẫn tương ứng được dùng trong HTML. Chưa xác minh tải ảnh khi chạy. |

### 3.2. Giao diện, trải nghiệm người dùng và khả năng tương thích

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Bố cục có quy tắc responsive cho các kích thước màn hình | **Đạt** | [`assets/css/styles.css`](../assets/css/styles.css) dùng bố cục mobile-first, breakpoint từ 768px và 1280px; ảnh chụp xác nhận lưới dự án hiển thị 1/2/3 cột ở viewport mobile/tablet/desktop. |
| Có trạng thái focus bàn phím và hỗ trợ giảm chuyển động | **Đạt** | CSS định nghĩa `:focus-visible` và `prefers-reduced-motion`. Chưa kiểm thử thao tác bàn phím hoặc thiết lập hệ điều hành trên trình duyệt. |
| Màu chữ, nền và thành phần tương tác đủ dễ đọc | **Cần cải thiện** | Một số biến màu trong stylesheet có độ sáng gần nhau và màu nền `#15e133` rất rực; cần đo tương phản theo WCAG và kiểm tra trạng thái hover/focus trước nghiệm thu. |
| Hình ảnh và nội dung có hiển thị phù hợp trên mobile/tablet/desktop | **Cần cải thiện** | Đã chụp ảnh tại các viewport 390×844, 768×1024 và 1440×1000: [Mobile](screenshots/responsive-mobile.png), [Tablet](screenshots/responsive-tablet.png), [Desktop](screenshots/responsive-desktop.png). Bằng chứng là ảnh chụp viewport trình duyệt, chưa phải thiết bị vật lý; cần tiếp tục kiểm tra khả năng đọc, tương phản màu và hiển thị trên thiết bị/trình duyệt thực tế. |
| Liên kết và nhãn liên hệ rõ ràng với người dùng | **Cần cải thiện** | Nhãn “facebook” và “sdt” chưa nhất quán về cách viết; liên kết đang là placeholder như nêu ở tiêu chí chức năng. |
| Tương thích với các trình duyệt mục tiêu | **Cần cải thiện** | README nêu Chrome, Firefox, Edge và Safari, nhưng chưa có kết quả kiểm thử trên bất kỳ trình duyệt/phiên bản cụ thể nào. |

### 3.3. Khả năng vận hành, xử lý lỗi và hiệu năng cơ bản

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Website khởi chạy theo hướng dẫn bàn giao | **Cần cải thiện** | README hướng dẫn mở `index.html`, chạy Python HTTP server hoặc dùng Docker/Nginx; chưa thực thi các cách chạy này trong lần đánh giá. |
| Tài nguyên CSS và hình ảnh tải đúng khi phục vụ từ thư mục gốc | **Cần cải thiện** | Các đường dẫn tương đối trong HTML trỏ đến `assets/css/` và `assets/img/`; cần kiểm tra log mạng/console khi chạy qua file, HTTP server và Docker. |
| Có cơ chế xử lý lỗi runtime phù hợp | **Đạt** | Website hiện là HTML/CSS tĩnh, không có JavaScript hoặc luồng gọi API trong phạm vi sản phẩm mô tả; vì vậy không có luồng lỗi ứng dụng động để đánh giá. Trạng thái này không xác nhận máy chủ hoặc tài nguyên luôn sẵn sàng. |
| Hiệu năng tải cơ bản phù hợp | **Cần cải thiện** | Không thấy phụ thuộc framework hoặc bước build trong README; chưa đo dung lượng ảnh, thời gian tải, Core Web Vitals hoặc hiệu năng trên mạng chậm. |
| Trang hoạt động khi một liên kết ngoài hoặc tài nguyên không khả dụng | **Cần cải thiện** | Chưa có kết quả thử nghiệm khi ngắt mạng hoặc thiếu ảnh/CSS; cần xác nhận nội dung vẫn dễ hiểu và lỗi được nhận biết. |

### 3.4. Bảo mật, quản lý cấu hình và dữ liệu

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Không đưa thông tin bí mật vào mã nguồn hoặc repository | **Cần cải thiện** | Trong các tệp được rà soát không thấy cấu hình bí mật; đây không phải kiểm tra toàn bộ lịch sử Git hoặc quét secret tự động. |
| Thu thập, lưu trữ hoặc truyền dữ liệu người dùng | **Đạt** | README mô tả website không có backend, API tích hợp hay biểu mẫu gửi dữ liệu; cần đánh giá lại nếu bổ sung các khả năng này. |
| Thông tin liên hệ công khai đã được chủ sở hữu xác nhận | **Cần cải thiện** | Email, số điện thoại và liên kết Facebook được hiển thị trong [`index.html`](../index.html). Cần xác nhận chủ sở hữu đồng ý công khai trước khi xuất bản. |
| Cấu hình môi trường và thông tin triển khai được quản lý an toàn | **Cần cải thiện** | README cho biết không cần biến môi trường; chưa rà soát cấu hình thực tế của hosting, DNS, TLS hoặc quyền truy cập máy chủ. |
| Máy chủ production áp dụng HTTPS và header bảo mật phù hợp | **Cần cải thiện** | Không thể xác minh từ repository tĩnh; cần kiểm tra tại môi trường triển khai trước khi bàn giao. |

### 3.5. Chất lượng mã nguồn, cấu trúc repository và tài liệu bàn giao

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Cấu trúc HTML và CSS tách biệt, có thể bảo trì | **Đạt** | HTML nằm trong [`index.html`](../index.html), stylesheet tách tại [`assets/css/styles.css`](../assets/css/styles.css); cấu trúc trang chia thành các section dễ định vị. |
| Cây thư mục trong README khớp repository | **Chưa đạt** | README liệt kê `assets/img/` nhưng phần cây thư mục mẫu không thể hiện `docs/`; repository hiện có `docs/` chứa tài liệu. Cần cập nhật cây thư mục bàn giao. |
| Nội dung README phản ánh đúng sản phẩm | **Cần cải thiện** | README mô tả đúng website tĩnh và hạn chế backend/API; cần đối chiếu lại chi tiết liên hệ, thư mục và trạng thái các dự án trước khi bàn giao. |
| Có tài liệu phát hành và nhật ký thay đổi cần thiết | **Cần cải thiện** | Có README và mẫu nhật ký AI tại [`AI_LOG.md`](./AI_LOG.md); hiện chưa thấy `RELEASENOTE.md` trong repository. Cần bổ sung ghi chú phát hành và cập nhật phiên bản/ngày phát hành nhất quán; chưa có kiểm thử tài liệu tự động. |
| Mã nguồn không chứa nội dung hoặc chú thích gây hiểu nhầm | **Cần cải thiện** | Trong CSS có một số chú thích mô tả màu sắc không khớp với giá trị màu hiện tại; nên sửa chú thích hoặc điều chỉnh token để tài liệu mã nguồn chính xác. |

### 3.6. Khả năng triển khai, kiểm thử và cung cấp minh chứng

| Hạng mục kiểm tra | Trạng thái | Ghi chú/Minh chứng |
|---|---|---|
| Có hướng dẫn chạy cục bộ | **Đạt** | README cung cấp hướng dẫn mở trực tiếp và chạy HTTP server bằng Python trên Windows/macOS/Linux. Chưa chạy xác nhận từng lệnh. |
| Có hướng dẫn triển khai bằng Docker/Nginx | **Cần cải thiện** | README cung cấp lệnh Docker chạy Nginx; chưa thực thi trên Windows/macOS/Linux và chưa kiểm tra nội dung sau triển khai. |
| Có bộ test chức năng/giao diện và kết quả thực thi | **Chưa đạt** | Chưa có test case, kết quả pass/fail hoặc báo cáo tự động trong phạm vi repository được rà soát. |
| Có minh chứng trực quan và thông tin môi trường kiểm thử | **Chưa đạt** | Chưa có ảnh chụp màn hình, danh sách trình duyệt/phiên bản, viewport hoặc URL môi trường kiểm thử đính kèm. |
| Có tiêu chí nghiệm thu và quyết định bàn giao được ghi nhận | **Cần cải thiện** | Báo cáo này cung cấp checklist ban đầu; người phụ trách cần cập nhật kết quả sau khi chạy kiểm thử thực tế và ghi nhận phê duyệt. |

## 4. Đánh giá tổng kết và đề xuất

### Nhận định chung

Sản phẩm có phạm vi gọn, là website CV tĩnh được xây dựng bằng HTML/CSS, có các khu vực nội dung chính, bố cục responsive và hướng dẫn chạy cơ bản. Tuy nhiên, báo cáo hiện dựa trên rà soát tĩnh; chưa có xác nhận bằng chạy thử trên trình duyệt hoặc môi trường triển khai. Một số liên kết đang là placeholder, màu sắc cần đánh giá tương phản, và tài liệu repository cần được đồng bộ. **Chưa đủ minh chứng để kết luận sản phẩm sẵn sàng bàn giao chính thức.**

### Các việc cần ưu tiên trước khi bàn giao

1. Thay `href="#"` ở liên kết dự án, Facebook và số điện thoại bằng đích sử dụng được; nếu chưa có đích, hiển thị dưới dạng văn bản không tương tác.
2. Xác nhận nội dung và thông tin liên hệ công khai; bảo đảm mô tả Todo List/Weather Dashboard không khiến người dùng hiểu nhầm là tính năng đang chạy.
3. Kiểm tra và điều chỉnh độ tương phản màu; kiểm thử trực quan ở viewport mobile, tablet và desktop.
4. Chạy thử website qua hướng dẫn cục bộ và Docker/Nginx; kiểm tra CSS, ảnh, liên kết, console và network errors.
5. Cập nhật README để cây thư mục, tài liệu phát hành, phiên bản và nội dung repository nhất quán.
6. Ghi lại trình duyệt/phiên bản, thiết bị hoặc viewport, kết quả từng checklist và ảnh minh chứng; xác minh HTTPS/header tại hosting nếu triển khai production.

### Kết luận bàn giao

**Trạng thái đề xuất: Chưa nghiệm thu bàn giao ở thời điểm lập báo cáo.** Có thể xem xét bàn giao sau khi xử lý các mục **Chưa đạt**, hoàn tất kiểm thử thực tế các mục **Cần cải thiện**, đính kèm minh chứng và được người phụ trách xác nhận.

## 5. Xác nhận

| Vai trò | Họ tên | Ngày | Xác nhận |
|---|---|---|---|
| Người kiểm thử |  |  |  |
| Người phụ trách sản phẩm |  |  |  |
| Người nghiệm thu/bàn giao |  |  |  |