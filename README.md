# Track1 Day17 — Problem Interview Practice

## 1. Thông tin cá nhân và nhóm

- **MHV:** 2A202602736
- **Họ và tên:** Nguyễn Duy Khánh 
- **Tên nhóm:** Deminer
- **Thành viên:**
  - Nguyễn Phạm Oanh Oanh - 2A202602518
  - Nguyễn Duy Khánh - 2A202602736
  - Hoàng Bích Ngọc - 2A202602766
- **Case đã chọn:** Case C — AI Support Radar

> Đây là bài luyện Problem Interview. Các kết quả dưới đây là hypothesis và practice evidence, **không được xem là validation của solution hoặc problem**.

---

# 2. Problem Hypothesis Brief

## 2.1. Solution directive

Sau mỗi phiên học, hệ thống phân tích các tín hiệu học tập của learner để suy đoán learner nào có thể cần hỗ trợ, xác định phần nội dung có vấn đề và tạo danh sách ưu tiên cho instructor xem xét.

---

## 2.2. Capability trung tính

Giúp người hỗ trợ **nhận biết những learner có thể đang gặp khó khăn, hiểu được context của điểm vướng và quyết định ai cần được hỗ trợ trước**, kể cả khi learner chưa chủ động yêu cầu giúp đỡ.

Capability này không phụ thuộc vào việc phải sử dụng AI hay Support Queue.

---

## 2.3. Expected Change

Nhóm giả định chuỗi thay đổi:

**Nhận biết learner có dấu hiệu gặp khó khăn**

→ **Instructor/Lab Coach có thêm context**

→ **Biết learner nào cần được kiểm tra hoặc hỗ trợ**

→ **Can thiệp đúng người và đúng thời điểm**

→ **Learner tháo gỡ điểm vướng sớm hơn**

→ **Giảm việc học tiếp khi chưa hiểu hoặc mắc kẹt quá lâu**

### Output

Thông tin về learner có khả năng cần hỗ trợ và context liên quan.

### Behavior change cần xảy ra

Instructor/Lab Coach phải sử dụng thông tin đó để kiểm tra hoặc hỗ trợ learner.

### Desired outcome

Learner nhận được sự hỗ trợ phù hợp và kịp thời hơn.

---

# 2.4. Actors

| Actor | Job hiện tại | Pain có thể có |
|---|---|---|
| Learner | Hiểu nội dung và hoàn thành bài học | Không biết mình đang sai, không biết hỏi gì hoặc không tìm được hỗ trợ phù hợp |
| Lab Coach / TA | Phát hiện và hỗ trợ learner gặp vướng mắc | Khó nhận biết learner im lặng hoặc chưa biết cách đặt câu hỏi |
| Instructor | Theo dõi tiến độ và hỗ trợ nhiều learner | Thời gian hạn chế, nhiều learner cùng cần hỗ trợ và thiếu context trước khi trả lời |

### Actor ưu tiên điều tra

**Learner**, đồng thời thu thập evidence bổ sung từ **Lab Coach/Instructor**.

### Lý do

Outcome cuối cùng chỉ có ý nghĩa nếu learner thực sự tồn tại những tình huống bị mắc kẹt hoặc hiểu sai mà các cơ chế hỗ trợ hiện tại chưa xử lý được tốt.

---

# 2.5. Situation & Job

### Situation

Khi learner gặp một phần nội dung chưa hiểu hoặc không biết cách tiếp tục trong quá trình học/làm bài.

### Job

Learner cần xác định điểm mình đang vướng và tìm đủ thông tin hoặc hỗ trợ để tiếp tục bài học.

### JTBD Hypothesis

> Khi gặp một phần nội dung mình chưa hiểu trong quá trình học, tôi muốn nhanh chóng xác định vấn đề và tìm được sự hỗ trợ phù hợp để có thể tiếp tục học mà không bị mắc kẹt hoặc hiểu sai phần nền tảng.

---

# 2.6. Competing Pain Hypotheses

## Pain Hypothesis A

> Khi gặp nội dung khó, một số learner gặp khó khăn trong việc nhận được hỗ trợ kịp thời vì họ không biết mình cần hỏi gì, không chủ động yêu cầu giúp đỡ hoặc không thể hiện rõ rằng mình đang gặp vấn đề, dẫn đến việc tiếp tục học khi chưa hiểu hoặc mất nhiều thời gian tự xử lý.

## Pain Hypothesis B

> Learner có thể tự nhận ra phần chưa hiểu và đã có các workaround như tài liệu, AI, checkpoint và Lab Coach; pain chính không phải thiếu người phát hiện learner cần hỗ trợ mà là chất lượng, context và thời gian của quá trình hỗ trợ hiện tại.

### Hypothesis ưu tiên điều tra

Nhóm tiếp tục kiểm tra **Pain Hypothesis A**, nhưng sau lượt practice cần giữ **Pain Hypothesis B** như một competing explanation mạnh.

---

# 2.7. Evidence Map

| Cần kiểm tra | Evidence làm nhóm tin hơn | Evidence khiến nhóm nghi ngờ |
|---|---|---|
| Situation có thật | Learner kể được một sự kiện gần đây bị vướng | Không nhớ được tình huống cụ thể |
| Learner khó tự nhận diện vấn đề | Không biết mình sai/không biết hỏi gì | Có workflow tự kiểm tra rõ ràng |
| Workaround chưa đủ | Đã dùng tài liệu/AI/người hỗ trợ nhưng vẫn mắc | Workaround giải quyết nhanh và ổn định |
| Consequence có ý nghĩa | Mất nhiều thời gian, bỏ bài, học tiếp khi chưa hiểu | Chỉ mất vài phút, không ảnh hưởng kết quả |
| Instructor khó phát hiện | Learner im lặng thường xuyên bị bỏ sót | Instructor dễ phát hiện qua tương tác hiện tại |
| Pain có lặp lại | Nhiều sự kiện tương tự gần nhau | Chỉ xảy ra hiếm |
| Intervention có giá trị | Hỗ trợ sớm giúp learner tháo gỡ đáng kể | Learner không muốn hoặc không cần can thiệp |

---

# 2.8. Practice Evidence hiện tại

## Learner-side

Learner được phỏng vấn xác nhận:

- thường có những nội dung chưa hiểu;
- có lúc không biết nên bắt đầu từ đâu hoặc quy trình nên thực hiện như thế nào;
- sử dụng tài liệu, AI, checkpoint và Lab Coach như workaround;
- nếu AI/tool đã cung cấp đủ thông tin thì không cần hỏi người khác;
- nếu cần Lab Coach thì chủ động hỏi trực tiếp;
- đa số vấn đề cuối cùng được giải quyết;
- tool có thể giải quyết trong khoảng vài phút, trường hợp cần người hỗ trợ có thể lâu hơn.

### Ý nghĩa

Evidence này xác nhận **situation tồn tại**, nhưng làm yếu giả định rằng learner được phỏng vấn cần một hệ thống chủ động phát hiện để nhận hỗ trợ.

---

## Lab Coach / support-side

Practice interview cho thấy một pain khác đáng chú ý:

- có learner không biết mình nên hỏi gì nên không hỏi;
- learner có thể ngồi im dù đang gặp khó khăn;
- người hỗ trợ hiện dựa nhiều vào biểu hiện bên ngoài và kinh nghiệm cá nhân để nhận ra learner cần hỗ trợ;
- lớp đông khiến việc quan sát toàn bộ learner khó hơn;
- một số learner cũng không muốn người hỗ trợ can thiệp.

### Ý nghĩa

Đây là evidence ban đầu ủng hộ việc tiếp tục kiểm tra nhóm learner **không chủ động yêu cầu hỗ trợ**, thay vì giả định mọi learner gặp khó khăn đều giống participant learner đã phỏng vấn.

---

## Instructor-side

Instructor interview cho thấy:

- trong một buổi có thể có khoảng 5–7 learner hỏi trực tiếp;
- khi đông, learner phải chờ nhau;
- một số learner lên hỏi nhưng chưa chuẩn bị đủ context nên trình bày dài và mất thời gian;
- câu hỏi qua chat thường có context tốt hơn vì learner phải chuẩn bị nội dung trước;
- instructor không cho rằng workload hiện tại đang ở mức quá tải;
- instructor thường yêu cầu learner tự tìm hiểu/brainstorm trước rồi quay lại với nhiều dữ kiện hơn;
- xử lý hiện tại chủ yếu theo từng case thay vì ranking cứng.

### Ý nghĩa

Evidence này làm yếu giả định đơn giản rằng pain chính của instructor là “quá nhiều yêu cầu cần được ranking”.

Một pain khác có vẻ đáng điều tra hơn là:

> **thiếu context và chất lượng câu hỏi trước khi learner tiếp cận người hỗ trợ.**

---

# 2.9. Problem Hypothesis sau Practice

Sau lượt practice, nhóm điều chỉnh hypothesis thành:

> Khi learner gặp điểm chưa hiểu trong quá trình học, phần lớn có thể tự xử lý thông qua tài liệu, AI hoặc chủ động hỏi người hỗ trợ. Tuy nhiên, có thể tồn tại một nhóm learner không xác định rõ vấn đề, không biết nên hỏi gì hoặc không chủ động yêu cầu hỗ trợ. Trong môi trường lớp đông, Lab Coach/Instructor khó nhận ra đầy đủ những learner này chỉ từ quan sát trực tiếp, khiến một số điểm vướng có nguy cơ không được xử lý kịp thời.

Đây vẫn là **hypothesis cần fieldwork kiểm chứng**, chưa phải kết luận.

---

# 2.10. Điều phải đúng để hypothesis đứng vững

Ít nhất một số điều sau phải xảy ra đủ thường xuyên:

1. Learner thực sự gặp vấn đề nhưng không yêu cầu hỗ trợ.
2. Learner không biết cách diễn đạt vấn đề mình đang gặp.
3. Người hỗ trợ thường không phát hiện được learner đó đủ sớm.
4. Việc không được hỗ trợ dẫn đến consequence đáng kể.
5. Các workaround hiện tại không giải quyết pain đủ tốt.

---

# 2.11. Điều có thể khiến nhóm sửa hoặc bác bỏ hypothesis

Nhóm sẽ phải xem lại hypothesis nếu fieldwork cho thấy:

- phần lớn learner tự nhận ra vấn đề rất nhanh;
- tài liệu/AI/Lab Coach hiện tại giải quyết phần lớn điểm vướng với chi phí thấp;
- learner im lặng không đồng nghĩa learner cần hỗ trợ;
- learner không muốn bị can thiệp chủ động;
- instructor/Lab Coach đã nhận diện learner cần hỗ trợ đủ tốt;
- consequence của việc hỗ trợ muộn không đáng kể.

---

# 2.12. Solution Parking Lot

| Hướng giải quyết có thể có | AI / Không AI |
|---|---|
| Learner chủ động đánh dấu “Tôi đang bị vướng” | Không AI |
| Check-in nhanh sau từng phần học | Không AI |
| Form chuẩn hóa context trước khi learner hỏi | Không AI |
| Peer support / buddy system | Không AI |
| AI tutor giúp learner tự làm rõ câu hỏi trước khi escalate | AI |
| Phân tích tín hiệu để gợi ý learner có thể cần kiểm tra | AI |
| Dashboard tổng hợp các nội dung nhiều learner cùng gặp khó | AI / Analytics |

Nhóm chưa chọn solution ở giai đoạn này.

---

# 3. Conversation Guide — Final

## 3.1. Recruitment Criteria

### Learner

Cần nói chuyện với learner đã gặp ít nhất một phần nội dung chưa hiểu hoặc không biết cách tiếp tục trong **7 ngày gần đây**.

### Instructor / Lab Coach

Cần nói chuyện với người đã trực tiếp hỗ trợ learner trong thời gian gần đây và có trải nghiệm nhận biết/xử lý learner gặp điểm vướng.

---

# 3.2. Recruitment Check

### Learner

> Trong 7 ngày gần đây bạn có lần nào gặp một phần nội dung trong buổi học hoặc bài tập mà bạn không hiểu hoặc không biết làm tiếp không?

### Instructor / Lab Coach

> Trong thời gian gần đây bạn có trực tiếp hỗ trợ một learner đang gặp khó khăn trong quá trình học không?

Recruitment check chỉ dùng để xác nhận participant phù hợp, không dùng làm evidence chính.

---

# 3.3. Opening

> Bọn mình đang tìm hiểu cách mọi người xử lý những điểm chưa hiểu hoặc khó khăn xảy ra trong quá trình học. Không có câu trả lời đúng hay sai; mình quan tâm đến những gì thực sự đã xảy ra trong một tình huống gần đây. Mình xin phép ghi âm cuộc trao đổi để xem lại phục vụ bài học. Bản ghi không được chia sẻ công khai.

---

# 3.4. Story Opener — Learner

> Kể mình nghe về lần gần nhất bạn gặp một phần nội dung trong buổi học hoặc bài tập mà bạn không hiểu hoặc không biết làm tiếp như thế nào?

---

# 3.5. Big 3

| Điều cần học | Evidence cần tìm |
|---|---|
| Learner thực sự gặp pain gì khi bị vướng? | Một sự kiện gần đây + mức độ khó |
| Learner thực sự làm gì để xử lý? | Behavior + workaround |
| Khi nào workaround không đủ và consequence là gì? | Escalation + time/cost/outcome |

---

# 3.6. Main Questions — Learner

1. Kể mình nghe về lần gần nhất bạn gặp một phần nội dung mà bạn không hiểu hoặc không biết làm tiếp.
2. Lúc đó điều gì khiến bạn nhận ra mình đang bị vướng?
3. Ngay sau đó bạn đã làm gì đầu tiên?
4. Bạn đã thử những cách nào để giải quyết?
5. Trong lần đó, khi nào bạn quyết định tìm người khác hỗ trợ?
6. Bạn đã hỏi người đó như thế nào?
7. Điều gì xảy ra sau khi bạn nhận được hỗ trợ?
8. Bạn mất khoảng bao lâu từ lúc gặp vấn đề đến khi có thể tiếp tục?
9. Lần gần nhất trước đó xảy ra tình huống tương tự là khi nào?
10. Có lần gần đây nào bạn gặp điểm chưa hiểu nhưng vẫn tiếp tục mà không giải quyết không? Chuyện gì xảy ra sau đó?

---

# 3.7. Main Questions — Instructor / Lab Coach

1. Kể mình nghe về lần gần nhất bạn nhận ra một learner đang gặp khó khăn.
2. Điều gì khiến bạn nhận ra learner đó đang gặp vấn đề?
3. Learner đó có chủ động yêu cầu hỗ trợ không?
4. Trong trường hợp đó bạn đã làm gì?
5. Bạn cần biết những thông tin gì trước khi có thể hỗ trợ?
6. Có trường hợp gần đây nào learner không biết nên hỏi gì không?
7. Bạn xử lý trường hợp đó như thế nào?
8. Lần gần nhất có nhiều learner cùng cần hỗ trợ thì chuyện gì xảy ra?
9. Có learner nào bạn chỉ phát hiện đang gặp khó khăn sau một khoảng thời gian không?
10. Có lần nào bạn tưởng learner cần hỗ trợ nhưng thực tế họ vẫn ổn không?

---

# 3.8. Probe Bank

Khi participant kể một sự kiện đáng chú ý, ưu tiên đào sâu thay vì đọc tiếp danh sách câu hỏi:

- “Lúc đó chuyện gì xảy ra tiếp theo?”
- “Bạn đã làm gì?”
- “Vì sao lúc đó bạn chọn cách đó?”
- “Bạn nhớ mất khoảng bao lâu không?”
- “Sau đó thì sao?”
- “Bạn đã thử cách nào khác chưa?”
- “Điều gì khiến bạn quyết định hỏi / không hỏi?”
- “Kết quả cuối cùng là gì?”
- “Lần gần nhất trước đó là khi nào?”

---

# 4. Practice Reflection

> **Lưu ý:** Phần dưới là draft cần được cá nhân tự đối chiếu với recording trước khi nộp.

## 4.1. Câu hỏi nào giúp user kể một tình huống cụ thể?

Câu hiệu quả nhất là:

> “Bạn có thể kể cho mình nghe lần gần nhất bạn gặp một phần nội dung mà bạn không hiểu hoặc không biết làm như thế nào không?”

Khi neo vào “lần gần nhất”, participant bắt đầu kể về một bài/lab cụ thể và mô tả cách mình sử dụng tài liệu, AI và Lab Coach thay vì chỉ đưa ra nhận xét chung về việc học.

---

## 4.2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?

Trong practice, một số câu hỏi của mình vẫn:

- quá dài;
- chứa nhiều câu hỏi trong cùng một lượt;
- đưa ra trước các phương án trả lời;
- hỏi về “bình thường/thường thì” thay vì giữ participant ở một sự kiện cụ thể;
- đôi lúc diễn giải thay participant.

Ví dụ kiểu hỏi:

> “Có lần nào bạn gặp thắc mắc nhưng bạn không hỏi không? Hoặc bạn tự giải quyết được không?”

đưa ra sẵn hai hướng trả lời.

Ở fieldwork, mình cần hỏi ngắn hơn:

> “Trong lần đó, sau khi gặp điểm vướng, bạn làm gì tiếp?”

Sau đó follow dựa trên câu trả lời thật của participant.

---

## 4.3. Sau practice, nhóm sửa Conversation Guide ở đâu và vì sao?

Nhóm thực hiện ba thay đổi:

**1. Neo mạnh hơn vào một sự kiện gần đây.**

Thay các câu hỏi như:

> “Bình thường bạn có hay...?”

bằng:

> “Trong lần gần nhất bạn vừa kể...?”

**2. Giảm câu hỏi giả định và câu hỏi đưa sẵn phương án.**

Thay:

> “Bạn hỏi giảng viên hay Lab Coach?”

bằng:

> “Sau đó bạn tìm sự hỗ trợ ở đâu?”

**3. Bổ sung counter-evidence.**

Conversation Guide cuối thêm câu:

> “Có lần gần đây nào bạn gặp điểm chưa hiểu nhưng vẫn tiếp tục mà không giải quyết không?”

và với instructor:

> “Có lần nào bạn tưởng learner cần hỗ trợ nhưng thực tế họ vẫn ổn không?”

Mục đích là tránh chỉ tìm evidence ủng hộ hypothesis.

---

# 5. AI Support Log

## Công cụ AI đã sử dụng

ChatGPT.

## AI đã hỗ trợ những gì?

AI được sử dụng **sau giai đoạn suy luận cá nhân/nhóm** để:

- rà soát cấu trúc Problem Hypothesis;
- phân biệt problem với solution;
- gợi ý cách viết JTBD và competing Pain Hypotheses;
- rà soát Conversation Guide theo nguyên tắc The Mom Test;
- phát hiện câu hỏi dẫn dắt, câu hỏi giả định và câu hỏi quá dài;
- hỗ trợ cấu trúc hóa notes từ transcript có sẵn.

## AI không được sử dụng cho việc gì?

AI không được sử dụng để:

- tạo participant giả;
- bịa interview evidence;
- bịa exact quote;
- thay đổi nội dung participant đã nói;
- tuyên bố hypothesis được validated.

## Điểm AI có thể sai hoặc hời hợt

AI có thể diễn giải mạnh hơn evidence thực tế hoặc biến một observation của một participant thành pattern chung.

Ví dụ, một learner có workflow tự giải quyết tốt không có nghĩa tất cả learner đều như vậy.

Do đó nhóm giữ các cách diễn đạt:

- “participant này...”
- “evidence ban đầu...”
- “có thể...”
- “cần fieldwork kiểm chứng...”

thay vì kết luận rằng problem đã được xác nhận.

## Cách tự sửa

Nhóm đối chiếu các nhận định với recording/transcript, giữ facts và interpretation ở các phần riêng, đồng thời giữ lại evidence làm hypothesis yếu đi thay vì loại bỏ chúng.