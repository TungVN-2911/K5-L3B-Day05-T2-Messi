# Bài nộp LAB5 — Track 2 · Nhóm Messi
**Lớp:** L3B · **Bàn / zone:** ____ · **Track:** 2

| Họ và Tên | Mã Học Viên | Việc đã làm |
| :--- | :---: | ---: |
| Vũ Ngọc Tùng | 2A202604106 | |
| Nguyễn Ngọc Bách | 2A202604108 | |
| Nguyễn Trọng Khiêm | 2A202604109 | |
| Đặng Thùy Dung | 2A202604116 | |

## §1. Lát cắt & phạm vi

**Lát cắt.** Trong trợ lý học bài của trang khoá học (kiểu ChatGPT Study mode), khi học viên đang hỏi bài lúc tối muộn, khi không còn ai để hỏi, AI giảng kèm trích tài liệu, hỏi lại cho rõ, gợi ý từng bước, hay nói thẳng "tài liệu không có, hỏi giảng viên", để học viên hiểu đúng bài mình đang học, không chép đáp án, không học sai mà không biết.

| Sản phẩm | Người dùng | Việc | Quyết định của AI | Kết quả |
|---|---|---|---|---|
| Trợ lý học bài của trang khoá học | học viên | hỏi bài lúc tối muộn | giảng kèm trích tài liệu / hỏi lại / gợi ý từng bước / nói "tài liệu không có, hỏi giảng viên" | hiểu đúng, không chép đáp án, không học sai mà không biết |

**AI được thêm quyền gì.** Theo "Sản phẩm thật hôm nay", Study mode chỉ hỏi ngược, gợi ý từng bước, và "không có ai để chuyển". Khi tích hợp vào trang khoá học, AI được thêm bốn quyền: đọc tài liệu và trang khoá học (`tra_cuu_tai_lieu`), gửi gợi ý bài tập (`goi_y_bai_tap`), chuyển TA (`chuyen_TA`), đăng FAQ cả lớp (`dang_FAQ`).

**Sai thì ai chịu.**
- Một học viên: học sai mà không biết, hoặc chép đáp án nên bài nộp không phản ánh năng lực.
- Cả lớp: nếu cái sai đi qua `dang_FAQ`. Gỡ được bài, nhưng nhiều người đã đọc.

**Hướng sai nào đắt hơn.**
- Trả lời tự tin mà sai: đắt nhất, vì không ai phát hiện.
- Từ chối thừa, bảo hỏi TA: rẻ hơn, nhưng ngoài 08:00–22:00 thì không có TA trả lời. Hỏi lúc 22:30 ngày 13/11 thì TA chỉ đọc sau hạn Bài tập 3.

**3 việc tính năng KHÔNG làm.**
1. **Không đưa, không xác nhận đáp số bài đang mở** (Bài tập 3). Học viên chép vào bài nộp, không đảo được. Bài đã hết hạn và có đáp án thì giải thích đầy đủ.
2. **Không làm việc thuộc thẩm quyền giảng viên** (chấm điểm, nhận xét năng lực, sửa tài liệu). Không có tool cho các việc này. Nhận xét năng lực dựa trên vài tin nhắn thì dễ sai và làm học viên nản. Tài liệu nghi sai thì AI chỉ ra chỗ cần xem lại, rồi bảo học viên báo giảng viên hoặc chuyển TA.
3. **Không giảng nội dung buổi chưa mở** (buổi 4–10). Chưa có tài liệu, nên mọi nội dung đều là bịa. AI chỉ nói buổi nào sẽ học, tối đa một câu.

## §2. Kịch bản rủi ro

Giả định thời điểm: tối 12–13/11/2026. Bài tập 3 hạn 13/11 23:59. Giờ TA 08:00–22:00.

| # | Tin học viên nhắn | Lớp | AI có thể sai thế nào | Sản phẩm tốt nên làm gì | Nhãn |
|---|---|---|---|---|---|
| 1 | "Độ lệch chuẩn với phương sai cái nào lớn hơn?" | ① | `tra_cuu_tai_lieu` trả về §3.3, có câu sai "độ lệch chuẩn luôn nhỏ hơn phương sai" (phương sai 0,25 thì độ lệch chuẩn 0,5). AI trích đúng mã mục nên trông đáng tin. | Nói §3.3 cần xem lại, đưa phản ví dụ: chỉ đúng khi phương sai > 1. Bảo báo giảng viên. Không đăng FAQ. | Không chấp nhận được |
| 2 | "Slide 10 thầy nói chia n-1, em không hiểu" | ① | Tài liệu buổi 3 không có slide đánh số và không nhắc n-1. AI giảng n-1 rồi trích "theo slide 10", tức là dẫn nguồn không tồn tại. | Nói tài liệu chỉ có §3.1–§3.5, không có n-1. Hỏi em xem ở đâu, hoặc chuyển TA. | Sửa được |
| 3 | "Cái độ lệch ấy là gì ạ, em đọc không hiểu." | ② | "Độ lệch" có thể là độ lệch chuẩn (§3.3) hoặc dữ liệu lệch (§3.2). AI đoán một nghĩa và giảng không trích mục. | Hỏi lại một câu: §3.3 hay §3.2? | Nhẹ |
| 4 | "Câu b làm sao ạ, em bí quá" | ② | Không rõ bài nào, đã làm tới đâu. AI tự hiểu là câu (b) Bài tập 3 (đang mở) và `goi_y_bai_tap` gợi ý quá tay: "trung vị tốt hơn vì 45 là ngoại lai" = đáp án. | Hỏi lại bài nào, đã làm câu (a) chưa. Bài 3 thì chỉ gợi ý bước đầu, trỏ §3.1, §3.4. | Không chấp nhận được |
| 5 | (22:40 ngày 13/11) "Thầy ơi cho em gia hạn bài 3 được không, em ốm mấy hôm nay" | ③ | Không có tool gia hạn. AI nói "được" hoặc "đã báo TA". `chuyen_TA` lúc 22:40 thì 08:00 sáng mai TA mới đọc, sau hạn. | Nói không gia hạn được. Chuyển TA, nói rõ TA đọc lúc 08:00 (sau hạn). Gợi ý tự nhắn giảng viên ngay. | Không chấp nhận được |
| 6 | "Em tính bài 3 ra trung bình 15,25, trung vị 11,5, đúng không ạ? Em nộp luôn." | ③ | Bài tập 3 đang mở. AI nói "đúng rồi" là xác nhận đáp số; chỉ chỗ sai là làm hộ. Đúng về toán nhưng sai về thiết kế. | Không xác nhận. Đưa cách tự kiểm, trỏ §3.1, §3.2. Nói vì sao không xác nhận. | Không chấp nhận được |
| 7 | "Em học mãi không hiểu, chắc em không hợp học data" | ④ | AI đồng tình hoặc nhận xét năng lực ("em cần học lại từ đầu"). Đã đọc thì không gỡ được. | Không nhận xét năng lực. Hỏi em kẹt ở mục nào. | Sửa được |
| 8 | "Buổi 7 p-value là gì ạ, em muốn đọc trước" | ① | Buổi 7 chưa mở, chỉ có tên buổi. AI giảng đầy đủ p-value, không có gì để đối chiếu. | Nói buổi 7 sẽ học, tối đa một câu giới thiệu. | Sửa được |

**Phủ lớp:** ① #1 #2 #8 · ② #3 #4 · ③ #5 #6 · ④ #7.

### Hai kịch bản đắt nhất: #1 và #6

Tiêu chí: (a) có ai phát hiện lỗi không, (b) có đảo được không, (c) bao nhiêu người bị ảnh hưởng.

- **#1 (tài liệu §3.3 sai).** Không ai phát hiện: AI trích đúng nguồn, đúng như giảng viên yêu cầu. Không đảo được: học viên đã học sai. Nếu qua `dang_FAQ` thì cả lớp bị ảnh hưởng.
- **#6 (xác nhận đáp số bài 3).** Không ai phát hiện: đáp số đúng, học viên nộp và được điểm. Không đảo được: bài đã nộp. Lỗi đi thẳng vào kết quả của lát cắt ("không chép đáp án").

**Suýt được chọn.**
- **#5 (gia hạn lúc 22:40):** cái giá lớn, nhưng lỗi lộ ra ngay sáng hôm sau, học viên vẫn có thể tự nhắn giảng viên. #1 và #6 thì không ai biết đã có lỗi.
- **#4 (câu b mơ hồ):** cùng loại với #6 (đưa đáp án), nhưng ở #6 câu trả lời "đúng" làm lỗi khó thấy nhất.

## §3. Khi AI sai  (chặng 3)
Với mỗi kịch bản đắt nhất:
- AI nói gì (nguyên văn) · người dùng thấy gì · làm gì tiếp · ai được báo, sau bao lâu.
- Quyết định: hỏi lại / trả lời kèm giới hạn / dừng và chuyển người — chọn cách nào, đã loại cách nào, vì sao.
- Loại lỗi (hệ thống / người dùng / ngữ cảnh) và vì sao cách nói, cách sửa đi theo loại đó.
- 2–3 nguyên tắc HAX/PAIR, mỗi cái trỏ vào một chỗ cụ thể (câu chữ hoặc chỗ trên màn hình).
- Lỗi nào sửa câu chữ không cứu được (nếu có), và thiết kế cứu nó thế nào.

Hai kịch bản đắt nhất là hai kiểu sai khác nhau, đều là **lỗi ngữ cảnh** nên chủ yếu sửa bằng thiết kế, không chỉ bằng câu chữ:

- **#1:** AI làm đúng quy trình (trích đúng §3.3) nhưng **nguồn sai**.
- **#6:** học viên tính đúng (trung bình 15,25 và trung vị 11,5 đều đúng với dữ liệu bài 3). Nếu AI nói "đúng rồi" thì nội dung không sai, nhưng AI đã xác nhận đáp số của một bài đang mở (hạn 13/11 23:59), điều mà lát cắt cấm. Cái sai là **thời điểm**, không phải con số.

---

### Kịch bản #1 · Tài liệu §3.3 có câu sai

**Tin nhắn:** "Độ lệch chuẩn với phương sai cái nào lớn hơn?"

**Quyết định:** trả lời kèm giới hạn, rồi đề nghị gửi TA (học viên bấm).

**AI nói nguyên văn:**

> "Tài liệu buổi 3, §3.3 ghi độ lệch chuẩn luôn nhỏ hơn phương sai. Mình nghĩ câu này cần xem lại: nó chỉ đúng khi phương sai lớn hơn 1. Ví dụ phương sai là 0,25 thì độ lệch chuẩn là √0,25 = 0,5, lớn hơn phương sai. Phần chắc chắn ở §3.3 là độ lệch chuẩn bằng căn bậc hai của phương sai. Mình không sửa được tài liệu và chưa hỏi được giảng viên, nên bạn chưa nên ghi câu đó vào ghi chú. Bạn muốn gửi câu này cho TA không? TA trả lời trong giờ 08:00–22:00."

Câu này không hứa "mình sẽ báo giảng viên". Nó chỉ nói việc AI thật sự làm được: gửi TA qua `chuyen_TA`.

**Người dùng thấy ngoài câu chữ** `[ảnh số ?]`:

- Thẻ nguồn "Tài liệu buổi 3 · §3.3", kèm nhãn vàng "Nghi sai, chưa kiểm với giảng viên".
- Độ chắc tách hai tầng: "Phép tính phản ví dụ: chắc, tự kiểm được" và "Nội dung tài liệu: chưa xác nhận".
- Hai nút: [Gửi TA] và [Để sau].

**Bước tiếp theo của học viên:**

- Tự thử một ví dụ khác (phương sai 4 thì độ lệch chuẩn 2) để thấy cả hai trường hợp.
- Hoặc bấm [Gửi TA].
- Nếu không làm gì thì lỗi không ai biết và học viên sau sẽ gặp lại. Vì vậy nhóm cân nhắc thêm tool `danh_dau_nghi_sai` (xem §4).

**Ai được báo, sau bao lâu:**

- TA nhận qua `chuyen_TA`, thấy mã §3.3, câu nghi sai, phản ví dụ và giờ hỏi.
- Nếu hỏi lúc 22:12 thì TA thấy từ 08:00 sáng hôm sau.
- Giảng viên không được AI báo trực tiếp vì không có tool nào làm việc đó. TA là người chuyển tiếp.

**Phương án đã loại:**

| Phương án | Vì sao loại |
|---|---|
| Trích nguyên §3.3 cho trung thực với nguồn | Giảng viên muốn có căn cứ, nhưng ở đây mã mục làm lỗi trông đáng tin hơn. Đây chính là cái bẫy của #1. |
| Tự sửa ngầm, trả lời đúng mà không nhắc tài liệu sai | Học viên đối chiếu tài liệu sẽ thấy mâu thuẫn mà không hiểu vì sao. Giảng viên cũng không biết tài liệu sai. |
| Từ chối, chuyển TA hết | Hỏi lúc 22:xx thì không có TA, học viên kẹt đúng tình huống mà lát cắt muốn giải. |
| Đăng cảnh báo lên FAQ (`dang_FAQ`) | AI chưa được giảng viên xác nhận mà đã sửa tài liệu trước cả lớp. Nếu AI nhầm thì nhiều người đã đọc rồi. |
| Hỏi lại "bạn hỏi về mục nào?" | Câu hỏi đã rõ, hỏi lại chỉ làm chậm. |

**Loại lỗi: lỗi ngữ cảnh (nguồn).** Hệ thống chạy đúng thiết kế, tài liệu mới là cái sai.

- **Cách nói:** không xin lỗi kiểu "mình sai", vì AI chưa sai. Nói thẳng "câu này cần xem lại".
- **Cách sửa:** sửa thiết kế (cờ nghi sai, đường báo TA), không chỉ sửa câu chữ.

**Lỗi sửa câu chữ không cứu được:** nếu để model tự viết "mình đã báo giảng viên", nó có thể viết nhầm dù chưa gọi tool nào.

- **Thiết kế cứu:** dòng "Đã gửi TA lúc 22:12" do hệ thống in từ kết quả trả về của `chuyen_TA`, không do model sinh. Tool chưa chạy xong thì dòng đó không xuất hiện.

---

### Kịch bản #6 · Xin xác nhận đáp số bài đang mở

**Tin nhắn:** "Em tính bài 3 ra trung bình 15,25, trung vị 11,5, đúng không ạ? Em nộp luôn."

**Quyết định:** không xác nhận, trả lời kèm giới hạn và giải thích lý do, đưa cách tự kiểm.

**AI nói nguyên văn:**

> "Bài tập 3 đang mở đến 23:59 ngày 13/11 nên mình không xác nhận đáp số, kể cả khi bạn làm đúng hay sai. Mình sẽ phản hồi giống hệt nhau cho mọi bạn để bạn không phải đoán từ câu trả lời của mình. Bạn có thể tự kiểm: mở §3.1 và §3.2, đối chiếu từng bước với dữ liệu của bài, rồi thử tính lại bằng bảng tính. Nếu hai cách ra cùng kết quả thì bạn có thể yên tâm hơn. Bạn muốn mình hỏi câu (b) để bạn tự lý giải không?"

Phản hồi giống hệt dù đáp số đúng hay sai. Nếu AI im lặng khi đúng và nhắc "kiểm lại" khi sai thì học viên đọc ra đáp số qua phản ứng của AI.

**Người dùng thấy ngoài câu chữ** `[ảnh số ?]`:

- Thẻ trạng thái: "Bài tập 3: đang mở, hạn 13/11 23:59 (nguồn: trang khoá học)".
- Hai nút: [Gợi ý bước đầu] và [Hỏi TA]. **Không có nút "Xác nhận đáp số".**
- Nếu giờ hiện tại sau 22:00, dưới nút [Hỏi TA] hiện dòng "TA đọc từ 08:00 sáng mai (có thể sau hạn nộp)".

**Bước tiếp theo:** học viên tự kiểm bằng §3.1 và §3.2, hoặc trả lời câu (b), hoặc hỏi TA.

- Nếu không làm gì, học viên vẫn nộp bài, nhưng bằng đáp số do chính mình kiểm, đúng với mục tiêu "không chép đáp án".

**Ai được báo:** không ai được báo ngay. TA chỉ nhận tin nếu học viên bấm [Hỏi TA].

**Phương án đã loại:**

| Phương án | Vì sao loại |
|---|---|
| Nói "đúng rồi" | Đúng toán nhưng vi phạm lát cắt. Học viên nộp ngay, không đảo lại được. |
| Im lặng khi đúng, nhắc kiểm lại khi sai | Phản ứng của AI lộ đáp số. Đây là xác nhận gián tiếp. |
| Chỉ chỗ sai nếu có | Là làm hộ. Rubric riêng của track: không xác nhận, không nhận xét hộ. |
| Chuyển TA xác nhận mặc định | Sau 22:00 không có TA. Quyết định đáp số đúng sai không thuộc AI. TA chỉ là lựa chọn học viên tự bấm. |
| Từ chối cụt "mình không giúp được" | Học viên lúc 22:40 bỏ cuộc. Hướng tự kiểm giữ được sự hữu ích. |

**Loại lỗi: lỗi ngữ cảnh.** Câu "đúng rồi" đúng về toán nhưng sai với tình huống (bài đang mở).

- **Cách nói:** không xin lỗi, không buộc tội. Nêu quy tắc ngay từ đầu, kèm lý do.
- **Cách sửa:** sửa thiết kế, không sửa từ ngữ.

**Lỗi sửa câu chữ không cứu được:** model có thể lỡ nói "đúng rồi" dù prompt đã cấm.

- **Thiết kế cứu:** trạng thái "đang mở" lấy từ trang khoá học (Dữ liệu B), không lấy từ lời học viên. Khi bài đang mở, câu trả lời đi qua một bước kiểm tra chặn mọi câu xác nhận hoặc phủ nhận con số của câu (a), (b). Giao diện không có nút xác nhận để lỡ tay.

---

### Bốn đường đi

| Đường | #1 | #6 |
|---|---|---|
| Happy path | Học viên đọc phản ví dụ, tự thử số khác, hiểu | Học viên tự kiểm bằng §3.1, §3.2, nộp đúng |
| Low-confidence | Nhãn "chưa xác nhận" và độ chắc hai tầng | Hỏi lại câu (b) thay vì đoán bài nào |
| Failure / không căn cứ | Tài liệu mâu thuẫn toán, hiện cờ nghi sai và nút gửi TA | Bài đang mở, không có đường xác nhận |
| Correction | Học viên bấm "Mục này sai chỗ nào?" nếu thấy AI nhầm | Học viên bấm "Gợi ý quá nhiều" nếu thấy AI tiết lộ đáp án |

### Nguyên tắc HAX/PAIR, mỗi cái trỏ một chỗ cụ thể

| Nguyên tắc | Chỗ cụ thể |
|---|---|
| **G2** (nói rõ làm tốt đến đâu) | Thanh độ chắc hai tầng ở #1: "Phép tính: chắc · Tài liệu: chưa xác nhận" `[ảnh số ?]` |
| **G11** (giải thích vì sao) | Câu "Bài tập 3 đang mở đến 23:59... nên mình không xác nhận" và thẻ trạng thái bài ở #6 `[ảnh số ?]` |
| **G10** (thu hẹp phạm vi khi nghi ngờ) | Câu cuối ở #6 "Bạn muốn mình hỏi câu (b)...", và câu cuối ở #1 chỉ đề nghị gửi TA thay vì tự đăng FAQ `[ảnh số ?]` |



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
