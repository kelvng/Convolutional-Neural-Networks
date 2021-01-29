# Tìm Hiểu Convolutional Neural Networks Cho Phân Loại Ảnh

## Giới Thiệu
Convolutional Neural Networks (CNN) is one of the most popular and most influential deep learning models in the Computer Vision community. CNN is used in many problems such as image recognition, video analysis, MRI images, or for articles in the field of natural language processing, and most of them solve these problems well. <br/> <br/> CNN also has a long history. The original architecture of the CNN model was introduced by a Japanese computer scientist in 1980. Then, in 1998, Yan LeCun first trained the CNN model with the backpropagation algorithm for the handwriting recognition problem. . However, it wasn't until 2012, when Ukrainian computer scientist Alex Krizhevsky (filed by Geoffrey Hinton) built a CNN (AlexNet) model and used a GPU to speed up training deep nets to reach the top. 1 in the ImageNet annual Computer Vision competition with top 5 classification error reduced by more than 10% compared to previous traditional models, created a strong wave of using deep CNN with the help of GPUs to solve. more and more problems in Computer Vision.

## Image Classification 
Trong bài blog này, mình giới thiệu kiến trúc cụ thể của mô hình CNN cho bài toán phân loại ảnh. Phân loại ảnh là một bài toán quan trọng bậc nhất trong lĩnh vực Computer Vision. Chúng ta đã có rất nhiều nghiên cứu để giải quyết bài toán này bằng cách rút trích các đặc trưng rất phổ biến như SIFT, HOG rồi cho máy tính học nhưng những cách này tỏ ra không thực sự hiểu quả. Nhưng ngược lại, đối với con người, chúng ta lại có bản năng tuyệt vời để phân loại được những đối tượng trong khung cảnh xung quanh một cách dễ làm.

Dữ liệu đầu vào của bài toán là một bức ảnh. Một ảnh được biểu ảnh bằng ma trận các giá trị. Mô hình phân lớp sẽ phải dự đoán được lớp của ảnh từ ma trận điểm ảnh này, ví dụ như ảnh đó là con mèo, chó, hay là chim. 

<div class="img-div" markdown="0">
    <img src="/images/cnn_input.png" />
</div>

Để biểu diễn một bức ảnh 256x256 pixel trong máy tính thì ta cần ma trận sẽ có kính thước 256x256 chiều, và tùy thuộc vào bức ảnh là có màu hay ảnh xám thì ma trận này sẽ có số kênh tương ứng, ví dụ với ảnh màu 256x256 RGB, chúng ta sẽ có ma trận 256x256x3 để biểu diễn ảnh này. 

## Mối liên kết giữ CNN và thị giác
CNN có mối liên kết chặt chẽ với sinh học, cụ thể là của võ não thị giác, nơi xử lý thông tin liên quan đến hình ảnh từ các tế bào cảm thụ ánh sánh nằm ở mắt người. Năm 1962, 2 nhà thần kinh học người Mỹ là Hubel and Wiesel đã thực hiện thí nghiệm khám phá cách tổ chức của các tế bào não để xử lý thông tin thị giác và các tổ chức này đảm nhận nhiệm vụ nào. Trong [video](https://www.youtube.com/watch?v=Cw5PKV9Rj3o) này, các bạn có thể nghe được âm thanh đại diện cho các tế nào não phản ứng lại với các hình ảnh, góc cạnh, hướng của các đường thẳng xuất hiện trong video theo một trật tự nhất định. Điều này có nghĩ là mỗi neuron được thiết lập để phản ứng lại một số đặc điểm cố định của neuron đó.  
<div class="img-div" markdown="0">
    <img src="/images/cnn_visual_cortex.jpg" />
</div>


# Dataset
Các bạn có thể download tập dataset đã được xử lý tại [đây](https://drive.google.com/open?id=1ABhwNb5ioRzUEV9iLDpVSEIV_76yofNm) nhé

