# Week 7 KHDL

Dự án Machine Learning toàn diện (End-to-End) phân tích và dự đoán kết quả học tập của học sinh dựa trên dữ liệu về nhân khẩu học, thói quen sinh hoạt và hoàn cảnh gia đình.

## Tổng quan dự án (Project Overview)

Mục tiêu của dự án này là áp dụng các kỹ thuật Học máy (Machine Learning) đa dạng để khai thác bộ dữ liệu **Student Performance**. Không chỉ dừng lại ở việc dự đoán điểm số cuối kỳ (`G3`), dự án còn đi sâu vào phân tích các yếu tố ảnh hưởng, phân nhóm học sinh, giải thích quyết định của mô hình (Explainable AI) và đánh giá tính công bằng (Ethical AI).

## Dữ liệu (Dataset)

Bộ dữ liệu được sử dụng bao gồm thành tích học tập của học sinh ở hai môn:

- **Toán học (Math):** `student-mat.csv`
- **Tiếng Bồ Đào Nha (Portuguese):** `student-por.csv`

Dữ liệu gốc chứa hơn 30 thuộc tính (features) bao gồm độ tuổi, quy mô gia đình, nghề nghiệp của phụ huynh, thời gian tự học, mức độ đi chơi, v.v. Trong dự án này, cả hai tập dữ liệu được gộp lại để tăng kích thước mẫu huấn luyện, giúp mô hình tổng quát hóa tốt hơn.

## Cấu trúc thư mục (Project Structure)

Dự án được chia thành 7 notebooks tương ứng với 7 khía cạnh khác nhau của bài toán Data Science:

- **`1_Regression_PredictingG3.ipynb`**: Xây dựng mô hình Hồi quy tuyến tính (Linear Regression) để dự đoán điểm số cuối kỳ `G3`.
- **`2_Classification_Passfail.ipynb`**: Chuyển đổi bài toán thành Phân loại nhị phân (Đỗ/Trượt) sử dụng Hồi quy Logistic / Random Forest.
- **`3_Clustering_StudentSegmentation_K-means.ipynb`**: Phân nhóm học sinh (Segmentation) bằng thuật toán học không giám sát K-Means Clustering và tìm kiếm cụm tối ưu qua phương pháp Elbow.
- **`4_DimensionReduction_PCA.ipynb`**: Giảm chiều dữ liệu (Dimensionality Reduction) từ hơn 30 đặc trưng xuống không gian 2D bằng thuật toán PCA.
- **`5_EDA.ipynb`**: Phân tích khám phá dữ liệu (Exploratory Data Analysis), trực quan hóa phân phối điểm số và ma trận tương quan giữa các biến.
- **`6_ModelInterpretation_ExplainableAI.ipynb`**: Sử dụng thư viện SHAP (Explainable AI) để "mở hộp đen" mô hình, giải thích chi tiết mức độ đóng góp của từng thói quen/hoàn cảnh đến điểm số của học sinh.
- **`7_Ethical_BiasFairness.ipynb`**: Đánh giá tính đạo đức và sự công bằng (Fairness) của mô hình AI đối với các nhóm nhạy cảm (như Giới tính) bằng Fairlearn.

## Thư viện sử dụng (Technologies Used)

- **Xử lý dữ liệu:** `pandas`, `numpy`
- **Trực quan hóa:** `matplotlib`, `seaborn`
- **Machine Learning:** `scikit-learn`
- **Giải thích mô hình (XAI):** `shap`
- **Đánh giá công bằng (Fairness):** `fairlearn`
