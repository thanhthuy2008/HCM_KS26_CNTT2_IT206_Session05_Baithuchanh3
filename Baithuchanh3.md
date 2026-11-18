# Bài thực hành 3: Phân tích và giải quyết tình huống khách hàng khiếu nại

## 1. Prompt hoàn chỉnh

```
Bạn là chuyên viên chăm sóc khách hàng cho cửa hàng laptop, làm việc cẩn trọng, dựa trên dữ kiện.

Khiếu nại của khách:
"Tôi mua laptop cách đây 10 ngày. Máy thường xuyên bị nóng, quạt kêu to và pin chỉ sử dụng được khoảng 2 tiếng. Tôi đã mang đến cửa hàng kiểm tra nhưng nhân viên chỉ vệ sinh máy và trả lại. Sau 2 ngày, tình trạng vẫn tiếp diễn. Tôi muốn đổi máy hoặc hoàn tiền."

Quy tắc:
- Chỉ dùng thông tin trong khiếu nại. KHÔNG tự giả định chính sách đổi trả/bảo hành; nếu chưa có, ghi "Chưa xác định – cần đối chiếu chính sách".
- Gắn nhãn mọi nhận định: [DỮ KIỆN] (khách nêu), [GIẢ THUYẾT] (suy luận, cần kiểm chứng), [CHƯA XÁC ĐỊNH] (thiếu thông tin).
- Không kết luận nguyên nhân lỗi khi chưa có kết quả kiểm tra. Không hứa hẹn điều cửa hàng chưa xác nhận.

Hãy suy luận từng bước (Chain-of-Thought), không nhảy cóc:
Bước 1: Liệt kê sự kiện theo thời gian.
Bước 2: Xác định các vấn đề khách gặp.
Bước 3: Đánh giá mức độ nghiêm trọng từng vấn đề (Cao/TB/Thấp) kèm lý do.
Bước 4: Liệt kê thông tin còn thiếu cần xác minh.
Bước 5: Đề xuất đúng 2 phương án xử lý (ưu điểm, hạn chế).
Bước 6: Tự kiểm tra xem có suy diễn quá mức hoặc ngầm giả định chính sách không.
Bước 7: Soạn phản hồi gửi khách (khoảng 150 từ, đồng cảm, không cam kết đổi/hoàn tiền).

Trả lời bằng tiếng Việt, theo đúng thứ tự các bước.
```

## 2. Báo cáo phân tích

**Bước 1 – Sự kiện** (đều là lời khách, chưa kiểm chứng): mua máy ~10 ngày → máy nóng, quạt ồn, pin ~2 giờ → cửa hàng chỉ vệ sinh máy → 2 ngày sau lỗi vẫn còn → khách muốn đổi máy hoặc hoàn tiền.

**Bước 2 – Các vấn đề:** (1) máy nóng, (2) quạt ồn, (3) pin yếu, (4) lần xử lý đầu không hiệu quả, (5) yêu cầu đổi/hoàn tiền.

**Bước 3 – Mức độ nghiêm trọng**

| Vấn đề | Mức độ | Lý do |
|---|---|---|
| Máy nóng | Cao | Lỗi tái diễn sau xử lý, có thể ảnh hưởng độ bền [GIẢ THUYẾT] |
| Quạt ồn | Trung bình | Có thể liên quan máy nóng [GIẢ THUYẾT] |
| Pin ~2 giờ | Trung bình | Cần so với thông số hãng [CHƯA XÁC ĐỊNH] |
| Xử lý lần 1 không hiệu quả | Cao (dịch vụ) | Khách quay lại nhiều lần, dễ leo thang khiếu nại |
| Đổi/hoàn tiền | Cao | Phụ thuộc chính sách [CHƯA XÁC ĐỊNH] |

## 3. Thông tin cần xác minh

- [ ] Hóa đơn, ngày mua, model, số serial
- [ ] Hồ sơ lần tiếp nhận trước (nhân viên đã làm gì, có biên nhận không)
- [ ] Kết quả kiểm tra: nhiệt độ, quạt, dung lượng pin so với thông số hãng
- [ ] Cách khách sử dụng (tác vụ, độ sáng, chế độ nguồn)
- [ ] Tình trạng máy (có dấu hiệu rơi, vào nước, tác động vật lý không)
- [ ] Chính sách đổi trả/hoàn tiền/bảo hành của cửa hàng (không tự giả định)

## 4. Hai phương án xử lý

| | Phương án A: Kiểm tra trước, quyết định sau | Phương án B: Xử lý song song |
|---|---|---|
| Nội dung | Tiếp nhận máy, kiểm tra chuyên sâu, lập biên bản, rồi mới sửa/đổi/hoàn tiền theo chính sách | Kiểm tra ưu tiên, đồng thời chuyển ngay yêu cầu đổi/hoàn tiền lên quản lý xem xét |
| Ưu điểm | Có căn cứ rõ ràng, giảm rủi ro cho cửa hàng | Nhanh, giữ được khách, giảm nguy cơ leo thang |
| Hạn chế | Khách phải chờ thêm, chưa đáp ứng ngay yêu cầu | Chỉ làm được nếu chính sách cho phép; có thể tốn chi phí, tạo tiền lệ |

**Gợi ý:** bắt đầu bằng A; chuyển sang B nếu quản lý xác nhận chính sách cho phép.

 **Phản hồi gửi khách hàng**

> Kính gửi Anh/Chị,
>
> Cảm ơn Anh/Chị đã phản hồi. Chúng tôi rất tiếc vì chiếc laptop chưa đáp ứng kỳ vọng và lần xử lý trước chưa giải quyết được vấn đề.
>
> Để xử lý chính xác, Anh/Chị vui lòng cung cấp hóa đơn (hoặc SĐT đã dùng khi mua) và mang máy đến để kỹ thuật viên kiểm tra chuyên sâu, có biên bản ghi nhận.
>
> Sau khi có kết quả và đối chiếu chính sách áp dụng, chúng tôi sẽ thông báo cụ thể các hướng giải quyết, bao gồm đề nghị đổi máy hoặc hoàn tiền của Anh/Chị.
>
> Trân trọng,
> [Tên nhân viên] – Bộ phận Chăm sóc khách hàng
