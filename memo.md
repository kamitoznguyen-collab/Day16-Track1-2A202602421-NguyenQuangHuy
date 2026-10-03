
# Memo Teardown — Notion (Notion AI)

**Họ tên:** Nguyễn Quang Huy
**Mã sinh viên:** 2A202602421

**Vì sao chọn sản phẩm này:** Notion là ví dụ điển hình nhất của việc chuyển từ một công cụ SaaS truyền thống (wiki/docs) sang một sản phẩm AI-native. Quá trình ra mắt Notion AI minh chứng rõ nét cho nguyên lý: AI Model có thể bị bắt kịp, nhưng "Moat" (hào cản) thực sự nằm ở việc AI được nhúng thẳng vào luồng làm việc (workflow) và dữ liệu (data) có sẵn của người dùng.

---

**§1. Timeline các cập nhật lớn**

| Thời điểm | Cập nhật | Context lúc đó | Nguyên lý |
|---|---|---|---|
| 11/2022 | [Ra mắt Notion AI (Waitlist)](https://www.notion.so/blog/introducing-notion-ai) | ChatGPT sắp ra mắt, ngành docs/productivity đang đua nhau thử nghiệm Generative AI. Khái niệm AI writing assistant còn mới. | **Wrapper mỏng để test thị trường:** Đưa mô hình ngôn ngữ vào dưới dạng tính năng (draft, summarize) để học hành vi người dùng, đánh đổi chiều sâu lấy tốc độ ra mắt. |
| 02/2023 | [Notion AI chính thức phát hành rộng rãi (General Availability)](https://www.notion.so/blog/notion-ai-is-here-for-everyone) | Hype về AI đang ở đỉnh điểm. Nhiều tool AI "wrapper" mọc lên như nấm nhưng người dùng lười copy/paste qua lại. | **Tích hợp vào Workflow (Moat):** Đưa AI vào đúng nơi người dùng đang thao tác văn bản. Giảm ma sát (friction) bằng không, biến AI thành công cụ chứ không phải điểm đến. |
| 11/2023 | [Ra mắt Q&A (Hỏi đáp nội bộ)](https://www.notion.so/blog/introducing-q-and-a) | RAG (Retrieval-Augmented Generation) bắt đầu phổ biến. Doanh nghiệp đau đầu vì thông tin nội bộ phân mảnh. | **Trải nghiệm x10:** Thay vì dùng thanh search truyền thống và phải đọc lướt hàng chục docs, AI đọc và tổng hợp câu trả lời ngay lập tức từ dữ liệu công ty. |
| 06/2024 | [Ra mắt Notion Sites (Tích hợp AI SEO/Content)](https://www.notion.so/blog/sites) | Nhu cầu public tài liệu, làm portfolio, trang tuyển dụng tăng cao nhưng setup web truyền thống quá rườm rà. | **Mở rộng Use Case:** Biến data đã có (doc) thành public asset (web) chỉ với 1 click, dùng AI tự tối ưu hóa SEO để tăng giá trị cho content. |
| 08/2024 | [Cập nhật Notion AI (Connect Google Drive, Slack...)](https://www.notion.so/blog/ai-can-now-search-slack-google-drive) | Notion nhận ra họ không thể chứa 100% data của doanh nghiệp. Mọi người vẫn dùng Slack để chat và Drive để lưu file. | **Định nghĩa "Tốt" = Gom Context:** AI chỉ giỏi khi có đủ context. Việc search chéo qua các tool khác giúp Notion AI trở thành "não bộ" trung tâm của doanh nghiệp. |
| 10/2024 | [Công bố Notion Mail & Forms](https://www.notion.so/blog/notion-mail-forms-custom-layouts) | Notion muốn thách thức Google Workspace/Microsoft 365, giữ chân user ở lại hệ sinh thái lâu hơn. | **Hệ sinh thái Vertical AI khép kín:** Cố gắng kiểm soát toàn bộ vòng đời thông tin (từ thu thập qua Forms, xử lý nội bộ qua Docs, đến giao tiếp qua Mail) để AI có dữ liệu tốt nhất. |

**Vì sao chọn những mốc này:** Đây đều là các quyết định lớn định hình chiến lược (từ thử nghiệm tính năng viết -> search bằng AI -> kết nối app ngoài -> mở rộng thành hệ sinh thái). Mình đã loại bỏ các mốc như "Cập nhật giao diện Darkmode" hay "Thêm template mới" vì chúng chỉ là vá lỗi hoặc tối ưu bề mặt, không làm thay đổi bản chất luồng dữ liệu của AI.

---

**§2. Tệp user & JTBD**

| | Early adopters (Giai đoạn đầu) | Tệp hiện tại (B2B/Enterprise) |
|---|---|---|
| **Đặc điểm** | Freelancer, sinh viên, startup founders quy mô nhỏ (tech-savvy). | Đội ngũ PM, HR, Operations tại các doanh nghiệp vừa & lớn. |
| **JTBD chính** | "Viết nháp nhanh hơn, tóm tắt tài liệu cá nhân, lập kế hoạch cá nhân." | "Tìm kiếm tri thức nội bộ công ty ngay lập tức và tự động hóa quy trình quản lý dự án." |
| **Trước đó họ làm bằng cách nào** | Dùng Evernote, Google Docs cá nhân, hoặc gõ chay từ đầu. | Dùng Confluence/Jira, dùng thanh search truyền thống hoặc nhắn tin hỏi đồng nghiệp trên Slack. |

**Dịch chuyển tệp:** Sự dịch chuyển xảy ra mạnh mẽ nhất từ cột mốc **11/2023 (Ra mắt tính năng Q&A)** và **08/2024 (Connect Drive/Slack)**. Việc tóm tắt văn bản cá nhân không khiến user trả 10$/tháng lâu dài, nhưng việc tiết kiệm hàng giờ đồng hồ tìm kiếm tài liệu công ty cho nhân viên là bài toán mà các doanh nghiệp sẵn sàng chi tiền mạnh tay.

**Switching cost (map 4 forces):**
*   **Pull (Lực kéo từ Notion):** Lực mạnh nhất. Mọi thứ quy về một nơi (All-in-one). AI tự có context mà không cần copy-paste hay huấn luyện rườm rà.
*   **Push (Lực đẩy từ cách cũ):** Quá mệt mỏi với việc thông tin công ty nằm rải rác ở Slack, Drive, Jira. Nhân viên mới onboarding mất quá nhiều thời gian.
*   **Habit (Thói quen):** Lực cản người dùng chuyển sang Notion - họ đã quá quen thuộc với bộ Office (Word/Excel) từ hàng chục năm nay, đặc biệt là tư duy quản lý theo "Folder" (Thư mục) truyền thống.
*   **Anxiety (Lo âu):** Lo sợ về bảo mật dữ liệu khi cho AI đọc toàn bộ thông tin nội bộ. Lo ngại chi phí chuyển đổi (migrating data) từ hệ thống cũ sang Notion mất nhiều tháng.
*   *Kết luận:* Lực đang giữ user ở lại Notion mạnh nhất là **Switching Cost về mặt Dữ liệu (Data Moat)**. Nếu công ty rời bỏ Notion, họ mất toàn bộ "não bộ" đã được cấu trúc và liên kết chặt chẽ.

---

**§3. Ba dự đoán hướng đi (6–12 tháng tới)**

**Dự đoán 1** *(loại: Mở rộng tính năng)*
- **Dự đoán:** Notion AI sẽ phát triển thành "AI Agent" có khả năng thực thi hành động, thay vì chỉ truy xuất thông tin (ví dụ: Tự động giao task, tự động gửi email dựa trên update của project).
- **Lập luận:** Dựa vào cột mốc 10/2024 (Ra mắt Forms & Mail). Khi Notion đã nắm giữ luồng đầu vào (Form) và đầu ra giao tiếp (Mail), kết hợp với JTBD của tệp Enterprise hiện tại là tự động hóa quy trình, việc cho phép AI tự động trigger các hành động là bước đi x10 tiếp theo bắt buộc phải có.

**Dự đoán 2** *(loại: Đe dọa từ Big Tech & Phản ứng)*
- **Dự đoán:** Notion sẽ tung ra các gói bảo mật "On-premise" hoặc "Private AI" dành riêng cho Enterprise, cam kết tuyệt đối không train model trên data của user với các chứng chỉ bảo mật cấp cao hơn.
- **Lập luận:** Theo §2, lực Anxiety lớn nhất của doanh nghiệp là bảo mật dữ liệu. Trong khi đó, Microsoft Copilot đang dùng chính lớp khiên bảo mật của hệ sinh thái Microsoft để ép các doanh nghiệp lớn không được dùng tool ngoài. Notion buộc phải xây dựng lớp phòng thủ này nếu muốn giữ chân tệp khách hàng Enterprise.

**Dự đoán 3** *(loại: Mô hình kiếm tiền & Pricing)*
- **Dự đoán:** Notion sẽ chia nhỏ gói AI theo từng nghiệp vụ (Vertical AI for Notion), ví dụ: Gói "Notion AI for PMs", "Notion AI for HR" thay vì bán một gói General AI dùng chung như hiện tại.
- **Lập luận:** Dựa vào sự chuyển dịch tệp user ở §2, khi sản phẩm đi sâu vào doanh nghiệp, các phòng ban sẽ có workflow và cấu trúc database cực kỳ khác nhau. Vertical AI (Domain Expert + AI Expert) sẽ giúp Notion bán được giá cao hơn (up-sell) cho từng phòng ban chuyên biệt.

---

**§4. AI Log**

| Việc | AI làm hay bạn làm? | Bạn kiểm chứng/phán đoán lại thế nào? |
|---|---|---|
| Xác định sản phẩm (Notion) và chiến lược tiếp cận bài toán. | Bạn (Huy) & AI thảo luận | Lựa chọn Notion vì nó có sự chuyển mình rõ rệt từ SaaS thường sang AI-native, dữ liệu public dồi dào, phù hợp với kiến thức lý thuyết (Moat, x10). |
| Tìm kiếm các cột mốc lịch sử, thời gian cụ thể (Tháng/Năm) và lấy link nguồn gốc. | AI tổng hợp (Truy xuất dữ liệu) | Tự click vào từng link blog/changelog của Notion để đối chiếu ngày tháng, loại bỏ các bản vá lỗi nhỏ không phản ánh "quyết định sản phẩm". |
| Map các cột mốc về các nguyên lý cốt lõi (Wrapper, Workflow, x10). | Bạn & AI cùng viết | AI đề xuất nguyên lý sơ bộ, mình (Huy) điều chỉnh lại wording để chuẩn với các concept học trong lớp Day 16. |
| Phân tích 4 forces và dịch chuyển tệp User. | Bạn định hướng, AI hoàn thiện văn phong | Đảm bảo phần JTBD được viết theo chuẩn "việc cần làm" (hành động sinh lời/tiết kiệm thời gian) thay vì viết theo tên tính năng. |
| Phán đoán 3 hướng đi trong 6-12 tháng tới. | Bạn (Huy) đưa ra core idea, AI hỗ trợ lập luận | Đảm bảo các dự đoán (đặc biệt là AI Agent và Security) móc nối logic 100% với dữ liệu từ §1 và §2. |
