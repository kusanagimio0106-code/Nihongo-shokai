# にほんご — App dạy tiếng Nhật sơ cấp cho bé

Một trang web duy nhất (`index.html`), không cần cài gì, chạy thẳng trên GitHub Pages.

- **Bảng chữ cái** — Hiragana và Katakana (chữ cơ bản, biến âm, âm ghép). Bấm vào một chữ để xem hình động thứ tự nét viết, số thứ tự từng nét và phiên âm romaji.
- **Từ vựng** — 12 chủ đề cơ bản, có bài tập trắc nghiệm.
- **Mẫu câu** — 6 tình huống giao tiếp, có bài tập trắc nghiệm.

## Đưa lên GitHub Pages

1. Tạo một repository mới trên GitHub (để **Public**).
2. Bấm **Add file → Upload files**, kéo `index.html` và `README.md` vào, rồi **Commit changes**.
3. Vào **Settings → Pages**. Ở mục *Source* chọn **Deploy from a branch**, branch **main**, thư mục **/ (root)**, bấm **Save**.
4. Đợi khoảng một phút, địa chỉ web sẽ là:
   `https://<tên-tài-khoản>.github.io/<tên-repo>/`

Mở địa chỉ đó trên điện thoại hay máy tính bảng là dùng được ngay, thêm vào màn hình chính cho bé càng tiện.

## Sửa nội dung từ vựng và mẫu câu

Có hai cách, tuỳ lúc:

Khung sửa nội dung **được khoá**, bé vào học bình thường sẽ không nhìn thấy.

**Cách nhanh (sửa tạm trên máy đang dùng).** Thêm `?edit=1` vào cuối địa chỉ trang, ví dụ:

```
https://<tên-tài-khoản>.github.io/<tên-repo>/?edit=1
```

Trang sẽ hỏi mã khoá — mặc định là `1234`. Nhập đúng thì cuối phần Từ vựng và Mẫu câu hiện khung **Sửa nội dung**, gõ vào ô rồi bấm **Lưu**. Nội dung lưu trong trình duyệt của máy đó, không ảnh hưởng máy của bé. Nút **Tải về file .txt** giúp giữ lại bản đã sửa.

Đổi mã khoá: mở `index.html`, sửa dòng `const MA_KHOA_CUA_CO = "1234";` ở đầu vùng dữ liệu.

**Cách chính thức (sửa hẳn trong app, mọi máy đều thấy).** Trên GitHub mở `index.html`, bấm biểu tượng bút chì, tìm dòng:

```
/* ===============  VÙNG DỮ LIỆU — CÔ SỬA Ở ĐÂY  =============== */
```

Bên dưới là hai khối `VOCAB_DEFAULT` và `SENT_DEFAULT`. Sửa xong bấm **Commit changes**, khoảng một phút sau trang web tự cập nhật.

### Cách viết nội dung

Mỗi dòng một mục, ba phần ngăn bằng dấu `|`:

```
tiếng Nhật | romaji | nghĩa tiếng Việt
```

Dòng bắt đầu bằng `#` là tên một chủ đề mới. Ví dụ:

```
# Trái cây
りんご | ringo | quả táo
バナナ | banana | quả chuối
```

Lưu ý: nếu trước đó đã bấm **Lưu** ở khung “Sửa nội dung”, máy đó sẽ ưu tiên bản lưu trong trình duyệt. Bấm **Khôi phục nội dung gốc** để quay lại bản trong `index.html`.

## Bản quyền dữ liệu nét viết

Đường nét chữ lấy từ [KanjiVG](http://kanjivg.tagaini.net) của Ulrich Apel, giấy phép [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). Khi chia sẻ lại xin giữ phần ghi công ở cuối trang.
