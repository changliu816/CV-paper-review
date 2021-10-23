# Category

|:dog:|:mouse:|:hamster:|:tiger:|
|------|------|------|------|
|[1.Domain Adaptation](#1)|[2.Domain Generalization](#2)|[3.Image Self-supervised Learning](#3)|[4.Video Self-supervised Learning](#4)|
|[5.Semi-supervised Learning](#5)|[6.Long-tailed Recognition](#6)|[7.Noisy-label learning](#7)|[8.Data Augmentation](#8)|
|[9.Few-shots/Meta Learning](#9)|[10.Metric Learning](#10)|[11.Adversarial Learning](#11)|[12.Image2Image Translation](#12)|
|[13.Transformer](#13)|[0.General](#0)|

 e.g  * [SOE-Net: A Self-Attention and Orientation Encoding Network for Point Cloud Based Place Recognition](https://openaccess.thecvf.com/content/CVPR2021/papers/Xia_SOE-Net_A_Self-Attention_and_Orientation_Encoding_Network_for_Point_Cloud_CVPR_2021_paper.pdf)<br>:open_mouth:oral:star:[code](https://github.com/Yan-Xia/SOE-Net)


<a name="1"/>

## 1.Domain Adaptation



<a name="2"/>

## 2.Domain Generalization


<a name="3"/>

## 3.Image Self-supervised Learning

<a name="4"/>

## 4.Video Self-supervised Learning


<a name="5"/>

## 5.Semi-supervised Learning


<a name="6"/>

## 6.Long-tailed Recognition

<a name="7"/>

## 7.Noisy-label learning


 
 <a name="8"/>

## 8.Data Augmentation


<a name="9"/>

## 9.Few-shots/Meta Learning



 <a name="10"/>
 
 ## 10.Metric Learning


<a name="11"/>

## 11.Adversarial Learning

<a name="12"/>

## 12.Image2Image Translation


<a name="13"/>

## 13.Transformer 



<a name="0"/>

## 0. General
[Towards Learning Spatially Discriminative Feature Representations, ICCV2021](https://arxiv.org/pdf/2109.01359.pdf)<br>:open_mouth:oral:star:[code](xxx)

* Motivation:  Intuitively, if we constrain CAAMs (class-agnostic acitivation maps) closer to CAMs (class acitivation maps) of target categories,
features of the target categories will be expressed well and those of non-target categories will be suppressed simultaneously. 
* propose CAM-loss to push CAAM and CAM to be close by l1 distance. 
* **Comments**: 1.CAAMs代表所有objects出现的地方的attention, CAM代表某个特定object的attention. 一般来说，非target objects会干扰分类，所以让CAAM去拉近CAM可以避免这个问题。2. 可以拓展到Knowledge distillation. 用teacher的CAM 去guide student的CAAMs.

