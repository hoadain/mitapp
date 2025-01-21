# Hướng dẫn tạo ứng dụng với MIT App Inventor

## Mô tả ứng dụng
Ứng dụng bao gồm hai chức năng chính:
1. **Giới thiệu thông tin cá nhân** (Screen1): Hiển thị ảnh, thông tin cá nhân và phát nhạc MP3.
2. **Giải toán** (MathScreen): Chuyển sang màn hình giải các bài toán cơ bản.

---

## Các bước thực hiện

### Bước 1: Tạo màn hình chính (Screen1)
1. **Thêm ảnh và thông tin cá nhân:**
   - Thêm thành phần **Image** để hiển thị ảnh cá nhân.
   - Thêm thành phần **Label** để hiển thị họ tên.
   - Tải ảnh lên bằng cách nhấn **Upload File...** trong mục **Media**.

2. **Thêm Player để phát nhạc:**
   - Kéo thành phần **Player** từ mục **Media** vào giao diện (Player sẽ không hiển thị trên màn hình).
   - Tải file MP3 lên (nhấn **Upload File...**).

3. **Thêm nút phát nhạc:**
   - Kéo thành phần **Button** từ **User Interface** vào giao diện.
   - Đổi tên nút (ví dụ: `ButtonPlay`).
   - Đặt thuộc tính **Text** là "Phát nhạc".

4. **Lập trình phát/dừng nhạc:**
   - Chuyển sang tab **Blocks**.
   - Tạo khối lệnh như sau:
     ```plaintext
     When ButtonPlay.Click
       If Player1.IsPlaying
         Then Call Player1.Stop
         Else Call Player1.Start
     ```
cách này em vẫn đang mắc phải một số lỗi đang fix thêm ạ
5. **Thêm nút chuyển sang màn hình giải toán:**
   - Thêm một **Button** khác (ví dụ: `ButtonSwitch`).
   - Đổi thuộc tính **Text** là "Chuyển sang giải toán".
   - Lập trình khối lệnh chuyển màn hình:
     ```plaintext
     When ButtonSwitch.Click
       Call open another screen
       ScreenName: "MathScreen"
     ```
cái phần này em đang nghiên cứu thêm để chuyển qua trang khác mượt hơn
---

### Bước 2: Tạo màn hình giải toán (MathScreen)
1. **Thêm giao diện:**
   - **TextBox:** Thêm 2 ô nhập liệu (đổi tên thành `TextBox1`, `TextBox2`).
   - **Button:** Thêm các nút bấm cho các phép tính (Cộng, Trừ, Nhân, Chia) với tên tương ứng (`ButtonAdd`, `ButtonSubtract`, ...).
   - **Label:** Thêm một nhãn để hiển thị kết quả (tên là `LabelResult`).

2. **Lập trình các phép tính:**
   - Chuyển sang tab **Blocks**.
   - Tạo khối lệnh cho từng nút. Ví dụ, với nút Cộng:
     ```plaintext
     When ButtonAdd.Click
       Set LabelResult.Text to (TextBox1.Text + TextBox2.Text)
     ```
   - Lặp lại cho các nút Trừ, Nhân, Chia với phép tính tương ứng.

---

### Bước 3: tải ứng dụng trên điện thoại androi, còn về phần iphone thì chưa có app này, phần này em đã được rồi
1. **Kiểm tra ứng dụng:**
   - Kết nối điện thoại với MIT App Inventor bằng ứng dụng **MIT AI2 Companion**.
   - Quét mã QR để kiểm tra ứng dụng trực tiếp.
