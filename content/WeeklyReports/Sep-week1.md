---
title: Aug-week4
linktitle: Aug-week4
type: book
date: '2019-05-05T00:00:00+01:00'
# Prev/next pager order (if `docs_section_pager` enabled in `params.toml`)
weight: 2
---

This is the weekly report by Wentao from 2022/08/23  to  2022/09/05

## topics

- Diffusion model
- Gesture Generation
- stable diffusion
- skin lesion classification

## Reading list (some papers are briefly reviewed)

- **Diffusion model**

[1] A DIFFUSION GENERATED METHOD FOR ORTHOGONAL MATRIX-VALUED FIELDS

[2] The iterative convolutionâ€“thresholding method (ICTM) for image segmentation

[3] DIFFUSION GENERATED METHODS FORDENOISING TARGET-VALUED IMAGES

[4] High-Resolution Image Synthesis with Latent Diffusion Models

[5]Hierarchical Text-Conditional Image Generation with CLIP Latents

- **Geture generation**

[1] Towards Automatic Speech to Sign Language Generation

[2] ANONYSIGN: Novel Human Appearance Synthesis for Sign 

[3] Speech Drives Templates: Co-Speech Gesture Synthesis with Learned Templates 

[4] Speech Gesture Generation from the Trimodal Context of Text, Audio, and Speaker Identity

[5] Text2video: text-driven talking-head video synthesis with personalized phoneme - pose dictionary

[6] SEEG: Semantic Energized Co-speech Gesture Generation 

[7] SignPose: Sign Language Animation Through 3D Pose Lifting

[8] Gesture2Vec: Clustering Gestures using Representation Learning Methods for Co-speech Gesture Generation

[9] Evaluation of text-to-gesture generation model using convolutional neural network

[10] Everybody Sign Now: Translating Spoken Language to Photo Realistic Sign Language Video

[11] Progressive Transformers for End-to-End Sign Language Production

[12] Modeling Intensification for Sign Language Generation: A Computational Approach

[13] Can Everybody Sign Now? Exploring Sign Language Video Generation from 2D Poses

[14] Analyzing Input and Output Representations for Speech-Driven Gesture Generation

[15] Learning Hierarchical Cross-Modal Association for Co-Speech Gesture Generation

- **skin lesion classification** 

[1] Unsupervised and semi-supervised learning with Categorical Generative Adversarial Networks assisted by Wasserstein distance for dermoscopy image Classification
[2] Skin lesion classification with ensemble of squeeze-and-excitation networks and semi-supervised learning
[3]Semi-supervised medical image classification with relation-driven self-ensembling model
[4]Leveraging undiagnosed data for glaucoma classification with teacher-student learning
[5]Semi-weakly supervised learning for prostate cancer image classifi cation with teacher-student deepconvolutional networks

[6] Federated Semi-supervised Medical Image Classifi cation via Inter-client Relation Matching. In MICCAI2021.
[7] FedPerl: Semi-Supervised Peer Learning for Skin Lesion Classification. In MICCAI2021.
[8] Neighbor Matching for Semi-supervised Learning. In MICCAI2021.
[9] Semi-supervised Classifi cation of Diagnostic Radiographs with NoTeacher: A Teacher that is Not Mean. 
[10] Semi-supervised Medical Image Classifi cation with Global Latent Mixing. In MICCAI2020.
[11]Weakly supervised deep learning for thoracic diseaseclassifi cation and localization on chest x-rays. ACM BCB 2018.Yan, C., Yao, J., Li, R., Xu, Z. and Huang, J.  



## details

### **Diffusion model**

čŻ´ĺ?°ć‰©ć•Łć¨ˇĺž‹ďĽŚä¸€č?¬çš„ć–‡ç« é?˝äĽšćŹ?ĺ?°č?˝é‡Źć¨ˇĺž‹ďĽ?Energy-based ModelsďĽ‰ă€?ĺľ—ĺ?†ĺŚąé…ŤďĽ?Score MatchingďĽ‰ă€?ćś—äą‹ä¸‡ć–ąç¨‹ďĽ?Langevin EquationďĽ‰ç­‰ç­‰ďĽŚç®€ĺŤ•ćťĄčŻ´ďĽŚć?Żé€ščż‡ĺľ—ĺ?†ĺŚąé…Ťç­‰ćŠ€ćśŻćťĄč®­ç»?č?˝é‡Źć¨ˇĺž‹ďĽŚç„¶ĺ?Žé€ščż‡é?Žäą‹ä¸‡ć–ąç¨‹ćťĄć‰§čˇŚä»Žč?˝é‡Źć¨ˇĺž‹çš„é‡‡ć ·ă€‚

ä»Žç?†č®şä¸ŠćťĄč®˛ďĽŚčż™ć?Żä¸€ĺĄ—ĺľ?ć??ç†źçš„ć–ąćˇ?ďĽŚĺŽźĺ?™ä¸ŠĺŹŻä»Ąĺ®žçŽ°ä»»ä˝•čżžç»­ĺž‹ĺŻąč±ˇďĽ?čŻ­éźłă€?ĺ›ľĺ?Źç­‰ďĽ‰çš„ç”źć??ĺ’Śé‡‡ć ·ă€‚ä˝†ä»Žĺ®žč·µč§’ĺş¦ćťĄçś‹ďĽŚč?˝é‡Źĺ‡˝ć•°çš„č®­ç»?ć?Żä¸€ä»¶ĺľ?č‰°éšľçš„äş‹ć?…ďĽŚĺ°¤ĺ…¶ć?Żć•°ćŤ®ç»´ĺş¦ćŻ”čľ?ĺ¤§ďĽ?ćŻ”ĺ¦‚é«?ĺ?†čľ¨çŽ‡ĺ›ľĺ?ŹďĽ‰ć—¶ďĽŚĺľ?éšľč®­ç»?ĺ‡şĺ®Śĺ¤‡č?˝é‡Źĺ‡˝ć•°ćťĄďĽ›ĺŹ¦ä¸€ć–ąéť˘ďĽŚé€ščż‡ćś—äą‹ä¸‡ć–ąç¨‹ä»Žč?˝é‡Źć¨ˇĺž‹çš„é‡‡ć ·äąźćś‰ĺľ?ĺ¤§çš„ä¸Ťçˇ®ĺ®šć€§ďĽŚĺľ—ĺ?°çš„ĺľ€ĺľ€ć?Żĺ¸¦ćś‰ĺ™ŞĺŁ°çš„é‡‡ć ·ç»“ćžśă€‚ć‰€ä»Ąĺľ?é•żć—¶é—´ä»ĄćťĄďĽŚčż™ç§ŤäĽ ç»źč·Żĺľ„çš„ć‰©ć•Łć¨ˇĺž‹ĺŹŞć?Żĺś¨ćŻ”čľ?ä˝Žĺ?†čľ¨çŽ‡çš„ĺ›ľĺ?Źä¸Šĺ?šĺ®žéŞŚă€‚

ĺ¦‚ä»Šç”źć??ć‰©ć•Łć¨ˇĺž‹çš„ĺ¤§ç?«ďĽŚĺ?™ć?Żĺ§‹äşŽ2020ĺą´ć‰€ćŹ?ĺ‡şçš„[DDPM](https://link.zhihu.com/?target=https%3A//arxiv.org/abs/2006.11239)**ďĽ?Denoising Diffusion Probabilistic ModelďĽ‰ďĽŚč™˝ç„¶äąźç”¨äş†â€ść‰©ć•Łć¨ˇĺž‹â€ťčż™ä¸Şĺ?Ťĺ­—ďĽŚä˝†äş‹ĺ®žä¸Šé™¤äş†**é‡‡ć ·čż‡ç¨‹**çš„ĺ˝˘ĺĽŹćś‰ä¸€ĺ®šçš„ç›¸äĽĽäą‹ĺ¤–ďĽŚDDPMä¸ŽäĽ ç»źĺźşäşŽćś—äą‹ä¸‡ć–ąç¨‹é‡‡ć ·çš„ć‰©ć•Łć¨ˇĺž‹ĺŹŻä»ĄčŻ´ĺ®Śĺ…¨ä¸Ťä¸€ć ·ďĽŚčż™ĺ®Śĺ…¨ć?Żä¸€ä¸Şć–°çš„čµ·ç‚ąă€?ć–°çš„çŻ‡ç« ă€‚

ĺ‡†çˇ®ćťĄčŻ´ďĽŚDDPMĺŹ«â€ś**ć¸?ĺŹ?ć¨ˇĺž‹**â€ťć›´ä¸şĺ‡†çˇ®ä¸€äş›ďĽŚć‰©ć•Łć¨ˇĺž‹čż™ä¸€ĺ?Ťĺ­—ĺŹŤč€Śĺ®ąć?“é€ ć??ç?†č§Łä¸Šçš„čŻŻč§ŁďĽŚäĽ ç»źć‰©ć•Łć¨ˇĺž‹çš„č?˝é‡Źć¨ˇĺž‹ă€?ĺľ—ĺ?†ĺŚąé…Ťă€?ćś—äą‹ä¸‡ć–ąç¨‹ç­‰ć¦‚ĺżµďĽŚĺ…¶ĺ®žč·źDDPMĺŹŠĺ…¶ĺ?Žç»­ĺŹ?ä˝“é?˝ć˛ˇä»€äą?ĺ…łçł»ă€‚ćś‰ć„Źć€ťçš„ć?ŻďĽŚDDPMçš„ć•°ĺ­¦ćˇ†ćž¶ĺ…¶ĺ®žĺś¨ICML2015çš„č®şć–‡[ă€ŠDeep Unsupervised Learning using Nonequilibrium Thermodynamicsă€‹](https://link.zhihu.com/?target=https%3A//arxiv.org/abs/1503.03585)ĺ°±ĺ·˛ç»Źĺ®Ść??äş†ďĽŚä˝†DDPMć?Żé¦–ć¬ˇĺ°†ĺ®?ĺś¨é«?ĺ?†čľ¨çŽ‡ĺ›ľĺ?Źç”źć??ä¸Šč°?čŻ•ĺ‡şćťĄäş†ďĽŚä»Žč€ŚĺĽ•ĺŻĽĺ‡şäş†ĺ?Žéť˘çš„ç?«ç?­ă€‚ç”±ć­¤ĺŹŻč§?ďĽŚä¸€ä¸Şć¨ˇĺž‹çš„čŻžç”źĺ’Śćµ?čˇŚďĽŚĺľ€ĺľ€čż?éś€č¦?ć—¶é—´ĺ’Śćśşé?‡.

### **ć‹†ćĄĽĺ»şćĄĽ**ďĽš

ĺ®žé™…ä¸ŠďĽŚç›¸ćŻ”äşŽäĽ ç»źçš„ć‰©ć•Łć¨ˇĺž‹ďĽŚDDPMĺ®žé™…ä¸Šć›´ĺ?ŹVAEč€Śä¸Ťć?Żć‰©ć•Łć¨ˇĺž‹ďĽ?ç”±äşŽçŻ‡ĺą…ĺ·˛ç»Źĺľ?é•żäş†ďĽŚVAEé?¨ĺ?†ĺ°±ä¸Ťĺ?šä»‹ç»Ťäş†ďĽ‰ă€‚ĺľ?ĺ¤šć–‡ç« ĺś¨ä»‹ç»ŤDDPMć—¶ďĽŚä¸ŠćťĄĺ°±ĺĽ•ĺ…Ąč˝¬ç§»ĺ?†ĺ¸?ďĽŚćŽĄçť€ĺ°±ć?ŻĺŹ?ĺ?†ćŽ¨ć–­ďĽŚä¸€ĺ †ć•°ĺ­¦č®°ĺŹ·ä¸‹ćťĄďĽŚĺ…?ĺ?“č·‘äş†ä¸€çľ¤äşşďĽŚĺ†ŤĺŠ äą‹äşşä»¬ĺŻąäĽ ç»źć‰©ć•Łć¨ˇĺž‹çš„ĺ›şćś‰ĺŤ°č±ˇďĽŚć‰€ä»Ąĺ°±ĺ˝˘ć??äş†â€śéś€č¦?ĺľ?é«?ć·±çš„ć•°ĺ­¦çźĄčŻ†â€ťçš„é”™č§‰ă€‚äş‹ĺ®žä¸ŠďĽŚDDPMäąźĺŹŻä»Ąćś‰ä¸€ç§Ťĺľ?â€śĺ¤§ç™˝čŻťâ€ťçš„ç?†č§ŁďĽŚĺ®?ĺą¶ä¸ŤćŻ”ćś‰çť€â€śé€ ĺ?‡-é‰´ĺ?«â€ťé€šäż—ç±»ćŻ”çš„GANć›´éšľă€‚

é¦–ĺ…?ďĽŚć?‘ä»¬ć?łč¦?ĺ?šä¸€ä¸Şĺ?ŹGANé‚Łć ·çš„ç”źć??ć¨ˇĺž‹ďĽŚĺ®?ĺ®žé™…ä¸Šć?Żĺ°†ä¸€ä¸ŞéšŹćśşĺ™ŞĺŁ°zĺŹ?ćŤ˘ć??ä¸€ä¸Şć•°ćŤ®ć ·ćś¬xçš„čż‡ç¨‹ďĽš

![img](https://pic4.zhimg.com/80/v2-95c127c567960398e548c5153fbe1497_720w.jpg)

![image-20220906111504712](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906111504712.png)

ĺ¦‚ćžść?‘ä»¬ćŠŠä¸€ä¸Şĺ™ŞĺŁ°çś‹ć??ä¸€ä¸Şć˛ˇćś‰äż®ĺ»şçš„ĺś°ĺźşďĽŚé‚Łäą?ć?‘ä»¬ĺ˘žĺŠ é«?ć–Żĺ™ŞĺŁ°çš„čż‡ç¨‹ĺ°±ç­‰äşŽć?Żĺś¨čż™ä¸Şĺś°ĺźşä¸Šć·»ç –ĺŠ ç“¦ďĽŚćś€ĺ?Žć?‘ä»¬ĺŹ?ćŤ˘ĺ®Ść??ďĽŚĺľ—ĺ?°ä¸€ä¸Şĺ®Ść•´çš„ć ·ćś¬ć•°ćŤ®ă€‚

č®ľ
$$
x=x_0â†’x_1â†’x_2â†’â‹Żâ†’x_{Tâ?’1}â†’x_T=z
$$
x~0~ä¸şĺ»şĺĄ˝çš„é«?ćĄĽĺ¤§ĺŽ¦ďĽ?ć•°ćŤ®ć ·ćś¬ďĽ‰ďĽŚx~T~ä¸şć‹†ĺĄ˝çš„ç –ç“¦ć°´ćłĄďĽ?éšŹćśşĺ™ŞĺŁ°ďĽ‰ďĽŚĺ?‡č®ľâ€ść‹†ćĄĽâ€ťéś€č¦?Tć­ĄďĽŚć•´ä¸Şčż‡ç¨‹ĺŹŻä»Ąčˇ¨ç¤şä¸şĺ»şé«?ćĄĽĺ¤§ĺŽ¦çš„éšľĺş¦ĺś¨äşŽďĽŚä»ŽĺŽźćť?ć–™x~T~ĺ?°ćś€ç»?é«?ćĄĽĺ¤§ĺŽ¦x~0~çš„č·¨ĺş¦čż‡ĺ¤§ďĽŚĺľ?éšľç?†č§Łx~T~ć?Żć€Žäą?ä¸€ä¸‹ĺ­?ĺŹ?ć??x~0~çš„ă€‚ä˝†ć?ŻďĽŚĺ˝“ć?‘ä»¬ćś‰äş†â€ść‹†ćĄĽâ€ťçš„ä¸­é—´čż‡ç¨‹x~1~,x~2~,â‹Ż,x~T~ĺ?ŽďĽŚć?‘ä»¬çźĄé?“x~t-1~â†’x~t~ä»Łčˇ¨çť€ć‹†ćĄĽçš„ä¸€ć­ĄďĽŚé‚Łäą?ĺŹŤčż‡ćťĄx~t~â†’x~t-1~ä¸Ťĺ°±ć?Żĺ»şćĄĽçš„ä¸€ć­ĄďĽźĺ¦‚ćžść?‘ä»¬č?˝ĺ­¦äĽšä¸¤č€…äą‹é—´çš„ĺŹ?ćŤ˘ĺ…łçł»x~t-1~=ÎĽ(x~t~)ďĽŚé‚Łäą?ä»Žx~t~ĺ‡şĺŹ‘ďĽŚĺŹŤĺ¤Ťĺś°ć‰§čˇŚx~t-1~=ÎĽ(x~t~)ă€?x~t-2~=ÎĽ(x~t-1~)ă€?...ďĽŚćś€ç»?ä¸Ťĺ°±č?˝é€ ĺ‡şé«?ćĄĽĺ¤§ĺŽ¦x~0~ĺ‡şćťĄďĽź



### ĺ‰Ťĺ?‘čż‡ç¨‹(ć‹†ćĄĽ)

ćŠŠĺ?‘ĺ‰Ťčż‡ç¨‹ćŻ”ĺ–»ć??ć‹†ćĄĽďĽŚĺ®žé™…ä¸Šć?‘ä»¬ć?ŻĺŹŻä»ĄçźĄé?“ćŻŹć¬ˇć‹†ä¸‹çš„ĺŽźćť?ć–™ć?Żä»€äą?çš„ďĽŚć‰€ä»Ąĺ‰Ťĺ?‘čż‡ç¨‹ć?Żä¸Ťĺ?«ĺŹŻĺ­¦äą ĺŹ‚ć•°çš„ďĽŚéšŹçť€ t ä¸Ťć–­ĺ˘žĺ¤§ďĽŚćś€ç»?ĺ?†ĺ¸?ĺŹ?ć??ĺ?„ĺ?‘ç‹¬ç«‹çš„é«?ć–Żĺ?†ĺ¸?ďĽŚäąźĺ°±ć?Żć?‘ä»¬ć‰€č°“çš„"ĺś°ĺźş"ďĽŚĺ®šäą‰çśźĺ®žć•°ćŤ®ĺ?†ĺ¸? x0â?Ľq(x) ďĽŚć?‘ä»¬ĺś¨ĺ‰Ťĺ?‘čż‡ç¨‹ä¸­é€?ć­ĄĺŠ ĺ…Ąä¸€ä¸Şĺ°Źçš„é«?ć–Żĺ™ŞĺŁ°ďĽŚä¸€ĺ…±ĺŠ ĺ…Ą T ć­ĄďĽŚä»Žč€Śäş§ç”źäş†ä¸€çł»ĺ?—ĺŠ ĺ™Şçš„ć ·ćś¬ x1,x2,â€¦,xT ďĽŚĺŠ ĺ…Ąĺ™ŞĺŁ°çš„ĺť‡ĺ€Ľĺ’Ść–ąĺ·®ç”± Î˛t ĺ†łĺ®šďĽŚĺ…¶ĺś¨ (0,1) äą‹é—´ďĽŚä¸” Î˛1<Î˛2<â‹Ż<Î˛T ďĽŚčż™ć„Źĺ‘łçť€ć‰€ĺŠ çš„ĺ™ŞĺŁ°ć?Żč¶ŠćťĄč¶Šĺ¤§çš„ă€‚

![image-20220906175008176](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906175008176.png)

ćś€ç»?ć?‘ä»¬ĺŹŻä»Ąĺľ—ĺ?°ä»Žx0ĺ?°ä»»ć„Źä¸€ä¸Şć—¶é—´tçš„ć¦‚çŽ‡ĺ?†ĺ¸?ďĽ?ç”¨x0ĺ’ŚÎ±čˇ¨ç¤şďĽŚäąźć?Żä¸€ä¸Şé«?ć–Żĺ?†ĺ¸?ďĽ‰ďĽŚĺą¶ä¸”ć?‘ä»¬ĺŹŻä»ĄćŠŠĺ‰Ťĺ?‘çš„ćŻŹä¸€ä¸Şć¦‚çŽ‡ĺ?†ĺ¸?é?˝ç”¨é«?ć–Żĺ?†ĺ¸?čˇ¨čľľĺ‡şćťĄă€‚

### é€†ć‰©ć•Łčż‡ç¨‹ďĽ?ĺ»şćĄĽďĽ‰

é€†čż‡ç¨‹ć?Żä»Žé«?ć–Żĺ™ŞĺŁ°ä¸­ć?˘ĺ¤ŤĺŽźĺ§‹ć•°ćŤ®ďĽŚäąźĺ°±ć?Żć?‘ä»¬č¦?ćŠŠĺŽźćť?ć–™ä¸€ć­Ąä¸€ć­Ąçš„ć”ľĺ›žĺŽ»ďĽŚćś‰äş†ć‹†ćĄĽçš„čż‡ç¨‹ďĽŚĺ…¶ĺ®žć?‘ä»¬ĺ°±çźĄé?“ć‹†ćĄĽçš„ćŻŹä¸€ć­Ąć?Żć€Žäą?ć‹†çš„äş†ďĽŚä˝†ć?Żć‹†ćĄĽč·źç›–ćĄĽć?Żä¸€ä¸ŞĺŹŤĺ?‘çš„čż‡ç¨‹ďĽŚć?‘ä»¬čż?ć?Żä¸ŤçźĄé?“ćŻŹä¸€ć­Ąçš„ĺ…·ä˝“ć“Ťä˝śďĽ?äąźĺ°±ć?Żĺ?†ĺ¸?ďĽ‰ďĽŚç”±äşŽć­Łĺ?‘čż‡ç¨‹ä¸­ć?‘ä»¬ćŻŹć¬ˇĺŠ çš„ĺ™ŞĺŁ°ĺľ?ĺ°ŹďĽŚć‰€ä»Ąć?‘ä»¬ĺ?‡č®ľĺŹŤĺ?‘čż‡ç¨‹p(xtâ?’1|xt) äąźć?Żä¸€ä¸Şé«?ć–Żĺ?†ĺ¸?ďĽŚć?‘ä»¬ĺŹŻä»Ąä˝żç”¨çĄžç»Źç˝‘ç»śčż›čˇŚć‹źĺ??ă€‚é€†čż‡ç¨‹äąźć?Żä¸€ä¸Şé©¬ĺ°”ç§‘ĺ¤«é“ľčż‡ç¨‹ă€‚ć?‘ä»¬çš„ç›®ć ‡ć?Żç”¨çĄžç»Źç˝‘ç»śćťĄć‹źĺ??ćŻŹä¸€ć­Ąć‰©ć•ŁďĽ?ĺ»şćĄĽďĽ‰çš„é«?ć–Żĺ?†ĺ¸?

![image-20220906174833194](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906174833194.png)

čż™ć ·ďĽŚć?‘ä»¬ĺ°±ĺŹŞéś€č¦?ç”¨çĄžç»Źç˝‘ç»śćťĄć‹źĺ??čż™ä¸¤ä¸Şĺ?†ĺ¸?çš„ĺŹ‚ć•°

![image-20220906174928039](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906174928039.png)

čż™ć ·ďĽŚć?‘ä»¬ĺ°±ĺľ—ĺ?°ä¸€ä¸Şĺ»şćĄĽçš„ć•™ç¨‹,çŽ°ĺś¨ä˝ ĺ‘ŠčŻ‰ć?‘ĺ?°äş†ĺ“Şä¸€ć­ĄďĽŚć?‘ĺ°±çźĄé?“ĺş”čŻĄĺ?šä»€äą?ć“Ťä˝śďĽ?ç”±äşŽć?Żé«?ć–Żĺ?†ĺ¸?ä¸­é‡‡ć ·ďĽŚčż?ć?Żćś‰éšŹćśşć€§ďĽ‰ďĽŚčż™ć ·ä¸€ć­Ąć­Ąçš„čż­ä»ŁďĽŚĺ°±ĺ»şĺĄ˝äş†ä¸€ä¸Şć–°çš„ĺ¤§ćĄĽ



## č®­ç»?ĺ’Śé‡‡ć ·čż‡ç¨‹

č®­ç»?čż‡ç¨‹ďĽšä»Žć•°ćŤ®é›†ä¸­é‡‡ć · x0ďĽŚä»Žĺť‡ĺŚ€ĺ?†ĺ¸?é‡‡ć · tďĽŚĺŹŻä˝żć¨ˇĺž‹é˛?ćŁ’ďĽŚé‡‡ć ·ĺ™ŞĺŁ°ďĽŚč®ˇç®— Loss ć›´ć–°ć¨ˇĺž‹ă€‚

é‡‡ć ·čż‡ç¨‹ďĽšä»Žć ‡ĺ‡†ć­Łć€?ĺ?†ĺ¸?é‡‡ć · xT ďĽŚčż­ä»Łč®ˇç®— xtâ?’1 ďĽŚĺ·˛çźĄĺť‡ĺ€Ľ ÎĽÎ¸(xt,t) ĺ’Śĺ¸¸ć•°ć–ąĺ·® Î˛t ĺ?©ç”¨ĺŹ‚ć•°é‡Ťć•´ĺŚ–ĺŹŻč®ˇç®—ĺ‡ş xtâ?’1 ďĽŚç›´ĺ?° x0ă€‚

![image-20220906174654613](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906174654613.png)

------

### **Stable Diffusion**

é¦–ĺ…?ďĽŚä»Žĺ?Ťĺ­—**Stable Diffusion**ĺ°±ĺŹŻä»Ąçś‹ĺ‡şďĽŚčż™ä¸Şä¸»č¦?é‡‡ç”¨çš„ć‰©ć•Łć¨ˇĺž‹ďĽ?Diffusion ModelďĽ‰ă€‚

ç®€ĺŤ•ćťĄčŻ´ďĽŚć‰©ć•Łć¨ˇĺž‹ĺ°±ć?ŻĺŽ»ĺ™Şč‡ŞçĽ–ç ?ĺ™¨çš„čżžç»­ĺş”ç”¨ďĽŚé€?ć­Ąç”źć??ĺ›ľĺ?Źçš„čż‡ç¨‹ă€‚stable diffusionĺ»¶ç»­äş†ddpmďĽŚdalleďĽŚglidesďĽŚdalle2ç­‰ä¸€çł»ĺ?—ĺ·Ąä˝śďĽŚé¦–ĺ…?ďĽŚä˝żç”¨çĽ–ç ?ĺ™¨ĺ°†ĺ›ľĺ?ŹxĺŽ‹çĽ©ä¸şčľ?ä˝Žç»´çš„ć˝śĺś¨ç©şé—´čˇ¨ç¤şzďĽ?xďĽ‰ĺ®?ä¸Žć—¶é—´ć­Ąé•żtä¸€čµ·ďĽŚä»Ąç®€ĺŤ•čżžćŽĄĺ’Śäş¤ĺŹ‰ä¸¤ç§Ťć–ąĺĽŹďĽŚćł¨ĺ…Ąĺ?°ć˝śĺś¨ç©şé—´čˇ¨ç¤şä¸­ĺŽ»ă€‚éšŹĺ?Žĺś¨zďĽ?xďĽ‰ĺźşçˇ€ä¸Ščż›čˇŚć‰©ć•Łä¸ŽĺŽ»ĺ™Şă€‚ćŤ˘č¨€äą‹ďĽŚ ĺ°±ć?Żć¨ˇĺž‹ĺą¶ä¸Ťç›´ćŽĄĺś¨ĺ›ľĺ?Źä¸Ščż›čˇŚč®ˇç®—ďĽŚä»Žč€Śĺ‡Źĺ°‘äş†č®­ç»?ć—¶é—´ă€?ć•?ćžść›´ĺĄ˝ă€‚ĺ€Ľĺľ—ä¸€ćŹ?çš„ć?ŻďĽŚStable DIffusionçš„ä¸Šä¸‹ć–‡ćśşĺ?¶éťžĺ¸¸ç?µć´»ďĽŚyä¸Ťĺ…‰ĺŹŻä»Ąć?Żĺ›ľĺ?Źć ‡ç­ľďĽŚĺ°±ć?Żč’™ç‰?ĺ›ľĺ?Źă€?ĺśşć™Żĺ?†ĺ‰˛ă€?ç©şé—´ĺ¸?ĺ±€ďĽŚäąźč?˝ĺ¤źç›¸ĺş”ĺ®Ść??ă€‚ĺ…¶ä¸­ä¸Šä¸‹ć–‡ďĽ?ContextďĽ‰yďĽŚĺŤłčľ“ĺ…Ąçš„ć–‡ćś¬ćŹ?ç¤şďĽŚç”¨ćťĄćŚ‡ĺŻĽxçš„ĺŽ»ĺ™Şă€‚

stable diffusionć?Żç”±ć…•ĺ°Ľé»‘ĺ¤§ĺ­¦ćśşĺ™¨č§†č§‰ä¸Žĺ­¦äą ç ”ç©¶ĺ°Źç»„ĺ’ŚRunwayçš„ç ”ç©¶äşşĺ‘?ďĽŚĺźşäşŽCVPR2022çš„ä¸€çŻ‡č®şć–‡ă€ŠHigh-Resolution Image Synthesis with Latent Diffusion Modelsă€‹ďĽŚĺą¶ä¸Žĺ…¶ä»–ç¤ľĺŚşĺ›˘é?źĺ??ä˝śĺĽ€ĺŹ‘çš„ä¸€ć¬ľĺĽ€ćş?ć¨ˇĺž‹ă€‚ć ¸ĺż?ć•°ćŤ®é›†ć?ŻLAION-5Bçš„ä¸€ä¸Şĺ­?é›†ďĽŚĺ®?ć?Żä¸“ä¸şĺźşäşŽCLIPçš„ć–°ć¨ˇĺž‹č€Śĺ?›ĺ»şă€‚ĺ?Ść—¶ďĽŚĺ®?äąźć?Żé¦–ä¸Şĺś¨4000ä¸ŞA100 Ezra-1 AIč¶…ĺ¤§é›†çľ¤ä¸Ščż›čˇŚč®­ç»?çš„ć–‡ćś¬č˝¬ĺ›ľĺ?Źć¨ˇĺž‹ă€‚

ç›®ĺ‰Ťć?‘ć??ĺŠźĺś¨ćś¬ĺś°é?¨ç˝˛éˇąç›®ďĽŚĺą¶ä¸”é?¨ç˝˛äş†ç˝‘éˇµGUIďĽŚĺ°ťčŻ•äş†ä˝żç”¨ć–‡ćś¬ďĽ?é˘†ĺźźĺ†…ä¸€č?¬ĺŹ«promptďĽ‰čż›čˇŚç”źć??ă€‚ĺś¨ćś¬ĺś°3070tić?ľĺŤˇä¸ŠďĽŚĺ¤§çş¦15sĺŹŻä»Ąç”źć??ä¸€ĺĽ ĺ›ľç‰‡ďĽŚä»Ąä¸‹ć?Żä¸€äş›ç”źć??çš„ĺ›ľç‰‡ĺ’Śç›¸ĺş”çš„promptďĽš

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00010-450910884_high_quality_3_d_render_very_cute_fluffy_cyborg!!_cat_plays_trumpet,_cyberpunk_highly_detailed,_unreal_engine_cinematic_smooth,_.jpg" alt="grid-00010-450910884_high_quality_3_d_render_very_cute_fluffy_cyborg!!_cat_plays_trumpet,_cyberpunk_highly_detailed,_unreal_engine_cinematic_smooth,_" style="zoom: 33%;" />

<center>ďĽ?high_quality_3_d_render_very_cute_fluffy_cyborg!!_cat_plays_trumpet,_cyberpunk_highly_detailed,_unreal_engine_cinematic_smoothďĽ‰
</center>



<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00046-2099638317_a_portrait_of_a_chinese_-_african_princess,_candle_light,_finely_detailed_features,_perfect_art,_at_an_ancient_city,_gapmoe_yand.jpg" alt="grid-00046-2099638317_a_portrait_of_a_chinese_-_african_princess,_candle_light,_finely_detailed_features,_perfect_art,_at_an_ancient_city,_gapmoe_yand" style="zoom: 20%;" />

         <center>ďĽ?a_portrait_of_a_chinese_-_african_princess,_candle_light,_finely_detailed_features,_perfect_art,_at_an_ancient_city,_gapmoe_yandďĽ‰
         </center>

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00043-1017762050_realistic_beautiful_gorgeous_natural_cute,_fantasy,_elegant,_lovely,_princess_girl,_art_drawn_full_hd,_4_k,_highest_quality,_in_.jpg" alt="grid-00043-1017762050_realistic_beautiful_gorgeous_natural_cute,_fantasy,_elegant,_lovely,_princess_girl,_art_drawn_full_hd,_4_k,_highest_quality,_in_" style="zoom: 25%;" />

            <center>
               ďĽ?realistic_beautiful_gorgeous_natural_cute,_fantasy,_elegant,_lovely,_princess_girl,_art_drawn_full_hd,_4_k,_highest_qualityďĽ‰ 
            </center>



<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00035-1843528981_side_portrait_of_a_rugged_girl_witch_wearing_magic_school_uniform,_cinematic,_elaborate,_elegant,_masterpiece,_illustration,_dig.jpg" alt="grid-00035-1843528981_side_portrait_of_a_rugged_girl_witch_wearing_magic_school_uniform,_cinematic,_elaborate,_elegant,_masterpiece,_illustration,_dig" style="zoom:33%;" />

  <center>
      ďĽ?side_portrait_of_a_rugged_girl_witch_wearing_magic_school_uniform,_cinematic,_elaborate,_elegant,_masterpiece,_illustration,_digďĽ‰
  </center>

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00029-1133231789_cat_theme_logo,_cat_theme_banner,_cat_design,_art_photography_style,_trending_on_artstation,_warm_light,_lovely_and_cute,_fantas.jpg" alt="grid-00029-1133231789_cat_theme_logo,_cat_theme_banner,_cat_design,_art_photography_style,_trending_on_artstation,_warm_light,_lovely_and_cute,_fantas" style="zoom: 25%;" />

   <center>ďĽ?cat_theme_logo,_cat_theme_banner,_cat_design,_art_photography_style,_trending_on_artstation,_warm_light,_lovely_and_cute,_fantasďĽ‰</center>

<img src="C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906092447207.png" alt="image-20220906092447207" style="zoom:50%;" />

           <center>ďĽ?high_quality_3_d_render_very_cute_princess_girl!!_princess,intricate_cotton_dress,_girl_plays_games,_cyberpunk,_unreal_engineďĽ‰
           </center>





çŽ°ĺś¨ĺş”ç”¨çš„diffusion generation modelé?˝ćś‰ä¸€ä¸Şĺľ?é‡Ťč¦?çš„ć–ąćł•ĺ°±ć?Ż text guided generationďĽ?äąźĺ°±ć?Żç”¨ć–‡ćś¬ĺŽ»ĺĽ•ĺŻĽdiffusion modelçš„ć‰©ć•Łć–ąĺ?‘ďĽ‰ďĽŚé˘†ĺźźĺ†…ä¸€č?¬ćŠŠčż™ä¸Şć–‡ćś¬ĺŹ«ĺ?šďĽ?promptďĽ‰

äąźćś‰from image to imageçš„ĺş”ç”¨ďĽ?masked or cropďĽ‰

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\img2img-samples\grid-00002-3160133777_ultra_cute_anime_girl_portraits,_chibi_art,_painting_by_gaston_bussiere,_craig_mullins,_j._c._leyendecker.jpg" alt="grid-00002-3160133777_ultra_cute_anime_girl_portraits,_chibi_art,_painting_by_gaston_bussiere,_craig_mullins,_j._c._leyendecker" style="zoom: 33%;" />

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\img2img-samples\grid-00001-2902298627_ultra_cute_anime_girl_portraits,_chibi_art,_painting_by_gaston_bussiere,_craig_mullins,_j._c._leyendecker.jpg" alt="grid-00001-2902298627_ultra_cute_anime_girl_portraits,_chibi_art,_painting_by_gaston_bussiere,_craig_mullins,_j._c._leyendecker" style="zoom:50%;" />

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\img2img-samples\grid-00004-2632476034_digital_anime_art!!,_gamer_girl_bedroom_sleeping_desk,_azure_blue_eyes,_pink_hair,_wlop,_rossdraws,_artgerm,_ross_tran.jpg" alt="grid-00004-2632476034_digital_anime_art!!,_gamer_girl_bedroom_sleeping_desk,_azure_blue_eyes,_pink_hair,_wlop,_rossdraws,_artgerm,_ross_tran" style="zoom: 25%;" />

ć€»č€Śč¨€äą‹ďĽŚć?łč¦?ç”źć??ć•?ćžśĺĄ˝ďĽŚćś€é‡Ťč¦?çš„ĺ°±ć?Żćś‰ä¸€ä¸Şé€‚ĺ˝“çš„promptĺ’Śä¸€ä¸Şĺ¤§çš„ĺ°şĺŻ¸ďĽ?ć?‘çš„ç”µč„‘ćś€ĺ¤šĺŹŞč?˝čż?čˇŚ576x640ďĽ‰![image-20220906094422437](C:\Users\41885\AppData\Roaming\Typora\typora-user-images\image-20220906094422437.png)

ĺ…¶ä¸­promptçš„é€‰ĺŹ–ć?Żćś€č®˛ç©¶çš„ďĽŚä¸€č?¬ĺŹŻä»Ąĺ?†ć??äş”ç±»ďĽ?ç±»ĺž‹ă€?ĺ†…ĺ®ąďĽŚéŁŽć ĽďĽŚä˝śč€…ďĽŚç¬¦ĺŹ·ďĽ‰ďĽŚć?‘čż™é‡ŚćŠŠĺ†…ĺ®ąĺ’ŚéŁŽć Ľé?¨ĺ?†ĺŹ?ĺ?šäş†ä¸€äş›ç»†ĺ?†ďĽš

- ĺ›ľç‰‡éŁŽć ĽďĽ?animeă€?pen and inkă€?unreal engine cinematic smooth,A digital illustrationă€?Full shot sketchă€?Lineart onlyă€?filmă€?portrait ďĽ‰
- ĺ›ľç‰‡ĺ†…ĺ®ąďĽ?cat/girlďĽ‰
- ĺ›ľç‰‡ĺ…łçł»ďĽ?ĺŠ¨ä˝śďĽŚä˝Ťç˝®ĺ…łçł»ďĽŚdoing somethingďĽŚonďĽŚinç­‰ďĽ‰
- ĺ›ľç‰‡ç±»ĺž‹(drone of footageă€?a cover of)
- č§†č§’ďĽ?side viewďĽŚlow angleă€?medium shotă€?closeup headshotă€?full shotă€?side portraitďĽ‰

- ç»´ĺş¦ďĽ?2d/3d renderďĽ‰
- ĺ›ľç‰‡č´¨é‡ŹďĽ?intricateă€?high quality uhd8kďĽŚsharp focus highly detailedă€?post - processing high resolutionă€?hdrďĽ‰
- ç¬¦ĺŹ·ďĽ?é—®ĺŹ·ďĽŚć„źĺŹąĺŹ·ďĽźďĽ?ďĽ‰

- ĺ…‰çşżďĽ?moody lightďĽŚmatte paintingă€?volumetric lightingďĽ‰

- č‰˛ĺ˝©ďĽ?fantasy vivid colorsă€?yellow color schemeďĽ‰

- ç”»ĺ®¶ćŹŹčż°ďĽ?greg rutkowski and thomas KinkadeďĽ‰

- ç»?ç”»ĺąłĺŹ°ďĽ?Trending on artstationďĽ‰

- ĺą´ä»ŁďĽ?renaissance backgroundă€?neoclassicală€?ultrarealistică€?traditional chinese paintingďĽ‰

- ćśŤéĄ°ďĽ?intricate cotton dressă€?lolitafashionďĽ‰

- çš®č‚¤ďĽ?porcelain skinďĽ‰

- ĺŤŠčş«ďĽ?half bodyďĽŚfull bodyďĽ‰
- ĺśşć™ŻďĽ?wuxiaă€?warďĽ‰
- ĺ›˝ĺ®¶ďĽ?Chineseă€?africanďĽ‰
- ĺ˝˘ĺ®ąčŻŤďĽ?gorgeousďĽ‰

ĺ…¶ä¸­éŁŽć ĽďĽŚç±»ĺž‹ďĽŚč´¨é‡Źç±»çš„promptäĽšĺŻąç”źć??çš„ĺ›ľç‰‡ćś‰ĺ·¨ĺ¤§çš„ĺ˝±ĺ“Ťă€‚



ć?‘čż?ĺ?šäş†ä¸€äş›ĺ®žéŞŚďĽŚä¸»č¦?ćŽ˘ç´˘ä»Ąä¸‹é—®é˘?ďĽš

**Q1:čŻ­ĺşŹé—®é˘?ć?Żĺ?¦ĺ˝±ĺ“Ťç”źć??ďĽź**

**A:äĽšĺ˝±ĺ“Ťç”źć??ďĽŚćš‚ć—¶ä¸Ťçˇ®ĺ®šĺ‰Ťĺ?Žçš„ĺ˝±ĺ“Ťĺ“Şä¸Şć›´ĺ¤§**

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\samples\girl_and_boy\00000-50_k_lms_1.png" alt="00000-50_k_lms_1" style="zoom: 50%;" />

                                                                                                           <center>
                                                                                                               ďĽ?girl and boyďĽ‰
                                                                                                           </center>



<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\samples\boy_and_girl\00001-50_k_lms_1.png" alt="00001-50_k_lms_1" style="zoom:50%;" />

																							<center>
																							    ďĽ?boy and girlďĽ‰
																							</center>





**Q2:ĺŤ•ä¸ŞčŻŤčŻ­ĺ’ŚĺŹĄĺ­?çš„ĺŚşĺ?«ďĽź**

**A:ĺŤ•ä¸ŞĺŤ•čŻŤäą‹é—´äĽĽäąŽĺ˝Ľć­¤ä¸ŤäĽšĺŻąĺ†…ĺ®ąäş§ç”źĺ¤Şĺ¤§çš„ĺ˝±ĺ“ŤďĽ?č€¦ĺ??ç¨‹ĺş¦ä˝ŽďĽ‰ďĽŚĺś¨ä¸€ä¸ŞĺŹĄĺ­?ĺ†…ďĽŚĺŤłä˝żčŻ´ć?Žäş†ĺ†…ĺ®ąé—´çš„ĺ…łçł»ďĽŚčż?ć?Żä¸ŤĺŹŻé?żĺ…Ťĺś°äĽšäş’ç›¸ĺ˝±ĺ“Ť**

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\samples\girlďĽ›boy\00000-50_k_lms_1.png" alt="00000-50_k_lms_1" style="zoom:50%;" />

                                                                                                <center>
                                                                                              ďĽ?girlďĽ›boyä˝żç”¨ĺ?†ĺŹ·éš”ĺĽ€ďĽ‰      
                                                                                                </center>



<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\samples\girl_and_boy\00002-50_k_lms_1.png" alt="00002-50_k_lms_1" style="zoom:50%;" />

                                                                                   <center>
                                                                                         (girl and boyďĽŚĺ…¶ä¸­boyçš„é?¨ĺ?†äĽĽäąŽäĽšĺŹ—ĺ?°girlçš„ĺ˝±ĺ“ŤďĽ‰
                                                                                   </center>



**Q3ďĽšćź?äş›ç¬¦ĺŹ·ć?Żĺ?¦äĽšĺŻąç”źć??ćś‰ĺ˝±ĺ“ŤďĽź**

**AďĽšé—®ĺŹ·ĺ’Ść„źĺŹąĺŹ·äĽšĺŻąčˇ¨ć?…ĺ’Śĺśşć™Żćś‰ä¸€ĺ®šçš„ĺ˝±ĺ“Ť**

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00084-1_girl_boy.jpg" alt="grid-00084-1_girl_boy" style="zoom:50%;" />

<center>(girl ďĽźďĽźboyďĽŚĺ…¶ä¸­ä¸¤ä¸Şé—®ĺŹ·äĽĽäąŽç»™ĺ›ľç‰‡äş§ç”źäş†ä¸€ä¸Şç–‘é—®çš„çĄžć?…)</center>

<img src="G:\program\stable-diffusion-main\stable-diffusion-main\scripts\outputs\txt2img-samples\grid-00086-1_girl_!!boy.jpg" alt="grid-00086-1_girl_!!boy" style="zoom:50%;" />

                                                      <center>
                                                             (girl ďĽ?ďĽ?ďĽźďĽźboyďĽŚĺś¨ä¸¤ä¸Şé—®ĺŹ·çš„ĺźşçˇ€ä¸ŠĺŠ äş†ä¸¤ä¸Şć„źĺŹąĺŹ·č®©çĄžć?…ĺŹ?ĺľ—ć›´ĺŠ ć?Šç–‘
                                                      </center>





ĺ?Žç»­äĽšç»§ç»­ćŽ˘ç´˘ĺŠ¨ç”»ç”źć??çš„é?¨ĺ?†

### **Gesture Generation**

ĺŻąĺ§żć€?ç”źć??č®şć–‡çš„č°?ç ”ćŠĄĺ‘Šć±‡ć€»ĺś¨éˇąç›®çš„ć–‡ćˇŁĺ†…ďĽ?ĺŚ…ć‹¬15çŻ‡č®şć–‡çš„ç®€ä»‹ďĽŚĺŹ‚č€?ä»·ĺ€Ľĺ’Śä¸€ä¸Şć€»ç»“ďĽ‰



### **skin lesion classification**

ĺŻąçš®č‚¤ç—…ĺ?†ç±»č®şć–‡çš„č°?ç ”ćŠĄĺ‘Šć±‡ć€»ĺś¨éˇąç›®çš„ć–‡ćˇŁĺ†…ďĽ?ĺŚ…ć‹¬11çŻ‡č®şć–‡çš„ç®€ä»‹ďĽŚĺŹ‚č€?ä»·ĺ€Ľĺ’Śä¸€ä¸Şć€»ç»“ďĽ‰



## reference

[1]č‹Źĺ‰‘ćž—. (Jun. 13, 2022). ă€Šç”źć??ć‰©ć•Łć¨ˇĺž‹ćĽ«č°?ďĽ?ä¸€ďĽ‰ďĽšDDPM = ć‹†ćĄĽ + ĺ»şćĄĽ ă€‹[Blog post]. Retrieved from https://kexue.fm/archives/9119

[2]ă€Šé˘„č®­ç»?čŻ­č¨€ć¨ˇĺž‹çš„ĺ‰Ťä¸–ä»Šç”źă€‹[Blog post] https://www.cnblogs.com/nickchen121/p/16470569.html

[3]DALLÂ·E 2ă€?č®şć–‡ç˛ľčŻ»ă€‘https://www.bilibili.com/video/BV17r4y1u77B?spm_id_from=333.337.search-card.all.click&vd_source=44aab6c8d4a7cdc7288eec8d0f60b618

[4]ĺŹ?ĺ?†č‡ŞçĽ–ç ?ĺ™¨ VAE é˛?éąŹ  https://www.bilibili.com/video/BV1Zq4y1h7Tu?spm_id_from=333.337.search-card.all.click&vd_source=44aab6c8d4a7cdc7288eec8d0f60b618
