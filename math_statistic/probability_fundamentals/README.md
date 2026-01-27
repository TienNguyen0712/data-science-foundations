# 📘 **Xác suất cơ bản**
> Xác suất giúp khoa học dữ liệu mô hình hóa sự không chắc chắn và ra quyết định trong điều kiện thiếu thông tin hoàn hảo

[Notebook](probability_fundamentals.ipynb)

## **1. Mục tiêu của xác suất**

> Nếu thống kê trả lời "điều gì đã xảy ra" thì xác suất trả lời "điều gì có thể xảy ra và mức độ tin cậy là bao nhiêu"

Trong thực tế thế giới dữ liệu là không chắc chắn
- Dữ liệu nhiễu
- Dữ liệu thiếu
- Quan sát không lặp lại y hệt
- Hành vi con người khó đoán

🔥 **Xác suất là ngôn ngữ toán học cho sự bất định**

Trong Khoa học dữ liệu 
- Dữ liệu sinh **sinh ra từ một phân phối xác suất**
- Mỗi điểm dữ liệu là một **biến ngãu nhiên**

🔥 Không có xác suất -> **sẽ không có mô hình thống kê**

Ta sẽ không bao giờ có toàn bộ dữ liệu. Do đó xác suất giúp:
- Ưóc lượng tham số
- Tính độ tin cậy
- Đánh giá sai só

🔥 Câu trả lời **luôn là xác suất**, không phải chắc chắn

---

## **2. Khái niệm cốt lõi**
### **2.1. Phép thử ngẫu nhiên**
- Là kết quả không thể biết được dù thực hiện cùng một điều kiện
- **Không gian mẫu:** là tập hợp của tất cả các kết quả có thể xảy ra của phép thử
- **Biến cố:** là tập con của không gian mẫu
  - Biến cố chắc chắn: là biến cố chắc chắn xảy ra p(Ω) = 1  
  - Biến cố đối: là biến cố ngược với biến cố xảy ra p(-) = 1 - p

Trong khoa học dữ liệu
- Phép thử = mỗi lần thu thập dữ liệu
- Kết quả là không chăc chăn và không lặp lại y hệt

### **2.2 Biến ngẫu nhiên**
- **Rời rạc:** Ghi nhận các giá trị rời rạc (đếm được)
- **Liên tục:** Nhận vô số giá trị trong một khoảng liên tục

Trong khoa học dữ liệu 
- Mỗi đặc trưng (feature) = một biến ngẫu nhiên
- Nhãn (label) = biến ngẫu nhiên

### **2.3. Kỳ vọng & Phương sai**
- **Kỳ vọng:** Là giá trị trung bình "lý thuyết" của biến ngẫu nhiên nếu lặp lại rất nhiều lần
- **Phương sai:** Đo mức độ phân tán của biến ngẫu nhiên quanh kỳ vọng

Trong khoa học dữ liệu 
- Định lượng mức độ trung bình và bất ổn của dữ liệu

--- 

## **3. Xác suất có điều kiện**
> Thu hẹp không gian -> suy luận khi có thông tin phụ

- Xác suất biến cố **A xảy ra khi biết B đã xảy ra**
- Khi có thêm thông tin B, không gian mẫu bị thu hẹp
- Hầu hết trong Khoa học dữ liệu đều là:
  - Xác suất rời bỏ khi biết hành vi
  - Xác suất bệnh khi biết triệu chứng
---

## **4. Định lý Bayes**
> Đảo chiều điều kiện -> Suy luận, cơ chế học và cập nhật niềm tin

- Cập nhậy xác suaastkho có dữ liệu mới
- Dùng cho chuẩn đoán, phân loại, học máy
- Cách máy "suy nghĩ" khi có dữ liệu mới
- Prior + Data -> Posterior

---

## **5. Luật số lớn**
> Hội tụ giá trị 

Lấy mẫu càng nhiều thì trung bình càng chính xác

- Giari thích vì sao trung bình mẫu đại diện cho dữ liệu thật

--- 

## **6. Định lý giới hạn trung tâm**
> Hội tụ phân phối 

Trung bình mẫu có phân phối gần chuẩn dù biến gốc không chuản
- Cho phép dùng phân phối chuẩn trong hầu hết bài toán
  - Ưóc lượng
  - Kiểm định
  - Khoảng tin cậy
> Khoa học dữ liệu không tìm "sự thật tuyệt đối", mà tìm quyết định tốt nhất trong điều kiện không chắc chắn -- bằng xác suất  
