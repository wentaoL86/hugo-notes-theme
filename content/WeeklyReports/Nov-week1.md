This is the weekly report by Wentao from 2022/10/28 to  2022/11/4

## topics

- Gesture Generation
- Stable Diffusion aniamtion

## details



### **Gesture Generation**

### 主要工作：

- [x] 中文拼音词向量的训练
- [x] 文本特征的处理
- [x] 文本特征和音频特征的融合



### 具体细节：

经过调研之后发现没有现成可用的拼音词向量（只有字和词的），所以需要自己训练一个



### 中文拼音word2vec训练

想要训练好word2vec模型，一份高质量的中文语料库是必要的，目前常用质量较好的中文语料库为维基百科的中文语料库，对得到的语料库进行了进一步处理（Wiki语料库中的文档含有繁体中文，利用工具包opencc将繁体转换为简体；去掉了其中的空格和英语）

将得到的中文语料库转换为拼音，使用python的gensim模块提供的word2vec函数进行训练，得到中文拼音的word2vec. 目前定义的word embedding的维度是300



### 文本特征提取

由于我们拥有text.grid形式的文本标注，所以可以得到每一帧对应的音素。这里进行了一个处理因为训练的拼音word2vec是针对音节的（单个音素由于维度太低没办法做词向量）而我们得到的标注是单个因素的。

这里采用音频标注进行了一个分段，对于一个字所对应的所有音素，我们把这一段间隔内的所有音素组成的音节作为这一段间隔的标注。（比如15-20帧对应w，20-25帧对应o，就处理成15-25帧对应wo，这样才能处理）。对于没有标注的间隔部分处理为0

得到的一个视频的词向量维度为（帧数x300，也就是100帧的视频就是一个100x300的词向量，和音频特征在帧数维度是对齐的，音频特征使用的是MFCC特征，维度是帧数x13，在帧数这个维度是对齐的）

为了进一步提取文本特征的信息，使用一个TCN网络来进行文本特征的编码，目前设计的网络得到的是13维的特征，也就是最后的特征也是（维度为帧数x13）的特征，和音频特征对应，这部分后期可能还需要根据具体效果修改



### 文本特征和音频特征的融合

目前采用的是在特征层面进行一个concat，因为两者的特征维度都是（13x帧数），所以融合之后得到的是一个26x帧数的特征，直接进行特征的拼接。



### **diffusion model animation**



这是MMLab最近的一篇用diffusion model来进行基于文本的动作生成的论文，我正在尝试复现

<img src="https://mingyuan-zhang.github.io/static/images/MotionDiffuse/pipeline.png" alt="img" style="zoom: 33%;" />



这是第一个基于扩散模型的文本驱动运动生成框架，它的优点优点：

（1）它不是一个确定的语言-运动映射，而是通过一系列的去噪步骤来生成运动，其中注入了变化。

（2）合成效果较为真实，MotionDiffuse擅长建模复杂的数据分布和生成生动的运动序列。可以进行进行任意长度的运动合成

（3）较为稳定和可控



和我们的工作的对比和借鉴点：

1.无法直接使用预训练模型，我们可能要重新训练动作和文本的特征提取器

2.动作比较简单，没有脸部表情

3.可以借鉴这种diffusion model的思路





### **References**

[1]MotionDiffuse: Text-Driven Human Motion Generation with Diffusion Model
Mingyuan Zhang*,  Zhongang Cai*,  Liang Pan,  Fangzhou Hong,  Xinying Guo,  Lei Yang,  Ziwei Liu





















