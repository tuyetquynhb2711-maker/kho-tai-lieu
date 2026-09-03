# Hướng dẫn VS Code + Claude Code cho người mới

> Tài liệu tổng hợp cách cài đặt VS Code, kết nối Claude Code, kết nối GitHub và các phím tắt phổ biến.

---

## MỤC LỤC

1. [Cài đặt VS Code cơ bản](#phần-1-cài-đặt-vs-code-cơ-bản)
2. [Cài Claude Code và đăng nhập](#phần-2-cài-claude-code-và-đăng-nhập)
3. [Claude Code - Slash Commands](#phần-3-claude-code---slash-commands-lệnh)
4. [Kết nối GitHub](#phần-4-kết-nối-github)
5. [Phím tắt VS Code phổ biến](#phần-5-phím-tắt-vs-code-phổ-biến)
6. [Mẹo cho người mới](#mẹo-cho-người-mới)
7. [Module nâng cao sau](#module-nâng-cao-sau)

---

## PHẦN 1: Cài đặt VS Code cơ bản

### Bước 1: Tải và cài
- Vào [code.visualstudio.com](https://code.visualstudio.com) tải bản Windows và cài đặt
- Khi cài, TICK 2 ô: **"Add to PATH"** và **"Open with Code"** (chuột phải)

---

## PHẦN 2: Cài Claude Code và đăng nhập

### Bước 1: Cài extension Claude Code
1. Mở VS Code
2. Bấm icon 4 ô vuông bên trái (`Ctrl + Shift + X`)
3. Tìm **"Claude Code"** (của Anthropic)
4. Bấm **Install**

### Bước 2: Mở Claude chat trong VS Code
1. `Ctrl + Shift + P` gõ `Claude` chọn **"Open Claude Code"**
2. Cửa sổ chat Claude sẽ hiện ra bên phải

### Bước 3: Đăng nhập với tài khoản Claude web (QUAN TRỌNG)
1. Trong cửa sổ chat Claude vừa mở, bạn sẽ thấy 1 **đường link Subscription/Login** hiển thị
2. **Bấm vào đường link đó** trình duyệt sẽ tự mở ra trang claude.ai
3. Đăng nhập bằng tài khoản Claude web (Google/Email) đã đăng ký gói Pro/Max
4. Cho phép kết nối, quay lại VS Code là dùng được

> **Lưu ý:** Phải có tài khoản Claude Pro/Max ở [claude.ai](https://claude.ai) trước rồi mới đăng nhập được trong VS Code.

---

## PHẦN 3: Claude Code - Slash Commands (/lệnh)

### Các lệnh `/` phổ biến

| Lệnh | Chức năng |
|---|---|
| `/help` | Xem toàn bộ hướng dẫn |
| `/clear` | Xóa hội thoại, bắt đầu mới |
| `/init` | Tạo file CLAUDE.md ghi nhớ dự án |
| `/config` | Cài đặt Claude Code |
| `/model` | Đổi model (Opus/Sonnet/Haiku) |
| `/fast` | Bật/tắt chế độ nhanh |
| `/review` | Review Pull Request |
| `/seo` | Chạy SEO audit tự động |
| `/security-review` | Review bảo mật |
| `/simplify` | Rà soát code, đơn giản hóa |

### Cú pháp `@` (đính kèm file)
- `@filename.md` đính kèm 1 file cụ thể
- `@folder/` đính kèm cả folder
- Kéo thả file vào chat cũng được

### Cú pháp `!` (chạy lệnh shell)
- `!git status` chạy lệnh git, kết quả tự động vào context
- `!ls` liệt kê file

---

## PHẦN 4: Kết nối GitHub

### Cách 1: Đăng nhập qua VS Code (dễ nhất)
1. Bấm icon người ở góc trái dưới cùng
2. Chọn **"Sign in with GitHub"**
3. Trình duyệt mở, cho phép truy cập, xong

### Cách 2: Cài Git thủ công
1. Tải Git: [git-scm.com](https://git-scm.com) và cài đặt (Next hết)
2. Mở terminal trong VS Code (`` Ctrl + ` ``), gõ:

```bash
git config --global user.name "Tên của bạn"
git config --global user.email "email@gmail.com"
```

### Clone (tải) 1 repo về máy
`Ctrl + Shift + P` gõ `Git: Clone` dán link GitHub chọn folder lưu

### Push (đẩy) code lên GitHub
1. Bấm icon nhánh cây bên trái
2. Bấm `+` để stage file
3. Gõ commit message bấm `✓` Commit
4. Bấm `...` chọn **Push** (hoặc **Publish Branch** nếu lần đầu)

### Tạo repo mới từ folder có sẵn
1. Mở folder trong VS Code
2. Icon Git chọn **"Publish to GitHub"** chọn Public/Private xong

---

## PHẦN 5: Phím tắt VS Code phổ biến

### Phím tắt cần thuộc lòng

| Phím | Chức năng |
|---|---|
| `Ctrl + P` | Mở nhanh file bất kỳ (gõ tên file) |
| `Ctrl + Shift + P` | Command Palette - làm mọi thứ |
| `Ctrl + F` | Tìm trong file hiện tại |
| `Ctrl + Shift + F` | Tìm trong TOÀN BỘ project |
| `Ctrl + H` | Tìm và thay thế |
| `` Ctrl + ` `` | Mở/đóng terminal |
| `Ctrl + B` | Ẩn/hiện sidebar |
| `Ctrl + /` | Comment/uncomment dòng |
| `Alt + ↑/↓` | Di chuyển dòng lên/xuống |
| `Shift + Alt + ↓` | Copy dòng xuống dưới |
| `Ctrl + D` | Chọn từ giống nhau tiếp theo |

### Multi-cursor (con trỏ nhiều nơi)
- `Alt + Click` chuột: đặt thêm con trỏ ở nhiều vị trí
- `Ctrl + D` liên tục: chọn nhiều từ giống nhau để sửa cùng lúc
- Cực nhanh khi đổi tên biến hoặc sửa danh sách

### Split editor (chia màn hình)
- `Ctrl + \`: chia editor làm 2 cột
- Kéo tab sang phải/trái để tự chia
- Hữu ích khi so sánh 2 file

### Zen Mode (tập trung tối đa)
- `Ctrl + K` rồi `Z`: ẩn hết chỉ còn code
- `Esc Esc`: thoát

### Command Palette - "thần thánh"
Bấm `Ctrl + Shift + P` rồi gõ:
- `format document`: format code
- `change language mode`: đổi ngôn ngữ file
- `toggle word wrap`: xuống dòng tự động
- `settings`: mở cài đặt

### Mẹo năng suất
- **Zoom code**: `Ctrl + +/-`
- **Đi tới dòng số N**: `Ctrl + G`
- **Đi tới định nghĩa hàm**: `F12` (đứng trên tên hàm)
- **Quay lại**: `Alt + ←`
- **Đổi tên biến toàn project**: `F2` (đứng trên tên biến)
- **Xem lỗi**: `Ctrl + Shift + M`

---

## Mẹo cho người mới

1. **Luôn gõ tiếng Việt** với Claude - hiểu 100%
2. **Không sợ hỏi lại** - gõ "giải thích chi tiết hơn" bất cứ lúc nào
3. **`/clear` khi đổi task** - giữ context sạch, tiết kiệm token
4. **Đính kèm file mẫu** thay vì mô tả - Claude học nhanh hơn
5. **CLAUDE.md là bộ nhớ vàng** - viết rõ style, quy tắc vào đó 1 lần dùng mãi

### 5 phím tắt vàng học ngay
- `Ctrl + P` - mở file nhanh
- `Ctrl + Shift + P` - Command Palette
- `Ctrl + Shift + F` - tìm toàn project
- `` Ctrl + ` `` - mở terminal
- `Ctrl + D` - multi-cursor

Chỉ vậy là đã nhanh gấp 3 lần rồi.

---

## Module nâng cao sau

> Phần này dành cho khi đã quen với VS Code và Claude Code cơ bản. Có thể bỏ qua ở lần đọc đầu tiên.

### A. Tạo Schedule Task viết bài tự động (module nâng cao sau)

#### Cách 1: Dùng `/schedule` (chạy trên cloud, tự động 24/7)

Gõ trong Claude Code:

```
/schedule
```

**Ví dụ tạo routine viết bài hàng ngày:**

```
Tạo schedule chạy 8h sáng mỗi ngày, đọc file d:/blog/topics.md,
chọn 1 chủ đề chưa viết, viết bài SEO 1500 từ theo style Meetup Travel,
lưu vào d:/blog/posts/YYYY-MM-DD.md
```

Claude sẽ hỏi:
- **Tên routine**: `viet-bai-hang-ngay`
- **Cron**: `0 8 * * *` (8h sáng hàng ngày)
- **Prompt**: nội dung công việc

#### Các cron mẫu thường dùng

| Cron | Ý nghĩa |
|---|---|
| `0 8 * * *` | 8h sáng mỗi ngày |
| `0 8 * * 1` | 8h sáng thứ Hai |
| `0 */3 * * *` | Mỗi 3 tiếng |
| `0 9 1 * *` | 9h sáng ngày 1 hàng tháng |
| `30 7 * * 1-5` | 7h30 thứ 2 đến thứ 6 |

#### Cách 2: Dùng `/loop` (chạy trong session hiện tại)

```
/loop 30m /kiem-tra-email
```

Cứ 30 phút chạy lệnh 1 lần cho tới khi bạn tắt.

#### Cách 3: Quản lý schedule đã tạo

- **Xem danh sách**: gõ `liệt kê schedule của tôi`
- **Xóa**: gõ `xóa schedule tên viet-bai-hang-ngay`
- **Chạy thử ngay**: gõ `chạy schedule viet-bai-hang-ngay ngay bây giờ`

---

### B. Workflow đề xuất viết bài SEO (module nâng cao sau)

#### Setup 1 lần:
1. Tạo folder `d:/meetup-blog/`
2. Trong đó có:
   - `topics.md` (danh sách chủ đề)
   - `style-guide.md` (quy tắc viết)
   - `posts/` (thư mục lưu bài)
3. Chạy `/init` trong folder, Claude tự tạo CLAUDE.md ghi nhớ style

#### Hàng ngày:
1. Mở Claude Code
2. Gõ: `viết bài về [chủ đề] theo style Meetup Travel, lưu vào posts/`
3. Xong

#### Tự động (không cần mở máy):
- Setup `/schedule` chạy sáng, Claude tự viết và push lên GitHub
- Sáng ra check email/GitHub xem bài mới
