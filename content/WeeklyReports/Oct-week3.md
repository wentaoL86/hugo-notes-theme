This is the weekly report by Wentao from 2022/10/7  to  2022/10/14

## topics

- Gesture Generation
- Skin lesion classification

## details



### **Gesture Generation**

### 主要工作：

- [x] 这周主要在进行文本特征的处理



后续计划：

- [ ] 继续增加数据集数量，调整标注信息
- [ ] 尝试调整检测算法，修改模型标准，提高检测点的稳定性和数量

### 模型详情：

新增一个text-encoder进行文本信息的编码，在得到文本特征之后和语音特征进行融合



### 文本特征

利用一个中文的word2vec来进行从中文到词向量的编码，通过一个编码器得到文本特征和语音特征进行融合

参考了https://github.com/liuhuanyong/ChineseEmbedding的方法进行尝试：

使用中文维基百科(zhiwiki)作为训练语料来源.

![image-20221021141734178](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221021141734178.png)

![image-20221021141812369](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221021141812369.png)

![image-20221021141821748](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221021141821748.png)

![image-20221021141831371](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221021141831371.png)























### Skin lesion classification

### 主要工作：

- [x] 修改了ICASSP论文的论文abstract，introduction和method部分。
- [x] 完成了有关图结构的实验
- [x] 修改了框架图![image-20221014221811479](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20221014221811479.png)

