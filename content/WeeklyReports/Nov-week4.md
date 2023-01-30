This is the weekly report by Wentao from 2022/11/18 to  2022/11/25

## topics

- Gesture Generation

## details



### **Gesture Generation**

### 主要工作：

- [x] 节奏模块实验
- [ ] 检测算法优化



### 节奏特征提取

我们用一段运动序列的平均偏移量来定义这段运动的节奏特征

![image-20221111141901541](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221111141901541.png)



![image-20221111141845359](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221111141845359.png)



M表示某一段运动序列，我们使用一个CNN网络来生成某段给定语音特征（MFCC特征）的运动节奏，得到运动的节奏之后和多模态动作进行合成



### 本周进度：

完成了节奏模块的性能测试，并复现了论文《Rhythmic Gesticulator: Rhythm-Aware Co-Speech Gesture Synthesis with Hierarchical Neural Embeddings》中的方法，这也是一个使用节奏特征的方法，通过音频分段来获取低层和高级特征，用底层特征控制节奏，高层特征控制风格。



![image-20221125142831214](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221125142831214.png)



### 实验结果

在PCK，FGD，PMB三个指标上进行了测试:



FGD(Fréchet Gesture Distance),衡量两段动作间的距离

PMB (percentage of matched beats), 如果一个运动节拍与附近音频节拍的时间距离小于阈值，则认为它匹配

![image-20221125142527400](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221125142527400.png)



下一步计划：优化检测算法，提高输入质量





### References

[1]Rhythmic Gesticulator: Rhythm-Aware Co-Speech Gesture Synthesis with Hierarchical Neural Embeddings
