
# 🎓 Phân loại cảm xúc sinh viên bằng Machine Learning

## 📌 Giới thiệu
Đề tài tập trung vào việc **phân loại cảm xúc sinh viên** (Positive, Negative, Neutral) dựa trên bộ dữ liệu phản hồi giả lập (synthetic feedback).  
Mục tiêu: Xây dựng mô hình học máy có khả năng nhận diện và phân loại cảm xúc trong văn bản tiếng Việt, phục vụ cải thiện môi trường học tập.

---

## 🎯 Mục tiêu & Ý nghĩa
- Ứng dụng các kỹ thuật xử lý ngôn ngữ tự nhiên (NLP) cho tiếng Việt.  
- So sánh hiệu suất các phương pháp biểu diễn văn bản: **Bag-of-Words (BoW), TF-IDF, Sentence Embeddings**.  
- Huấn luyện và đánh giá các mô hình: **Logistic Regression, LinearSVC**.  
- Xác định tổ hợp mô hình tối ưu theo chỉ số **F1-score Macro**.

**Ý nghĩa thực tiễn**:  
- Giúp giảng viên và nhà trường nắm bắt được mức độ hài lòng của sinh viên.  
- Cải thiện phương pháp giảng dạy, chương trình học và cơ sở vật chất.  
- Ứng dụng cho hệ thống **Smart Learning** và quản lý phản hồi trực tuyến.  

---

## 🗂️ Dữ liệu
- `synthetic_train.csv`: Tập huấn luyện (~4000 mẫu).  
- `synthetic_val.csv`: Tập kiểm thử (~1000 mẫu).  

**Cấu trúc dữ liệu**:
- `sentence`: Câu phản hồi của sinh viên.  
- `sentiment`: Nhãn cảm xúc (`positive`, `negative`, `neutral`).  
- `topic`: Chủ đề phản hồi (`lecturer`, `curriculum`, `facility`).  

📊 **Phân phối dữ liệu**: cân bằng giữa 3 lớp (≈33.3% mỗi lớp).  

---

## 🛠️ Công nghệ sử dụng
- **Ngôn ngữ**: Python 3.x  
- **Môi trường**: Google Colab / Jupyter Notebook  
- **Thư viện chính**:
  - `pandas`, `numpy`, `matplotlib`, `seaborn` (tiền xử lý & trực quan hóa)  
  - `underthesea` (tách từ tiếng Việt)  
  - `scikit-learn` (vector hóa, huấn luyện mô hình, đánh giá)  
  - `sentence-transformers` (tạo sentence embeddings)  

---

## 🚀 Cách chạy code
1. Mở file notebook: **`Nhóm_1.ipynb`** trên Google Colab.  
2. Upload hai file dữ liệu `synthetic_train.csv` và `synthetic_val.csv`.  
3. Cài đặt thư viện cần thiết:
   ```bash
   pip install underthesea sentence-transformers scikit-learn
   ```
4. Chạy lần lượt các cell trong notebook để:
   - Tiền xử lý dữ liệu  
   - Vector hóa văn bản (BoW, TF-IDF, Embeddings)  
   - Huấn luyện Logistic Regression và LinearSVC  
   - Đánh giá mô hình và xuất báo cáo kết quả  

---

## ✅ Kết quả chính
- **Sentence Embeddings + LinearSVC** đạt kết quả tốt nhất.  
- Hiệu suất trung bình:
  - Accuracy: ~87.1%  
  - Macro F1-score: ~0.871  
- Vấn đề còn tồn tại: khó phân biệt lớp **Neutral** do mơ hồ ngữ nghĩa.  

📌 **Tóm tắt so sánh**:  
- BoW + LR: Accuracy ~81.7%  
- TF-IDF + LR: Accuracy ~83.5%  
- Embeddings + LR: Accuracy ~86.5%  
- Embeddings + SVC: **Accuracy ~87.1% (tốt nhất)**  

---

## 📊 Demo trực quan
- 📈 Biểu đồ phân phối nhãn cảm xúc.  
- 📊 Histogram tỷ lệ cảm xúc theo chủ đề (Lecturer, Curriculum, Facility).  
- ☁️ Word Cloud minh họa từ ngữ nổi bật.  
- 🔎 Ma trận nhầm lẫn (Confusion Matrix) cho mô hình tốt nhất.  

---

## 👨‍💻 Thành viên
- **Nguyễn Gia Thái** – 1771020618  
- **Lê Đức Thọ** – 1771020651  

📍 Trường Đại học Đại Nam – Lớp PTPM 17-12  

---

## 📖 Tài liệu tham khảo
1. Alan Beaulieu, *Learning SQL*, O’Reilly Media, 2020.  
2. Adam Freeman, *Pro ASP.NET Core 7*, Manning, 2023.  
3. Mark J. Price, *C# 13 and .NET 9*, Packt, 2024.  
4. RB Whitaker, *The C# Player’s Guide*, 2022.  
5. Phạm Văn Tiệp, *Thiết kế và lập trình Back-End*, Đại học Đại Nam, 2025.  

---

✨ *README.md được xây dựng để trình bày bài tập lớn học phần **Nhập môn học máy** – Đề tài: Phân loại cảm xúc sinh viên.*
