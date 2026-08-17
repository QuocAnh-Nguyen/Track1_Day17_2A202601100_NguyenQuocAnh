# Track1_Day17_2A202601100_NguyenQuocAnh

## 1. Thông tin cá nhân và nhóm
|  STT | Teammate        | Student ID  |
| ---: | --------------- | ----------- |
|    1 | Nguyễn Quốc Anh | 2A202601100 |
|    2 | Trương Ái Linh  | 2A202601496 |

## 2. Problem Hypothesis Brief
### **Case B — AI Notes: Personal Learning Notes**

---

#### **1\. Solution — Gỡ solution khỏi hình thức cụ thể**

**Solution directive:** Trong khi học, học viên có thể highlight một đoạn nội dung, đánh dấu "Chưa hiểu", hoặc viết một câu hỏi/ghi chú ngắn. Khi bài học kết thúc, AI Notes kết hợp những dấu vết này với nội dung bài để tạo ra một bản ghi chú cá nhân có cấu trúc, phản ánh đúng lỗ hổng tư duy và cách hiểu riêng của từng học viên. Học viên chỉnh sửa và xác nhận trước khi lưu.

| Thành phần   | Solution đã mô tả                                                      |
| ------------ | ---------------------------------------------------------------------- |
| Trigger      | Học viên hoàn thành bài học                                            |
| Input        | Nội dung bài, highlights, điểm "Chưa hiểu", câu hỏi và ghi chú cá nhân |
| AI action    | Chọn lọc, nhóm và tổ chức thông tin                                    |
| Output       | Bản ghi chú cá nhân có cấu trúc                                        |
| User control | Học viên chỉnh sửa và xác nhận trước khi lưu                           |

**Capability trung tính (gộp 2 bản):** Nhận diện được học viên đang hiểu / chưa hiểu ở đâu qua chính cách họ diễn đạt (highlight, đánh dấu, câu hỏi), rồi tổng hợp những khúc mắc đó với nội dung bài để tạo ra một bản ghi chú được cá nhân hóa cho từng học viên, dựa trên đúng lỗi sai trong tư duy và lỗ hổng hiểu biết riêng của họ.

**Người phù hợp để phỏng vấn:** Trong 7 ngày gần đây đã ghi chú, highlight hoặc lưu lại nội dung bài học để xem lại sau.

---

#### **2\. Change — Làm lộ chuỗi thay đổi được kỳ vọng**

* **User sẽ biết/làm được điều gì khác?** Từ chỗ phải tự take note tay/digital rồi hỏi trực tiếp hoặc DM lab coach, giảng viên, GPT, Gemini → có sẵn ngay một bản ghi chú cá nhân hóa sau mỗi bài học, **không cần thao tác nhiều và không cần chuyển sang nền tảng khác** để take note.  
* **Hành vi nào phải thay đổi để outcome xảy ra?** Học viên phải take note / đánh dấu khúc mắc thường xuyên trong lúc học — đây là input bắt buộc để model có đủ context suy luận.  
* **Trạng thái/kết quả nào được kỳ vọng thay đổi?** Học bị động → Học chủ động.  
* **Chuỗi nhân quả kỳ vọng:** có sẵn bản ghi chú mà không tốn công sức tổng hợp → học viên học tốt hơn, tiết kiệm thời gian ghi chép → có sẵn tài liệu để ôn tập → chất lượng học tập của học viên tốt hơn.  
* **Đâu là output team tạo ra, đâu là outcome team chỉ có thể ảnh hưởng?** Output: bản ghi chú cá nhân hóa. Outcome (không kiểm soát trực tiếp): phương pháp học và mức độ hiểu bài của học viên, và xa hơn là chất lượng học tập nói chung.  
* **Nếu user không thay đổi hành vi, solution còn tạo được outcome không?** Không — nếu học viên không highlight/đánh dấu/ghi chú trong lúc học, AI Notes không có input để hoạt động.

---

#### **3\. Actor — Xác định các nhóm người có liên quan**

* Ai trực tiếp sử dụng solution?: Học viên, lab coach, giảng viên  
* Ai trực tiếp trải nghiệm pain?: Học viên, lab coach  
* Ai phải thay đổi hành vi để outcome xảy ra?: Học viên, lab coach  
* Ai chịu hậu quả nếu problem không được giải quyết?: Học viên, lab coach  
* Ai hưởng lợi gián tiếp?: Giảng viên, **đội ngũ phát triển Vlearn**  
* Người nhận feature có chắc là người sở hữu pain chính không?: Chắc chắn

| Actor                     | Họ đang làm gì?                                                      | Pain hoặc hậu quả có thể có                                                                                                     | Họ hưởng lợi thế nào?                                                                                              |
| ------------------------- | -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------ |
| Học viên (trong giờ học)  | Vừa đọc slide vừa nghe giảng trên giảng đường                        | Nội dung slide khó hiểu, dày chữ; giảng viên giảng nhanh; không liên kết được các nội dung trong bài giảng                      | Học một cách chủ động; hiểu được lỗ hổng trong tư duy của mình; có được ghi chú cá nhân hóa                        |
| Học viên (ngoài giờ học)  | Ghi chú ra Notion, vở, hoặc chuẩn bị nội dung trước buổi học kế tiếp | Ghi chú tay/Notion tốn thời gian; nhiều nội dung không hiểu, cần tổng hợp lại các lỗ hổng để được giải thích trước buổi học sau | Nếu vẫn không hiểu thì có thể hỏi trực tiếp lab coach/giảng viên hôm sau, với câu hỏi đã được chắt lọc sẵn         |
| Lab Coach                 | Chuẩn bị nội dung, nghiên cứu những khúc mắc thường có của học viên  | Không có nhiều chuyên môn như giảng viên; áp lực giống học viên khi phải trả lời nhiều câu hỏi                                  | Tự tin hơn trước những khúc mắc của học viên vào buổi học                                                          |
| Giảng viên                | Giảng bài trên lớp, nhận quá nhiều khúc mắc từ học viên              | Không có đủ thời gian để giải quyết vấn đề cho từng học viên; không biết học viên đang không hiểu ở đâu                         | Giảm số lượng câu hỏi trong buổi học, chỉ tập trung vào câu hỏi khó/nhiều người hỏi; chất lượng bài giảng tăng lên |
| Đội ngũ phát triển Vlearn | Phát triển và cải tiến sản phẩm Vlearn                               | Không biết nên thêm tính năng gì để học viên học tốt hơn, tính năng thêm vào có đáng thêm hay không                             | Có tín hiệu và dữ liệu rõ ràng hơn để cải thiện Vlearn                                                             |

**Actor nhóm chọn để điều tra trước:** Học viên **Vì sao:** Học viên vừa là actor trực tiếp trải nghiệm pain và phải thay đổi hành vi nhiều nhất, vừa là đối tượng bị ảnh hưởng trực tiếp và lớn nhất khi tính năng ra mắt — output của solution (bản ghi chú) nhắm thẳng vào họ.

---

#### **4\. Situation & Job — User đang cố làm gì trong tình huống nào?**

* **Tình huống bắt đầu khi chuyện gì xảy ra? Lúc đó user đang cố hoàn thành việc gì?** Khi đang học trên lớp có khúc mắc nhưng chưa được lab coach/giảng viên giải đáp; khi chuẩn bị bài trước buổi học kế tiếp với nội dung khó hiểu; hoặc khi ôn tập lại kiến thức sau buổi học.  
* **Vì sao việc đó quan trọng với họ?** Ảnh hưởng trực tiếp tới quá trình học tập, tích lũy, áp dụng kiến thức của học viên.  
* **Hiện tại họ đang thực hiện việc đó như thế nào?** Ghi chú tay hoặc trên Notion/vở, hỏi trực tiếp giảng viên/lab coach, hoặc gửi slide và hỏi AI như GPT, Gemini.  
* **Họ bắt đầu gặp vướng mắc ở điểm nào?** Số lượng khúc mắc vượt quá khả năng trả lời của giảng viên/lab coach; việc note tay/Notion tốn thời gian và có thể khiến lỡ nội dung đang giảng; các AI phổ thông như GPT, Gemini không có đủ context để đưa ra ghi chú cá nhân hóa.

**JTBD Hypothesis (gộp, viết theo đúng góc nhìn của user):** *Khi đang học và gặp phải khúc mắc, hoặc khi cần ôn tập lại kiến thức đã học, tôi muốn có một cách ghi chú nhanh, ít tốn công sức, để cuối cùng có được một tài liệu ôn tập được cá nhân hóa đúng theo lỗ hổng hiểu biết của riêng mình — thay vì phải tự chắp vá thông tin và học vẹt.*

*(Ghi chú: bản Case 2 vốn đã viết JTBD đúng cấu trúc first-person hơn — mình giữ cấu trúc đó, nhưng bổ sung nội dung "cá nhân hóa theo lỗ hổng tư duy" từ bản Case B để không mất phần quan trọng nhất của solution.)*

---

#### **5\. Pain — Viết các cách giải thích cạnh tranh**

> Hai bản đặt tên Hypothesis A/B khác nhau nhưng nội dung **không trùng nhau hoàn toàn**. Gộp lại, nhóm thực ra có 3 góc nhìn về pain, không phải 2:

**Pain 1 — Thiếu ngữ cảnh cá nhân hóa khi tự giải quyết khúc mắc** *(Case B – Hypothesis A)* Khi ôn tập lại bài học hoặc cố gắng làm rõ một nội dung khó, học viên gặp khó khăn trong việc hệ thống hóa kiến thức và lấp đầy lỗ hổng vì các công cụ AI (như ChatGPT/Gemini) trả lời quá chung chung, không nắm được mạch tư duy/lỗi sai trước đó của họ, còn giảng viên/lab coach thì không có đủ thời gian phản hồi ngay lập tức, dẫn đến học viên mất rất nhiều thời gian chắp vá thông tin, vẫn không hiểu tận gốc vấn đề và dễ quay lại trạng thái học vẹt, học thụ động.

**Pain 2 — Quá tải thông tin, đứt gãy tập trung khi đang nghe giảng** *(Case B – Hypothesis B, trùng ý với Case 2 – Hypothesis A)* Khi đang nghe giảng trên lớp hoặc đọc tài liệu dài, học viên gặp khó khăn trong việc ghi chú lại những điểm mình chưa hiểu vì tốc độ bài giảng quá nhanh và thông tin quá dày đặc — nếu dừng lại để viết chi tiết khúc mắc thì sẽ bị lỡ mất nội dung tiếp theo — dẫn đến khi kết thúc bài học, học viên quên mất mình đã không hiểu ở đâu, các lỗ hổng kiến thức bị bỏ trôi và tích tụ dần qua từng buổi học.

**Pain 3 — Không biết mình đã hiểu bài hay chưa** *(Case 2 – Hypothesis B)* Khi muốn hiểu bài học, học viên gặp khó khăn vì chưa xác định được rõ ràng mình đã thực sự hiểu nội dung hay chưa.

**Giả thuyết nhóm chọn để điều tra trước:** Pain 1

**Lý do (gộp cả hai bản):** Pain 1 cộng hưởng trực tiếp với outcome kỳ vọng ở mục 2 (chuyển từ học bị động sang chủ động, hiểu được lỗ hổng tư duy), và đúng với cơ chế mà AI Notes giải quyết — điểm khác biệt giữa AI Notes với GPT/Gemini nằm ở chỗ có context cá nhân hóa mà công cụ phổ thông không có.

Pain 2 tuy không phải pain chính mà solution nhắm tới, nhưng lại là **điều kiện tiên quyết** quan trọng: nếu học viên không kịp ghi chú/đánh dấu khúc mắc ngay trong lúc học vì bị cuốn theo tốc độ giảng, thì AI Notes sẽ không có input để hoạt động. Nên hỏi như một câu hỏi phụ/rủi ro trong buổi phỏng vấn, không phải câu hỏi chính.

Pain 3 có thể dùng như tín hiệu bổ trợ cho Pain 1 — cảm giác "không biết mình hiểu đến đâu" chính là một biểu hiện cụ thể của việc thiếu ngữ cảnh cá nhân hóa.

---

#### **6\. Evidence — Xác định điều cần tìm trước khi viết câu hỏi**

| Cần kiểm tra        | Evidence làm nhóm tin hơn (Tín hiệu xanh)                                                                                                                     | Evidence làm nhóm nghi ngờ hoặc bác bỏ (Tín hiệu đỏ)                                       |
| ------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| Situation có thật   | Học viên kể chi tiết được một lần gần đây (trong 7 ngày) họ ngồi ôn lại bài và bị "kẹt" ở một khái niệm/slide cụ thể                                          | Trả lời chung chung: "lúc nào rảnh em mới xem lại", hoặc chỉ ôn thi vào đêm trước ngày thi |
| Pain có ý nghĩa     | Miêu tả cảm giác ức chế, bối rối; ước tính đã lãng phí 1–2 tiếng chỉ để cố hiểu một khái niệm nhỏ                                                             | Nhún vai: "không hiểu phần đó thì em bỏ qua, cũng không ảnh hưởng điểm số mấy"             |
| Workaround tồn tại  | Đưa ra được bằng chứng: lịch sử chat với GPT (phải hỏi đi hỏi lại nhiều lần), tin nhắn DM dài dòng cho lab coach, hoặc ghi chú chi chít trên Notion/sổ tay/vở | Không take note, không dùng AI, cũng không nhắn tin hỏi ai khi không hiểu bài              |
| Consequence tồn tại | Điểm kém ở bài quiz, không làm được bài tập thực hành, thừa nhận chỉ đang "học vẹt" để qua môn                                                                | Vẫn đạt điểm cao, vẫn hiểu bài và làm được bài tập bình thường mà không cần ôn tập kỹ      |
| Pattern có lặp      | Xảy ra ở nhiều môn học, lặp lại hàng tuần                                                                                                                     | Chỉ xảy ra đúng một lần ở một bài giảng có chất lượng slide quá tệ                         |

---

#### **Chốt Problem Hypothesis mang sang Chặng 2**

> "Học viên hiện nay mất rất nhiều thời gian và công sức để tự giải quyết các khúc mắc sau buổi học. Dù đã sử dụng các công cụ AI phổ thông hoặc hỏi giảng viên, họ vẫn không nhận được sự giải thích sát với mạch tư duy và lỗ hổng kiến thức của riêng mình, khiến họ dễ nản chí và quay về cách học thụ động."

**Điều gì phải đúng để giả thuyết đứng vững:**

* Học viên thực sự có ý thức muốn giải quyết khúc mắc, thay vì mặc kệ nó.  
* Học viên đã và đang ghi chú (highlight, gạch chân, viết tay, gõ phím) những chỗ không hiểu trong quá trình học.  
* Các công cụ như ChatGPT/Gemini hiện tại chưa làm họ thỏa mãn (vì thiếu context).

**Điều gì có thể khiến nhóm sửa hoặc bác bỏ giả thuyết:**

* Học viên thấy ChatGPT hiện tại đã quá đủ tốt, không cần thêm tool nào khác.  
* Học viên hoàn toàn không có thói quen đánh dấu/ghi chú trong lúc học (nếu đúng, sẽ không có input để AI Notes hoạt động).

---

#### **Solution Parking Lot (Brainstorm các hướng giải quyết — tạm gác lại, không mang vào phòng phỏng vấn)**

| Hướng giải quyết có thể có                                                                                                                                                                      | AI / Không sử dụng AI                         |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------- |
| 1\. AI Personalized Notes (solution ban đầu): tổng hợp highlight, câu hỏi của user thành bản ghi chú cá nhân hóa dựa trên lỗ hổng tư duy của họ                                                 | Có sử dụng AI                                 |
| 2\. AI Socratic Tutor: AI không đưa sẵn bản ghi chú, mà dựa vào khúc mắc để đặt ngược câu hỏi gợi mở, ép học viên tự tư duy ra câu trả lời                                                      | Có sử dụng AI                                 |
| 3\. Trợ lý "gom nhóm câu hỏi" cho Lab Coach: AI đọc toàn bộ khúc mắc của lớp, tự động nhóm các lỗi sai tư duy giống nhau, báo cáo cho Lab Coach để tổ chức 1 buổi Q\&A 15 phút giải quyết chung | Có sử dụng AI                                 |
| 4\. Structured "Muddiest Point" Template: UI/form có cấu trúc cứng ("Tôi đang hiểu là...", "Tôi bị kẹt ở...", "Tôi đoán lý do là...") ép học viên điền thay vì note tự do                       | Không sử dụng AI (chỉ UI/UX)                  |
| 5\. Peer-to-Peer Micro Tutoring: tự động ghép một học viên đánh dấu "Chưa hiểu" ở section A với một học viên đạt điểm tối đa/"Đã hiểu rất rõ" ở section A để DM giải thích cho nhau             | Không sử dụng AI (thuật toán matching cơ bản) |

## 3. Conversation Guide phiên bản cuối


> ⚠️ **Rút kinh nghiệm Round 1:** lúc luyện tập đã lỡ nói "giúp mình cải thiện sản phẩm cho lab của mình" ngay phần mở đầu. Đọc đúng nguyên văn câu trên, không ứng biến thêm — kể cả khi thấy không khí đang thân mật, dễ buột miệng.

### Story opener
"Kể mình nghe về lần gần nhất bạn đang học hoặc ôn bài mà bị 'kẹt' ở một chỗ không hiểu rõ — lúc đó chuyện gì đã xảy ra?"

> ⚠️ **Checkpoint bắt buộc:** không chuyển sang Big 3 Questions nếu chưa có ít nhất một câu chuyện cụ thể (thời điểm, môn học, hành động) từ câu hỏi này. Round 1 đã hỏi thẳng recruitment check rồi nhảy luôn vào Big 3, bỏ qua bước neo câu chuyện.

### Big 3 Questions — v2 (đã sửa sau Round 1)

| #   | Câu hỏi sẽ dùng                                                                                                                                       | Lỗi Round 1 cần tránh                                                                                                    |
| --- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------ |
| 1   | "Lúc đó bạn đã làm gì đầu tiên?" — hỏi xong, **im lặng chờ**, không tự thêm "hay là...". Nếu cần, probe: "Bạn có ghi/đánh dấu lại nó không?"          | Đã thêm "...hay là bạn lên ChatGPT để hỏi?" ngay trong câu hỏi → biến thành câu hỏi mớm 2 lựa chọn                       |
| 2   | "Trong lúc ghi chú đó, có phần nào khiến bạn thấy khó hay mất công không?" → nếu im lặng, probe: "Phần nào khó nhất?"                                 | Đã hỏi "...mất quá nhiều thời gian khiến bạn không tập trung...?" → mớm sẵn giả thuyết pain vào ngay trong câu hỏi       |
| 3   | "Sau khi ghi chú xong, bạn làm gì tiếp theo với nó?" → probe: "Rồi sao nữa?", "Kết quả có giúp bạn hiểu trọn vẹn không, hay vẫn phải tự mày mò thêm?" | Đã hỏi "...note nó rời rạc như thế... dump lên GPT hay tự review?" → vừa mớm giả định ("rời rạc") vừa cho sẵn 2 lựa chọn |

> 📌 **Quy tắc cứng:** câu trả lời chung chung → Anchor ngay ("Lần gần nhất là khi nào?"). User hé lộ một workaround/công cụ đang dùng → Dig ngay trước khi chuyển câu hỏi khác (Round 1 đã bỏ lỡ đoạn "đưa note cho AI giải thích" — lẽ ra phải đào sâu ngay tại đó).

### Ba phản xạ khi data bắt đầu lệch

> Dùng ngay trong câu tiếp theo — không được "À ok ok" rồi đổi hẳn sang chủ đề khác (lỗi đã mắc ở Round 1, hai lần liền).
---

## Phần D — Nhật ký luyện tập (Practice Log) — Round 1

**Thời lượng:** ~2 phút · Speaker 0 phỏng vấn, Speaker 1 trả lời.

### Bảng lỗi cụ thể phát hiện từ bản ghi

| Thời điểm   | Trích dẫn (diễn giải)                                                        | Lỗi cụ thể                                                                                                              | Nguyên tắc bị vi phạm                                                    | Cách sửa                                                                                                |
| ----------- | ---------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------- |
| 00:00–00:16 | "...giúp mình cải thiện sản phẩm cho lab của mình"                           | Lời mở đầu để lộ mục đích "cải thiện sản phẩm", khiến interviewee dễ chuyển sang vai người góp ý thay vì kể chuyện thật | Vi phạm quy tắc "không xin feedback tính năng" của Lời mở đầu            | Đọc đúng nguyên văn Lời mở đầu đã soạn, không ứng biến                                                  |
| 00:16–00:27 | Hỏi đúng recruitment check, nhưng sau đó không hỏi tiếp Story opener         | Nhảy thẳng vào Big 3 khi chưa có 1 câu chuyện cụ thể (thời điểm, môn học) để neo xuyên suốt                             | Bỏ qua bước bắt buộc trong Conversation Guide                            | Thêm checkpoint: không sang Big 3 nếu chưa có story cụ thể                                              |
| 00:35–00:51 | "Bạn có đánh dấu, ghi chú lại hay là bạn lên ChatGPT để hỏi...?"             | Câu hỏi đóng, mớm sẵn 2 lựa chọn (leading/compound)                                                                     | Vi phạm nguyên tắc hỏi mở, không mớm đáp án                              | Sửa thành câu hỏi mở, bỏ hẳn phần "hay là..."                                                           |
| 00:51–01:00 | User trả lời chung chung "Chắc ban đầu... tùy hoàn cảnh..."                  | Không dùng phản xạ Anchor dù câu trả lời chưa neo vào 1 tình huống cụ thể                                               | Bỏ lỡ tín hiệu cần Anchor (Ba phản xạ)                                   | Hỏi ngay "Lần gần nhất chuyện đó xảy ra là khi nào?"                                                    |
| 01:02–01:13 | "...ghi chú mất quá nhiều thời gian khiến bạn không tập trung...?"           | Câu hỏi mớm sẵn giả thuyết pain thay vì hỏi hành vi mở                                                                  | Vi phạm nguyên tắc hỏi hành vi, không hỏi xác nhận giả thuyết            | Đổi thành câu hỏi mở về khó khăn khi ghi chú                                                            |
| 01:24–01:41 | "...note nó rời rạc như thế... dump hết lên GPT hay tự review...?"           | Mớm giả định ("rời rạc") + cho sẵn 2 lựa chọn                                                                           | Vi phạm nguyên tắc hỏi mở                                                | Đổi thành "Bạn làm gì tiếp theo với nó?"                                                                |
| 01:41–01:53 | "...đưa cho AI để nó giải thích ra... mắc quá thì hỏi giảng viên, lab coach" | User hé lộ workaround gần giống chính solution, nhưng không được Dig sâu — phỏng vấn kết thúc ngay sau đó               | Bỏ lỡ tín hiệu cần Dig; Big 3 #3 (hậu quả cụ thể) chưa thu được evidence | Dig ngay: hỏi AI trả lời có sát vấn đề không, có phải hỏi lại nhiều lần không, kết quả cuối cùng ra sao |
| Toàn bài    | ~2 phút, 0 probe từ probe bank được dùng                                     | Phỏng vấn quá ngắn, thiếu độ sâu                                                                                        | Thiếu áp dụng probe bank                                                 | Đặt mục tiêu tối thiểu ≥1 probe cho mỗi Big 3 trước khi chuyển câu                                      |

### Thay đổi đã áp dụng vào Conversation Guide (xem Phần B)
- Thêm cảnh báo dưới Lời mở đầu, nhắc đọc đúng nguyên văn.
- Thêm checkpoint bắt buộc: phải có Story opener trước khi vào Big 3.
- Viết lại cả 3 câu Big 3 Questions thành bản v2 — ngắn hơn, mở hơn, bỏ hết lựa chọn mớm sẵn, kèm cột "Lỗi Round 1 cần tránh" để nhắc trực tiếp khi đọc lại.
- Thêm quy tắc cứng: bắt buộc Anchor/Dig ngay trong câu kế tiếp, không được đổi chủ đề trước khi dùng phản xạ.

### Practice Reflection

**1. Câu hỏi nào đã giúp user kể một tình huống cụ thể?**
Chưa có câu nào lấy được một câu chuyện đầy đủ (thời điểm + môn học + hành động cụ thể), vì Story opener bị bỏ qua. Gần nhất là câu hỏi (dù leading) về việc ghi chú mất thời gian — user kể được chi tiết cơ chế thật: "slide PDF không copy được chữ, phải đánh tay" và "slide dài quá không biết take note kiểu gì". Đây là tín hiệu cụ thể, đáng giữ lại, nhưng cần xác nhận lại bằng một câu hỏi mở ở vòng phỏng vấn thật để chắc chắn không phải do bị mớm.

**2. Chỗ nào mình cần làm tốt hơn ở lần phỏng vấn thật?**
- Đọc đúng nguyên văn Lời mở đầu, không tự ý nói "cải thiện sản phẩm".
- Không bỏ qua Story opener — luôn lấy được 1 câu chuyện cụ thể trước khi vào Big 3.
- Bỏ thói quen thêm "hay là..." / đưa sẵn 2 lựa chọn ở cuối câu hỏi.
- Chủ động Anchor khi câu trả lời chung chung, Dig khi user hé lộ workaround, thay vì "À ok ok" rồi đổi chủ đề.
- Dành đủ thời gian khai thác Big 3 #3 (hậu quả cụ thể) trước khi kết thúc, thay vì kết thúc ngay sau một câu trả lời ngắn.

**3. Sau khi luyện, nhóm đã sửa Conversation Guide ở đâu và vì sao?**
Sửa ở Phần B — Lời mở đầu (thêm cảnh báo), Story opener (thêm checkpoint bắt buộc), và Big 3 Questions (viết lại thành bản v2, ngắn và mở hơn, kèm cột lỗi cần tránh ngay trong bảng). Lý do: cả ba lỗi lớn nhất của Round 1 đều là hỏi mớm/đóng và bỏ lỡ phản xạ Anchor/Dig — nên guide cần được thiết kế để giảm khả năng ứng biến sai ngay tại thời điểm hỏi, thay vì chỉ dựa vào trí nhớ của người phỏng vấn giữa lúc phỏng vấn thật.

## 5. AI Support Log

Claude: Tổng hợp, diễn đạt mà không mất ý hai bài làm của nhóm tôi
Claude: Dựa vào tài liệu trên và nội dung Case B. Hãy thiết kế sườn Interview Design hoàn chỉnh.