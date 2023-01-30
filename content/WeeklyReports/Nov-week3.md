This is the weekly report by Wentao from 2022/11/11 to  2022/11/18

## topics

- Gesture Generation
- ACM MM Paper

## details



### **Gesture Generation**

### 主要工作：

- [x] 节奏特征的提取和生成
- [ ] 检测算法的优化
- [ ] 姿态生成论文调研



### 节奏特征提取

我们用一段运动序列的平均偏移量来定义这段运动的节奏特征

![image-20221111141901541](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221111141901541.png)



![image-20221111141845359](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221111141845359.png)



M表示某一段运动序列，我们使用一个CNN网络来生成某段给定语音特征（MFCC特征）的运动节奏，得到运动的节奏之后和多模态动作进行合成



本周完成了节奏模块的代码，正在进行测试，预计下周先完成：（1）PCK指标测试（2）坐标曲线的测试



##### 调研了两篇姿态生成的论文

##### 第一篇：Rhythmic Gesticulator: Rhythm-Aware Co-Speech Gesture Synthesis with Hierarchical Neural Embeddings

2022年10月份北大提出的一种新的Co-speech合成方法，该方法在节奏和语义上都取得了不错的结果。

对于节奏，他们使用一个包含一个鲁棒的基于节奏的分割pipeline，以确保声音和手势之间明确的时间一致性。

对于手势语义，他们基于语言理论设计了一种有效地分离语音和动作的低级和高级神经表示的机制。

高级表示对应语义，而低级表示涉及微妙的变化。最后，在语音和动作的多层表示上，产生有节奏和语义的姿态。

用现有的客观指标、新提出的节奏指标和人类反馈进行的评估表明，我们的方法明显优于最先进的系统。

##### 参考：

- 目前有开源仓库，但是还没有代码。
- 提出了一个新的节奏检测标准：PMB (percentage of matched beats), 如果一个运动节拍与附近音频节拍的时间距离小于阈值，则认为它匹配、
- 他们也用一个分支来提取节拍信息，但是和我们所用的思路很不一样，他们是先分割成block再做节奏的匹配



##### 第二篇：ZeroEGGS: Zero-shot Example-based Gesture Generation from Speech

##### 简介：

2022年8月份育碧公司提出的一个用于零样本风格控制的语音驱动姿态生成的神经网络框架ZeroEGGS。

风格可以通过一个示范动作来控制，在训练中不用到动作风格。

模型使用变分框架来学习样式表示，使得通过潜在空间操作或样式表示的混合来修改样式变得容易。

框架的概率性质进一步允许在给定相同输入的情况下生成各种输出，解决手势运动的随机性质。

实验中展示了模型对新的说话者和风格的灵活性和普遍性。主观测试中展示了模型在运动的自然性、讲话的适当性和风格刻画方面优于先前的最先进技术。最后，发布了一个高质量的全身姿态动作数据集，包括手部和语音，跨越19种不同的风格

代码可以在https://github.com/ubisoft/ubisoft-laforge-ZeroEGGS上公开获取。

##### 参考：

- 有开源代码和数据
- 使用的是VAE框架
- 用一个init动作来控制风格









