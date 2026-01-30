# 🔗 **Correlation (Tương quan)**
> Đo lường mức độ và chiều hướng mà hai biến thay đổi cùng nhau.

[Notebook](correlation_causation.ipynb)

## **1. Pearson Correlation (Tuyến tính)**

Là Corr đo mức độ tuyến tính hai biến liên tục

---

## **2. Spearman Correlation (Phi tuyến)**

Đo mối quan hệ đơn điệu 

> Khi x tăng Y có xu hướng tăng hoặc giảm, không cần tuyến tính

---

## **3. Kendall's Tau**

Kendall đo xác suất hai biến cùng "đồng thuận" về thứ tự.

---

## **4. Partial Correlation**

Đo mối liên hệ giữa X và Y sau khi đã loại bỏ một vài ảnh hưởng cảu một (hoặc nhiều) biến kiểm soát Z

> Nếu giữ Z khổng đổi, X và Y còn liên quan với nhau không?

So sánh các tương quan 

| Tiêu chí           | Pearson | Spearman   | Kendall |
| ------------------ | ------- | ---------- | ------- |
| Tuyến tính         | ✔️      | ❌          | ❌       |
| Đơn điệu           | ❌       | ✔️         | ✔️      |
| Outlier            | Nhạy    | Ít nhạy    | Rất ít  |
| Ordinal            | ❌       | ✔️         | ✔️      |
| Mẫu nhỏ            | ❌       | Trung bình | ✔️      |
| Diễn giải xác suất | ❌       | ❌          | ✔️      |

---

### **So sánh Corr và Cov**

Các tiêu chí lựa chọn Corr và Cov

| Tiêu chí   | **Cov (Covariance)**             | **Cor (Correlation)**      |
| ---------- | -------------------------------- | -------------------------- |
| Đo cái gì  | Hai biến **biến động cùng nhau** | **Mức độ & chiều** liên hệ |
| Giá trị    | (-\infty \rightarrow +\infty)    | **[-1, 1]**                |
| Đơn vị     | **Có đơn vị** (X·Y)              | **Không đơn vị**           |
| So sánh    | ❌ Khó so sánh                    | ✅ So sánh trực tiếp        |
| Dùng nhiều | Nền tảng toán học                | Phân tích thực tế          |
| Câu hỏi | X và Y có cùng lệch khỏi trung bình không? | Mối quan hệ mạnh đến mức nào? |
| Đặc điểm | X và Y có cùng lệch khỏi trung bình không? | Mối quan hệ mạnh đến mức nào? |
| | Chỉ quan tâm cùng chiều hay ngược chiều | Chuẩn hóa → dễ hiểu |
| | Không nói rõ mạnh hay yếu | Có dấu |
| Dùng khi | Học lý thuyết thống kê | Khám phá dữ liệu (EDA) |
|  | Làm PCA / multivariate statistics | So sánh mối quan hệ |
|  | Làm nền cho correlation, regression | Trình bày cho người khác |

**Giả sử:**
- X = chiều cao (cm)
- Y = cân nặng (kg)
  - Cov(X,Y) = 120 ❓ → 120 là nhiều hay ít? (khó nói)
  - Cor(X,Y) = 0.8 ✅ → liên hệ mạnh

---

### **Tổng hợp bẫy hay gặp trong Correlation**

| Bẫy          | Vấn đề                       | Cách tránh             |
| ------------ | ---------------------------- | ---------------------- |
| Cor ≠ Cause  | Nhầm lẫn quan sát & nhân quả | Thiết kế thí nghiệm    |
| Spurious Cor | Trùng hợp                    | Kiểm tra logic & trend |
| Simpson      | Gộp dữ liệu sai              | Phân tích theo nhóm    |
| Confounder   | Biến ẩn                      | Kiểm soát biến         |


Các cách để né các bẫy
| Cách                     | Khi nào dùng                    |
| ------------------------ | ------------------------------- |
| **Spearman Correlation** | Quan hệ đơn điệu, có outlier    |
| **Kendall’s tau**        | Mẫu nhỏ                         |
| Scatter plot             | Luôn luôn nên vẽ                |
| Xử lý outlier            | Winsorize, trim, robust methods |


Giới hạn của Correlation trong Machine Learning
-  (1) Chỉ đo tuyến tính
-  (2) Không phản ánh tương tác feature
-  (3) Nhạy với outlier
-  (4) Không gắn với performance
-  (5) Không nói gì về nhân quả

---

### **Khi nào NÊN / KHÔNG NÊN dùng Cor trong ML**

| ✅ NÊN                | ❌ KHÔNG NÊN                   |
| ------------------------ | ------------------------------- |
| EDA ban đầu | Là tiêu chí chọn feature duy nhất    |
| Linear models       | Áp dụng mù quáng cho phi tuyến                       |
| Giảm feature trùng lặp             | Diễn giải như nhân quả            |
| Phát hiện multicollinearity            |  |

---

| Correlation      | Causation              |
| ---------------- | ---------------------- |
| Quan sát         | Can thiệp              |
| Dễ tính          | Khó chứng minh         |
| Có thể giả       | Mang ý nghĩa hành động |
| Dùng để khám phá | Dùng để quyết định     |



## Correlation vs Causation

Khi nào dùng correlation

Khi nào cần causation

Vì sao ML thường chỉ học correlation

Luôn vẽ DAG trước khi phân tích

Không tin regression mù quáng

Ưu tiên thí nghiệm nếu có thể

Luôn hỏi: “Nếu tôi can thiệp thì sao?”
