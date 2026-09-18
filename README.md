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

Khung sửa nội dung **được khoá**, bé vào học bình thường sẽ không nhìn thấy. Chị mở bằng cách thêm `?edit=1` vào cuối địa chỉ trang, ví dụ:

```
https://<tên-tài-khoản>.github.io/<tên-repo>/?edit=1
```

Trang sẽ hỏi mã khoá — mặc định là `1234` (đổi ở dòng `const MA_KHOA_CUA_CO = "1234";` đầu vùng dữ liệu trong `index.html`). Nhập đúng thì cuối phần Từ vựng và Mẫu câu hiện khung **Sửa nội dung**, có hai chỗ cần phân biệt:

- **Sửa từng ô** — mỗi từ/câu là một hàng có ô riêng cho tiếng Nhật, romaji, nghĩa tiếng Việt; có nút xoá từng dòng, thêm dòng, thêm/xoá cả chủ đề. Dễ nhìn, không lo gõ sai dấu `|`.
- **Sửa dạng văn bản** — cho ai quen gõ nhanh, mỗi dòng viết `tiếng Nhật | romaji | nghĩa tiếng Việt`, dòng bắt đầu bằng `#` là tên chủ đề mới. Hai chế độ đồng bộ dữ liệu với nhau, chuyển qua lại được.

Sau khi sửa xong, có ba nút:

1. **Lưu tạm trên máy này** — xem thử ngay trên trình duyệt đang mở, nhưng chỉ máy này thấy, chưa đụng tới file gốc trên GitHub.
2. **Xuất mã cho GitHub** — hiện ra khối mã đã format sẵn kèm nút **Sao chép**. Chị chép khối này, qua GitHub mở `index.html` (bấm bút chì để sửa), tìm dòng `const VOCAB_DEFAULT = \`` (phần từ vựng) hoặc `const SENT_DEFAULT = \`` (phần mẫu câu), dán đè lên toàn bộ nội dung nằm giữa hai dấu `` ` `` ngay sau dòng đó, rồi bấm **Commit changes**. Khoảng một phút sau, **mọi máy** mở link — kể cả máy của bé — đều thấy nội dung mới.
3. **Khôi phục nội dung gốc** — quay lại đúng nội dung đang có trong file, bỏ hết chỗ vừa sửa tạm.

Nút **Tải về file .txt** để giữ lại một bản phòng khi cần.

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
