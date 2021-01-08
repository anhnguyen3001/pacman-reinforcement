# pacman-reinforcement
- Câu 1:
  - Sử dụng công thức Bellman
    - Hàm computeQValueFromValues: tính Q*
    - Hàm computeActionFromValues: tính V*
    
  <img src="./bellman equation.PNG"/>
- Câu 2:
  - Cập nhật noise: noise/=2 => Đến khi thành công
- Câu 3:
- Câu 4:
- Câu 5:
- Câu 6:
- Câu 7:
- Câu 8:
  - Với hàm getQValue:
    + Lấy ra feature vector, loop trên đó tính theo công thức:
    <img src="./q8-qfunction.PNG"/>
  - Với hàm update:
    + Tính difference theo công thức dưới
    + Lấy ra feature vector, loop trên đó cập nhật weight:
    <img src="./q8-updatefunction.PNG"/>
