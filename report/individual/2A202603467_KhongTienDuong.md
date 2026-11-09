# Báo cáo cá nhân — 2A202603467_KhongTienDuong

> File: `report/individual/2A202603467_KhongTienDuong.md` (MSSV trước, dấu `_`, họ tên viết liền không dấu).
> Template chi tiết và prompt mẫu cho từng mục: [docs/01-worksheet.md](../../docs/01-worksheet.md).
> Mỗi thành viên một file trong `report/individual/` trên repo nhóm: commit bằng tài khoản GitHub của bạn. Không viết hộ người khác.

## 1. Thông tin học viên

- Họ tên: KhongTienDuong *(bạn sửa lại có dấu nếu muốn, ví dụ Khổng Tiến Dương)*
- MSSV: 2A202603467
- Email trường :
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
| Cảm nhận nhanh | Agent, thay đổi được  |

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
| Cảm nhận nhanh | Rule, có thể thay đổi, chỉ cần chú ý  |

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
| Cảm nhận nhanh | Rule +Agent , có thể thay đổi được  |

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
| **[Card #1] Bottleneck chưa có số phút** | ✅ Đồng ý | **Đã sửa đúng lúc đó:** điền "mất khoảng 1 tiếng trao đổi" vào Bottleneck; quy trình nháp có giờ từng bước (1–2', 5–10', 5'/1 tiếng) + đánh dấu BOTTLENECK |
| **[Card #1] Metric "5 phút đọc hiểu" chưa rõ cách đo ("hiểu đủ" là gì)** | Đồng ý một phần | Giữ số metric như bảng chấm top 3; **chưa sửa ngay** — cần định nghĩa "hiểu đủ" khi nhóm viết Problem Statement v0/v1 (CP5–CP6) |
| **[Card #1] Chọn Agent nhưng không có giả thuyết AI / chưa giải thích vì sao không Rule/Workflow** | Đồng ý một phần | **Chưa sửa trong card** — sẽ giải trình khi nhóm so sánh 4 mức ở CP6 (trả lời "vì sao không chọn mức đơn giản hơn") |
| **[Card #1] File mô tả (bước 3, do AI làm) nhưng người nhận vẫn không hiểu → file thất bại** | ✅ Đồng ý | Chuyển thành **giả định quan trọng để kiểm chứng ở CP4**: "file mô tả sai/thiếu vì sao?" (khớp cả problem #7: tài liệu không thống nhất định dạng) |
| **[Card #2] Job Story chứa solution trá hình ("tôi muốn tạo 1 file…")** | Đồng ý một phần | Giữ bản gốc để pitch; nếu nhóm phản biện cùng hướng thì viết lại theo gợi ý: problem = "mất 5–10 phút xử lý lại từng lỗi lặp lại", file là giải pháp |
| **[Card #2] Bước 2 mơ hồ (ai check, để lại dấu vết gì)** | Đồng ý một phần | Bước 2 đã có giờ (1–2'); phần "sau fix để lại dấu vết gì" chưa có dữ liệu thật — để CP4 kiểm chứng |
| **[Card #2] Metric "10 → 1–2 phút" chưa có cách đo** | Đồng ý một phần | Quy trình nháp đã ghi rõ nguồn con số (ước lượng 10 phút/lần); cách đo chuẩn (log prompt/thời gian) để CP5 khi viết metric |
| **[Card #3] "Rule + Agent" là 2 mức cùng lúc** | ✅ Đồng ý | **Chưa chốt trong card** — giữ vấn đề để nhóm chấm/so sánh ở CP3; sẽ chọn 1 mức khi so sánh 4 mức ở CP6 (và trả lời vì sao mức còn lại không đủ) |
| **[Card #3] Impact lặp lại metric (2–3 tiếng đọc module)** | Đồng ý một phần | **Chưa sửa** — học được rằng impact cần nói hậu quả rộng hơn (deploy/sửa nhầm, mở rộng chậm, rủi ro bug); sẽ bổ sung khi nhóm viết Problem Statement |

**Kết luận cá nhân:** đã sửa ngay 1 điểm (số phút bottleneck Card #1 — điều kiện tối thiểu C2 ✅), 3 điểm chuyển thành giả định kiểm chứng CP4 / phần chốt CP6, còn lại giữ nguyên có lý do.

*(Gợi ý: chọn ít nhất 2 điểm bạn đồng ý để sửa card — rubric C2 yêu cầu sửa ít nhất 1 điểm mới đạt đủ 10 điểm.)*

---

**## 4. Tôi đã tham gia phần nào (CP3 → CP7)**
---
| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng tới bài nhóm |
|---|---|---|
| Pitch Problem Card | Trình bày Card #1 về việc mất nhiều thời gian họp và nhắn tin hỏi tiến độ. Tôi đưa ra vấn đề mất khoảng 2 giờ mỗi ngày và đề xuất cách giảm thời gian cập nhật tiến độ | Giúp nhóm có thêm một vấn đề để xem xét, đặc biệt là việc lead phải liên tục hỏi tiến độ từng thành viên |
| Phản biện bài của bạn khác | Câu hỏi tôi đã đặt: Nếu chỉ sử dụng standup 15 phút và bảng cập nhật công việc cuối ngày thì có thể giảm được một nửa thời gian họp và hỏi tiến độ không? | Giúp nhóm nhìn nhận thêm khả năng giải quyết vấn đề bằng cách đơn giản, chưa cần sử dụng AI |
| Nhận phản biện | Tôi nhận được góp ý về việc số liệu 2 giờ mỗi ngày mới chỉ là ước lượng, chưa có thời gian đo thực tế. Ngoài ra, có ý kiến cho rằng vấn đề chờ phân việc có thể giải quyết bằng backlog | Tôi ghi nhận những góp ý này và xác định cần đo lại thời gian thực tế, đồng thời xem xét các giải pháp không dùng AI trước |
| Gom cluster / cây OST | Tôi đóng góp các vấn đề liên quan đến việc cập nhật tiến độ, chờ phân công công việc và hai người cùng code nhưng không nắm được thay đổi của nhau | Giúp nhóm nhìn ra những vấn đề có liên quan đến việc phối hợp và chia sẻ thông tin trong quá trình làm dự án |
| Chọn candidate problem | Tôi đề xuất Card #1 vì vấn đề xảy ra thường xuyên, ảnh hưởng đến nhiều người và có số liệu ước lượng khoảng 120 phút mỗi ngày | Có thêm cơ sở để nhóm đánh giá và so sánh với các vấn đề khác trước khi chọn vấn đề chính |
| Kiểm chứng / research | Tôi đề xuất kiểm tra lại thời gian họp, nhắn tin hỏi tiến độ và tìm hiểu xem các nhóm khác đang sử dụng công cụ nào để quản lý công việc | Giúp nhận ra số liệu ban đầu vẫn cần được kiểm chứng, không nên xem những con số ước lượng là kết quả chính thức |
| Quy trình nhóm | Tôi mô tả quy trình hiện tại khi lead hỏi tiến độ, chờ phản hồi, tổ chức họp và thông báo lại cho những người liên quan | Giúp nhóm xác định được bước mất nhiều thời gian nhất là họp cập nhật tiến độ, khoảng 60 phút mỗi ngày theo ước lượng |
| Problem Statement | Tôi góp ý cần xác định rõ vấn đề, đối tượng bị ảnh hưởng và metric để đánh giá kết quả. Không nên đưa giải pháp AI vào ngay khi chưa làm rõ problem | Giúp Problem Statement tập trung vào vấn đề thực tế thay vì chỉ mô tả một công cụ muốn xây dựng |
| Mức can thiệp AI | Tôi đề xuất AI có thể hỗ trợ tổng hợp tiến độ từ commit, Pull Request và tin nhắn. Tuy nhiên, AI chỉ nên đưa ra bản tóm tắt để lead kiểm tra trước khi gửi | Giúp nhóm cân nhắc mức độ sử dụng AI phù hợp, tránh để AI tự quyết định hoặc giao việc khi chưa cần thiết |
| Quyết định | Tôi cho rằng nên thử standup 15 phút và bảng cập nhật công việc trước. Nếu vẫn mất nhiều thời gian tổng hợp thông tin thì mới xem xét sử dụng AI | Giúp nhóm có thêm góc nhìn về việc ưu tiên giải pháp đơn giản trước, chỉ sử dụng AI khi thực sự cần thiết |

---
## 5. Dùng AI

**## 5. Dùng AI**
---
| Checkpoint | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai hoặc hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| CP1 Scan | Không dùng AI, tự tìm và ghi ra 8 vấn đề trước rồi mới sử dụng AI ở các bước sau | — | — | — |
| CP2 Problem Card | Đưa 3 card cho AI phản biện như một PM khó tính; nhờ AI vẽ lại quy trình bằng ASCII, có thời gian từng bước và đánh dấu bottleneck | Giúp phát hiện những chỗ còn thiếu như thời gian từng bước, bottleneck, metric chưa rõ cách đo và Job Story còn lẫn giải pháp | AI yêu cầu phải có số liệu đo thực tế trong khi dữ liệu của tôi mới chỉ là ước lượng. Ngoài ra AI có lúc sửa format và chính tả chưa chính xác | Tôi tự kiểm tra lại các góp ý, bổ sung thời gian và bottleneck. Những số liệu chưa được kiểm chứng thì giữ ở dạng ước lượng và sẽ kiểm tra thêm ở các bước sau |
| CP4 Research | Nhờ AI gợi ý một số công cụ và cách làm tương tự để tham khảo, như FAQ, memory bank và Decision Log | Giúp tìm hướng nghiên cứu nhanh hơn và biết thêm một số cách giải quyết vấn đề | Có lúc AI đưa link nhưng nội dung bên trong không đúng như mô tả | Tôi tự mở và kiểm tra lại từng link, chỉ giữ những tài liệu thực sự liên quan đến vấn đề của nhóm |
| CP5 Quy trình | Nhờ AI chuyển quy trình của nhóm thành sơ đồ ASCII hoặc Mermaid, có thời gian từng bước và đánh dấu bottleneck | Giúp trình bày quy trình rõ ràng hơn, dễ nhìn ra bước nào mất nhiều thời gian | AI đôi khi gộp hai bước thành một hoặc đặt sai vị trí bottleneck | Tôi đối chiếu lại từng bước với quy trình thực tế của nhóm trước khi đưa vào báo cáo |
| CP5–6 Problem Statement | Nhờ AI đọc và phản biện Problem Statement để tìm những điểm còn thiếu hoặc chưa hợp lý, không nhờ AI viết lại | Giúp nhận ra metric chưa rõ cách đo và cần xác định rõ giới hạn của AI | AI có xu hướng muốn viết lại toàn bộ Problem Statement thay vì chỉ ra vấn đề | Tôi chỉ lấy những góp ý phù hợp, sau đó cùng nhóm tự chỉnh sửa và đưa ra Problem Statement cuối cùng |
| CP6 Mức can thiệp / quyết định | Nhờ AI góp ý so sánh các mức độ can thiệp của AI và những rủi ro có thể gặp | Giúp tôi nhìn được ưu nhược điểm của từng mức và có thêm cơ sở để giải thích lựa chọn của nhóm | AI đôi khi đề xuất sử dụng AI nhiều hơn mức thực tế cần thiết | Nhóm tự đánh giá và lựa chọn mức can thiệp dựa trên vấn đề thực tế và kết quả kiểm chứng, không chọn chỉ vì AI đề xuất |

---

## 6. Reflection (CP7)

Trả lời bằng trải nghiệm thật của bạn, tối thiểu 200 từ cho các câu 6.1–6.6 (không tính 6.7, câu này được chấm riêng ở tiêu chí C5). **Không dùng AI để viết thay.**

**6.1. Tôi học được gì khi nghe top 3 problems của các bạn khác?**
Tôi học được cách để đảo lộn vấn đề, các mặt trái và cách 1 vấn đề được phân tích, cách làm việc của các bạn khác

**6.2. Nhóm có lúc nào bị "solution-first" (nghĩ giải pháp trước khi hiểu vấn đề) không? Lúc đó nhóm nhận ra và xử lý thế nào?**
không, đa số dựa vào trải nghiệm thực tế của các bạn

**6.3. Tôi có đổi ý sau khi bị phản biện không? Kể một lần cụ thể.**
Không

**6.4. Kết quả kiểm chứng (phỏng vấn/survey/research) có làm tôi bất ngờ không? Điều gì?**
có bất ngờ, vì dự án phần trao đổi qua lại giữa các thành viên team dev về 1 chức năng lâu hơn tôi nghĩ

**6.5. Điều khó nhất khi viết Problem Statement là gì?**
phải có kinh nghiệm

**6.6. Nếu làm lại, tôi sẽ đổi gì? Tôi sẽ phản biện nhóm mạnh hơn ở điểm nào?**
Tôi tạm thời chưa đổi gì
tôi sẽ phản biện phần logic 

**6.7. Hiểu bài:** giải thích bằng 5–8 câu, không nhìn tài liệu, chuỗi *problem → quy trình → metric → boundary → mức can thiệp AI → quyết định* của bài nhóm mình.
problem: phải xem tất cả các tài liệu từ các ứng dụng khác như zalo, fb, discord, ... dẫn đến rối
Quy trình : Tạo gg sheet lên để đánh dấu các việc, có thông báo
Mức can thiệp: chủ yếu trải nghiệm thực tế
quyết định : giữ phần gg sheet và có thể tích hợp thêm thông báo 

---

## 7. Tài liệu tham khảo

-
