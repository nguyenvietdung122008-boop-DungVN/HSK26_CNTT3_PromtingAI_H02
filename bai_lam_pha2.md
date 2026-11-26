# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:**Nguyễn Việt Dũng
- **Lớp:**CNTT3
- **Link repository Pha2:**https://github.com/nguyenvietdung122008-boop-DungVN/HSK26_CNTT3_PromtingAI_H02
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**Gemini

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
([
  {
    "loai_ve": "VECH",
    "ngay_choi": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_tu": "nho",
    "ghi_chu": null
  },
  {
    "loai_ve": "VECN",
    "ngay_choi": "2027-01-03",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_tu": null,
    "ghi_chu": "Một người đang bó bột tay"
  },
  {
    "loai_ve": "VEVIP",
    "ngay_choi": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_tu": "lon",
    "ghi_chu": "Một bạn đi xe lăn"
  }
])
```

**Link trò chuyện:**https://gemini.google.com/app/892ae557cf728af9?hl=vi

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
(Dưới đây là chi tiết tính toán cho đoàn trường theo từng bước dựa trên bảng giá và quy tắc soát vé:Tiền vé người lớn:Đoàn mua vé cả ngày (VECN), giá vé người lớn là 250.000 đồng/vé.Đoàn có 8 người lớn → Tiền vé người lớn = $8 \times 250.000 = \mathbf{2.000.000}$ đồng.Tiền vé trẻ em:Theo quy tắc 1, trẻ cao từ 1 m đến 1,4 m tính 60% giá vé người lớn: $250.000 \times 60\% = \mathbf{150.000}$ đồng/vé.Có 4 trẻ cao 1,05 m, 1,15 m, 1,2 m và 1,3 m (tất cả đều nằm trong khoảng từ 1 m đến 1,4 m) → $4 \times 150.000 = \mathbf{600.000}$ đồng.Có 2 bé cao dưới 1 m → Miễn phí (0 đồng).Tiền vé trẻ em = $600.000 + 0 = \mathbf{600.000}$ đồng.Tổng vé:Tổng tiền vé (trước giảm giá) = Tiền vé người lớn + Tiền vé trẻ em = $2.000.000 + 600.000 = \mathbf{2.600.000}$ đồng.Giảm giá đoàn:Theo quy tắc 2, đoàn từ 8 người lớn trở lên được giảm 10% trên tổng tiền vé (tiền vé người lớn + tiền vé trẻ em). Đoàn có đúng 8 người lớn nên đủ điều kiện áp dụng.Số tiền được giảm = $2.600.000 \times 10\% = \mathbf{260.000}$ đồng.Tiền vé sau giảm = $2.600.000 - 260.000 = \mathbf{2.340.000}$ đồng.Phụ thu:Theo quy tắc 3, phụ thu thuê áo phao là 40.000 đồng/chiếc và không được giảm giá.Đoàn thuê 6 áo phao → Phụ thu = $6 \times 40.000 = \mathbf{240.000}$ đồng.Tổng tiền:Theo quy tắc 4, Tổng tiền = Tiền vé sau giảm + Phụ thu = $2.340.000 + 240.000 = \mathbf{2.580.000}$ đồng.)
```

**Link trò chuyện:**https://gemini.google.com/app/3e5604305cc147ec?hl=vi

### b) Kiểm tra kết quả AI

([RESULT: 2.580.000 đồng] kết quả của AI đúng rồi)

## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
([
  {
    "loai_su_co": "dong_khu_choi",
    "so_khach": 4,
    "so_khu_bi_dong": 2,
    "tom_tat": "Khu trượt nước chính và khu sóng nhân tạo đóng cửa cả ngày 02/11/2026 nhưng website không thông báo trước cho đoàn 4 khách."
  },
  {
    "loai_su_co": "ve_sinh",
    "so_khach": 0,
    "so_khu_bi_dong": 0,
    "tom_tat": "Không có khiếu nại về vấn đề vệ sinh."
  },
  {
    "loai_su_co": "nhan_vien",
    "so_khach": 0,
    "so_khu_bi_dong": 0,
    "tom_tat": "Khách hàng khen ngợi nhân viên cứu hộ chu đáo, không có khiếu nại về nhân viên."
  }
])
```

**Link trò chuyện:**https://gemini.google.com/app/fb9581c30cfed855?hl=vi

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text


| Tiêu chí | Điểm | Minh chứng | Đề xuất sửa |
| --- | --- | --- | --- |
| **Đúng thông tin (50%)** | 2.5 / 5.0 | "Vé chiều bên em 150k thôi ạ" / "hoàn tiền mặt 100%" *(Chưa có dữ liệu chuẩn đối chiếu nên tạm trừ điểm rủi ro cam kết hoàn tiền mặt cứng nhắc, cần xác minh lại chính sách bảo lưu/hoàn tiền của công ty)* | "Dạ vé khung giờ chiều bên em có giá 150.000đ ạ. Trường hợp khu vui chơi đóng cửa do thời tiết xấu, bên em hỗ trợ hoàn tiền 100% (hoặc bảo lưu vé) theo quy định của công ty ạ." |
| **Đầy đủ (30%)** | 1.5 / 3.0 | "Cần gì ới em nhé!" *(Đã trả lời đủ 2 ý về giá vé và chính sách thời tiết, nhưng thiếu lời mời khách cung cấp ngày đi và số lượng vé để hỗ trợ đặt chỗ)* | "Chị dự định đi vào ngày nào và cần đặt bao nhiêu vé để em hỗ trợ giữ chỗ cho mình ạ?" |
| **Giọng điệu (20%)** | 0.5 / 2.0 | "Hello chị!", "mát rượi luôn", "nha", "ới em nhé!" *(Dùng từ ngữ suồng sã, thiếu tính chuyên nghiệp trong giao tiếp CSKH)* | "Dạ em chào chị ạ! ... Chị cần hỗ trợ thêm thông tin gì cứ nhắn em nhé ạ." |
| **TỔNG ĐIỂM** | **4.5 / 10** | | |


**Link trò chuyện:**https://gemini.google.com/app/4fed9808c0e510fe?hl=vi


```