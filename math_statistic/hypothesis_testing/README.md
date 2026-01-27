> Sự khác biệt này có thật hay chỉ là ngẫu nhiên


📊 Bảng chọn nhanh (Data Science style)
Bài toán	Kiểm định
So sánh 2 phiên bản	t-test / z-test
So sánh nhiều nhóm	ANOVA
Biến phân loại	Chi-square
Không chuẩn	Mann–Whitney
Trước – sau	Wilcoxon
Tương quan	Pearson / Spearman

🧠 Data Scientist thường dùng kiểm định khi nào?

A/B testing

Feature selection

Kiểm tra bias dữ liệu

Đánh giá kết quả mô hình

Phân tích hành vi người dùng

📌 Kiểm định tham số phổ biến

z-test

t-test (1 mẫu, 2 mẫu, cặp)

ANOVA

Pearson correlation


📌 Kiểm định phi tham số phổ biến

Mann–Whitney U

Wilcoxon signed-rank

Kruskal–Wallis

Spearman correlation

Chi-square

👉 Dữ liệu càng đẹp → càng nên dùng tham số
👉 Dữ liệu càng bẩn → chuyển sang phi tham số


8. Bảng so sánh nhanh (rất hay ra thi)
Mục tiêu	Tham số	Phi tham số
1 trung bình	Z / t	—
2 nhóm độc lập	t-test	Mann–Whitney
Trước – sau	Paired t	Wilcoxon
≥ 3 nhóm	ANOVA	Kruskal–Wallis
Phương sai	F-test	—


👉 Câu hỏi cốt lõi của mọi kiểm định chỉ là:

“Dữ liệu ta thu được có quá khác thường nếu giả thuyết ban đầu là đúng hay không?”

H₀: điều “bình thường”

Thống kê kiểm định: đo mức độ khác thường

p-value: xác suất thấy dữ liệu “lạ như vậy” nếu H₀ đúng

👉 p nhỏ ⇒ dữ liệu khó xảy ra nếu H₀ đúng ⇒ nghi ngờ H₀

Kiểm định	Câu hỏi bản chất
Z / t	Trung bình lệch bao nhiêu σ?
Paired t	Mức thay đổi có khác 0?
F-test	Hai độ phân tán có khác?
ANOVA	Khác biệt giữa nhóm > nhiễu?
Mann–Whitney	Nhóm nào thường lớn hơn?
Wilcoxon	Thay đổi có xu hướng tăng/giảm?
Kruskal–Wallis	Nhóm nào có hạng cao hơn

Bài toán DS	Kiểm định
So sánh 2 mô hình	Paired t / Wilcoxon
A/B testing	Z-test / t-test
So sánh nhiều nhóm người dùng	ANOVA / Kruskal–Wallis
Kiểm tra phân phối đặc trưng	F-test
Feature có khác giữa class?	t-test / Mann–Whitney
