This is the weekly report by Wentao from 2022/09/24  to  2022/09/30

## topics

- Gesture Generation
- stable diffusion animation

## details



### **Gesture Generation**

### 主要工作：

- [x] 这周主要在修改代码和进行数据处理的工作，完成了数据载入模块，用我们中文线索语数据集尝试进行了生成



后续计划：

- [ ] 增加数据集数量，调整标注信息
- [ ] 尝试进行多模态输入

### 训练详情：

使用了alphapose对中文线索语视频进行了标注，之后转成了通用的openpose格式，最终维度为3x136的向量，用json形式保存

语音部分采用wav文件进行存储，使用MFCC特征作为输入

文本部分采用textgrid格式进行存储

通过一个VAE来进行生成。



### 中文生成

目前使用中文线索语生成的视频十分不稳定，主要分析有以下原因：

1.alphapose对于半身人体检测的body pose部分检测不准确，有一些帧存在检测不到的情况

2.目前使用的训练数据的数量比较少

下周会针对这部分问题进行改进，提高生成效果

![image-20220930224958832](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220930224958832.png)







### stable diffusion animation

进一步尝试了Deforum Stable Diffusion的几种动画模式：

### 动画模式：

● animation mode包括none,2D,3D,Video Input, Interpolation几个选择：

● NONE模式，按照提示列表的规定输出一批相互不相关的连贯图像。要生成的图像数量在后面的batches下的单元格中定义。

● 2D动画生成：根据预定好的某些帧的prompt生成。 2D 模式将尝试将在一系列连贯输出中产生的图像串起来。要创建的输出图像的数量由“maxframes”定义。控制 2D 模式的运动算子如下：边框、角度、缩放、translation_x、translation_y、noise_schedule、 contrast_schedule、
color_coherence、diffusion_cadence 和保存深度图”。其他动画参数在 2D 模式下无效。Resume_from_timestring 在 2D 模式下可用。

● 3D动画生成，选择后将忽略“无模式”提示，并参考前面带有帧号的计划提示。 3D 模式将尝试将在一系列连贯输出中生成的图像串起来。要创建的输出图像的数量由“max_frames”定义。控制 3D 模式的运动算子如下：“Border、translation_x、translation_y、rotation_3d_x、rotation_3d_y、rotation_3d_z、noise_schedule、contrast_schedule、color_coherence、diffusion_cadence、3D depthwarping、midas_weight、fov、padding_mode、sampling_mode 和 save_depth_map。Resume_from_timestring 在 3D 模式下可用。 

● video_input视频输入， 选中后将尝试根据输入的视频，由video_init_path 指定。参考之前带有帧数的prompt。在 video_input 模式下，“Max_frames”被忽略，而是跟随从视频长度中提取的帧数。笔记本会将视频中的图像作为引导来生成视频。

●Interpolation插值， 选中后，尝试在列出的动画提示之间混合输出帧。如果 interpolate_key_frame 模式被选中，输出帧的数量将遵循prompt list

### 其他参数：

●角度的度数：顺时针/逆时针旋转画布
●缩放，2D 运算符缩放画布大小，乘法[static = 1.0]
● translation_x，2D 和 3D以每帧像素为单位向左/向右移动画布
● translate_y，以每帧像素为单位向上/向下移动画布的
● translate_z，用于将画布移向/远离视图的 3D 操作符 [由 FOV 设置的速度]
● rotation_x，3D 操作符到向上/向下倾斜画布，以每帧角度为
● rotation_y，以每帧角度为单位向左/向右平移画布的
● roation_z用于顺时针/逆时针滚动画布的 3D 操作
● contrast schedule，调整 t每帧的整体对比度 [默认中性为 1.0]



### 运行原理：

![image-20220930231604739](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220930231604739.png)

在上面的示例中，我们有两组提示：

上面的静止帧 *prompts* 和下面的动画提示。

**在“NONE”动画模式**下，扩散将寻找最上面的一组提示来生成图像。在所有其他模式下（2D、3D 等），扩散将参考下面的的prompts。仔细注意这些提示的语法对于能够运行扩散至关重要。
对于静止帧图像输出，数字不要放在提示符前面，因为在一批图像期间不需要“调度”。上述提示将生成并显示森林图像和女性的单独图像，作为输出。



**在 2D//3D 动画运行期间**，将按指定引用带有帧数的prompt。在上面的示例中，我们从第 0帧开始：  生成了一个苹果图像。随着帧的进展，它仍然是一个苹果输出，直到第 20 帧出现，此时扩散现在将被引导开始包括一个香蕉作为主要主题，最终取代以前不再引用的苹果。



**Interpolation插值模式**将以这样一种方式“补间”提示，首先，从提示列表中生成一张图像。将画出一个苹果、香蕉、椰子和榴莲。然后扩散开始绘制应该存在于提示之间的框架，制作苹果和香蕉的混合体 - 然后继续填补香蕉和椰子之间的空白，最后解决并停止在最后一个榴莲图像上，作为它的最终帧。



## references

[1]https://github.com/HelixNGC7293/DeforumStableDiffusionLocal

[2]https://github.com/nateraw/stable-diffusion-videos

[3]https://github.com/TheTempAccount/Co-Speech-Motion-Generation