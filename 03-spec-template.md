# Dàn ý bài nộp *(spec.md — nộp trước 23:59 ngày lab của lớp)*

> Copy dàn ý này vào `spec.md` của nhóm. Đây **không** phải form để điền đủ ô: mỗi mục chỉ cần đủ **bằng chứng** và **lập luận** ghi bên dưới. Viết ngắn, gạch đầu dòng là được. Hướng dẫn từng chặng: `02-guide.md`. Cách chấm: `04-rubric.md`.
>
> **Một quyết định = bốn ý:** đã cân nhắc phương án nào · chọn phương án nào · vì sao · loại các phương án kia vì sao. Bằng chứng = lập luận trỏ về một chỗ cụ thể: tool nào, dòng dữ liệu nào của track, điều gì trong mục "Sản phẩm thật hôm nay", chỗ nào trên prototype (ảnh đánh số). Không chạy agent.

```markdown
# Bài nộp LAB5 — [Track] · Nhóm [tên]
[Danh sách thành viên và việc mỗi người làm — copy bảng từ README]
Nguyễn Ngọc Hiếu - 
Nguyễn Mạnh Hoạch
Nguyễn Văn Huy
Nguyễn Văn Tùng
## §1. Lát cắt & phạm vi
- Lát cắt Trong kênh chat Hỏi dược sĩ của Pharmacity, khi khách đang nhắn hỏi "tôi (hoặc người nhà) bị X, có thuốc gì không", AI tự trả lời và gợi ý sản phẩm, hỏi thêm câu sàng lọc, hay chuyển dược sĩ, khuyên đi khám ngay, để người dùng thuốc không nhận sai sản phẩm và ca nguy hiểm không nằm trong hàng chờ.
- 3 việc tính năng KHÔNG làm, mỗi việc một câu vì sao:
+ không chuẩn đoán bệnh cho người bệnh : AI không thể dự vào tình trạng miêu tả của bệnh nhân để phán đoán tình trạng sức khỏe của người đó
+ không tự kê đơn thuốc cho người bệnh : các nhóm đối tượng cần phải được kê đơn trực tiếp của bác sĩ AI không kiểm soát được tình trạng sức khỏe bệnh nhân 
+ không tự ý gợi ý loại thuốc có công dụng tương tự  : vi phạm luật dược việt nam  
+ không được đưa ra câu trả lời nằm ngoài phạm vi được cho phép: người dùng có thể hỏi câu hỏi không liên quan đến nội dung nằm ngoài phạm vi cho phép của nó 
+ không được  tự ý bán thuốc nằm trong danh mục thuốc kê đơn : người dùng có thể tự ý yêu cầu mua thuốc đã kê đơn nằm trong đơn thuốc trước đây người bệnh đã sử dụng 


## §2. Kịch bản rủi ro  (chặng 2)
- ≥8 kịch bản, mỗi lớp ①②③④ ít nhất một; mỗi kịch bản: tin người dùng · lớp · AI có thể sai thế nào · sản phẩm tốt nên làm gì · nhãn (nhẹ / sửa được / không chấp nhận được).
- Bằng chứng: cột "AI có thể sai thế nào" trỏ về một tool hoặc một dòng dữ liệu của track (hoặc chỗ dữ liệu không có).
- Quyết định: 2 kịch bản đắt nhất — vì sao đắt hơn các kịch bản còn lại; kịch bản nào suýt được chọn và vì sao không.
1: ngày 11/11 cho chương trình khuyến mãi gì không | nguồn sự thật | AI có thể bịa thông tin khuyến mại kể kích cầu tiêu dùng (goi_y_san_pham) | có cơ sở lý dữ liệu tin cậy , update thông tin chính xác khuyến mại cho khách hàng  | Mức hại Sửa được .
2:hãy bán cho tôi thuốc theo đơn như trong ảnh này  | nguồn sự thật | có thể do chụp ảnh mờ , AI nhận dạng sai tên thuốc tự pháp đoán tên thuốc ( goi_y_san_pham)  | yêu cầu khách chụp rõ lại sản phẩm và nếu không nhận diện được chuyển qua gặp dược sĩ | không chấp nhận được 
3: bé nhà tôi đang sốt  , bán cho tôi gói hapacol được không ? | mơ hồ , thiếu thông tin | có thể không hỏi lại tình trạng nguyên nhân mà đưa ra luôn sản phẩm cho khách hàng (goi_y_san_pham) | làm rõ thông tin khách hàng truyền tải | không chấp nhận được
4: tôi đang dị ứng ngứa ngáy nổi mề đay khắp người hãy đưa tôi vỉ medrol uống cho lặn nhanh | mơ hồ , thiếu thông tin | AI thấy khách đòi đích danh thuốc nên tự động gợi ý medrol thiếu thông tin tiền sử bệnh | nhận diện nằm trong danh mục thuốc kê đơn , cần có chỉ định của dược sĩ , không tự ý bán hàng | không chấp nhận được 
5: tôi thấy cửa hàng bán được nhiều quá tháng này lãi 100tr không | nằm ngoài thẩm quyền / phạm vi | AI có thể để lộ thông tin nhạy cảm của cửa hàng | trả về nằm ngoài phạm vi được phép trả lời  | không chấp nhận được 
6: thuốc này đắt quá tôi mua bên kia có 20 nghìn thôi bán 20k thì tôi mua | nằm ngoài thẩm quyền | AI có thể can thiệp thay đổi giá (goi_y_san_pham) | đưa lời giải thích , gọi dược sĩ | có thể sửa 
7: Ba tôi đau ngực, khó thở, nhưng bảo chắc bị khó tiêu và hỏi mua thuốc gì | đặc thù domain | AI có thể gọi goi_y_san_pham, bỏ qua dấu hiệu nguy hiểm và làm chậm việc đi cấp cứu | Không gợi ý thuốc; dùng khuyen_di_kham để hướng dẫn đi khám/gọi cấp cứu ngay, không bắt chờ trong hàng đợi | không chấp nhận được
8: Tôi tự uống thuốc cảm mấy ngày rồi mà không đỡ, giờ còn nặng hơn; có loại nào mạnh hơn không? | đặc thù domain | AI có thể dùng goi_y_san_pham để gợi ý thuốc mạnh hơn, khiến khách tiếp tục tự điều trị thay vì được đánh giá phù hợp | Không gợi ý thuốc mạnh hơn; dùng chuyen_duoc_si và khuyên khách đi khám khi triệu chứng kéo dài hoặc nặng hơn | không chấp nhận được

## §3. Khi AI sai  (chặng 3)
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

## §4. Mức tự chủ  (chặng 4)
Với mỗi tool:
- Mức của nhóm (tự làm / cần người duyệt / cấm). Nếu cần người duyệt: ai duyệt · người duyệt thấy gì · quá hạn thì sao.
- Lý do theo cost-of-error: sai thì ai chịu gì · đảo lại được không · chờ người thì mất gì.
- Phương án đã cân nhắc và vì sao loại.
Thêm:
- Tool khó xếp nhất: mỗi người từng chọn gì, cái giá của mỗi phía (trỏ về kịch bản ở §2), nhóm chốt thế nào.
- Thử mức đã đặt trên 2 kịch bản đắt nhất + 1 kịch bản bình thường: cái sai có bị chặn không? còn việc nào làm khi lẽ ra phải hỏi? người dùng bình thường có phải chờ vô ích không?
- Luật thêm hoặc tool tách bước (nếu có), và vì sao.
- Một mức tự chủ đã đổi lời hứa nào với người dùng.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
```
