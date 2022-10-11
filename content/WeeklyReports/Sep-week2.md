---
title: Aug-week4
linktitle: Aug-week4
type: book
date: '2019-05-05T00:00:00+01:00'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

This is the weekly report by Wentao from 2022/09/6  to  2022/09/15

## topics

- Gesture Generation
- skin lesion classification

## Reading list 

- **Geture generation**

[1]Free-form Body Motion Generation from Speech

- **skin lesion classification** 

[1]Soft-Attention Improves Skin Cancer Classification Performance

[2]Cats, not CAT scans: a study of dataset similarity in transfer learning for 2D medical image classification

[3]MT-TransUNet: Mediating Multi-Task Tokens in Transformers for Skin Lesion Segmentation and Classification

## details



### **Gesture Generation**

### 主要工作：

- [x] 搜集整理了数据集【done】
- [ ] 部署了几个SLP(sign language production)和co-speech生成的项目【ongoing】
- [x] 实现了一个co-speech生成的pipeline，生成了关键点动画【done】
- [ ] 确定了主要的框架和方法、模型

下周计划：

- [ ] 给数据集增加关键点注释信息
- [ ] 完成数据载入模块，用我们中文线索语数据集尝试进行生成



### 数据集：

目前用于生成的数据集包括：

**手语：**

ISL数据集(印度语)

ASL数据集（英语）

**Co-speech：**

Trinty gesture 数据集（英语）

PHOENIX-14T（德语）

Speech2Gesture(英语)

Ted Gesture dataset (英语)

都已经搜集和归类完成



### 框架：

基于论文“Free-form Body Motion Generation from Speech” 搭建了一个基于语音特征的生成框架，目前已经在英语数据集上跑通

生成效果：

<img src="C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220915231523711.png" alt="image-20220915231523711" style="zoom: 50%;" />



目前正在给我们的中文线索语数据集建立关键点标注，后续会用我们的数据集做生成实验

### **skin lesion classification**

主要工作：

- [x] 了解了skin lesion classification的分类依据【done】
- [x] 整理了数据集的分布和特点【done】
- [x] 画了分类的特征矩阵，寻找模型的瓶颈【done】
- [ ] 整理了ICASSP论文，在修改方法和重新画图（对之前的图有一点不满意）【ongoing】
- [ ] 调研了几篇新的skinlesion的文章【ongoing】



#### ISIC2018数据集分布：

数量：

Melanoma（黑素瘤）: 1113 

Melanocytic nevus（色素痣）: 6705

Basal cell carcinoma（基底细胞癌）: 514

Actinic keratosis（光化角质病）: 327

Benign keratosis（良性角质病）: 1099

Dermatofibroma（皮肤纤维瘤）: 115

Vascular lesion（血管损害）: 142

测试集：

Melanoma（黑素瘤）: 227

Melanocytic nevus（色素痣）: 1341

Basal cell carcinoma（基底细胞癌）: 108

Actinic keratosis（光化角质病）: 68

Benign keratosis（良性角质病）: 203

Dermatofibroma（皮肤纤维瘤）: 24

Vascular lesion（血管损害）: 32



**confusion matrix**

   [73,     **97**,    11,  21,  18,  3,  4],

​    [ 15, 1286,  13,   6,    17,  0,  4],

​    [  0,    15,     83,  8,     1,    1,  0],

​    [  2,     9,      **17,**  32,   7,    1,  0],

​    [  8,    **51,**    16,  18,  107,  3,  0],

​    [  1,    3,       0,    4,      4,   12,  0],

​    [  0,    6,       0,    0,      0,   0,  26]],



**AUROC:**

 **Melanoma:0.851212** 

Melanocytic nevus:0.927263 

Basal cell carcinoma:0.964771 

**Actinic keratosis:0.927329** 

**Benign keratosis:0.903610** 

Dermatofibroma:0.926794 

Vascular lesion:0.983939

主要瓶颈在于Melanoma、Actinic keratosis和Benign keratosis



可能原因：

1.Melanocytic nevus的样本数量太多了，导致学到的特征偏向这一类，导致其他类的sensitivity比较低（加上不平衡问题的方法）

2.了解了一些皮肤病的判别方法之后，其中有一些类的图片特征是很相似的，可能需要细粒度分类（细粒度处理）



### **skin lesion classification**

主要工作：

复现了Neighbor Matching for Semi-supervised Learning

Semi-supervised classification of radiology images with NoTeacher: A Teacher that is not Mean的方法



目前正在进行相关方法的实验

## references

[1]https://github.com/TheTempAccount/Co-Speech-Motion-Generation
