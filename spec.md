# Bài nộp LAB5 — Track 2 · Nhóm Messi
**Lớp:** L3B · **Bàn / zone:** ____ · **Track:** 2

| Họ và Tên | Mã Học Viên | Việc đã làm |
| :--- | :---: | ---: |
| Vũ Ngọc Tùng | 2A202604106 | |
| Nguyễn Ngọc Bách | 2A202604108 | |
| Nguyễn Trọng Khiêm | 2A202604109 | Chặng 4: mức tự chủ cho bốn tool, đối chiếu ba kịch bản và quy tắc bàn giao UX/prototype. |
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
- Từ chối thừa, bảo hỏi TA: rẻ hơn, nhưng ngoài 08:00–22:00 thì phải chờ ca trực tiếp theo. Hỏi lúc 22:30 ngày 13/11 thì ca trực tiếp theo bắt đầu sau hạn Bài tập 3, chưa có cam kết giờ trả lời.

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
| 5 | (22:40 ngày 13/11) "Thầy ơi cho em gia hạn bài 3 được không, em ốm mấy hôm nay" | ③ | Không có tool gia hạn. AI nói "được" hoặc "đã báo TA" khi chưa gửi. Với `chuyen_TA`, ca trực tiếp theo bắt đầu 08:00 sáng mai, sau hạn; không có cam kết giờ trả lời. | Nói không có quyền gia hạn. Cho xem trước nội dung và xác nhận chuyển TA, báo ca tiếp theo bắt đầu sau hạn. Gợi ý tự nhắn giảng viên ngay. | Không chấp nhận được |
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

Hai kịch bản đắt nhất là hai kiểu sai khác nhau, đều là **lỗi ngữ cảnh** nên chủ yếu sửa bằng thiết kế, không chỉ bằng câu chữ:

- **#1:** AI làm đúng quy trình (trích đúng §3.3) nhưng **nguồn sai**.
- **#6:** học viên tính đúng (trung bình 15,25 và trung vị 11,5 đều đúng với dữ liệu bài 3). Nếu AI nói "đúng rồi" thì nội dung không sai, nhưng AI đã xác nhận đáp số của một bài đang mở (hạn 13/11 23:59), điều mà lát cắt cấm. Cái sai là **thời điểm**, không phải con số.

---

### Kịch bản #1 · Tài liệu §3.3 có câu sai

**Tin nhắn:** "Độ lệch chuẩn với phương sai cái nào lớn hơn?"

**Quyết định:** trả lời kèm giới hạn, rồi đề nghị gửi TA (học viên bấm).

**AI nói nguyên văn:**

> "Tài liệu buổi 3, §3.3 ghi độ lệch chuẩn luôn nhỏ hơn phương sai. Mình nghĩ câu này cần xem lại: nó chỉ đúng khi phương sai lớn hơn 1. Ví dụ phương sai là 0,25 thì độ lệch chuẩn là √0,25 = 0,5, lớn hơn phương sai. Phần chắc chắn ở §3.3 là độ lệch chuẩn bằng căn bậc hai của phương sai. Mình không sửa được tài liệu và chưa hỏi được giảng viên, nên bạn chưa nên ghi câu đó vào ghi chú. Bạn muốn xem trước câu hỏi để gửi TA không? TA trực 08:00–22:00; gửi ngoài giờ phải chờ ca tiếp theo, chưa có cam kết giờ trả lời."

Câu này không hứa "mình sẽ báo giảng viên". Nó chỉ nói việc AI thật sự làm được: gửi TA qua `chuyen_TA`.

**Người dùng thấy ngoài câu chữ**:

- Thẻ nguồn "Tài liệu buổi 3 · §3.3", kèm nhãn vàng "Nghi sai, chưa kiểm với giảng viên".
- Độ chắc tách hai tầng: "Phép tính phản ví dụ: chắc, tự kiểm được" và "Nội dung tài liệu: chưa xác nhận".
- Hai nút: [Gửi TA] và [Để sau].

**Bước tiếp theo của học viên:**

- Tự thử một ví dụ khác (phương sai 4 thì độ lệch chuẩn 2) để thấy cả hai trường hợp.
- Hoặc bấm [Gửi TA] để xem trước câu hỏi, nguồn và nội dung hội thoại sẽ chuyển, rồi bấm [Xác nhận chuyển TA].
- Nếu chọn [Để sau], nhãn nghi sai vẫn hiện trong hội thoại; chưa gửi TA và không đăng FAQ. Nhãn này là trạng thái hiển thị, không phải tool mới. Rủi ro còn lại là TA chưa biết lỗi nếu học viên không gửi.

**Ai được báo, sau bao lâu:**

- Sau khi học viên xác nhận và gửi thành công, TA nhận qua `chuyen_TA`, thấy mã §3.3, câu nghi sai, phản ví dụ và giờ gửi.
- Nếu gửi lúc 22:12, giao diện báo ca trực tiếp theo bắt đầu 08:00 sáng hôm sau; không hứa TA đọc hoặc trả lời đúng 08:00.
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

**Người dùng thấy ngoài câu chữ**:

- Thẻ trạng thái: "Bài tập 3: đang mở, hạn 13/11 23:59 (nguồn: trang khoá học)".
- Hai nút: [Gợi ý bước đầu] và [Hỏi TA]. **Không có nút "Xác nhận đáp số".**
- Sau 22:00, dưới nút [Hỏi TA] hiện dòng "Ca TA tiếp theo bắt đầu 08:00 sáng mai; chưa có cam kết giờ trả lời". Riêng tối 13/11, thêm cảnh báo "Ca tiếp theo bắt đầu sau hạn Bài 3".

**Bước tiếp theo:** học viên tự kiểm bằng §3.1 và §3.2, hoặc trả lời câu (b), hoặc hỏi TA.

- Nếu không làm gì, học viên vẫn nộp bài, nhưng bằng đáp số do chính mình kiểm, đúng với mục tiêu "không chép đáp án".

**Ai được báo:** không ai được báo ngay. Nút [Hỏi TA] mở phần xem trước; chỉ sau [Xác nhận chuyển TA] và gửi thành công, TA mới nhận tin. TA thấy: bài tập 3, câu hỏi của học viên, giờ gửi, và dòng "học viên đang xin xác nhận đáp số, AI đã không xác nhận". Nếu gửi sau 22:00, ca trực tiếp theo bắt đầu 08:00 sáng hôm sau, chưa có cam kết giờ trả lời.

**Phương án đã loại:**

| Phương án | Vì sao loại |
|---|---|
| Nói "đúng rồi" | Đúng toán nhưng vi phạm lát cắt. Học viên nộp ngay, không đảo lại được. |
| Im lặng khi đúng, nhắc kiểm lại khi sai | Phản ứng của AI lộ đáp số. Đây là xác nhận gián tiếp. |
| Chỉ chỗ sai nếu có | Là làm hộ. Rubric riêng của track: không xác nhận, không nhận xét hộ. |
| Chuyển TA xác nhận mặc định | Sau 22:00 không có TA. Quyết định đáp số đúng sai không thuộc AI. TA chỉ là lựa chọn học viên tự bấm. |
| Từ chối cụt "mình không giúp được" | Học viên lúc 22:40 bỏ cuộc. Hướng tự kiểm giữ được sự hữu ích. |
| Chỉ hỏi lại "bạn muốn xác nhận câu nào?" | Học viên đã nói rõ đáp số, nên hỏi lại không làm rõ thêm gì và vẫn chưa trả lời việc xác nhận. Hỏi lại chỉ dùng được ở câu cuối (hỏi câu (b)) để dẫn học viên tự làm. |

**Loại lỗi: lỗi ngữ cảnh.** Câu "đúng rồi" đúng về toán nhưng sai với tình huống (bài đang mở).

- **Cách nói:** không xin lỗi, không buộc tội. Nêu quy tắc ngay từ đầu, kèm lý do.
- **Cách sửa:** sửa thiết kế, không sửa từ ngữ.

**Lỗi sửa câu chữ không cứu được:** model có thể lỡ nói "đúng rồi" dù prompt đã cấm.

- **Thiết kế cứu:** trạng thái "đang mở" lấy từ trang khoá học (Dữ liệu B), không lấy từ lời học viên. Với yêu cầu xác nhận đáp số như #6, hệ thống dùng cùng phản hồi tự kiểm ở trên, không chọn phản hồi theo đáp số đúng hay sai. Gợi ý bổ sung chỉ dùng bước đầu đã chuẩn bị cho bài, không chứa đáp số hay nhận xét đúng/sai; nội dung vượt giới hạn không được gửi. Giao diện không có nút xác nhận đáp số.

---

### Bốn đường đi

| Đường | #1 | #6 |
|---|---|---|
| Happy path | Học viên đọc phản ví dụ, tự thử số khác, hiểu | Học viên tự kiểm bằng §3.1, §3.2, nộp đúng |
| Low-confidence | Nhãn "chưa xác nhận" và độ chắc hai tầng | Nếu học viên chỉ nói "câu b" như #4, hỏi rõ bài nào trước khi gợi ý; ở #6 đã rõ Bài 3 nên không hỏi lại tên bài |
| Failure / không căn cứ | Tài liệu mâu thuẫn toán, hiện cờ nghi sai và nút gửi TA | Bài đang mở, không có đường xác nhận |
| Correction | Học viên bấm "Mục này sai chỗ nào?" nếu thấy AI nhầm | Học viên bấm "Gợi ý quá nhiều" nếu thấy AI tiết lộ đáp án |

### Nguyên tắc HAX/PAIR, mỗi cái trỏ một chỗ cụ thể

| Nguyên tắc | Chỗ cụ thể |
|---|---|
| **G2** (nói rõ AI làm tốt đến đâu) | Ở #1, AI chắc về phép tính nhưng chưa chắc về nội dung tài liệu. Thanh độ chắc hai tầng ở #1: "Phép tính: chắc · Tài liệu: chưa xác nhận" |
| **G11** (giải thích vì sao AI làm vậy ) | Ở #6, AI từ chối xác nhận, nên phải nói lý do. Câu "Bài tập 3 đang mở đến 23:59... nên mình không xác nhận" để học viên không thấy bị gạt đi|
| **G10** (thu hẹp phạm vi khi nghi ngờ) | Cả 2 kịch bản, AI không làm liều: Câu cuối ở #6 "Bạn muốn mình hỏi câu (b)...", và câu cuối ở #1 chỉ đề nghị gửi TA thay vì tự đăng FAQ  |



## §4. Mức tự chủ  (chặng 4)

### §4.1. Mức tự chủ cho bốn tool

Căn cứ: bảng tool và Dữ liệu A/B trong track T2; các kịch bản ở §2. Bối cảnh vẫn là tối 12–13/11/2026, Bài 3 đang mở. Không thêm tool mới.

| Tool | Mức áp dụng | Sai thì ai chịu, sửa được không, chờ người thì mất gì? | Phương án loại và lý do |
|---|---|---|---|
| `tra_cuu_tai_lieu` | **Tự làm** | Chỉ đọc, không sửa tài liệu. Học viên vẫn có thể học sai nếu nguồn sai như #1; đóng kết quả không xoá được điều đã đọc. Bắt duyệt mọi lần tra cứu làm học viên phải chờ cả với câu đơn giản. | Không chọn cần duyệt cho mọi lần đọc vì làm chậm việc học; không cấm vì trợ lý cần căn cứ để trả lời. Có nguồn không đồng nghĩa nguồn đúng. |
| `goi_y_bai_tap` | **Tự làm trong giới hạn §4.2** | Gợi ý quá tay ở #4/#6 khiến học viên chép đáp án; thu hồi tin không thu hồi được kiến thức đã thấy. Chờ TA cho từng gợi ý có thể kéo qua hạn Bài 3. | Không giao học viên duyệt đáp án: bấm đồng ý không ngăn việc làm hộ. Không cấm toàn bộ vì vẫn cần gợi ý bước đầu và giải thích bài đã có đáp án. |
| `chuyen_TA` | **Cần học viên duyệt** | Chuyển nhầm làm lộ nội dung học viên không muốn gửi và tốn thời gian TA. Có thể rút khi còn chờ, nhưng không xoá điều TA đã đọc. Một lần xem trước ngắn ít tốn hơn chuyển nhầm; ngoài giờ vẫn phải chờ TA. | Không tự gửi vì học viên cần biết nội dung được chuyển; không cấm vì ca thiếu nguồn hoặc tài liệu nghi sai cần đường hỏi người. |
| `dang_FAQ` | **Cần TA duyệt** | Sai ở #1 có thể lan ra cả lớp. Gỡ bài không xoá điều người khác đã học. Chờ TA làm FAQ xuất hiện chậm hơn, nhưng học viên vẫn được hỗ trợ riêng trong phạm vi cho phép. | Không tự đăng vì phạm vi ảnh hưởng lớn; không cấm toàn bộ vì câu trả lời đã được kiểm tra vẫn hữu ích cho lớp. |

### §4.2. Điều kiện và quy tắc bàn giao UX/prototype

- **Tra cứu:** trả đoạn kèm mã mục; chỉ dựa vào dữ liệu được cấp. Không dựng slide hay nội dung buổi chưa mở (#2/#8). Cho đóng kết quả tra cứu; thao tác chỉ đọc không có thay đổi dữ liệu cần hoàn tác. Nếu thấy mâu thuẫn như câu cuối §3.3, chỉ rõ câu cần kiểm tra và mời chuyển TA; không tự sửa tài liệu.
- **Gợi ý:** chưa rõ bài nào thì hỏi lại trước (#4); trạng thái bài lấy từ Dữ liệu B, không từ lời học viên. Bài đang mở chỉ dùng gợi ý bước đầu đã chuẩn bị, trỏ mục liên quan; **cấm đưa/xác nhận đáp số hoặc viết nhận xét hộ**, kể cả học viên đồng ý (#6). Yêu cầu xác nhận dùng cùng phản hồi tự kiểm ở §3 dù đáp số đúng hay sai; nội dung vượt giới hạn không được gửi. Chỉ giải thích đầy đủ khi bài đã hết hạn **và** đã công bố đáp án, như Bài 2. Gỡ tin nhắn không khắc phục được việc đã lộ đáp án.
- **Chuyển TA:** trước nút `Xác nhận chuyển TA`, hiển thị câu hỏi, đoạn hội thoại sẽ gửi, nguồn liên quan và giờ TA 08:00–22:00. Học viên được sửa hoặc huỷ trước khi xác nhận; không xác nhận thì không gửi. Gửi thất bại phải báo chưa gửi và cho thử lại, không hiện đã chuyển.
- **Chờ TA:** chỉ khi gửi thành công mới hiện `Chờ TA`, kèm thời điểm bắt đầu ca trực tiếp theo nếu ngoài giờ; không hứa chắc giờ trả lời. Lúc 22:40 ngày 13/11, ca tiếp theo bắt đầu 08:00 ngày 14/11, sau hạn Bài 3; không có quyền gia hạn (#5). Khi còn chờ có nút `Rút câu hỏi`; đã được TA tiếp nhận thì không hứa rút lại nội dung đã đọc. Không xác nhận thì không gửi; gửi thất bại thì giữ nội dung để thử lại.
- **Đăng FAQ:** TA xem câu hỏi, câu trả lời và căn cứ trước khi bấm `Duyệt đăng`. Nếu còn nghi ngờ nguồn như #1, chưa đăng; TA cần kiểm tra với giảng viên. Không có TA duyệt thì tiếp tục chờ, không tự đăng sau một khoảng thời gian. Chưa có cam kết thời gian duyệt trong dữ liệu đề bài nên không tự đặt hạn. Nếu đã đăng sai, TA gỡ/đính chính để người đọc biết nội dung cũ có lỗi.
- **Việc cấm:** không có nút giải hộ/xác nhận đáp số bài đang mở, gia hạn, chấm điểm, nhận xét năng lực hoặc sửa tài liệu. Nhãn nghi sai ở §3 chỉ hiển thị trong hội thoại; việc báo người vẫn dùng `chuyen_TA` có xác nhận.

### §4.3. Tool khó xếp nhất: `goi_y_bai_tap`

**Quyết định: tự làm có giới hạn.** Tự làm không giới hạn có thể lộ đáp án ở #4/#6; bắt TA duyệt mọi gợi ý khiến học viên tối muộn phải chờ qua hạn Bài 3; cấm hẳn thì mất hỗ trợ học từng bước và cả việc giải thích Bài 2 đã có đáp án.

Vì vậy, giới hạn đặt ở nội dung được gửi: hỏi rõ bài khi thiếu thông tin; bài đang mở chỉ có gợi ý bước đầu; xin xác nhận đáp số nhận cùng hướng dẫn tự kiểm; bài hết hạn có đáp án được giải thích đầy đủ. Không dùng học viên làm người duyệt đáp án vì chính họ đang cần được giúp kiểm tra. Phương án này giảm thời gian chờ nhưng vẫn có giá: gợi ý có thể chưa đủ để học viên tự làm tiếp; học viên được chọn hỏi TA, không được mở khoá đáp án.

### §4.4. Đối chiếu mức tự chủ trên ba kịch bản

Phạm vi: đối chiếu thiết kế trên dữ liệu dựng của T2, chưa kiểm thử tương tác.

| Ca | Đường xử lý | Cái sai có bị chặn? | Có làm khi lẽ ra phải hỏi? | Có bắt chờ vô ích? |
|---|---|---|---|---|
| **#1 — tài liệu §3.3 sai** | Tra cứu §3.3; chỉ ra mệnh đề cần xem lại cùng phản ví dụ ở §2 #1; học viên chọn có chuyển TA không. Không đăng FAQ khi chưa được TA kiểm tra và duyệt. | Chặn tự đăng FAQ. Tra cứu riêng lẻ vẫn có thể truyền tải nguồn sai nếu bỏ sót mâu thuẫn; ở ca này dùng cảnh báo và phản ví dụ đã xác định tại §3. | Chưa gửi TA nếu học viên chưa xác nhận; chưa đăng FAQ nếu TA chưa duyệt. | Học viên thấy cảnh báo/căn cứ ngay, chỉ chờ người kiểm tra phần nghi sai. |
| **#6 — xin xác nhận đáp số Bài 3** | Dữ liệu B xác định bài đang mở; dùng phản hồi tự kiểm ở §3, không đổi phản hồi theo đáp số đúng/sai; gợi ý bước đầu trỏ §3.1/§3.2. | Chặn xác nhận trực tiếp và gián tiếp bằng cùng phản hồi cho yêu cầu xác nhận; không gửi gợi ý có đáp số hay nhận xét đúng/sai. | Không hỏi lại trạng thái đã có trong dữ liệu; chuyển TA vẫn cần xác nhận riêng. | Gợi ý bước đầu được gửi ngay, không chờ TA duyệt mọi câu. |
| **Bình thường — “Bài 2 đã có đáp án, vì sao trung bình của 4, 8, 6, 5, 7 là 6?”** | Đọc Dữ liệu B: đã hết hạn và có đáp án. Giải thích theo §3.1: tổng 30 chia 5 bằng 6, kèm căn cứ. | Không áp nhầm giới hạn của bài đang mở sang bài đã có đáp án. | Không có hành động gửi người khác hoặc đăng FAQ nên không cần xác nhận. | Trả lời ngay, không bắt chờ TA. |

**Giới hạn:** đối chiếu này không chứng minh khả năng tự phát hiện mọi lỗi tài liệu hoặc ngăn mọi cách xin đáp án. Nội dung phản hồi, nút duyệt/huỷ/rút và trạng thái gửi thất bại chưa được kiểm thử trên prototype.

### §4.5. Lời hứa với người dùng

> “Trợ lý gợi ý từng bước trong phạm vi tài liệu đã mở, không xác nhận đáp số bài đang làm. Câu hỏi chỉ được chuyển TA sau khi bạn xác nhận; nội dung FAQ chỉ được đăng sau khi TA duyệt. Ngoài giờ trực, câu hỏi sẽ chờ TA, không bảo đảm được trả lời trước hạn bài.”

Việc đặt `chuyen_TA` ở mức cần duyệt đổi lời hứa từ tự gửi sang người học quyết định nội dung nào được chuyển. `dang_FAQ` cần TA duyệt nên trợ lý không hứa câu trả lời sẽ xuất hiện ngay cho cả lớp.

## §5. Prototype  (chặng 5)
- Link hoặc file · công cụ · phần nào mock · có lời gọi AI thật không.
- 1–2 ảnh có đánh số; mỗi số: thể hiện gì · nguyên tắc HAX/PAIR nào · mức tự chủ nào.
- Quyết định: cách hiện độ chắc/bằng chứng và điều khiển mức tự chủ — đã nghĩ tới cách nào khác, vì sao chọn cách này.

## §6. Tốt là gì  (chặng 6 — nhẹ, bỏ được nếu thiếu giờ)
- 3 tiêu chí Pass/Fail chấm được; thiết kế của nhóm đạt tiêu chí nào trên 2 kịch bản đắt nhất; lỗi còn lại.

## §7. Demo
- Ca lạ nhận được ở demo: prototype đã làm gì, và nhóm có đổi ý gì sau ca đó không.
