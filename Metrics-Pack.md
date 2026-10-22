<a id="tong-quan"></a>

# Metrics Pack — SkinLog

*AI IN ACTION · TRACK 1 · DAY 20*

### SkinLog

Từ ảnh và ghi chú rời rạc
đến một mốc đối chiếu có ý nghĩa.

**Dự án:** Theo dõi một lần thêm sản phẩm mới vào routine chăm sóc da hiện có. Kết hợp nhật ký diễn biến da với lịch sử sản phẩm/routine để người dùng xem lại quá trình thử và ghi bước tiếp theo.

> **HÀNH VI CHỨNG MINH GIÁ TRỊ**
>
> Người dùng hoàn tất một mốc đối chiếu: xem lịch sử sử dụng và ghi nhận da, lưu điều quan sát được hoặc chưa biết, rồi chọn bước tiếp theo. Mở app, chụp ảnh hoặc AI tự tạo tóm tắt chưa đủ để được tính.

| Phần bài nộp | Nội dung & liên kết |
| --- | --- |
| 00 · Phạm vi | Persona, use case, core job, ranh giới sản phẩm · [00 — Dự án, persona và core job](#pham-vi) |
| 01 · Core Action | Khái niệm, Core Action Card, completion rule, Gate 1 · [01 — Core Action Card và 5 tiêu chí tự kiểm](#core-action) |
| 02 · Nature & cadence | Action Nature Card và nhịp theo đợt thử · [02 — Action Nature Card và kết luận cadence](#nature-cadence) |
| 03–04 · Metric & retention | Activation, engagement, NSM, retention, đúng–xong–tốn · [03 — Activation và engagement](#activation-engagement) |
| 05 · Product Loop | Hai chu kỳ và giả thuyết kiểm chứng · [05 — Product Loop qua hai chu kỳ](#product-loop) |
| 06 · Tracking | 8 event, hợp đồng đo và tiêu chí nghiệm thu · [06 — Bảng tracking với 8 core events](#tracking-events) |
| 07 · Tự soi & nộp | Đối chiếu yêu cầu, các gate, giả thuyết và nguồn · [07 — Tự kiểm tra yêu cầu và nguồn tham khảo](#self-review) |

Bản thiết kế để kiểm chứng · 22/10/2026

Nội dung giữ các quyết định đã chốt trong hội thoại đến hết Phase 1 và hoàn thiện Phase 2–5. Chưa có dữ liệu người dùng thật; mọi window, ngưỡng và kỳ vọng thử nghiệm mới đều là giả thuyết thiết kế, không phải kết quả đã đạt.

<a id="pham-vi"></a>

## Một persona, một tình huống

*00 · PHẠM VI / PHASE 0*

| Thành phần | Bản chốt |
| --- | --- |
| Dự án | SkinLog: lưu lịch sử sản phẩm/routine và hỗ trợ theo dõi diễn biến da khi thay đổi sản phẩm chăm sóc da. |
| Persona chính | Người chăm sóc da cho bản thân, đang duy trì routine và có nhu cầu thay đổi sản phẩm theo từng đợt. Hiện họ dùng ảnh trong điện thoại, ghi chú rời rạc hoặc trí nhớ để so sánh. |
| Use case của lab | Người dùng đã có routine tương đối ổn định, thêm **một sản phẩm mới** và theo dõi riêng đợt thử đó. Không giới hạn persona vào đúng thời điểm vừa mua sản phẩm. |
| Core job<br/>Bằng lời người dùng | “Khi thêm một sản phẩm mới, tôi muốn nhìn lại mình đã dùng gì và da thay đổi ra sao trong suốt đợt thử, để đánh giá bước tiếp theo có cơ sở và có thông tin rõ ràng để hỏi chuyên gia khi cần.” |
| Vấn đề hiện tại | Khó nối ảnh với thời điểm sử dụng, lần quên dùng và thay đổi routine. Góc chụp, ánh sáng, thời tiết hoặc nhiều thay đổi cùng lúc có thể làm phép so sánh thiếu chắc chắn. |
| Kết quả cần hỗ trợ | Một bản đối chiếu có nguồn dữ liệu, điều còn thiếu, nhận xét do người dùng xác nhận và bước tiếp theo. Có thể dùng lại khi xem lịch sử hoặc chuẩn bị câu hỏi tư vấn. |

### Phạm vi sản phẩm

**Trong phạm vi:** lưu routine và sản phẩm; ghi tình trạng ban đầu, diễn biến, lịch sử dùng/bỏ lỡ; hỗ trợ xem lại theo thời gian; lưu câu hỏi và bước tiếp theo. Ảnh là tùy chọn, có kiểm tra khả năng so sánh.

**Vai trò AI:** sắp xếp và tóm tắt dữ liệu đã có, chỉ rõ nguồn ghi nhận và giới hạn. Tương quan theo thời gian không đủ chứng minh nguyên nhân; không tự kết luận “hợp da/không hợp da”, chẩn đoán hoặc đổi điều trị.

**Ngoài use case lab:** người xây toàn bộ routine mới; thay cả liệu trình; người thử sản phẩm cho công việc; quy trình nhóm của clinic. “Da dễ kích ứng” có thể là đặc điểm/phân khúc phỏng vấn, không phải một persona thứ hai.

> **QUYẾT ĐỊNH GIỮ NGUYÊN**
>
> Gộp ý tưởng #3 Nhật ký phản ứng với mỹ phẩm mới và #6 Quản lý sản phẩm/routine. Không chuyển sang dự án theo phác đồ trị mụn. High engagement–high retention là cơ hội cần kiểm chứng, không phải thuộc tính đã được xác nhận.

<a id="core-action"></a>

## Định nghĩa việc tạo giá trị

*01 · CORE ACTION / PHASE 1*

| Khái niệm | Áp dụng cho SkinLog |
| --- | --- |
| Core job | Nhìn lại quá trình sử dụng và diễn biến da để xác định bước tiếp theo có cơ sở hơn. |
| Core action | Hoàn tất một mốc đối chiếu của đợt thử: xem dữ liệu liên quan, xác nhận nhận xét và lưu bước tiếp theo. |
| Core value | Hiểu rõ điều đã quan sát, điều chưa thể kết luận và có bản nhìn lại thay cho trí nhớ/ảnh rời rạc. |
| Core value event | **trial_review_completed**: mốc đối chiếu hợp lệ được người dùng hoàn tất và lưu. Chứng minh hành vi hoàn tất; chưa chứng minh quyết định đúng hay da đã cải thiện. |

### Core Action Card

| Thành phần | Định nghĩa |
| --- | --- |
| Target user | Người chăm sóc da cho bản thân, có routine tương đối ổn định, đang thêm một sản phẩm mới. |
| Core job | Xem lại diễn biến đợt thử cùng lịch sử dùng sản phẩm để biết điều gì đã thấy, chưa biết và cần làm tiếp. |
| Core action | Người dùng hoàn tất một mốc đối chiếu và lưu nhận xét cùng bước tiếp theo/câu hỏi còn mở. |
| Object | Một **review_id** thuộc **review_cycle_id** của **trial_id**, liên kết routine và các ghi nhận của đợt đó. |
| Preconditions | Có đợt thử xác định sản phẩm mới, tình trạng ban đầu và ít nhất một ghi nhận sau đó. Hiển thị lịch sử dùng/bỏ lỡ khi có dữ liệu; đánh dấu phần chưa ghi nhận. |
| Completion rule | Đã xem đối chiếu và chủ động lưu đủ: (1) điều quan sát/chưa thấy thay đổi; (2) mức chắc chắn/điều thiếu; (3) bước tiếp theo do mình chọn. Quy tắc chi tiết ở [Quy tắc hoàn tất một mốc đối chiếu](#completion-rule). |
| Core value | Có bản xem lại theo thời gian gắn với sử dụng thực tế và bối cảnh; biết giới hạn của dữ liệu. |
| Evidence of value | Bản đối chiếu được xác nhận và lưu. Bằng chứng mạnh hơn: người dùng dùng lại bản ghi hoặc dùng thông tin trong buổi tư vấn; cần đo riêng. |
| Candidate event | **trial_review_completed**, phát một lần khi lưu chuyển trạng thái từ chưa hoàn tất sang hoàn tất; gắn user_id, trial_id, review_id và review_cycle_id. |

<a id="completion-rule"></a>

## Hoàn tất thế nào mới được tính?

*01 · CORE ACTION / GATE 1*

### Quy tắc hoàn tất giữ theo brainstorm

**1.** Server xác nhận có baseline và ít nhất một ghi nhận phát sinh sau thời điểm baseline trong cùng đợt thử. Có thể chỉ có ghi nhận bằng chữ; không bắt buộc ảnh.

**2.** Người dùng đã xem phần đối chiếu; tự nhập hoặc sửa/xác nhận nhận xét cụ thể, độ chắc chắn/giới hạn và một bước tiếp theo. Không dùng checkbox “đã hiểu” đơn lẻ làm bằng chứng.

**3.** Bước tiếp theo có thể là tiếp tục quan sát kèm mốc xem lại; tạm dừng để tìm hỗ trợ; hoặc chuẩn bị câu hỏi chuyên gia. “Chưa đủ thông tin để đánh giá” vẫn hợp lệ nếu nêu rõ thiếu gì và định làm gì tiếp.

**4.** Chỉ sau khi transaction lưu thành công và mốc đổi sang completed mới ghi event. Bản AI tự sinh, bản nháp/autosave, mở trang và bấm nút nhưng lưu lỗi không được tính.

**5.** Không ép hoàn thành mốc đối chiếu khi người dùng cần hỗ trợ. Luồng tìm hỗ trợ độc lập, không bị chặn bởi baseline, ảnh hay các ô bắt buộc.

| Tiêu chí tự kiểm tra | Đánh giá & lý do |
| --- | --- |
| Gần core value | **Đạt:** biến dữ liệu rời rạc thành một bản nhìn lại có nhận xét và bước tiếp theo. |
| Có thể lặp lại | **Đạt:** xuất hiện tại mốc mới có lý do xem lại trong cùng đợt thử hoặc đợt sau. |
| Có thể quan sát | **Đạt:** có actor, object, preconditions, nội dung bắt buộc và trạng thái lưu thành công. |
| Tăng có ý nghĩa | **Đạt có điều kiện:** không đếm mở lại/sửa cùng mốc hay chia mốc giả tạo. Phase 3 đặt chất lượng cạnh số lượng. |
| Team tác động được | **Đạt:** giảm nhập liệu, trình bày timeline dễ đối chiếu, chỉ rõ dữ liệu thiếu và giúp lưu bước tiếp theo. |

### Các ứng viên bị loại

Mở app/chụp ảnh/ghi một lần bôi là đầu vào; chat và AI tạo phân tích là tương tác/output. Chỉ đếm kết thúc cả đợt thử thì quá muộn, đồng thời dễ ép kết luận “hợp/không hợp” khi chưa đủ cơ sở.

> **GATE 1 · ĐẠT Ở MỨC THIẾT KẾ**
>
> Core action có actor, object và completion rule; qua 5/5 tiêu chí với điều kiện kiểm soát chất lượng. Còn phải kiểm chứng người dùng có chịu hoàn tất mốc và thấy hữu ích hơn cách ghi chú hiện tại hay không.

<a id="nature-cadence"></a>

## Nhịp đến từ đợt thử

*02 · NATURE & CADENCE / PHASE 2*

| Action Nature Card | Bản điền |
| --- | --- |
| Actor | Cá nhân chăm sóc da, thực hiện trên một đợt thử sản phẩm của chính mình. |
| Intent | Muốn xem lại đã dùng gì, diễn biến nào đã được ghi nhận và cần theo dõi/hỏi thêm điều gì. |
| Trigger | Tự đến mốc đã định để xem lại; nhận thấy thay đổi; có dữ liệu mới đáng xem; hoặc chuẩn bị hỏi chuyên gia. Nhắc lịch chỉ hỗ trợ mốc có sẵn. |
| Effort | Cần baseline + ghi nhận tiếp theo; xem timeline, kiểm tra/sửa tóm tắt, ghi nhận xét và bước tiếp theo. Mục tiêu UX thử: khoảng 2–5 phút/mốc; chưa có đo thực tế. |
| Value timing | Giá trị đối chiếu xuất hiện khi hoàn tất mốc; giá trị lịch sử tích lũy qua nhiều mốc/đợt. Tạo baseline giúp bắt đầu nhưng chưa phải đã đối chiếu. |
| State | Lưu mốc đối chiếu, nguồn ghi nhận, điều chưa chắc, bước tiếp theo, trạng thái đợt và mốc xem lại kế tiếp nếu còn nhu cầu. |
| Dependency | Phụ thuộc thời gian có ghi nhận mới, chất lượng và độ đầy đủ đầu vào. Không cần chuyên gia phê duyệt mọi mốc; có nhu cầu chuyên môn thì đi luồng hỗ trợ riêng. |
| Repeat condition | Đợt vẫn cần theo dõi và tới mốc mới/có diễn biến mới; hoặc một đợt thử mới cần sử dụng lại lịch sử. Mở lại cùng bản ghi không tạo một lần lặp mới. |

### Dạng hành vi & kết luận cadence

**Dạng chính: theo dự án** (một đợt thử); có trigger theo mốc/sự kiện trong đợt. Việc ghi hằng ngày là đầu vào tùy chọn, không phải core action bắt buộc.

> **KẾT LUẬN THEO TEMPLATE ĐỀ**
>
> Đối với người đang thử thêm một sản phẩm vào routine, core action hoàn tất mốc đối chiếu thường xuất hiện khi tới mốc đã chọn hoặc có diễn biến cần xem lại, vì cần có dữ liệu mới và nhu cầu hiểu đợt thử. Do đó, nhịp đo phù hợp là theo cơ hội xem lại trong từng đợt thử ở cấp người dùng; giữa các đợt là nhịp không đều.

**Nature trước, nurture sau:** cho người dùng chọn mốc xem lại, sửa lịch và tắt nhắc. Không ép daily streak hay tạo mốc chỉ để tăng lượt dùng. Tăng tần suất có thể phản ánh lo lắng hoặc UX khó, không mặc nhiên tăng giá trị.

**Cách kiểm chứng:** phỏng vấn lần thay routine gần nhất; theo dõi thời gian từ bắt đầu đến mốc đầu và khoảng cách giữa các mốc; tách mốc theo lịch và mốc do diễn biến. Nếu dữ liệu không ủng hộ nhịp đề xuất, sửa window đo trước khi mở rộng.

GATE 2 · Cadence xuất phát từ tiến trình đợt thử và điều kiện lặp; không chọn daily/weekly chỉ vì dashboard quen dùng.

<a id="activation-engagement"></a>

## Activation và engagement

*03 · METRIC SYSTEM / PHASE 3*

**Ký hiệu dùng xuyên suốt:** C = mốc đạt completion rule Phase 1; Q = C qua quality gate ở [Tiêu chí chất lượng: tính đúng, hoàn tất và chi phí AI](#ai-metrics). Trong pilot, đánh giá tất cả mốc trong 48 giờ. Metric chất lượng chỉ chốt sau khi đủ thời gian đánh giá; gắn kết quả về thời điểm hoàn tất C.

| Activation metric | Định nghĩa tính được |
| --- | --- |
| Start event | **trial_started** đầu tiên: server lưu đợt thử có sản phẩm mới, routine snapshot và baseline. Không lấy đăng ký/đăng nhập làm start hay activation. |
| Activation event | **trial_review_completed** hợp lệ đầu tiên trong chính đợt thử đầu; được xác nhận Q. Event đánh giá chất lượng là điều kiện join, không thay hành vi core action. |
| Time window | Trong [start_at, start_at + 14 ngày). 14 ngày là window thử vận hành để có ghi nhận tiếp theo, **không phải thời gian đánh giá hiệu quả mỹ phẩm**. |
| Activation rate A14 | Số user có Q đầu tiên trong window / số user đã có start đầu tiên và đã quan sát đủ 14 ngày. Chỉ chốt sau thêm tối đa 48 giờ cho đánh giá chất lượng. |
| Quy tắc mẫu số | Mỗi user chỉ vào mẫu số một lần; không bỏ người dừng thử/bỏ dở sau start. Chỉ loại bot, QA và tài khoản nội bộ theo cờ có trước, nhất quán cho mọi metric. |
| Time to Value | P50/P75 thời gian từ start tới Q đầu tiên, dùng timestamp của C; báo kèm tỷ lệ chưa activated tại ngày 14. Không chỉ trình bày thời gian của nhóm thành công. |

### Active khác activated

**Active trong window:** có ít nhất một Q trong khoảng quan sát đang xét. **Activated:** đã đạt Q đầu tiên theo định nghĩa trên; đây là trạng thái lịch sử, không có nghĩa họ sẽ active ở mọi window sau. Mở app hoặc ghi ảnh chưa được tính active tạo giá trị.

### Chọn hai góc engagement

| Góc đo | Công thức & cách đọc |
| --- | --- |
| Frequency<br/>F_due | Số review_cycle đến hạn có Q trong window / số review_cycle đến hạn đã đủ quan sát. Một Q/cycle. Đo việc lặp theo nhu cầu thật, không khuyến khích tạo thêm mốc. |
| Depth<br/>D_reuse | Số Q được người dùng báo đã dùng lại để xem xét bước tiếp theo/trao đổi chuyên gia trong 14 ngày / số Q đã có đủ 14 ngày theo dõi. Mỗi review_id tính một lần; báo riêng tỷ lệ phản hồi và không phản hồi. |

D_reuse là bằng chứng người dùng tự khai, chưa xác minh hành vi ngoài app hay cải thiện da. Không dùng số session/phút chat làm engagement chính. Window 14 ngày cần kiểm chứng theo cadence thật.

<a id="north-star"></a>

## North Star và chỉ báo sớm

*03 · METRIC SYSTEM / PHASE 3*

> **NORTH STAR · N28**
>
> Số mốc đối chiếu Q khác nhau được người dùng hoàn tất trong 28 ngày báo cáo: **unit of value** = mốc đối chiếu; **quality threshold** = đạt rule cấu trúc và đánh giá chất lượng; **frequency** = tổng trong 28 ngày. Khoảng 28 ngày là chu kỳ báo cáo, không phải yêu cầu dùng mỗi 28 ngày.

**Công thức:** N28 = COUNT DISTINCT (user_id, trial_id, review_cycle_id) có C trong [T−28 ngày, T), trạng thái chất lượng mới nhất = passed. Chỉ công bố bản đã chốt khi đủ 48 giờ đánh giá cho cả window; bản sớm gắn nhãn provisional.

**Chống làm đẹp số:** một cơ hội xem lại có một review_cycle_id. Sửa/reload không tạo cycle mới. Cycle mới cần mốc xem lại mới hoặc ghi nhận/diễn biến mới có lý do xem lại. Báo song song unique users và số cycle/user để nhận ra hiện tượng chia nhỏ mốc.

### Tối đa ba leading indicators

| Chỉ báo | Định nghĩa & vì sao dự báo core action |
| --- | --- |
| L1 · Sẵn sàng dữ liệu | % user bắt đầu đợt thử có ít nhất một follow-up observation trong 7 ngày. Baseline không tính; dùng observation_recorded. Dữ liệu nối tiếp là điều kiện để có mốc đối chiếu. 7 ngày là giả thuyết vận hành. |
| L2 · Hoàn tất khi đã mở | % review_cycle lần đầu được mở mà có Q trong 48 giờ từ lần mở đầu. Chỉ chốt sau 48 giờ audit bổ sung. Giảm rơi rụng trong luồng có thể giúp giá trị xuất hiện sớm hơn. |
| L3 · Có kế hoạch tiếp | % Q còn trạng thái active có next_review_at và mục tiêu xem lại do user chọn, lưu cùng lần hoàn tất. Kế hoạch rõ là giả thuyết dự báo quay lại, cần kiểm chứng với R_due. |

### Counter-metrics đặt cạnh số tăng trưởng

**Chất lượng:** tỷ lệ mốc bị đánh giá fail, số lỗi nghiêm trọng và tỷ lệ phải sửa nhận xét AI. N28 tăng nhưng chất lượng giảm không được coi là thắng.

**Chi phí:** chi phí AI trên mỗi Q, tính cả lần lỗi, retry và output bị bỏ; xem thêm nhóm user dùng nhiều nhất. **Gánh nặng:** P75 thời gian hoàn tất mốc và phản hồi cho thấy lo lắng/phiền do việc theo dõi.

**Giữ quyền tự quyết:** tỷ lệ mốc kết thúc “chưa đủ thông tin” được theo dõi riêng, không xem là fail tự động. Không tối ưu giảm số lần tìm chuyên gia bằng cách giữ người dùng trong AI.

Không đặt chỉ tiêu “nhiều Q càng tốt” vô hạn cho từng người. Giá trị tăng khi nhiều nhu cầu thật được đáp ứng; không thưởng cho nhập nhiều ảnh, soi da liên tục hoặc kéo dài đợt thử.

<a id="ai-metrics"></a>

## Đặt xong cạnh đúng và tốn

*03 · AI METRICS / PHASE 3*

**“Xong” ở đây:** bản đối chiếu đã được người dùng xác nhận và lưu đúng trạng thái trong sản phẩm. Đây là trạng thái thật của tác vụ ghi nhận, **không phải bằng chứng da khỏe hơn** hay lời khuyên y tế đúng. Việc dùng lại thông tin và lợi ích thực tế đo riêng.

| Quality gate Q · pilot | Tiêu chuẩn pass/fail |
| --- | --- |
| Q1 · Dữ kiện có nguồn | Nhận xét khớp baseline, observation và routine snapshot. Không thêm dữ kiện chưa ghi nhận; có thể truy ngược nguồn. |
| Q2 · Giới hạn rõ | Nêu dữ liệu thiếu/yếu tố nhiễu; không suy ra sản phẩm gây ra thay đổi hoặc hiệu quả từ ảnh/chuỗi thời gian đơn thuần. |
| Q3 · Đúng phạm vi | Không chẩn đoán, kê đơn, sửa phác đồ, hoặc gắn phản ứng đáng lo là “bình thường” để thúc đẩy tiếp tục thử. |
| Q4 · Có thể dùng | Người dùng có nhận xét cụ thể và bước tiếp do mình xác nhận, phù hợp mức chắc chắn. Câu “chưa đủ dữ liệu” cần chỉ rõ thiếu gì/bước tiếp, không chỉ là tóm tắt chung chung. |

**Thực hiện:** pilot chấm 100% mốc hoàn tất trong 48 giờ, pass cả bốn tiêu chí mới là Q; người đánh giá không biết nhánh thử nghiệm. Chấm riêng bản AI đã hiện cho user và bản cuối user xác nhận để tránh việc user sửa đã che lỗi AI. Trường hợp nhạy cảm/bất đồng chuyển người có chuyên môn phù hợp; dùng rubric, ghi reviewer/version và lý do fail. Audit không chặn người dùng tìm hỗ trợ.

| Nhóm đo | Công thức / ngưỡng thử |
| --- | --- |
| Xong | Tỷ lệ Q / số review_cycle đã mở đủ 48 giờ hoàn tất + 48 giờ audit. Báo C thô, Q, pending và fail riêng. |
| Đúng | Số bản AI đã hiển thị đạt rubric / toàn bộ bản AI đã hiển thị được audit. Báo riêng lỗi dữ kiện, quá mức chắc chắn, vượt phạm vi; không dùng nút thích thay độ đúng. |
| Tốn | Cost per Q trong 48 giờ: tổng phí mọi attempt AI bắt đầu trong 48 giờ từ first_activity của cohort cycle / số cycle đó có Q trong 48 giờ. First_activity là mốc sớm nhất giữa mở đối chiếu và bắt đầu attempt AI; gồm cả cycle lỗi chưa mở được. Cohort theo kỳ first_activity; chốt sau audit/reconcile. Mẫu số 0: N/A. Báo thêm tổng phí AI thực phát sinh trong kỳ, phí audit và phí các attempt muộn, không giấu chi phí ngoài window. |
| Guardrail | **0 lỗi nghiêm trọng** vượt phạm vi hoặc khuyến khích trì hoãn hỗ trợ: gặp 1 lỗi thì dừng biến thể, rà soát. Ngưỡng pilot đề xuất: ≥95% bản AI pass rubric; không giảm chất lượng để tăng N28/giảm chi phí. |

**Lợi ích thật:** D_reuse và phỏng vấn tác vụ xem lại so với ảnh/ghi chú hiện tại. Theo dõi gánh nặng/lo lắng bằng phản hồi tự khai. Không suy ra an toàn, hiệu quả mỹ phẩm hay cải thiện sức khỏe từ retention.

<a id="retention"></a>

## Quay lại đúng cơ hội xem lại

*04 · RETENTION DEFINITION / PHASE 3*

**Metric chính: R_due** = tỷ lệ người dùng hoàn tất Q ở cơ hội xem lại kế tiếp đã định. Đo một lần chuyển sang mốc tiếp theo, phù hợp nhịp đợt thử; không gọi đây là D7 retention.

| 6 thành phần | Định nghĩa chính thức |
| --- | --- |
| Unit | **User**; chỉ dùng đợt thử đầu tiên đã activated của mỗi user để tránh người dùng nặng lặp vào cohort. Phân tích các đợt sau báo riêng. |
| Cohort entry | Q đầu tiên ở t0, đợt vẫn active và người dùng đã lưu một mốc xem lại kế tiếp d > t0 trong cùng lần hoàn tất. Cohort nhóm theo tuần của t0; tư cách entry không đổi theo hành vi về sau. |
| Return event | Một **trial_review_completed** mới đạt Q, review_cycle_id khác, cùng trial_id, completion_at > t0. Mở lại/sửa bản đầu không tính. |
| Window | Window theo cơ hội: [d − 48 giờ, d + 72 giờ). Chỉ xét C sau t0. Đây là khoảng dung sai UX thử, không là lịch y khoa. Chốt sau d + 72 giờ + 48 giờ audit. |
| Threshold | Ít nhất **1 Q** trong window của mốc kế tiếp. Nhiều Q trong cùng window không tăng số user retained. |
| Segment | Persona chính, thêm một sản phẩm vào routine; còn nhu cầu đối chiếu tại entry và đã chọn mốc kế tiếp. Tách mốc theo lịch và mốc do diễn biến khi phân tích. Không trộn persona B2B/clinic. |

### Công thức & quy tắc cố định mẫu số

**R_due =** số user của cohort có return event trong window / số user của cohort đã đủ thời gian quan sát. Mẫu số giữ nguyên sau entry; không loại người đóng đợt thử, cần chuyên gia hay mất liên lạc sau đó.

**Không đổi lịch để làm đẹp retention:** d được snapshot lúc entry. Người dùng vẫn được sửa lịch trong sản phẩm; báo riêng schedule_changed và không ghi đè d dùng cho R_due của cơ hội này. Lịch mới dùng để vận hành, không viết lại cohort cũ.

**Chưa có lịch tiếp:** user activated nhưng không chọn d chưa vào R_due. Bắt buộc báo **coverage = user đủ entry R_due / toàn bộ user activated** trong cohort t0 đã đủ audit; báo riêng nhóm chưa chọn lịch. Nhờ vậy R_due cao không che tỷ lệ tạo kế hoạch thấp.

> **KHỚP VỚI NATURE**
>
> Người dùng có thể ghi hằng ngày hoặc rất ít. Chỉ cần đối chiếu đúng cơ hội đã chọn. Mốc do diễn biến phát sinh ngoài window vẫn là Q và được tính N28; không tự động biến thành retained đúng hạn.

<a id="episode-status"></a>

## Kết thúc tốt khác mất liên lạc

*04 · RETENTION DEFINITION / PHASE 3*

| Trạng thái đợt thử | Cách hiểu & cách xử lý đo |
| --- | --- |
| Đang tiếp tục<br/>active | Còn nhu cầu theo dõi; có thể có/chưa có mốc tiếp. Không quy kết churn nếu chưa đến cơ hội hoặc chưa đủ quan sát. |
| Đã tổng kết<br/>concluded | Người dùng chủ động lưu tổng kết và bước tiếp theo. Không buộc kết luận sản phẩm hợp da. Nếu đã vào cohort R_due thì vẫn ở mẫu số, báo là successful exit riêng. |
| Tạm dừng, cần hỗ trợ<br/>paused_for_support | Có nhu cầu trao đổi với chuyên gia. Không xem giảm handoff là mục tiêu; không coi user đã liên hệ thật chỉ từ việc mở hướng dẫn. |
| Không thể đánh giá rõ<br/>inconclusive | Dữ liệu thiếu/nhiều thay đổi/ảnh khó so sánh. Vẫn có thể có Q nếu nêu rõ giới hạn và bước tiếp; không giả vờ kết luận được. |
| Mất liên lạc/chưa rõ<br/>unknown | Không có xác nhận tiếp tục/kết thúc. Đây là phân loại quan sát, không tự suy ra da đã ổn hay người dùng bỏ cuộc. |

### Ví dụ tính được · chỉ là dữ liệu minh họa

Một cohort có **10 user** đủ entry và đã đủ quan sát. Có 6 user có Q mới trong window; 2 user không quay lại nhưng đã chủ động tổng kết sớm; 1 user tạm dừng để tìm hỗ trợ; 1 user chưa rõ trạng thái. Các nhóm trong ví dụ này không chồng lấp.

> **KẾT QUẢ MINH HỌA**
>
> R_due = 6/10 = **60%**, không loại 3 người tổng kết/tìm hỗ trợ để thành 6/7. Báo cạnh: successful exit 2/10, paused_for_support 1/10, unknown 1/10. Không đồng nhất 4 người thiếu return event với 4 người thất bại.

### Retention giữa các đợt · metric phụ, không thay metric chính

**R_next90:** user đã chủ động concluded đợt đầu ở t_end là cohort entry; return event là Q trong một trial_id mới, có trial_started sau t_end, trong (t_end, t_end + 90 ngày]. Threshold ≥1; unit = user; segment = persona chính. Mẫu số là toàn bộ cohort đã đủ 90 ngày và audit, kể cả không phát sinh đợt thử mới.

90 ngày là window khám phá. R_next90 thấp có thể do không có nhu cầu mới; không tự gán cho UX kém. Phỏng vấn nhóm không trở lại để tách “không cần thay sản phẩm” khỏi “có nhu cầu nhưng dùng cách khác”.

GATE 3 · Có start/activation/window; hai góc engagement; retention đủ 6 thành phần; NSM có unit + chất lượng + kỳ báo cáo; có leading và counter-metrics. Tất cả là định nghĩa có thể triển khai, chưa phải số đo thực nghiệm.

<a id="product-loop"></a>

## Một loop, ít nhất hai chu kỳ

*05 · PRODUCT LOOP / PHASE 4*

**Loop chính: project loop.** Mỗi đợt thử là một tiến trình; trạng thái đã lưu giúp mốc tiếp theo hữu ích hơn. Không bắt đầu thiết kế từ streak hay badge.

| Thành phần | Chu kỳ 1 · nhận giá trị đầu | Chu kỳ 2 · lặp lại theo nhu cầu |
| --- | --- | --- |
| Natural trigger | Đã thêm sản phẩm; tới mốc muốn xem lại hoặc thấy diễn biến cần đối chiếu. | Đến mốc tiếp đã chọn hoặc có ghi nhận mới cần xem lại cùng lịch sử cũ. |
| Điều kiện đầu vào | Baseline, sản phẩm/routine và ít nhất một ghi nhận sau đó. | Có dữ liệu mới hoặc một câu hỏi đối chiếu mới; mở lại bản cũ không thành cycle mới. |
| Core action | Hoàn tất mốc đầu: xem lịch sử, xác nhận nhận xét/giới hạn, lưu bước tiếp. | Hoàn tất mốc kế: đối chiếu bổ sung dữ liệu mới, lưu điều thay đổi/chưa rõ và bước tiếp. |
| Immediate value | Nhìn được diễn biến thay cho trí nhớ; biết phần nào chưa đủ thông tin. | Hiểu diễn biến kể từ mốc trước, tránh đọc lại từ đầu và thấy điều chưa rõ có được bổ sung chưa. |
| Saved state / investment | Lưu review, nguồn ghi nhận, câu hỏi và mốc xem lại nếu còn nhu cầu. | Bổ sung lịch sử; cập nhật kế hoạch. Có thể tổng kết đợt hoặc tạm dừng tìm hỗ trợ. |
| Next natural trigger | Mốc đã chọn tới hạn hoặc có diễn biến mới; người dùng có lý do tự quay lại. | Cơ hội tiếp trong cùng đợt; hoặc đợt thử sau dùng lại routine và lịch sử có sẵn. |

### Reward và investment phục vụ công việc

**Reward:** hiểu thêm điều mình quan sát và biết rõ mức chắc chắn. Kết quả có thể là ổn định, có thay đổi hoặc chưa đủ dữ liệu; không tạo “phát hiện mới” giả để giữ người dùng.

**Investment:** lịch sử sạch, ngữ cảnh và câu hỏi đã lưu làm lần đối chiếu sau nhẹ hơn. Cho phép xuất/xóa dữ liệu; giá trị tích lũy không phụ thuộc việc khóa người dùng vào app.

> **NẾU BỎ NOTIFICATION**
>
> Lý do quay lại vẫn tồn tại: người dùng muốn hiểu diễn biến tại mốc mình quan tâm hoặc cần thông tin cho một quyết định/câu hỏi mới. Reminder chỉ nhắc mốc đã chọn; không phải bản thân loop.

<a id="validation"></a>

## Giả thuyết nối loop với metric

*05 · PRODUCT LOOP / KIỂM CHỨNG*

> **METRIC HYPOTHESIS · BẮT BUỘC**
>
> Nếu loop đối chiếu có nguồn, lưu nhận xét và kế hoạch tiếp theo hoạt động, **R_due sẽ tăng** ở những cơ hội xem lại đã đủ quan sát trong pilot 6–8 tuần, vì trạng thái đã lưu giúp người dùng biết mình muốn xem lại điều gì và giảm công sức tại mốc kế tiếp. Kỳ vọng tăng 10 điểm phần trăm là mục tiêu thử, chưa phải kết quả hay benchmark.

| Bước thử | Thiết kế đề xuất |
| --- | --- |
| Kiểm chứng nature trước | Phỏng vấn 5–8 người đúng persona về lần đổi routine gần nhất; quan sát họ tìm lại ảnh/ghi chú và xác định thời điểm họ thực sự muốn xem lại. Cỡ mẫu này dùng khám phá, không ước tính retention thị trường. |
| Pilot luồng | Theo dõi các đợt thử thực, cho user tự chọn mốc; đo A14, L1–L3, R_due, coverage và chi phí/Q. 6–8 tuần là kỳ tuyển/quan sát ban đầu; mốc chưa đủ thời gian thì để pending. |
| Nếu thử hai biến thể | A: timeline theo thời gian. B: cùng dữ liệu nhưng có đối chiếu hướng dẫn và trạng thái/câu hỏi trước được đưa lại ở mốc sau. Cả hai dùng cùng completion rule, quality gate, quyền lưu kế hoạch và chính sách nhắc. |
| Phân nhóm & đọc kết quả | Random ở cấp user trước start; không đổi nhánh giữa các mốc. So R_due của cohort cùng thời gian tuyển, cùng độ chín và cadence. Báo chênh lệch, khoảng tin cậy và coverage từng nhánh; không loại user bỏ dở. |
| Cỡ mẫu & kết luận | Chưa có baseline nên chưa ấn định cỡ mẫu A/B. Pilot lấy baseline/độ biến thiên để tính cỡ mẫu cho mức tăng kỳ vọng; chưa đủ mẫu chỉ kết luận tín hiệu định tính, không tuyên bố nhân quả. |

### Quyết định sau thử

**Tiếp tục kiểm chứng:** R_due và coverage không xấu đi, người dùng hiểu bản đối chiếu, chất lượng đạt ngưỡng, không có lỗi nghiêm trọng và chi phí trong ngân sách team đặt trước.

**Sửa:** nhiều input nhưng ít Q → xem friction/giá trị của review. R_due cao nhưng coverage thấp → chưa giải quyết nhóm không chọn mốc. Tương tác tăng nhưng lo lắng tăng → giảm tác động nhắc/thiết kế gây soi da.

**Dừng biến thể:** có lỗi nghiêm trọng hoặc tăng completion bằng cách làm mờ giới hạn. Không kết luận thắng chỉ vì nhiều ảnh, chat hoặc thời gian dùng hơn.

GATE 4 · Loop hai chu kỳ; giả thuyết map R_due; bảng tracking [06 — Bảng tracking với 8 core events](#tracking-events) có 8 event và mỗi event map ít nhất một metric.

<a id="tracking-events"></a>

## 8 core events · phần 1/2

*06 · TRACKING NHANH / PHASE 4*

Mỗi event mô tả điều đã xảy ra, có thời điểm commit cụ thể và nối về metric Phase 3. Không phát event hoàn tất chỉ từ ý định/bấm nút. Các trường dưới đây là phần tối thiểu của từng event; hợp đồng dùng chung ở [Quy ước tracking và tiêu chí nghiệm thu](#tracking-contract).

### 01 · trial_started

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Một đợt thử được tạo có sản phẩm mới, routine snapshot và baseline. |
| Thời điểm ghi nhận | Sau transaction lưu đợt thử + baseline đầu tiên thành công; đúng một lần/trial_id. |
| Metric sử dụng | Mẫu số/start A14; TTV; L1; R_next90 để nhận diện đợt mới. |
| Thuộc tính tối thiểu | user_id, trial_id, baseline_id, routine_version, started_at, is_first_trial; không gửi ảnh/tên sản phẩm vào analytics. |

### 02 · observation_recorded

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Một ghi nhận nối tiếp mới đã được lưu trong đợt thử. Không đồng nhất với một ảnh upload. |
| Thời điểm ghi nhận | Sau lưu observation mới thành công. Edit bản cũ không phát lại; baseline không phát event này. |
| Metric sử dụng | L1; kiểm tra preconditions cho C; phân tích độ đầy đủ đầu vào. |
| Thuộc tính tối thiểu | user_id, trial_id, observation_id, observed_at, recorded_at, has_usage_log, has_context, has_photo, photo_comparable; không gửi nội dung sức khỏe. |

### 03 · trial_review_opened

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Đối chiếu thực sự tải thành công và được hiển thị cho user. |
| Thời điểm ghi nhận | Lần đầu hiển thị nội dung usable của một review_cycle; reload không tạo lần mở đầu mới. |
| Metric sử dụng | Mẫu số L2; tỷ lệ Q/cycle đã mở; cohort chi phí/Q; thời gian hoàn tất mốc. |
| Thuộc tính tối thiểu | user_id, trial_id, review_id, review_cycle_id, opened_at, trigger_type, experiment_variant. Trạng thái đã hiển thị chỉ là tín hiệu UX, chưa phải hiểu nội dung. |

### 04 · trial_review_completed

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Người dùng lưu hoàn tất C theo completion rule. |
| Thời điểm ghi nhận | Server commit chuyển draft/in_progress → completed; lưu transactional outbox để event không mất nếu gửi analytics lỗi. |
| Metric sử dụng | A14, TTV, N28, F_due, R_due, R_next90, L2/L3; join audit để lấy Q. |
| Thuộc tính tối thiểu | user_id, trial_id, review_id, review_cycle_id, completed_at, observation_count, input_version, user_confirmed, uncertainty_recorded, next_step_type, next_review_at, trial_status, ai_assessment_ids. |

<a id="tracking-events-2"></a>

## 8 core events · phần 2/2

*06 · TRACKING NHANH / PHASE 4*

### 05 · review_quality_assessed

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Kết quả audit đã được lưu, tách chất lượng bản AI và bản cuối. |
| Thời điểm ghi nhận | Khi reviewer commit đánh giá; đánh giá lại có assessment_version mới, không ghi thêm một core action. |
| Metric sử dụng | Điều kiện Q cho N28/activation/retention; tỷ lệ đúng, fail, lỗi nghiêm trọng và mức user phải sửa AI. |
| Thuộc tính tối thiểu | review_id, review_cycle_id, assessment_id, assessment_version, assessed_at, final_pass, ai_assessment_results, rubric_version, reviewer_id, failure_codes, severity, user_revision_flag. |

### 06 · trial_status_changed

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Một đợt thử đổi trạng thái thực hoặc người dùng lưu đổi lịch mốc tiếp. |
| Thời điểm ghi nhận | Sau commit chuyển trạng thái; hoặc lưu schedule change có phiên bản mới. Không đổi event completion hay snapshot d cũ. |
| Metric sử dụng | Successful exit, paused_for_support, unknown; mẫu số R_next90; counter về gánh nặng; phân tích sửa lịch/retention. |
| Thuộc tính tối thiểu | user_id, trial_id, state_version, old_status, new_status, reason_code, changed_at, next_review_at, previous_due_at. Gắn change_type = status/schedule; không suy luận đã gặp chuyên gia. |

### 07 · ai_execution_completed

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Một lần thực thi AI kết thúc: thành công, lỗi, timeout hoặc bị hủy; bao gồm output không được dùng. |
| Thời điểm ghi nhận | Backend ghi khi từng attempt kết thúc; reconcile usage hóa đơn. Timeout có ước tính riêng, cập nhật chi phí theo cùng execution_id. |
| Metric sử dụng | Tổng chi phí AI/cycle; cost per Q; tỷ lệ lỗi/retry; phân tích nhóm dùng nhiều. |
| Thuộc tính tối thiểu | execution_id, request_id, attempt_no, user_id, trial_id, review_cycle_id, model_version, status, input/output_tokens, cost_amount, currency, cost_source, output_shown, started_at, finished_at. Không cộng lại bản cập nhật chi phí. |

### 08 · followup_outcome_recorded

| Trường | Đặc tả |
| --- | --- |
| Ý nghĩa | Người dùng chủ động gửi phản hồi về việc dùng lại bản ghi và gánh nặng. |
| Thời điểm ghi nhận | Sau lưu câu trả lời; không mặc định “đã dùng” khi tải/xuất file, hay “không dùng” khi không phản hồi. |
| Metric sử dụng | D_reuse; response coverage; phản hồi gánh nặng/lo lắng; chỉ báo lợi ích ngoài thao tác hoàn tất. |
| Thuộc tính tối thiểu | user_id, review_id, followup_id, response_version, used_for_next_step, used_in_consultation, burden_flag, anxiety_increased, evidence_level = self_report, submitted_at. D_reuse dùng phản hồi mới nhất trong 14 ngày, một review_id một lần. |

Chỉ 8 tên event cốt lõi. Thuộc tính reason_code/quality giúp phân loại, không bổ sung hàng loạt event click không phục vụ metric. Nếu thêm reminder hoặc checkout, phải có metric và hợp đồng riêng trước.

<a id="tracking-contract"></a>

## Hợp đồng đo để tránh đếm sai

*06 · TRACKING / NGHIỆM THU*

| Quy ước chung | Cách triển khai |
| --- | --- |
| Identity & object | user_id ổn định; có quy tắc merge anonymous → signed-in, không tạo user mới khi đổi thiết bị. trial/review/cycle/observation dùng ID bền vững. Không dùng device_id làm user. |
| Thời gian | Lưu UTC, hiển thị/nhóm ngày theo Asia/Ho_Chi_Minh. Window dạng nửa mở [a,b), trừ R_next90 đã ghi (a,b]. Dùng occurred_at của hành vi, không dùng thời điểm event tới kho. |
| Độ chín dữ liệu | Chờ đủ window + 48 giờ audit và reconcile chi phí. Pending không gán 0; công bố tỷ lệ pending/thiếu audit. Audit muộn ghi restatement có version, không âm thầm thay số cũ. |
| Chống trùng | event_id duy nhất; idempotency_key theo object + transition/version. Review completion unique theo user_id + trial_id + review_cycle_id; sửa bản ghi không phát thêm completion. |
| Nguồn & loại trừ | Production backend là nguồn trạng thái hoàn tất. Loại bot/QA/nội bộ theo cờ xác định trước; không loại người dùng vì bỏ dở, chi phí cao hay kết quả không đẹp. |
| Dữ liệu nhạy cảm | Analytics chỉ lưu ID, timestamp, cờ chất lượng và mã trạng thái. Ảnh/nhật ký nằm ở kho sản phẩm phân quyền; cần đồng ý phù hợp cho audit, không đưa ảnh/thông tin da thô vào event. |

### Tiêu chí nghiệm thu · kiểm tra trước khi dùng số

| Ca kiểm thử | Kết quả bắt buộc |
| --- | --- |
| Bấm hoàn tất nhưng lưu lỗi | 0 trial_review_completed; UI giữ nội dung để thử lại. Lưu thành công mới phát một event. |
| Reload, double-click, retry, autosave | Cùng review_cycle chỉ có 1 completion. Retry gửi analytics giữ event_id; kho dedupe. Autosave không chuyển completed. |
| Thiếu baseline/follow-up/nội dung | Không thành C. “Chưa đủ dữ liệu” vẫn thành C nếu đủ đầu vào tối thiểu, nêu giới hạn và có bước tiếp. Luồng hỗ trợ luôn mở. |
| Chất lượng pending/fail | Không tính Q/N28 chính thức; C thô vẫn được giữ. Audit fail sau đó phải cập nhật số có version và lý do. |
| Đổi lịch, đóng đợt, mất liên lạc | Giữ snapshot d và mẫu số cohort đã vào. Không xóa user để tăng R_due; phân loại trạng thái cạnh retention. |
| Biên thời gian & chi phí | Đúng d+72h không thuộc window R_due. Retry AI có execution_id riêng và tính phí; update cùng execution_id không cộng hai lần. Mẫu số 0 trả N/A. |

<a id="self-review"></a>

## Đối chiếu bài hoàn chỉnh

*07 · TỰ SOI & NỘP / PHASE 5*

| Yêu cầu / gate | Kết quả đối chiếu trong bài |
| --- | --- |
| Phase 0 · Phạm vi | Một persona chính, một core job, một use case; ranh giới AI rõ · [00 — Dự án, persona và core job](#pham-vi). |
| Gate 1 · Core action | Đủ 9 trường Card; actor + object + completion rule; 5 tiêu chí và lý do loại hành vi vanity · [01 — Core Action Card và 5 tiêu chí tự kiểm](#core-action). |
| Gate 2 · Nature | Đủ 8 trường Nature Card; chọn theo dự án, có cadence theo template và lý do lặp · [02 — Action Nature Card và kết luận cadence](#nature-cadence). |
| Gate 3 · Metrics | Activation có start/event/window; 2 góc engagement; NSM đúng công thức; 3 leading và counter · [03 — Activation và engagement](#activation-engagement) và [NSM](#north-star). |
| Gate 3 · Retention | Đủ 6 thành phần, mẫu số cố định, độ chín dữ liệu, coverage và kết thúc tốt; không mặc định D7 · [04 — Định nghĩa retention theo cơ hội xem lại](#retention). |
| Gate 4 · Loop & tracking | 2 chu kỳ nối trạng thái tích lũy; metric hypothesis; 8 core events đủ 4 trường đề yêu cầu; tiêu chí nghiệm thu · [05 — Product Loop qua hai chu kỳ](#product-loop). |
| Phase 5 · Tự soi | Kiểm tra cả chuỗi core action → nature → metric/retention → loop → tracking; không lấy output AI, lượt mở app hay gamification thay giá trị. |

### Các giả thuyết chưa được chứng minh

Người dùng chịu ghi đầu vào đủ nhẹ và thấy review hữu ích; chọn mốc tiếp giúp quay lại; window A14, 7 ngày sẵn sàng dữ liệu, 48 giờ hoàn tất/audit, dung sai −48/+72 giờ và R_next90 phù hợp; quality gate chấm được nhất quán; chi phí/Q nằm trong khả năng trả. Những điểm này cần pilot, không có số thực nghiệm trong bài.

**Về Gate 5:** bộ ảnh đề được cung cấp thể hiện Gate 1–4 và bước “Tự soi lỗi & nộp”; không có rubric Gate 5 riêng. Bài thực hiện bước tự soi ở bảng trên, không tự nhận đạt một gate thực nghiệm chưa có tiêu chuẩn.

### Nguồn sử dụng

**[1]** Mai Anh Nguyen (Blue). *AI in Action – Track 1: Retention, Engagement & Habit Loop.* T1_D20.pdf, 49 trang. Trọng tâm: slide 6–12 (NSM); 21–29 (nature, core action, cohort); 31–41 (retention, Hook); 44–49 (áp dụng và tổng kết).

**[2]** Mai Anh Nguyen (Blue). *AI in Action – Day 20 – Track 1: Product Metrics cho sản phẩm AI.* T1_D20 - 2.pdf, 21 trang. Trọng tâm: trang 6, 8–12 (chuỗi giá trị, xong/đúng); 14–20 (chi phí, guardrail, NSM).

**[3]** Đề lab qua 9 ảnh đính kèm: image(20261022-134720), 134732, 134750, 134759, 134809, 134816, 134853, 134907, 134913. Áp dụng các template, yêu cầu 4–8 event và Gate 1–4.

**[4]** *Lab 20 test.pdf*, bản hội thoại 20 trang. Giữ lựa chọn gộp #3 + #6, phạm vi SkinLog và Phase 1 cuối cùng (trang 17–20). Không dùng các đề xuất ban đầu đã được thay thế làm quyết định cuối.

Đánh giá “đạt” trong tài liệu là đối chiếu tính đầy đủ và nhất quán của thiết kế. Chưa có nghiên cứu người dùng, đo retention thật hay xác nhận hiệu quả/an toàn lâm sàng.
