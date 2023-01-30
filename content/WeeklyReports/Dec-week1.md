This is the weekly report by Wentao from 2022/11/25 to  2022/12/2

## topics

- Gesture Generation

## details



### **Gesture Generation**

### 主要工作：

- [x] 检测算法优化
- [ ] 数据处理



### 检测算法优化

将检测算法由alphapose改成了mediapipe

之前alphapose容易出现以下几个问题：

1.有时候会出现识别错误，躯干部分识别不准确

2.检测准确率不是很高，有一些帧会出现检测不出来的情况 

<img src="C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221202132912511.png" alt="image-20221202132912511" style="zoom:50%;" />



<img src="C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221202132939093.png" alt="image-20221202132939093" style="zoom:50%;" />



在修改了之后的结果：

<img src="C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221202133612060.png" alt="image-20221202133612060" style="zoom: 67%;" />

<img src="C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221202133711967.png" alt="image-20221202133711967" style="zoom: 67%;" />

基本解决了之前存在的问题，手部检测更加准确，且有效帧更多。但是似乎躯干存在不完整的情况，或许可以进行一个固定坐标的补全



由于目前常用的关键点模型还是openpose，我们暂时也用不到这么多关键点（543=468+42+33），所以在得到mediapipe关键点之后进行了处理，提取了部分关键点，转换为了openpose的数据格式



### Q语通反向的难点以及模板匹配方法的不足：

#### 模板匹配方法的不足：

##### 应用层面

- 难以进行个性化与多样性的生成
- 难以匿名化也可能会造成隐私问题

##### 方法层面

- 拼接的方法容易造成不够流畅的问题
- 对于手势转换的情况，拼接的方法不合理



### Q语通反向的难点：

- 需要同时生成脸部，身体，手部的姿态（目前Q语通没有同时生成三个部位的工作）
- 由于需要生成虚拟化和个性化的姿态，使用GAN直接生成图像不太合理，所以最好使用生成关键点姿态的方法
- 为了表达效果，需要产生流畅，富有节奏型的姿态
- 由于编码系统的规定，需要生成位置较为准确的姿态（例如手语只要有大概的象形意思就可以）









### References

[1]Mediapipe     https://github.com/ntu-rris/google-mediapipe
