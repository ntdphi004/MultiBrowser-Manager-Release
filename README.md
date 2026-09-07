# MultiBrowser Manager — Professional Anti-Detect Browser & Automation Engine

<p align="center">
  <img src="https://raw.githubusercontent.com/ntdphi004/MultiBrowser-Manager-Release/main/assets/banner.png" alt="MultiBrowser Manager" width="800" onerror="this.style.display='none'"/>
</p>

<p align="center">
  <b>Trình duyệt Anti-Detect thế hệ mới với nhân Chromium Patch Native C++ Blink</b><br>
  Khớp 100% TLS Fingerprint JA3/JA4 · Vượt qua CreepJS, Pixelscan, BrowserLeaks, Cloudflare Turnstile · Tối ưu hiệu năng vượt bậc
</p>

<p align="center">
  <a href="https://github.com/ntdphi004/MultiBrowser-Manager-Release/releases/latest"><img src="https://img.shields.io/github/v/release/ntdphi004/MultiBrowser-Manager-Release?color=blue&label=Latest%20Version" alt="Latest Release"></a>
  <img src="https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-success" alt="Platform">
  <img src="https://img.shields.io/badge/Engine-Chromium%20Native%20Patched%20C%2B%2B-blueviolet" alt="Chromium Native">
  <img src="https://img.shields.io/badge/Security-Local%20First%20%7C%20Zero%20Telemetry-green" alt="Security">
</p>

---

## 🌟 1. Điểm Mạnh Vượt Trội Của MultiBrowser Manager

Khác biệt hoàn toàn với các phần mềm nuôi tài khoản thông thường dùng JavaScript injection (rất dễ bị phát hiện bởi các hệ thống chống gian lận hiện đại), **MultiBrowser Manager** được thiết kế từ cấp độ lõi:

| Đặc tính kỹ thuật | MultiBrowser Manager (Native C++) | Trình duyệt Antidetect thông thường (JS Injection) |
|---|:---:|:---:|
| **Phương thức can thiệp vân tay** | **Native C++ Blink Level** (Biên dịch trực tiếp vào nhân Chromium) | Chèn JavaScript đè `navigator`, `WebGLRenderingContext` |
| **Bypass kiểm tra bot nâng cao** | **Đạt điểm tuyệt đối** trên CreepJS, Pixelscan, Incolumitas, BrowserLeaks | Dễ bị lộ thuộc tính sửa đổi (`toString()`, `getOwnPropertyDescriptor`) |
| **TLS / SSL Fingerprint (JA3 / JA4)** | **Khớp 100%** gói tin mạng của Google Chrome gốc | Thường bị lệch Cipher Suites hoặc Extension Orders |
| **Tiêu thụ tài nguyên (RAM / CPU)** | **Cực nhẹ**, chạy trực tiếp trên Windows Native, không cần máy ảo | Thường nặng nề, tốn nhiều RAM khi mở đồng thời nhiều profile |
| **Bảo mật dữ liệu** | **Local-First 100%**: Dữ liệu SQLite, Cookie, Token lưu trên máy khách | Nhiều tool tự ý đồng bộ dữ liệu người dùng lên server bên thứ ba |
| **Hỗ trợ tự động hóa (Automation)** | Trình điều khiển CDP Native tốc độ cao, hỗ trợ Puppeteer / Playwright | Dễ bị treo hoặc đứt kết nối khi mở số lượng lớn |

### Các Tính Năng Nổi Bật:
1. **Cách ly phần cứng & Môi trường độc lập hoàn toàn:**
   - **Canvas & WebGL:** Thuật toán tạo nhiễu noise thông minh, nhất quán trên từng profile mà không làm biến dạng hình ảnh render.
   - **WebGPU & Hardware Concurrency:** Giả lập trung thực số lõi CPU, bộ nhớ RAM, GPU Vendor và Renderer (NVIDIA, AMD, Intel, Apple Silicon).
   - **AudioContext & SpeechSynthesis:** Giả lập tần số âm thanh và danh sách giọng đọc hệ thống theo từng hệ điều hành.
   - **Font Fingerprinting:** Giả lập danh sách font chữ chính xác theo Windows, macOS hoặc Linux.
   - **WebRTC & Geolocation:** Chặn rò rỉ IP thật (WebRTC Leak Protection), tự động đồng bộ múi giờ (Timezone), ngôn ngữ (Accept-Language) và tọa độ vị trí theo IP Proxy.

2. **Quản lý Proxy Thông Minh:**
   - Hỗ trợ đầy đủ các giao thức: **HTTP, HTTPS, SOCKS5** (có hoặc không có User/Pass).
   - Cơ chế kiểm tra trạng thái Proxy thời gian thực (IP, quốc gia, độ trễ Ping) trước khi mở trình duyệt.

3. **Hệ thống Quản lý Cookie & Tài khoản Tiện Lợi:**
   - Import / Export Cookie định dạng JSON, Netscape.
   - Tự động mã hóa mật khẩu và token bằng thuật toán AES-256 an toàn.

---

## 🚀 2. Hướng Dẫn Tải Về & Cài Đặt

### Yêu Cầu Hệ Thống
- **Hệ điều hành:** Windows 10 / Windows 11 (64-bit).
- **RAM:** Tối thiểu 4 GB (Khuyến nghị 8 GB trở lên nếu chạy nhiều profile cùng lúc).
- **Ổ cứng:** Tối thiểu 1 GB dung lượng trống.

### Cách 1: Cài Đặt Bản Full Mới Nhất (Dành cho người dùng mới)
1. Truy cập trang phát hành: 👉 **[Tải Bản Cập Nhật Mới Nhất Tại Đây](https://github.com/ntdphi004/MultiBrowser-Manager-Release/releases/latest)**
2. Tải file cài đặt (ví dụ: `MultiBrowser-Manager-vX.Y.Z-customer-full.zip`).
3. Giải nén file `.zip` vào một thư mục bất kỳ (ví dụ: `D:\MultiBrowser-Manager`).
4. Double-click file **`MultiBrowser.exe`** (hoặc `CAI_TAT_CA.bat` nếu muốn cài đặt tự động toàn bộ môi trường).
5. Ứng dụng sẽ tự động khởi động và mở giao diện quản lý trên trình duyệt tại địa chỉ: `http://127.0.0.1:8080`.

### Cách 2: Cập Nhật Nhanh Bằng 1-Click (Dành cho người dùng đang sử dụng)
- **Cách A (Trên giao diện Web):** Khi có phiên bản mới, trên Dashboard sẽ xuất hiện thông báo cập nhật -> Bấm **"Cập nhật ngay"** -> **"Khởi động lại & Áp dụng"**.
- **Cách B (Khay hệ thống Windows Tray):** Chuột phải vào biểu tượng MultiBrowser ở góc phải màn hình -> Chọn **"Check for updates..."** (Kiểm tra cập nhật).
- **Cách C (File Batch 1-Click):** Double-click file **`CAP_NHAT.bat`** (hoặc `UPDATE.bat`) trong thư mục ứng dụng. Script sẽ tự động tải bản vá siêu nhẹ (~15-25MB), sao lưu và cập nhật trong vài giây mà **không làm mất dữ liệu profile hay cấu hình**.

---

## 📖 3. Hướng Dẫn Sử Dụng Cơ Bản

### Bước 1: Tạo Profile Trình Duyệt Mới
1. Bấm vào nút **"Tạo Profile"** (+ New Profile).
2. Điền tên profile (ví dụ: `Facebook_Acc_01`, `Amazon_Store_02`).
3. Chọn hệ điều hành giả lập (Windows / macOS / Linux) và phiên bản trình duyệt.
4. Cấu hình Fingerprint: Hệ thống đã chọn sẵn cấu hình ngẫu nhiên tối ưu nhất. Bạn có thể tùy chỉnh thêm Canvas, WebGL, Audio nếu có nhu cầu chuyên sâu.

### Bước 2: Gắn Proxy Cho Profile
1. Trong mục **Cấu hình Proxy**, chọn loại proxy (HTTP / HTTPS / SOCKS5).
2. Nhập theo định dạng: `IP:PORT` hoặc `IP:PORT:USERNAME:PASSWORD`.
3. Bấm **"Kiểm tra Proxy"** (Check Proxy) để đảm bảo IP hoạt động tốt và nhận diện đúng quốc gia.

### Bước 3: Khởi Chạy Profile
1. Bấm nút **"Mở Profile"** (Launch).
2. Trình duyệt chống phát hiện sẽ mở ra với đầy đủ thông số vân tay và IP của proxy đã chọn.
3. Bạn có thể sử dụng các trang web như [browserleaks.com](https://browserleaks.com), [creepjs](https://abrahamjuliot.github.io/creepjs/) để kiểm tra độ tin cậy của profile.

---

## 🛠️ 4. Các Lỗi Thường Gặp & Cách Khắc Phục (Troubleshooting)

### ❓ Lỗi 1: Windows Defender / Antivirus cảnh báo hoặc chặn file `.exe` / `.bat`
- **Nguyên nhân:** Do phần mềm được biên dịch AOT Native và chưa đăng ký chứng chỉ số đắt tiền của Microsoft (Code Signing Certificate), Windows SmartScreen có thể hiển thị cảnh báo *"Windows protected your PC"*.
- **Cách xử lý:**
  1. Khi xuất hiện bảng cảnh báo màu xanh của Windows SmartScreen, bấm **"More info"** -> Bấm **"Run anyway"**.
  2. Để tránh bị trình diệt virus quét nhầm trong quá trình chạy, hãy thêm thư mục cài đặt MultiBrowser Manager vào danh sách loại trừ (**Exclusion**) của Windows Security / Antivirus.

### ❓ Lỗi 2: Proxy báo lỗi không kết nối được hoặc tải trang bị Timeout
- **Nguyên nhân:** 
  - Proxy bị die, sai cổng hoặc sai user/password.
  - Một số proxy IP xoay (Rotating Proxy) có thể mất vài giây để kích hoạt IP mới.
- **Cách xử lý:**
  1. Kiểm tra lại định dạng: đảm bảo không có khoảng trắng thừa ở đầu/cuối chuỗi proxy.
  2. Đổi giao thức thử giữa HTTP và SOCKS5.
  3. Bấm nút "Kiểm tra Proxy" trong giao diện Profile để xem mã lỗi chi tiết.

### ❓ Lỗi 3: Không mở được trang quản trị `http://127.0.0.1:8080` (Trùng cổng Port 8080)
- **Nguyên nhân:** Cổng 8080 đang bị một phần mềm khác trên máy bạn chiếm dụng (như phần mềm kế toán, web server cục bộ, Docker).
- **Cách xử lý:**
  1. Mở file `.env` trong thư mục cài đặt bằng Notepad.
  2. Tìm dòng `MB_PORT=8080` và đổi thành cổng khác (ví dụ: `MB_PORT=8090` hoặc `MB_PORT=8888`).
  3. Bật lại `MultiBrowser.exe` và truy cập vào địa chỉ cổng mới.

### ❓ Lỗi 4: Báo lỗi file bị khóa khi cập nhật (File is locked by another process)
- **Nguyên nhân:** Trình duyệt hoặc tiến trình `MultiBrowser.exe` cũ vẫn còn đang chạy ngầm khi cố gắng ghi đè file mới.
- **Cách xử lý:**
  1. Double-click file **`CAP_NHAT.bat`**.
  2. Script đã được tích hợp cơ chế tự động tìm và tắt an toàn tất cả tiến trình liên quan trước khi giải nén đè bản vá.
  3. Nếu vẫn báo lỗi, hãy mở *Task Manager* (Ctrl+Shift+Esc), tắt các tiến trình `MultiBrowser.exe` hoặc `chrome.exe` rồi chạy lại `CAP_NHAT.bat`.

### ❓ Lỗi 5: Làm thế nào để sao lưu (Backup) toàn bộ dữ liệu Profile?
- Toàn bộ dữ liệu tài khoản, lịch sử duyệt web và cấu hình profile được lưu trữ tại:
  `%USERPROFILE%\.multibrowser-manager\` (thường là `C:\Users\<Tên_Bạn>\.multibrowser-manager\`).
- Để sao lưu sang máy khác hoặc dự phòng, bạn chỉ cần copy nguyên thư mục này lưu trữ an toàn.

---

## 🔒 5. Chính Sách Bảo Mật & Quyền Riêng Tư

- **Zero Telemetry:** Ứng dụng không thu thập lịch sử duyệt web, cookie, tài khoản hay hành vi sử dụng của bạn.
- **Local Storage:** Cơ sở dữ liệu SQLite và khóa mã hóa nằm hoàn toàn trên thiết bị của bạn.
- **Safe Updates:** Các bản vá cập nhật chỉ chứa file thực thi đã biên dịch và tài nguyên giao diện, được kiểm tra mã băm toàn vẹn **SHA256** trước khi áp dụng.

---

## 📞 6. Hỗ Trợ & Liên Hệ

Nếu bạn gặp bất kỳ khó khăn nào trong quá trình cài đặt và sử dụng, vui lòng liên hệ:
- **GitHub Issues:** [Gửi yêu cầu hỗ trợ / Báo lỗi](https://github.com/ntdphi004/MultiBrowser-Manager-Release/issues)
- **Telegram Bot:** [@MultiBrowser_Bot](https://t.me/MultiBrowser_Bot)

---

<p align="center">
  <i>MultiBrowser Manager — Giải pháp tối thượng cho bảo vệ danh tính số và vận hành tài khoản an toàn.</i>
</p>
