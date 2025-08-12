Tổng quan về bài toán

Thị trường bất động sản là một trong những thị trường được chú trọng nhất về giá cả và liên tục biến động. Đây là một trong những lĩnh vực chính để áp dụng các ý tưởng của máy học về cách cải thiện chi phí với độ chính xác cao. Mục tiêu của dự án là dự đoán giá trị thị trường của bất động sản. Hệ thống này giúp tìm giá khởi điểm cho một bất động sản dựa trên các biến đặc điểm của ngôi nhà. Bằng cách phá vỡ các khuôn mẫu thị trường và phạm vi giá trị trong quá khứ, kết hợp với những cải tiến về mặt kỹ thuật sẽ có thể dự đoán được giá trị trong tương lai. Việc này có nghĩa là dự đoán giá nhà ở Ames (Ames là một thành phố ở Quận Story, Iowa, Hoa Kỳ). Nó sẽ giúp khách hàng đưa các nguồn lực vào một yêu cầu mà không cần thông qua một nhà môi giới.
Ở đây chúng ta có một vấn đề: Yêu cầu một người mua nhà ở Ames, Iowa mô tả ngôi nhà mơ ước của họ, và họ có thể sẽ không bắt đầu với chiều cao của trần nhà hoặc khoảng cách với các siêu thị gần đó. Với những mô tả này, bạn bắt đầu dự đoán giá của ngôi nhà mơ ước này sẽ là bao nhiêu.

Dựa trên thông tin đó, chúng ta có thể thấy rằng chúng ta đang giải quyết vấn đề hồi quy: đưa ra một đầu vào bao gồm tất cả các đặc điểm về ngôi nhà, trả về giá của ngôi nhà như một đầu ra. Lần này, chúng ta sử dụng tập dữ liệu từ một cuộc thi trên Kaggle. Bộ dữ liệu này chứng minh rằng có nhiều sự ảnh hưởng nhiều hơn đến việc đàm phán giá so với số lượng phòng ngủ hoặc hàng rào màu trắng. Với 79 biến số mô tả (hầu hết) mọi khía cạnh của một ngôi nhà dân dụng, chúng ta sẽ dự đoán giá cuối cùng của mỗi ngôi nhà ở Ames. Sử dụng MSE (Mean squared error) giữa giá trị dự đoán và giá trị được quan sát thực làm chỉ số đo sự sai lệch, chúng ta muốn chỉ số này gần bằng 0. Đây là cách chúng ta đánh giá và chọn mô hình tốt nhất từ một loạt mô hình hồi quy với các tham số khác nhau. Mô hình có RMSE nhỏ nhất là mô hình cuối cùng của chúng ta.

Trong dự án này, chúng tôi sẽ thực hiện những việc sau:

    Tìm hiểu về tập dữ liệu thông qua các phân tích về dữ liệu bị thiếu, phân bố của dữ liệu đầu ra và độ tương quan giữa các đặc trưng.
    Xử lý các dữ liệu bị thiếu.
    Chuyển các biến hạng mục dưới sạng số sang biến hạng mục, bổ sung thêm biến mới.
    Mã hoá biến hạng mục sử dụng mã hóa số nguyên.
    Mã hóa các biến hạng mục còn lại sử dụng mã hóa one-hot.
    Co dãn và chuẩn hóa các đặc trưng dạng số.
    Sử dụng mô hình Lasso, phương pháp loại thuộc tính và thêm thuộc tính bằng đệ quy để lựa chọn thuộc tính cho bài toán.
    Sử dụng các mô hình cơ sở để lựa chọn ra mô hình phù hợp nhất.
    Tìm kiếm ra các bộ tham số tối ưu cho mô hình phù hợp nhất.
    Cải tiến các bước từ 2-6 để có một mô hình có độ chính xác cao hơn.
    Chạy dự đoán trên tập test, sau đó submit kết quả lên Kaggle.

