This is the weekly report by Wentao from 2022/09/16  to  2022/09/23

## topics

- Gesture Generation
- stable diffusion animation

## Reading list 

- **两篇多模态的Geture generation论文**

[1]Speech Gesture Generation from the Trimodal Context of Text, Audio, and Speaker Identity 

[2]Evaluation of text-to-gesture generation model using convolutional neural network

- **skin lesion classification**

[1]Neighbor Matching for Semi-supervised Learning

[2]Semi-supervised classification of radiology images with NoTeacher: A Teacher that is not Mean

[3]Semi-supervised Medical Image Classification with Global Latent Mixing

## details



### **Gesture Generation**

### 主要工作：

- [x] 给部分视频生成了关键点注释
- [x] 搭建了数据处理模块
- [x] 了解了multi-modal encoder的论文，为后面添加文本特征（多模态）做准备

下周计划：

- [ ] 完成数据载入模块，用我们中文线索语数据集尝试进行生成
- [ ] 尝试进行多模态输入

### 标注详情：

标注了部分视频信息，预计下周全部标注完，得到一个带完整的关键点位置标注的数据集。

共有136个关键点信息，包括脸部，身体，手部。包括三个维度（x坐标，y坐标，深度），最终维度为3x136的向量，用json形式保存

特征点情况：

身体：26个关键点

<img src="https://www.stubbornhuang.com/wp-content/uploads/2021/06/wp_editor_md_8b60abe0636eee8925dfa737317b832b.jpg" alt="姿态估计 – Halpe Full-Body136数据集骨骼关节keypoint标注对应-StubbornHuang Blog" style="zoom: 33%;" />

脸部：68个关键点

<img src="https://www.stubbornhuang.com/wp-content/uploads/2021/06/wp_editor_md_d9e5881e959945f985e6549a057d092f.jpg" alt="姿态估计 – Halpe Full-Body136数据集骨骼关节keypoint标注对应-StubbornHuang Blog" style="zoom: 33%;" />

手部：21个关键点（两只手一起42个关键点）

<img src="https://www.stubbornhuang.com/wp-content/uploads/2021/06/wp_editor_md_a665c915d85335372c425c2ea7040183.jpg" alt="姿态估计 – Halpe Full-Body136数据集骨骼关节keypoint标注对应-StubbornHuang Blog" style="zoom:33%;" />

### stable diffusion animation

参考了references中的DeforumStableDiffusionLocal项目在本地进行了部署,

通过设置镜头和某些帧的图片可以生成动画，如zoom和angle可以控制镜头的远近和角度

通过在不同帧之间进行连续的插入可以保证生成动画的连续性。

正在进行进一步尝试，下次的周报会具体报告

![image-20220923201941622](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220923201941622.png)

<video src="G:\program\DeforumStableDiffusionLocal\output\2022-09\Example_DGSpitzer\20220923201725.mp4"></video>



<video src="C:\Users\41885\Downloads\Video\nateraw_stable-diffusion-videos：通过探索潜在空间和文本提示之间的变形来创建具有稳定扩散的 🔥 视频.mp4"></video>



## references

[1]https://github.com/HelixNGC7293/DeforumStableDiffusionLocal

[2]https://github.com/nateraw/stable-diffusion-videos