# Báo cáo cá nhân — 2A202603467_KhongTienDuong

> File: `report/individual/2A202603467_KhongTienDuong.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu).
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: KhongTienDuong *(bạn sửa lại có dấu nếu muốn, ví dụ Khổng Tiến Dương)*
- MSSV: 2A202603467
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhom01Ban02
- Link repo nhóm: https://github.com/VuTriDung1123/K5-L3A-DAY02-Nhom01Ban02-DiscoveryProblemFraming.git

---

## 2. Scan problem (CP1)
Dương, Software engineer ở một công ty tầm 10 người, dùng claude code, codex và các phần mềm vibe code. Tuy nhiên, khi chuyển sang một ứng dụng mới hoặc tiếp nhận codebase do thành viên khác tạo ra, các kỹ sư thường phải tự tìm hiểu lại kiến trúc, cấu trúc thư mục, dependencies, business logic, quy ước coding và trạng thái phát triển.

Dương scan 8 problem:

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Tốn thời gian | Khi chuyển sang một ứng dụng mới hoặc tiếp nhận codebase do thành viên khác tạo ra, tôi muốn nhanh chóng hiểu kiến trúc, cấu trúc thư mục, dependencies và business logic, để có thể bắt đầu phát triển mà không phải tự lần mò từ đầu | Software Engineer, Tech Lead | Đo thời gian từ lúc nhận codebase đến khi hoàn thành task đầu tiên; có các rule chung để có thể trao đổi giữa các thành viên nhóm |
| 2 | Lặp lại | Khi bắt đầu một phiên làm việc mới với Claude Code hoặc Codex, tôi muốn không phải cung cấp lại toàn bộ ngữ cảnh dự án, để AI hiểu đúng cấu trúc và các quyết định kỹ thuật trước đó | Software Engineer + các thành viên trong team | Số lần phải giải thích lại context và thời gian chuẩn bị mỗi phiên |
| 3 | Tốn thời gian | Khi AI sinh ra code bị lỗi hoặc không hoạt động như mong đợi, tôi muốn xác định được nguyên nhân gốc rễ, để không phải yêu cầu AI sửa đi sửa lại nhiều lần | Software Engineer | Số lần prompt sửa lỗi và thời gian trung bình để xử lý một bug giống nhau bị lặp lại ở mỗi thành viên khi sửa |
| 4 | Lặp lại | Khi thay đổi một chức năng trong ứng dụng, tôi muốn biết những chức năng nào có khả năng bị ảnh hưởng, để không phải kiểm tra thủ công lại toàn bộ hệ thống sau mỗi lần sửa code | Software Engineer, QA | Thời gian regression testing và số bug phát sinh sau mỗi lần cập nhật khiến việc thay đổi bị ảnh hưởng nhiều chức năng khác |
| 5 | Cần đọc, tổng hợp nhiều thông tin | Khi sử dụng một framework hoặc thư viện mới, tôi muốn nắm được các API, các điểm thay đổi trong công nghệ mới so với công nghệ cũ | Software Engineer | Thời gian nghiên cứu công nghệ mới và số lỗi do sử dụng sai API/version |
| 6 | Cần đọc, tổng hợp nhiều thông tin | Khi AI tạo ra nhiều file code và module trong một lần thực hiện task, tôi muốn hiểu luồng thực thi và mối quan hệ giữa các thành phần, để có thể tự chỉnh sửa và mở rộng ứng dụng khi yêu cầu thay đổi | Software Engineer, Tech Lead | Thời gian đọc hiểu code và thời gian thực hiện task tiếp theo |
| 7 | Pain từ người khác | Khi một thành viên bàn giao ứng dụng được phát triển bằng vibe coding cho tôi, tôi muốn hiểu được các quyết định kỹ thuật, logic nghiệp vụ và trạng thái hiện tại của dự án, để tiếp tục phát triển mà không phải liên tục hỏi người tạo ban đầu | Software Engineer, Tech Lead | Số câu hỏi phải hỏi lại người bàn giao và thời gian onboarding; các tài liệu không thống nhất 1 định dạng |
| 8 | Pain từ người khác | Khi người dùng báo ứng dụng gặp lỗi, tôi muốn nhận được thông tin đầy đủ về thao tác và hoàn cảnh xảy ra lỗi, để có thể tái hiện và xử lý mà không phải trao đổi nhiều lần | Software Engineer, End User, QA | User báo cáo lỗi khi xảy ra ứng dụng; khi 1 dev sửa thì các chức năng khác lại thay đổi theo |

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- (Chưa dùng — bạn tự scan trước. Nếu sau này AI gợi ý thêm, ghi ở đây kèm lý do giữ/bỏ.)

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Tiếp nhận và hiểu codebase mới (#1) | Xảy ra khi các thành viên vibe code mà ko hiểu các chức năng phải làm hoặc sẵn có ở codebase mới, do file mô tả kia ko theo đúng định dạng | Thế nào là hiểu đủ kiến trúc và business logic để bắt đầu làm việc? |
| 2 | Debug code do AI sinh ra (#3) | Phù hợp với thực tế vibe coding, tốn thời gian sửa lỗi nhiều lần, có thể đo bằng thời gian debug và số lần sửa, hoàn toàn có thể sửa các lỗi hay gặp và các thành viên có thể chia sẻ các lỗi hay gặp và cách fix thành công | Làm sao phân biệt lỗi do AI sinh code, lỗi môi trường và lỗi yêu cầu ban đầu? Hay do dev? |
| 3 | Hiểu luồng thực thi và quan hệ giữa các module (#6) | Vấn đề phổ biến khi AI tạo nhiều file và module, khó deploy lên thực tế và ảnh hưởng đến bảo trì mở rộng sau này | Làm thế nào để đánh giá dev đã hiểu codebase? |

### Problem Card #1 — *(từ problem #1: tiếp nhận codebase mới)*

| Trường | Nội dung |
|---|---|
| Job Story | Khi tiếp nhận code mới, tôi muốn hiểu codebase mới, để khi bàn giao code hoặc nhận bàn giao, không bị chậm hoặc bị delay cả nhóm |
| Actor | Software dev (người tiếp nhận bàn giao) + team deploy |
| Thời điểm / bối cảnh | Khoảng 1 tháng trước, cả 2 team đã không có tiếng nói chung về vấn đề này khiến công việc bị gián đoạn, khi phải trao đổi logic code từ thành viên cũ để lại cho thành viên mới, thành viên mới đọc không hiểu |
| Quy trình hiện tại (3–7 bước) | 1. Các thành viên vibe code theo module chức năng · 2. Các thành viên add lên git branch của mình khi code chạy · 3. Các thành viên tạo file mô tả (do AI làm) · 4. Chuyển giao code cho người khác |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 4:mất khoảng 1 tiếng trao đổi |
| Impact (nếu không giải thì sao) | Rất mất thời gian, chậm tiến độ, không đảm bảo bàn giao kịp |
| Success metric (baseline → target) | 3 tiếng → 5 phút đọc hiểu |
| Phương án không dùng AI | Trao đổi miệng và giấy về codebase + logic code giữa các thành viên |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | Agent |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 4 bước

[1 Vibe code theo module chức năng: tùy phần và chức năng]
→ [2 Add lên git branch của mình khi code chạy: 1–2 phút]
→ [3 Tạo file mô tả (do AI làm): khoảng 5–10 phút]
→ [4 Chuyển giao code cho người khác: có file mô tả = 5 phút; không có file = phải đọc lại khoảng 1 tiếng] ← BOTTLENECK
```


### Problem Card #2 — *(từ problem #3: debug code do AI sinh ra)*

| Trường | Nội dung |
|---|---|
| Job Story | Khi debug code do AI sinh ra, tôi gặp rất nhiều lỗi lặp lại của các thành viên trước do vấn đề như thay đổi IDE, thay đổi package hoặc logic code, tôi muốn tạo 1 file các lỗi hay gặp và cách fix, để nhanh chóng hoàn thành khi gặp lỗi tương tự |
| Actor | Team developer |
| Thời điểm / bối cảnh | Khoảng 1 tháng rưỡi trước, bối cảnh ở công ty cũ của tôi |
| Quy trình hiện tại (3–7 bước) | 1. Dev gặp lỗi thì tự fix · 2. Fix xong thì đẩy lên repo nhánh để check, mà không có file ghi lỗi chung · 3. Dev khác gặp lại lỗi như vậy phải nhờ AI check để có thể sửa lại lỗi đã gặp trước đó |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: mất khoảng 5–10 phút mỗi lần |
| Impact (nếu không giải thì sao) | Mỗi thành viên đều mất tương tự thời gian lặp lại để fix lỗi đã fix trước đó |
| Success metric (baseline → target) | 10 phút → 1–2 phút |
| Phương án không dùng AI | Có 1 file chung để mọi người tự đọc và cập nhật |
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | Rule |

Quy trình nháp hiện tại:


```text
HIỆN TẠI — 3 bước

[1 Dev gặp lỗi, tự fix: ước lượng 10 phút mỗi lần]
→ [2 Push lên repo nhánh để check, không có file ghi lỗi chung: 1–2 phút]
→ [3 Dev khác gặp lại lỗi, phải nhờ AI check lại từ đầu: ~10 phút (bằng thời gian dev kia đã bỏ ra fix)] ← BOTTLENECK
```

### Problem Card #3 — *(từ problem #6: hiểu luồng thực thi và quan hệ giữa các module)*

| Trường | Nội dung |
|---|---|
| Job Story | Khi hoàn thành 1 module, đội dev thường không mô tả chuẩn dẫn đến sai lệch thông tin, mặc dù chạy được nhưng khi đội khác cần mở rộng sẽ gặp rất nhiều khó khăn do phải đọc lại từ đầu, tôi muốn các file mô tả hệ thống đúng định dạng và mô tả chuẩn, để các thành viên khác đọc |
| Actor | Tất cả mọi người trong team |
| Thời điểm / bối cảnh | Công ty cũ, 1 tháng trước |
| Quy trình hiện tại (3–7 bước) | 1. Dev hoàn thành xong 1 module chức năng và deploy lên · 2. Đội khác tiếp nhận · 3. Đội khác không hiểu logic, lại phải dò lại từ đầu |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3: mất khoảng 2–3 tiếng |
| Impact (nếu không giải thì sao) | Tất cả các thành viên mới sẽ mất ít nhất 2–3 tiếng để đọc module mới |
| Success metric (baseline → target) | 3 tiếng → 10 phút |
| Phương án không dùng AI |Họp và trình bày trước toàn đội|
| Giả thuyết về AI (nếu có) | |
| Cảm nhận nhanh | Rule +Agent  |

Quy trình nháp hiện tại:

```text
HIỆN TẠI — 3 bước

[1 Dev hoàn thành module chức năng và deploy: 2 tiếng]
→ [2 Đội khác tiếp nhận: 1–2 phút]
→ [3 Đội khác không hiểu logic, phải dò lại từ đầu: 2–3 tiếng] ← BOTTLENECK
```

### Card muốn pitch nhất

- Card số:2
- Vì sao: rất hay gặp và phổ biến. nếu có 1 file debug chung thì AI đỡ đọc cả 1 quy trình để gỡ lỗi đã mắc phải
- Câu hỏi muốn nhóm phản biện: Tại sao khi chỉ 1 file .md mà team ko làm việc đó ?

### AI đã phản biện card thế nào

*(AI đóng vai PM hoài nghi — `RULES.md` §2: AI chỉ phản biện, không viết lại thay bạn. Bạn tự trả lời 2 cột còn lại.)*

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| **[Card #1] Bottleneck chưa có số phút:** "phải trao đổi lại" không ghi mất bao nhiêu phút/lần — rubric trừ điểm nếu quy trình không có số phút từng bước | | |
| **[Card #1] Metric "5 phút đọc hiểu" chưa rõ cách đo:** đo ai, đo lúc nào, "hiểu đủ" theo tiêu chí nào? Chính bạn ghi ở bảng top 3 "chưa chắc: thế nào là hiểu đủ" — metric cần trả lời được câu đó, ví dụ: "đọc file mô tả xong, tự chạy build và giải thích được 3 module chính" | | |
| **[Card #1] Cảm nhận nhanh ghi "Agent" nhưng không có giả thuyết AI:** chưa nói Agent sẽ tự làm gì, và chưa giải thích vì sao Rule hoặc Workflow không đủ (CP6 sẽ bắt trả lời "vì sao không chọn mức đơn giản hơn") | | |
| **[Card #1] Bước 3 bạn đã "tạo file mô tả do AI làm" nhưng người tiếp nhận vẫn phải trao đổi lại (bước 4) → file mô tả thất bại:** thiếu gì trong file, sai định dạng nào? Đây chính là giả định quan trọng cần kiểm chứng ở CP4 | | |
| **[Card #2] Job Story đang chứa solution trá hình:** "tôi muốn tạo 1 file các lỗi hay gặp và cách fix" — "file" là giải pháp, không phải problem. Gợi ý viết lại theo problem: "Khi debug code do AI sinh ra, tôi muốn biết ngay lỗi này nhóm đã từng gặp và cách fix chưa, để không phải mất 5–10 phút xử lý lại mỗi lỗi lặp lại" | | |
| **[Card #2] Bước 2 mơ hồ:** "đẩy lên repo nhánh để check mà không có file lỗi" — ai check, ở đâu, xong bước này quy trình để lại dấu vết gì? Nếu sau fix không có gì được ghi lại thì bước 3 lặp lại là tất yếu | | |
| **[Card #2] Metric "10 phút → 1–2 phút" chưa có cách đo:** baseline 10 phút lấy từ bao nhiêu lần/là trung bình? Đo gì làm bằng chứng (log prompt, thời gian đóng ticket)? | | |
| **[Card #3] "Rule + Agent" là 2 mức cùng lúc:** bạn phải chọn 1 mức để so sánh công bằng, và trả lời được vì sao Rule không đủ nếu chọn Agent | | |
| **[Card #3] Impact lặp lại metric:** "mất 2–3 tiếng đọc module" trùng success metric. Impact nên nói hậu quả rộng hơn: deploy/sửa nhầm, mở rộng chậm, rủi ro bug khi đội mới không hiểu module | | |

*(Gợi ý: chọn ít nhất 2 điểm bạn đồng ý để sửa card — rubric C2 yêu cầu sửa ít nhất 1 điểm mới đạt đủ 10 điểm.)*

---

## 4. Tôi đã tham gia phần nào (CP3 → CP7)

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | | |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: | |
| Nhận phản biện | Câu hỏi tôi nhận được: | Tôi đã sửa gì: |
| Gom cluster / cây OST | | |
| Chọn candidate problem | | |
| Kiểm chứng / research | | |
| Quy trình nhóm | | |
| Problem Statement | | |
| Mức can thiệp AI | | |
| Quyết định | | |

---

## 5. Dùng AI

| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | | | | |
| CP2 Problem Card | Đưa 3 card vào AI đóng vai PM hoài nghi để phản biện; nhờ AI vẽ 3 quy trình nháp ASCII (có số phút, đánh dấu bottleneck) từ mô tả của tôi | Phát hiện bottleneck thiếu số phút, metric chưa rõ cách đo, Job Story chứa solution trá hình, Actor chứa 2 mức can thiệp cùng lúc | *(bạn tự điền: AI có điểm nào sai/thiếu so với thực tế của bạn?)* | *(bạn tự điền: chọn các điểm phản biện mà bạn đồng ý rồi sửa card/chọn giữ nguyên)* |
| CP4 Research | | | | |
| CP5 Quy trình | | | | |
| CP5–6 Problem Statement | | | | |
| CP6 Mức can thiệp / quyết định | | | | |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**

**6.5. Điều khó nhất khi viết Problem Statement là gì?**

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.

---

## 7. Tài liệu tham khảo

-
