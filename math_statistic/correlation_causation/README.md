| Correlation      | Causation              |
| ---------------- | ---------------------- |
| Quan sát         | Can thiệp              |
| Dễ tính          | Khó chứng minh         |
| Có thể giả       | Mang ý nghĩa hành động |
| Dùng để khám phá | Dùng để quyết định     |

## Cov và Cor

So ánh Cov avf Cor

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
