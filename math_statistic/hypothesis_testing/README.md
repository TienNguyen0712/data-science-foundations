# 🧮 **Kiểm định giả thuyết thống kê**

Mục tiêu chính của kiểm định giả thuyết chính là để trả lời cho câu hỏi
> Sự khác biệt này có thật hay chỉ là ngẫu nhiên

[Notebook](hypothesis_testing.ipynb)

## 🧪 **Phân loại các kiểm định**

> Data Science không phải là tìm p-value nhỏ,
mà là giảm rủi ro khi ra quyết định từ dữ liệu.

📉 **Kiểm định tham số và phi tham số:**

- **Kiểm định tham số** là các kiểm định thống kê:
  - **Giả định** dữ liệu tuân **theo một phân phối** xác định (thường là **phân phối chuẩn**)
  - Dựa trên các **tham số của tổng thể** như: **trung bình (μ), phương sai (σ²)**
- **Kiểm định phi tham số** là các kiểm định thống kê:
  - **Không yêu cầu** dữ liệu tuân theo phân phối cụ thể
  - Không dựa trực tiếp vào trung bình hay phương sai
  - Thường dựa trên **thứ hạng (rank)** hoặc trung vị

📊 Bảng chọn nhanh kiểm định

| Phân loại | Kiểm định | Mục đích | Khi dùng | 
|----------|---------|---------|-----------|
| Kiểm định tham số |  z-test |	So sánh 1 trung bình | Trung bình mẫu lệch trung bình giả định bao nhiêu σ? | 
| | ANOVA |	Từ 3 nhóm trở lên | Khác biệt giữa nhóm > nhiễu? | 
| | F-test | So sánh phương sai | Hai độ phân tán có khác? |
| | t-test 1 mẫu |  So sánh 1 trung bình | Trung bình mẫu lệch trung  bình giả định bao nhiêu ? |
| | t-test 2 mẫu | So sánh 2 trung bình của 2 nhóm | Hai nhóm này có liên quan tới nhau hay không?  
| | t-test cặp | So sánh trước sau trên cùng đối tượng | Hai nhóm trước sau có gì thay đổi hay không? |
| Kiểm định phi tham số | Mann–Whitney U | So sánh 2 nhóm độc lập | Nhóm nào thường lớn hơn? | 
| | Kruskal–Wallis | Từ 3 nhóm trở lên không phân phối chuẩn | Nhóm nào có hạng cao hơn, các nhóm có khác nhau hay không? | 
| | Wilcoxon signed-rank	|  So sánh trước sau không phân phối chuẩn | Thay đổi có xu hướng tăng/giảm? | 
| | Chi-square độc lập | Hai biến phân loại | Hai biến phân loại có liên quan đến nhau hay không ? |
| | Chi-square goodness of fit | Dữ liệu liên tục, mẫu nhỏ | Dữ liệu có phù hợp cho phân phối giả định hay không? |

- **👉 Dữ liệu càng đẹp → càng nên dùng tham số**
- **👉 Dữ liệu càng bẩn → chuyển sang phi tham số**

---

## 🧠 **Thường dùng kiểm định khi nào?**
- A/B testing _(Z-test / t-test)_
- Feature selection
- Feature có khác giữa class?	_(t-test / Mann–Whitney)_
- Kiểm tra bias dữ liệu phân phối đặc trưng _(F-test)_
- Đánh giá kết quả mô hình
- Phân tích hành vi người dùng
- So sánh 2 mô hình _(Paired t / Wilcoxon)_
- So sánh nhiều nhóm người dùng _(ANOVA / Kruskal–Wallis)_

---

## 📌 **Mục tiêu của mọi kiểm định**

Câu hỏi cốt lõi của mọi kiểm định chỉ là:

> “Dữ liệu ta thu được có quá khác thường nếu giả thuyết ban đầu là đúng hay không?”

- **Đặt H₀:** điều “bình thường”
- **Thống kê kiểm định:** đo mức độ khác thường
- **p-value:** xác suất thấy dữ liệu “lạ như vậy” nếu H₀ đúng
  - p nhỏ ⇒ dữ liệu khó xảy ra nếu H₀ đúng ⇒ nghi ngờ H₀
