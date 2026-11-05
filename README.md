# CV cá nhân – Đoàn Bá Trường

## Mô tả dự án

Website CV/portfolio cá nhân giới thiệu Đoàn Bá Trường, Frontend Developer. Trang cung cấp thông tin giới thiệu, kỹ năng, các dự án tiêu biểu và phương thức liên hệ. Giao diện được thiết kế responsive để hiển thị trên điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng nhanh đến các phần Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Trình bày thông tin cá nhân và định hướng nghề nghiệp.
- Hiển thị các kỹ năng và dự án dưới dạng thẻ nội dung kèm ảnh minh họa.
- Tự điều chỉnh bố cục theo kích thước màn hình bằng các breakpoint responsive.
- Hỗ trợ trạng thái focus bàn phím và tùy chọn giảm chuyển động của hệ điều hành.

> Đây là website tĩnh. Các dự án Todo List và Weather Dashboard chỉ được giới thiệu trên trang, không phải ứng dụng có chức năng tương tác đang chạy. Dự án hiện không có backend, API tích hợp hay biểu mẫu gửi dữ liệu.

## Công nghệ sử dụng

- **HTML5**: cấu trúc ngữ nghĩa và nội dung.
- **CSS3**: giao diện, responsive, Flexbox và CSS Grid.
- **Nginx** (tùy chọn): phục vụ website bằng Docker.

Không cần JavaScript, framework, Node.js, npm hoặc cơ sở dữ liệu để chạy website.

## Yêu cầu môi trường

### Chạy trực tiếp hoặc bằng máy chủ thử nghiệm

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Không cần cài thêm phần mềm nếu mở trực tiếp `index.html`.
- Cần Python 3 nếu muốn chạy máy chủ HTTP cục bộ.

### Chạy bằng Docker

- Docker Engine trên Linux hoặc Docker Desktop trên Windows/macOS.
- Kết nối Internet lần đầu để tải image `nginx:alpine`.

## Cài đặt

Mở terminal tại thư mục dự án (thư mục chứa `index.html`). Nếu lấy mã nguồn bằng Git:

```bash
git clone <URL-kho-ma-nguon>
cd <thu-muc-du-an>
```

Thay `<URL-kho-ma-nguon>` bằng địa chỉ kho mã nguồn thực tế. Nếu mã nguồn đã có trên máy, chỉ cần mở terminal tại thư mục đó. Không cần cài đặt thư viện hay chạy lệnh build.

## Cấu hình và tùy chỉnh

Dự án không yêu cầu file cấu hình hoặc biến môi trường.

- Chỉnh nội dung trang trong `index.html`.
- Chỉnh kiểu dáng và breakpoint responsive trong `assets/css/styles.css`.
- Thêm/thay ảnh trong `assets/img/` và cập nhật đường dẫn tương ứng trong `index.html`.
- Cập nhật email, Facebook hoặc số điện thoại trong phần Liên hệ của `index.html`.

Giữ nguyên cấu trúc thư mục tương đối để các liên kết đến CSS và hình ảnh hoạt động chính xác.

## Chạy thử

### Windows

Có thể mở trực tiếp `index.html` bằng trình duyệt. Để chạy máy chủ cục bộ, mở PowerShell tại thư mục gốc dự án và chạy:

```powershell
py -m http.server 8000
```

Nếu không có lệnh `py`, thử:

```powershell
python -m http.server 8000
```

### macOS

Mở Terminal tại thư mục gốc dự án:

```bash
python3 -m http.server 8000
```

### Linux

Mở terminal tại thư mục gốc dự án:

```bash
python3 -m http.server 8000
```

Sau khi chạy máy chủ bằng một trong các cách trên, mở <http://localhost:8000> trong trình duyệt. Dừng máy chủ bằng `Ctrl+C` (Windows/Linux) hoặc `Control+C` (macOS). Máy chủ Python chỉ phù hợp cho thử nghiệm, không dùng làm máy chủ production.

### Docker (Windows, macOS, Linux)

Không cần tạo Dockerfile. Chạy lệnh tại thư mục gốc dự án để mount mã nguồn chỉ đọc vào Nginx:

**Windows PowerShell:**

```powershell
docker run --rm --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS/Linux:**

```bash
docker run --rm --name my-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở <http://localhost:8080> để xem trang. Nhấn `Ctrl+C` (Windows/Linux) hoặc `Control+C` (macOS) trong terminal để dừng container. Nếu cổng `8080` đã được sử dụng, đổi cổng bên trái trong `-p 8080:80` (ví dụ `-p 8081:80`) và truy cập cổng mới.

## Thông tin liên hệ

- **Email:** [nguyenthiha151083@gmail.com](mailto:nguyenthiha151083@gmail.com)
- **Facebook:** [facebook.com/share/18TYUJLUAP](https://www.facebook.com/share/18TYUJLUAP/)
- **Điện thoại:** 0362471023

## Cấu trúc thư mục

```text
.
├── index.html
├── README.md
└── assets/
    ├── css/
    │   └── styles.css
    └── img/
        ├── doremon.jpg
        ├── hhh.jpg
        ├── meo.jpg
        └── meomeo.jpg
```