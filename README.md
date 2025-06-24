# Gender-Classification
### Thông tin chung. 
- Dự án cuối kỳ môn xử lý và phân tích hình ảnh - Làm cá nhân.
- Mô hình ResNet-18 phân loại giới tính (nhị phân).
- Vì dự án là một competition trên Kaggle, nên các thử nghiệm được lưu trữ trên Kaggle: https://www.kaggle.com/code/minhius/gender-classification

### Về dự án:
1. Mô hình.
- Mô hình ResNet-18 và ResNet-34 đã được pretrain trên tập dữ liệu Image1k_V1, và được fine-tune trên bộ dữ liệu do competition cung cấp trên Kaggle.
- Được train trên Kaggle với GPU T4 x 2 trong 1.5 giờ.
- Mô hình tốt nhất (ResNet-18) đạt accuracy trên tập train và trên tập validation 97.8%, với kết quả kiểm thử công khai là 99%.

![18_best_loss](https://github.com/user-attachments/assets/aeebf184-46c3-4d8b-baa9-26de678b8ddc)
![18_best_acc](https://github.com/user-attachments/assets/e2a8da88-12fa-4365-bfed-779855af7846)



2. Kiểm thử.
- Kiểm thử công khai sẽ sử dụng 30% bộ dữ liệu test, và 70% còn lại sẽ dành cho kiểm thử không công khai.
  + Kiểm thử công khai - **Accuracy**: 99%<br>
  + Kiểm thử không công khai - **Accuracy**: 97,57%<br>

3. Bộ dữ liệu huấn luyện.
- Bộ dữ liệu có kích thước 10 nghìn ảnh định dạng .jpg, với 2 labels: Male và Female.
- Train/val/test = 80/10/10, và được chia sẵn bởi competition.

4. Bộ dữ liệu kiểm thử.
- Là tập 1000 ảnh có phân bố giống tập huấn luyện và đánh giá, không gán nhãn do yêu cầu đề bài.

5. Các loại file.
- **gender-classification.ipynb**: File mã nguồn fine-tune mô hình và báo cáo.
- **Illustrations.zip**: File zip chứa các ảnh minh họa trong notebook và một số kết quả huấn luyện.

### Cách cài đặt.
- Notebook chạy một lượt từ đầu đến cuối.

### Disclaimer.
- Dữ liệu huấn luyện được cung cấp bởi viện AI-UET: https://www.kaggle.com/competitions/2425-ii-ait-3002-1-gender-classification
- Notebook trên Kaggle có 25 versions. Notebook gốc bao gồm khoảng 42 versions từ lúc bắt đầu làm đã bị mất do sơ xuất.
