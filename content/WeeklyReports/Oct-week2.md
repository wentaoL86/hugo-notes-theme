This is the weekly report by Wentao from 2022/10/7  to  2022/10/14

## topics

- Gesture Generation
- Skin lesion classification

## details



### **Gesture Generation**

### 主要工作：

- [x] 这周主要在处理数据，调整阈值，修改模型。



后续计划：

- [ ] 继续增加数据集数量，调整标注信息
- [ ] 尝试调整检测算法，提高检测点的稳定性和数量
- [ ] 尝试多模态信息

### 训练详情：

使用了alphapose对中文线索语视频进行了标注，之后转成了通用的openpose格式，最终维度为3x136的向量，用json形式保存

语音部分采用wav文件进行存储，使用MFCC特征作为输入

文本部分采用textgrid格式进行存储

通过一个VAE来进行生成。



### 中文生成

目前使用了50个视频进行训练，约1-2w帧

目前使用中文线索语生成的视频相比之前要稳定一些，但是仍然有以下问题：



1.alphapose对于半身人体检测的body pose部分检测不准确，有一些帧存在检测不到的情况，导致标注的很多点的坐标为0

2.训练的数据量可能还是有些少，导致对有一部分点的预测不准确

3.有一些帧的质量太低，导致训练效果不佳

4.可能预测的点数量太多了，导致任务过于复杂



后续计划：

1.对训练数据进行一个预处理，对于检测点质量太低的图片进行筛除

2.进一步增加训练数据的数量和多样性

3.或许可以录一些全身的数据集

4.尝试使用其他数据的预训练模型进行迁移



### Skin lesion classification

### 主要工作：

- [x] 修改了ICASSP论文的论文abstract，introduction和method部分。
- [x] 完成了有关图结构的实验
- [x] 修改了框架图![image-20221014221811479](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221014221811479.png)

