# Sentiment-Classification
📖 Giới thiệu Dự án
Dự án Sentiment-Classification do tác giả ThuThao-30604 phát triển, nhằm mục đích phân tích và phân loại cảm xúc từ các bài đăng trên mạng xã hội Twitter (tweet). Dữ liệu cốt lõi của dự án là tệp Tweets.csv, ghi nhận các phản hồi và đánh giá của khách hàng (Tích cực, Tiêu cực, Trung lập) đối với các hãng hàng không lớn tại Mỹ.
Mục tiêu chính là xây dựng một 파ypline Xử lý Ngôn ngữ Tự nhiên (NLP) hoàn chỉnh bằng Jupyter Notebook (100%) để tự động nhận diện cảm xúc văn bản và đánh giá trải nghiệm người dùng.
🗂️ Cấu trúc Kho lưu trữ (Repository Structure)
Dự án được phân chia thành các luồng công việc (workflow) rõ ràng, bao gồm mã nguồn, dữ liệu đặc trưng và các tệp mô hình đã huấn luyện:
1. Phân tích và Xử lý Dữ liệu
EDA.ipynb: Sổ tay (notebook) Phân tích Dữ liệu Khám phá (Exploratory Data Analysis) nhằm tìm hiểu phân phối dữ liệu, thống kê tần suất và bóc tách các nhóm nguyên nhân gây phàn nàn.
Data Processing.ipynb: Mã nguồn dùng để làm sạch văn bản, chuẩn hóa dữ liệu và tiền xử lý các trường thông tin thô từ tập Tweets.csv.
2. Huấn luyện và Tinh chỉnh Mô hình
Train model.ipynb: Quá trình huấn luyện các mô hình học máy cơ bản để phân loại cảm xúc.
Fine_tuning XGBoost.ipynb: Sổ tay chuyên sâu dùng để tinh chỉnh siêu tham số (Hyperparameter tuning) nhằm tối ưu hóa hiệu suất cho thuật toán XGBoost.
Test_model.ipynb: Đánh giá và kiểm thử độ chính xác của mô hình trên tập dữ liệu kiểm tra độc lập.
3. Dữ liệu Đầu vào & Đặc trưng (Features)
Tập dữ liệu gốc: Tweets.csv.
Ma trận TF-IDF (chứa đặc trưng đã được vector hóa): X_train_tfidf.npz, X_val_tfidf.npz, X_test_tfidf.npz.
Nhãn cảm xúc (Labels): y_train.csv, y_val.csv, y_test.csv.
4. Kết quả & Tài nguyên Xuất ra (Outputs)
Mô hình & Vectorizer đã lưu: best_model.pkl, best_xgboost_model.pkl, tfidf_vectorizer.pkl.
Cấu hình tốt nhất: best_params.json, best_model_name.txt.
Trực quan hóa đánh giá:
confusion_matrices.png: Ma trận nhầm lẫn để kiểm tra độ chính xác của từng nhãn.
model_comparison.png: Biểu đồ so sánh hiệu suất giữa các mô hình khác nhau.
smote_comparison.png & smote_comparison_validation.png: Trực quan hóa hiệu quả của kỹ thuật SMOTE trong việc xử lý tình trạng mất cân bằng dữ liệu.
Kết quả dự đoán áp dụng: skytrax_uzbekistan_all_predictions.csv (dự đoán thử nghiệm trên tập dữ liệu Skytrax).
🛠️ Công nghệ và Kỹ thuật Áp dụng
Ngôn ngữ lập trình & Môi trường: Python, Jupyter Notebook.
Biểu diễn ngôn ngữ (Text Vectorization): Sử dụng thuật toán TF-IDF để chuyển đổi văn bản thành dữ liệu số hóa.
Mô hình Học máy chính: XGBoost (Được tinh chỉnh sâu).
Xử lý dữ liệu mất cân bằng: Áp dụng thuật toán SMOTE (Synthetic Minority Over-sampling Technique) để khắc phục sự chênh lệch số lượng mẫu giữa các nhóm cảm xúc.
