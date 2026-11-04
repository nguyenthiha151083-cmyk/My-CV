# CV cá nhân – Đoàn Bá Trường

## Mô tả

Đây là website CV/portfolio cá nhân giới thiệu Đoàn Bá Trường, vị trí Frontend Developer. Trang gồm phần giới thiệu, kỹ năng, các dự án tiêu biểu và thông tin liên hệ. Giao diện được xây dựng theo hướng responsive, phù hợp với điện thoại, máy tính bảng và máy tính.

## Chức năng

- Điều hướng đến các mục Giới thiệu, Kỹ năng, Dự án và Liên hệ.
- Giới thiệu thông tin cá nhân và định hướng nghề nghiệp.
- Trình bày danh sách kỹ năng và dự án bằng các thẻ nội dung.
- Hiển thị ảnh minh họa từ thư mục `assets/img/`.
- Bố cục tự điều chỉnh theo kích thước màn hình.
- Hỗ trợ điều hướng bằng bàn phím và tùy chọn giảm chuyển động của hệ điều hành.

> Đây là website tĩnh. Các dự án và nội dung đang được trình bày dưới dạng giới thiệu; trang hiện không có backend, API đang chạy hoặc chức năng xử lý biểu mẫu.

## Công nghệ

- **HTML5**: cấu trúc và nội dung trang.
- **CSS3**: giao diện, responsive, Flexbox và CSS Grid.
- **Nginx (Docker, tùy chọn)**: phục vụ website tĩnh trong container.

Website không cần JavaScript, framework, Node.js, npm hay cơ sở dữ liệu để chạy.

## Yêu cầu môi trường

### Chạy trực tiếp hoặc bằng máy chủ cục bộ

- Windows, macOS hoặc Linux.
- Trình duyệt hiện đại như Chrome, Firefox, Edge hoặc Safari.
- Không cần cài thêm phần mềm nếu chỉ mở file HTML trực tiếp.
- Nếu muốn chạy máy chủ cục bộ: Python 3 (có sẵn hoặc cài riêng).

### Chạy bằng Docker

- Docker Engine trên Linux, hoặc Docker Desktop trên Windows/macOS.
- Có kết nối Internet lần đầu để tải image `nginx:alpine`.

## Cài đặt

Tải hoặc sao chép mã nguồn về máy, sau đó mở terminal tại thư mục gốc của dự án (thư mục chứa `index.html`). Ví dụ:

```bash
git clone <URL-kho-ma-nguon>
cd <thu-muc-du-an>
```

Thay `<URL-kho-ma-nguon>` bằng URL Git của dự án. Nếu đã có mã nguồn trên máy, chỉ cần mở terminal tại thư mục đó.

## Cấu hình

Dự án không yêu cầu file cấu hình hay biến môi trường.

- Sửa nội dung trang trong `index.html`.
- Sửa giao diện trong `assets/css/styles.css`.
- Thêm hoặc thay ảnh trong `assets/img/`; cập nhật đường dẫn ảnh tương ứng trong `index.html`.
- Cập nhật email, mạng xã hội và số điện thoại trong mục Liên hệ của `index.html` nếu cần.

Các đường dẫn tài nguyên hiện được viết tương đối từ `index.html`, vì vậy hãy giữ nguyên cấu trúc thư mục khi thay đổi hoặc triển khai.

## Chạy thử

### Windows

**Mở trực tiếp:** mở `index.html` bằng trình duyệt.

**Chạy máy chủ cục bộ bằng Python:** mở PowerShell tại thư mục gốc dự án:

```powershell
py -m http.server 8000
```

Nếu lệnh `py` không có trên máy, thử:

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

### Mở trang trên Windows, macOS hoặc Linux

Sau khi khởi động máy chủ cục bộ bằng một trong các lệnh trên, truy cập:

```text
http://localhost:8000
```

Nhấn `Ctrl+C` (Windows/Linux) hoặc `Control+C` (macOS) trong cửa sổ terminal để dừng máy chủ. Máy chủ Python chỉ phục vụ thử nghiệm; không nên dùng làm máy chủ triển khai production.

### Docker

Không cần Dockerfile cho dự án này. Lệnh dưới đây gắn thư mục dự án vào Nginx chỉ đọc và ánh xạ cổng `8080` trên máy vào cổng `80` trong container.

**Windows PowerShell** — chạy tại thư mục gốc dự án:

```powershell
docker run --rm --name my-cv -p 8080:80 -v "${PWD}:/usr/share/nginx/html:ro" nginx:alpine
```

**macOS hoặc Linux** — chạy tại thư mục gốc dự án:

```bash
docker run --rm --name my-cv -p 8080:80 -v "$(pwd):/usr/share/nginx/html:ro" nginx:alpine
```

Mở `http://localhost:8080` trên trình duyệt. Container sẽ dừng khi nhấn `Ctrl+C` (Windows/Linux) hoặc `Control+C` (macOS) trong terminal. Nếu cổng `8080` đang được sử dụng, thay `8080` trong phần `-p 8080:80` bằng một cổng khác, chẳng hạn `8081`, rồi truy cập cổng mới tương ứng.

## Thông tin liên hệ

Thông tin liên hệ được hiển thị trên trang:

- **Email:** [nguyenthiha151083@gmail.com](mailto:nguyenthiha151083@gmail.com)
- **Facebook:** [facebook.com/share/18TYUJLUAP](https://www.facebook.com/share/18TYUJLUAP/)
- **Điện thoại:** 0362471023

## Cấu trúc dự án

```text
.
├── index.html
└── assets/
    ├── README.md
    ├── css/
    │   └── styles.css
    └── img/
        ├── doremon.jpg
        ├── hhh.jpg
        ├── meo.jpg
        └── meomeo.jpg
```
