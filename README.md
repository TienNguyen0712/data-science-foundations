Nếu thiếu phần này, học Recommendation sẽ rất khó

🔹 Toán

Đại số tuyến tính

Vector, matrix

Dot product

Matrix factorization

Xác suất – thống kê

Mean, variance

Probability

Distribution cơ bản

👉 Không cần quá hàn lâm, chỉ cần hiểu và dùng được

🔹 Lập trình

Python

Numpy

Pandas

Matplotlib / Seaborn

SQL cơ bản (SELECT, JOIN, GROUP BY)

🔹 Machine Learning căn bản

Supervised vs Unsupervised

Loss function

Overfitting

Train / validation / test

📌 Gợi ý:

Nếu bạn chưa học ML → nên học ML cơ bản trước khi vào Recommendation

2️⃣ Hiểu bài toán Recommendation System

Trước khi học model, cần hiểu bài toán thực tế

🔹 Recommendation System là gì?

Gợi ý:

phim (Netflix)

sản phẩm (Shopee, Amazon)

video (YouTube, TikTok)

nhạc (Spotify)

🔹 Các loại dữ liệu

Explicit feedback

Rating (1–5 sao)

Implicit feedback

Click

View

Like

Purchase

🔹 Các vấn đề kinh điển

Cold start (user mới / item mới)

Sparsity (ma trận rất thưa)

Scalability (dữ liệu rất lớn)

3️⃣ Các mô hình Recommendation cơ bản (CỐT LÕI)
🔹 1. Popularity-based

Gợi ý item phổ biến nhất

Là baseline cực kỳ quan trọng

🔹 2. Content-based Filtering

Dựa trên đặc trưng của item

Ví dụ:

Gợi ý phim cùng thể loại

Kỹ thuật:

TF-IDF

Cosine similarity

🔹 3. Collaborative Filtering
a. User-based CF

Người giống nhau → thích giống nhau

b. Item-based CF

Item giống nhau → user thích giống nhau

👉 Dùng:

Cosine similarity

Pearson correlation

📌 Đây là nền móng của Recommendation

4️⃣ Matrix Factorization & mô hình nâng cao
🔹 Matrix Factorization

SVD

ALS (Alternating Least Squares)

Latent factors

👉 Hiểu khái niệm:

User embedding

Item embedding

🔹 Neural Recommendation

Neural Collaborative Filtering (NCF)

Deep Learning cho RecSys

🔹 Context-aware Recommendation

Time

Location

Device

5️⃣ Đánh giá hệ thống Recommendation
🔹 Offline metrics

RMSE

MAE

Precision@K

Recall@K

MAP, NDCG

🔹 Online metrics (khái niệm)

CTR

Conversion rate

A/B testing

📌 Nhiều người học RecSys nhưng bỏ qua phần evaluation → rất thiếu

6️⃣ Triển khai thực tế (Production)
🔹 Data pipeline

Thu thập dữ liệu

Preprocessing

Feature engineering

🔹 MLOps cho Recommendation

Batch vs Real-time recommendation

Model update

Cold start handling

🔹 Công nghệ thường dùng

Spark / PySpark

Kafka (streaming)

Redis (cache recommendation)

ự án nên làm (RẤT QUAN TRỌNG)
🔹 Project gợi ý

Movie Recommendation (MovieLens)

Product Recommendation (E-commerce)

Music Recommendation

News Recommendation

📌 Mỗi project nên có:

EDA

Baseline model

CF / MF model

Evaluation

Report

1. TÀI LIỆU HỌC FREE (ĐÃ ĐƯỢC CHỌN LỌC)
🔹 Nền tảng ML & Python
Python & Data

Kaggle Learn (FREE, rất thực hành)
👉 Python, Pandas, ML Intro

Python Data Science Handbook – Jake VanderPlas (free online)

Machine Learning

Coursera – Machine Learning (Andrew Ng)
👉 Có thể học free (audit)

StatQuest (YouTube)
👉 Cực dễ hiểu cho:

Matrix Factorization

SVD

Loss function

🔹 Recommendation System (CỐT LÕI)
📘 Sách / Notes

Recommender Systems Handbook (đọc chọn chương)

CS246 – Mining Massive Datasets (Stanford)
👉 Lecture về Collaborative Filtering (FREE)

🎥 Video

Google Developers – Recommendation Systems

Microsoft Recommenders (GitHub)
👉 Code + notebook rất thực tế

🧪 Dataset FREE

MovieLens (100K, 1M) ⭐

Amazon Product Review Dataset

Netflix Prize (đọc hiểu, không cần train full)
