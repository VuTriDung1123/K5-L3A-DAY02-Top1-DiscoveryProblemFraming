# Báo cáo cá nhân — 2A202603455_PhanHoangPhuc

> Đổi tên file theo quy tắc `MSSV_HoTen.md`, ví dụ `20241234_NguyenVanAn.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu). Sửa cả dòng tiêu đề phía trên cho khớp.
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: copy template này thành file mới, điền, rồi commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: Phan Hoàng Phúc
- MSSV: 2A202603455
- Email trường (không bắt buộc, repo có thể để public):
- Tên nhóm: Nhom01Ban02
- Link repo nhóm: https://github.com/VuTriDung1123/K5-L3A-DAY02-Nhom01Ban02-DiscoveryProblemFraming

---

## 2. Scan problem (CP1)

Lăng kính: **Lặp lại** · **Tốn thời gian** · **Cần đọc, tổng hợp nhiều thông tin** · **Pain từ người khác**.

| # | Lăng kính | Job Story: Khi… tôi muốn… để… | Ai chịu ảnh hưởng? | Dấu hiệu thật (thời gian, tần suất, số người, bằng chứng) |
|---:|---|---|---|---|
| 1 | Pain từ người khác | Khi làm chung dự án mà mỗi người một kiểu và ai cũng bận, ít họp được, tôi muốn nắm được ý kiến của từng thành viên, để cả nhóm đi cùng một hướng mà không phải kéo mọi người vào họp | Tôi, các thành viên, nhân viên trong dự án | Gặp ở mọi nhóm từ 2 người trở lên tôi từng làm; nhiều người quen làm startup cũng gặp |
| 2 | Pain từ người khác | Khi tôi và bạn tech còn lại cùng code, phải push/pull liên tục mới biết nhau làm tới đâu, tôi muốn nắm được tiến độ của nhau mà không cần pull code về xem, để hai bên không làm lệch hoặc trùng việc | Tôi, bạn tech còn lại (đều là tech lead) | Push/pull nhiều lần mỗi ngày vì code cùng AI nên làm rất nhanh, tiến độ đổi liên tục |
| 3 | Lặp lại | Khi tôi làm xong phần việc của mình, tôi muốn có sẵn việc tiếp theo nên làm, để không phải ngồi chờ người phân việc hay không biết làm gì tiếp | Tôi, bạn tech còn lại, người phân việc | Mỗi lần xong việc đều phải chờ trao đổi để phân việc tiếp |
| 4 | Lặp lại | Khi tôi ở vai trò lead cần biết dự án đang tới đâu, tôi muốn nắm được tiến độ từng người mà không phải hỏi lại liên tục, để không làm phiền và gây khó chịu cho người đang làm | Lead/CEO, các thành viên bị hỏi | Lead hỏi tiến độ mỗi ngày ("hôm nay làm tới đâu") |
| 5 | Tốn thời gian | Khi cần biết mọi người đang làm tới đâu, tôi muốn có thông tin tiến độ mới nhất ngay, để không phải tốn thời gian họp và nhắn tin hỏi qua lại | Tôi, cả nhóm | Đã thử Jira và công cụ quản lý việc nhưng mọi người cập nhật chậm, Jira chỉ hợp với quy trình lặp lại cố định. Tự ước lượng: khoảng 2 giờ/ngày (họp trực tiếp, họp online, nhắn tin hỏi tiến độ), tức khoảng 10 giờ/tuần làm việc |

**Ý chưa đưa vào bảng vì chưa có dấu hiệu đo được** (để kiểm chứng sau ở CP4):

- Khi có ý tưởng mới giữa chừng, tôi muốn đưa nó vào kế hoạch chung mà không làm rối việc mọi người đang làm, để ý hay không bị bỏ quên mà nhóm vẫn đi đúng hướng
- Khi nhóm đổi kế hoạch hoặc chốt một quyết định, tôi muốn những người liên quan đều biết, để không ai làm theo thông tin cũ

**Nếu có dùng AI để gợi ý thêm:** ý nào AI gợi ý mà bạn giữ lại, ý nào bỏ và vì sao.

- Các vấn đề đều do tôi tự nêu; AI (Claude) chỉ giúp viết lại thành Job Story và tách ý gộp thành dòng riêng (dòng 3, 4, 5 và hai ý chưa có bằng chứng tách từ cùng một ý ban đầu của tôi).
- Ý ban đầu của tôi là "cần một automation biết mọi người đang làm tới đâu, gợi ý chia việc theo plan". AI chỉ ra đây là giải pháp, không phải problem, nên tôi tách phần pain vào bảng và để ý giải pháp lại cho CP2/CP6.

---

## 3. Top 3 Problem Cards + quy trình nháp (CP2)

### Bảng chọn top 3

| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---:|---|---|---|
| 1 | Mất khoảng 2 giờ/ngày họp và nhắn tin hỏi tiến độ (gộp dòng 4 và 5) | Có số rõ nhất, lặp lại mỗi ngày, đã thử Jira mà không giải quyết được | 2 giờ là tự ước lượng, chưa bấm giờ thật |
| 2 | Xong việc phải chờ trao đổi mới có việc tiếp (dòng 3) | Bước nghẽn rõ, xảy ra mỗi lần xong việc | Chưa đo thời gian chờ thật mỗi lần |
| 3 | Hai tech lead phải push/pull mới biết tiến độ nhau (dòng 2) | Đặc thù khi code cùng AI, tiến độ đổi rất nhanh | Có thể chỉ cần quy ước commit/nhắn tin là đủ |

### Problem Card #1 — Họp và nhắn tin hỏi tiến độ

| Trường | Nội dung |
|---|---|
| Job Story | Khi cần biết mọi người đang làm tới đâu, tôi muốn có thông tin tiến độ mới nhất ngay, để không phải tốn thời gian họp và nhắn tin hỏi qua lại |
| Actor | Lead/tech lead trong nhóm làm dự án từ 2 người trở lên, và các thành viên bị hỏi |
| Thời điểm / bối cảnh | Mỗi ngày làm việc; mọi người bận, làm lệch giờ, code cùng AI nên tiến độ đổi nhanh |
| Quy trình hiện tại (3–7 bước) | 1. Lead nhắn hỏi từng người "hôm nay tới đâu" · 2. Chờ trả lời, hỏi lại người chưa trả lời · 3. Họp online/trực tiếp cập nhật · 4. Thống nhất ai làm gì tiếp · 5. Nhắn lại cho người vắng họp |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, họp cập nhật: khoảng 60 phút/ngày |
| Impact (nếu không giải thì sao) | Khoảng 2 giờ/ngày, 10 giờ/tuần mỗi người; người bị hỏi liên tục thấy khó chịu, mất tập trung |
| Success metric (baseline → target) | Thời gian họp + nhắn hỏi tiến độ từ khoảng 120 phút/ngày xuống dưới 30 phút/ngày |
| Phương án không dùng AI | Standup cố định 15 phút + mỗi người tự cập nhật bảng việc cuối ngày theo template |
| Giả thuyết về AI (nếu có) | Tự tổng hợp tiến độ từ commit, PR, tin nhắn thành bản tóm tắt mỗi ngày; lead duyệt trước khi gửi nhóm |
| Cảm nhận nhanh | Workflow |

Quy trình nháp hiện tại (số phút từng bước là ước lượng, tổng khoảng 120 phút/ngày):

```text
MỖI NGÀY — khoảng 120 phút

[1 Nhắn hỏi từng người: 15'] → [2 Chờ trả lời, hỏi lại: 20']
→ [3 Họp cập nhật: 60'] ← BOTTLENECK
→ [4 Thống nhất việc tiếp: 15'] → [5 Nhắn lại người vắng: 10']
```

### Problem Card #2 — Chờ phân việc tiếp theo

| Trường | Nội dung |
|---|---|
| Job Story | Khi tôi làm xong phần việc của mình, tôi muốn có sẵn việc tiếp theo nên làm, để không phải ngồi chờ người phân việc hay không biết làm gì tiếp |
| Actor | Thành viên code (tech lead) vừa xong một phần việc |
| Thời điểm / bối cảnh | Mỗi lần xong một việc, nhiều lần trong ngày vì code cùng AI làm rất nhanh |
| Quy trình hiện tại (3–7 bước) | 1. Làm xong, push code · 2. Báo nhóm/lead đã xong · 3. Chờ lead rảnh để trao đổi · 4. Trao đổi, phân việc mới · 5. Đọc yêu cầu, bắt đầu việc mới |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, chờ lead rảnh: khoảng 30 phút/lần |
| Impact (nếu không giải thì sao) | Thời gian chết giữa các việc; lead bị kéo vào phân việc liên tục |
| Success metric (baseline → target) | Thời gian từ lúc xong việc đến lúc bắt đầu việc mới: từ khoảng 30 phút xuống dưới 5 phút |
| Phương án không dùng AI | Danh sách việc (backlog) sắp sẵn theo ưu tiên; ai xong thì tự lấy việc đầu danh sách |
| Giả thuyết về AI (nếu có) | Gợi ý việc tiếp theo dựa trên plan và việc vừa xong; người làm xác nhận trước khi nhận |
| Cảm nhận nhanh | No AI / Rule |

Quy trình nháp hiện tại (số phút là ước lượng):

```text
MỖI LẦN XONG VIỆC — khoảng 65 phút

[1 Push code: 5'] → [2 Báo đã xong: 5']
→ [3 Chờ lead rảnh: 30'] ← BOTTLENECK
→ [4 Trao đổi, phân việc: 15'] → [5 Đọc yêu cầu, bắt đầu: 10']
```

### Problem Card #3 — Push/pull mới biết tiến độ của nhau

| Trường | Nội dung |
|---|---|
| Job Story | Khi tôi và bạn tech còn lại cùng code, phải push/pull liên tục mới biết nhau làm tới đâu, tôi muốn nắm được tiến độ của nhau mà không cần pull code về xem, để hai bên không làm lệch hoặc trùng việc |
| Actor | Hai tech lead cùng code một dự án |
| Thời điểm / bối cảnh | Nhiều lần mỗi ngày; code cùng AI nên mỗi lần push thay đổi nhiều |
| Quy trình hiện tại (3–7 bước) | 1. Bạn kia push · 2. Tôi pull về · 3. Đọc diff, chạy thử để hiểu bạn đã làm gì · 4. Nhắn hỏi lại chỗ chưa hiểu · 5. Chỉnh phần mình cho khớp |
| Bottleneck (bước nào, mất bao nhiêu phút) | Bước 3, đọc diff và chạy thử: khoảng 15 phút/lần |
| Impact (nếu không giải thì sao) | Mất thời gian mỗi lần đồng bộ; dễ làm lệch hoặc trùng việc |
| Success metric (baseline → target) | Thời gian để hiểu bạn kia vừa làm gì: từ khoảng 15 phút/lần xuống dưới 3 phút/lần |
| Phương án không dùng AI | Quy ước commit message rõ ràng + mỗi lần push nhắn 1 dòng "đã làm gì, còn gì" |
| Giả thuyết về AI (nếu có) | Tóm tắt thay đổi trong mỗi lần push thành vài dòng dễ hiểu, gửi vào kênh chat nhóm |
| Cảm nhận nhanh | Rule / Workflow |

Quy trình nháp hiện tại (số phút là ước lượng):

```text
MỖI LẦN ĐỒNG BỘ — khoảng 40 phút

[1 Bạn kia push: 2'] → [2 Tôi pull: 3']
→ [3 Đọc diff, chạy thử: 15'] ← BOTTLENECK
→ [4 Nhắn hỏi lại: 10'] → [5 Chỉnh phần mình: 10']
```

### Card muốn pitch nhất

- Card số: 1 và 2 (pitch chung)
- Vì sao: cả hai đều nghẽn ở quy trình việc trong nhóm: không nắm được tiến độ (card 1) và không có sẵn việc tiếp theo (card 2). Giải quyết được hai bước này thì nhóm không còn tình trạng thiếu chủ động. Card 1 có số đo rõ nhất (khoảng 2 giờ/ngày), người quen làm startup cũng gặp
- Câu hỏi muốn nhóm phản biện: Nếu chỉ đặt standup cố định 15 phút và một backlog sắp sẵn theo ưu tiên, có giảm được một nửa thời gian họp và thời gian chờ việc không?

### AI đã phản biện card thế nào

| Điểm yếu AI chỉ ra | Đồng ý? | Đã sửa gì |
|---|---|---|
| Ý ban đầu "cần automation theo dõi tiến độ, gợi ý chia việc" là giải pháp, không phải problem | Đồng ý | Tách phần pain vào bảng scan; giữ ý giải pháp lại cho CP6 |
| Baseline 2 giờ/ngày và số phút từng bước chỉ là ước lượng, chưa bấm giờ thật | Đồng ý | Ghi rõ "ước lượng" trong card; sẽ bấm giờ thật 1–2 ngày để kiểm lại |
| "Thiếu chủ động" là tính cách, không phải một bước trong quy trình | Không đồng ý | Giữ ý: thiếu chủ động là pain thật vì không biết làm gì tiếp, không có gì gợi ý việc tiếp theo. Thể hiện trong card 2 ở bước chờ phân việc |
| Card 2 có thể chỉ cần backlog sắp sẵn (No AI), chưa chắc cần AI | Đồng ý | Để cảm nhận nhanh card 2 là No AI / Rule, ghi backlog sắp sẵn làm phương án không dùng AI |

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
| CP1 Scan | Viết lại ý thô của tôi thành Job Story, tách các ý gộp thành dòng riêng, chỉ ra dòng nào còn thiếu số đo | Tách một ý "cần automation theo dõi tiến độ, gợi ý chia việc" thành nhiều pain riêng; chỉ ra đó là giải pháp chứ chưa phải problem | Hiểu sai "người kia" là người không code; lúc đầu cho rằng "thiếu chủ động" không phải điểm nghẽn | Tôi giải thích người kia cũng là tech lead, AI viết lại dòng 2. Tôi giữ quan điểm thiếu chủ động là pain vì không biết làm gì tiếp; bỏ 2 ý chưa có bằng chứng ra khỏi bảng |
| CP2 Problem Card | Đề xuất top 3, dựng quy trình nháp, đóng vai PM hoài nghi phản biện card | Gộp hai dòng trùng (hỏi tiến độ và tốn 2 giờ/ngày) thành card 1; gợi ý phương án không dùng AI (standup cố định, backlog sắp sẵn) | Số phút từng bước do AI đề xuất, không phải đo thật; vẫn coi "thiếu chủ động" là tính cách | Tôi kiểm và giữ số phút như ước lượng của mình, ghi rõ "ước lượng", sẽ bấm giờ thật; không đồng ý điểm thiếu chủ động; tự quyết pitch chung card 1 và 2 vì cùng là nghẽn quy trình việc |
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
