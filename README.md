# Fake-News-Detection
## 📌 Giới thiệu

Dự án này tập trung vào việc xây dựng mô hình AI để phát hiện tin giả (fake news) sử dụng các kỹ thuật xử lý ngôn ngữ tự nhiên (NLP) và học máy. Bộ dữ liệu bao gồm các bài báo thật từ nguồn uy tín (Reuters, NY Times) và tin giả từ các trang cực đoan.

## 📂 Bộ dữ liệu

MisinfoSuperset_TRUE.csv: Tin thật (34,526 bài)
MisinfoSuperset_FAKE.csv: Tin giả (34,078 bài)
Đặc điểm chính:
Cân bằng giữa 2 lớp (True/Fake)
Văn bản dài trung bình ~552 từ
Tin giả có nhiều dấu câu cảm thán, từ viết hoa, URL hơn tin thật
## 🔍 Phân tích dữ liệu

Phân phối nhãn: Cân bằng giữa True/Fake
Độ dài văn bản: Tin giả có nhiều outlier về số từ/câu
Từ vựng: Tin giả dùng nhiều từ giật gân, cảm xúc
Độ dễ đọc: Tin thật ổn định hơn, ít outlier
Cảm xúc: Tin giả có xu hướng chủ quan và cực đoan hơn
## ⚙️ Xử lý dữ liệu

Loại bỏ bản ghi trùng lặp
Giữ lại dấu câu, chữ hoa, URL (vì là đặc trưng quan trọng)
Không chuyển lowercase để bảo toàn ngữ cảnh
Xử lý outlier về độ dài văn bản


## 📊 Kết quả đánh giá mô hình

| Mô hình            | Accuracy | Precision | Recall  | F1-score |
|--------------------|----------|-----------|---------|----------|
| Naive Bayes        | 0.8872   | 0.9028    | 0.8666  | 0.8843   |
| Logistic Regression| 0.9479   | 0.9470    | 0.9485  | 0.9477   |
| LSTM               | 0.9447   | 0.9372    | 0.9524  | 0.9447   |
| BERT               | 0.9910   | 0.9935    | 0.9883  | 0.9909   |
| SVM                | 0.9177   | 0.9153    | 0.9196  | 0.9175   |
| XLNet              | 0.9954   | 0.9940    | 0.9957  | 0.9949   |
| DeBERTa            | 0.9976   | 0.9986    | 0.9960  | 0.9973   |
