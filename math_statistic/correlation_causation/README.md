Giới hạn của Correlation trong Machine Learning
🚧 (1) Chỉ đo tuyến tính

Bỏ sót quan hệ phi tuyến

Tree-based models không cần Cor cao

🚧 (2) Không phản ánh tương tác feature

X₁ * X₂ có thể quan trọng

Nhưng Cor(X₁, y), Cor(X₂, y) đều thấp

🚧 (3) Nhạy với outlier

Dữ liệu thực tế → rất nguy hiểm

🚧 (4) Không gắn với performance

Feature Cor cao ≠ improve accuracy

Feature Cor thấp ≠ vô dụng

🚧 (5) Không nói gì về nhân quả

ML dự đoán tốt ≠ hiểu đúng thế giới

---

| Correlation      | Causation              |
| ---------------- | ---------------------- |
| Quan sát         | Can thiệp              |
| Dễ tính          | Khó chứng minh         |
| Có thể giả       | Mang ý nghĩa hành động |
| Dùng để khám phá | Dùng để quyết định     |

## Tổng hợp bẫy 

| Bẫy          | Vấn đề                       | Cách tránh             |
| ------------ | ---------------------------- | ---------------------- |
| Cor ≠ Cause  | Nhầm lẫn quan sát & nhân quả | Thiết kế thí nghiệm    |
| Spurious Cor | Trùng hợp                    | Kiểm tra logic & trend |
| Simpson      | Gộp dữ liệu sai              | Phân tích theo nhóm    |
| Confounder   | Biến ẩn                      | Kiểm soát biến         |


## Cov và Cor


| Tiêu chí           | Pearson | Spearman   | Kendall |
| ------------------ | ------- | ---------- | ------- |
| Tuyến tính         | ✔️      | ❌          | ❌       |
| Đơn điệu           | ❌       | ✔️         | ✔️      |
| Outlier            | Nhạy    | Ít nhạy    | Rất ít  |
| Ordinal            | ❌       | ✔️         | ✔️      |
| Mẫu nhỏ            | ❌       | Trung bình | ✔️      |
| Diễn giải xác suất | ❌       | ❌          | ✔️      |


So ánh Cov avf Cor

| Cách                     | Khi nào dùng                    |
| ------------------------ | ------------------------------- |
| **Spearman Correlation** | Quan hệ đơn điệu, có outlier    |
| **Kendall’s tau**        | Mẫu nhỏ                         |
| Scatter plot             | Luôn luôn nên vẽ                |
| Xử lý outlier            | Winsorize, trim, robust methods |


| Tiêu chí   | **Cov (Covariance)**             | **Cor (Correlation)**      |
| ---------- | -------------------------------- | -------------------------- |
| Đo cái gì  | Hai biến **biến động cùng nhau** | **Mức độ & chiều** liên hệ |
| Giá trị    | (-\infty \rightarrow +\infty)    | **[-1, 1]**                |
| Đơn vị     | **Có đơn vị** (X·Y)              | **Không đơn vị**           |
| So sánh    | ❌ Khó so sánh                    | ✅ So sánh trực tiếp        |
| Dùng nhiều | Nền tảng toán học                | Phân tích thực tế          |

| Quan hệ            | Covariance | Correlation |
| ------------------ | ---------- | ----------- |
| Tuyến tính dương   | > 0        | > 0         |
| Tuyến tính âm      | < 0        | < 0         |
| Phi tuyến đối xứng | ≈ 0        | ≈ 0         |
| Không liên quan    | ≈ 0        | ≈ 0         |

🔹 Hiểu bằng trực giác
Covariance

“X và Y có cùng lệch khỏi trung bình không?”

Chỉ quan tâm cùng chiều hay ngược chiều

Không nói rõ mạnh hay yếu

Correlation

“Mối quan hệ mạnh đến mức nào?”

Chuẩn hóa → dễ hiểu

-1: ngược chiều hoàn hảo

0: không tuyến tính

1: cùng chiều hoàn hảo

Ví dụ 

Giả sử:

X = chiều cao (cm)

Y = cân nặng (kg)

Cov(X,Y) = 120 ❓ → 120 là nhiều hay ít? (khó nói)

Cor(X,Y) = 0.8 ✅ → liên hệ mạnh

✅ Dùng Cov khi:

Học lý thuyết thống kê

Làm PCA / multivariate statistics

Làm nền cho correlation, regression

✅ Dùng Cor khi:

Khám phá dữ liệu (EDA)

So sánh mối quan hệ

Trình bày cho người khác

## Correlation vs Causation

Khi nào dùng correlation

Khi nào cần causation

Vì sao ML thường chỉ học correlation

Luôn vẽ DAG trước khi phân tích

Không tin regression mù quáng

Ưu tiên thí nghiệm nếu có thể

Luôn hỏi: “Nếu tôi can thiệp thì sao?”
