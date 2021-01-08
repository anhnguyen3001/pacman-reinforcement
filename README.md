# pacman-reinforcement
- Câu 1:
  - Sử dụng công thức Bellman
    - Hàm computeQValueFromValues: tính Q*
    - Hàm computeActionFromValues: tính V*
    
  <img src="./bellman equation.PNG"/>
- Câu 2:
  - Cập nhật noise: noise/=2 => Đến khi thành công
- Câu 3:
  - close exit, risk the cliff: Giảm noise < 0.2
  - distant exit, risk the cliff: Tăng discount
  - distant exit, avoid the cliff: Tăng noise
- Câu 4:
  - Hàm init: values có cấu trúc dữ liệu Counter
  - Hàm getQValue: trả về giá trị của (state, action)
  - Hàm computeValueFromQValues:
    + Nếu không còn action return 0.0
    + Loop trên các action có thể từ state hiện tại
    + Lưu giá trị của từng action
    + Return giá trị max
  - Hàm computeActionFromQValues: Tương tự hàm computeValueFromQValues, tìm ra action có giá trị max 
  - Hàm update:
    + Update value của state, action bằng công thức dưới
    + Nếu kết thúc: không cần + phần discount
    <img src="./q4-updatefunction.PNG"/>
- Câu 5:
  - Ý tưởng: Lấy r = số random nếu:
    - r < epsilon: lấy random action từ list legalAction (exploration)
    - r >= epsilon:  lấy action tốt nhất (exploitation)
- Câu 6: 
  - Không thể
- Câu 8:
  - Với hàm getQValue:
    + Lấy ra feature vector, loop trên đó tính theo công thức:
    <img src="./q8-qfunction.PNG"/>
  - Với hàm update:
    + Tính difference theo công thức dưới
    + Lấy ra feature vector, loop trên đó cập nhật weight:
    <img src="./q8-updatefunction.PNG"/>
- Autograder:
  <img src="./autograder.PNG"/>
  