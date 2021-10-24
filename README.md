# Category

|:dog:|:mouse:|:hamster:|:tiger:|
|------|------|------|------|
|[1.Domain Adaptation](#1)|[2.Domain Generalization](#2)|[3.Image Self-supervised Learning](#3)|[4.Video Self-supervised Learning](#4)|
|[5.Semi-supervised Learning](#5)|[6.Long-tailed Recognition](#6)|[7.Noisy-label learning](#7)|[8.Data Augmentation](#8)|
|[9.Few-shots/Meta Learning](#9)|[10.Metric Learning](#10)|[11.Adversarial Learning](#11)|[12.Image2Image Translation](#12)|
|[13.Transformer/self-attention](#13)|[0.Classification/Fine-grained](#0)|

 e.g  * [SOE-Net: A Self-Attention and Orientation Encoding Network for Point Cloud Based Place Recognition](https://openaccess.thecvf.com/content/CVPR2021/papers/Xia_SOE-Net_A_Self-Attention_and_Orientation_Encoding_Network_for_Point_Cloud_CVPR_2021_paper.pdf)<br>:open_mouth:oral:star:[code](https://github.com/Yan-Xia/SOE-Net)

# Todo
- Read ICCV21 DA and SSL papers  -写论文的表格和图可以模仿FB的style
- 

<a name="1"/>

## 1.Domain Adaptation

[On Generating Transferable Targeted Perturbations, ICCV2021](https://arxiv.org/pdf/2103.14641.pdf)

[Adversarial Unsupervised Domain Adaptation with Conditional and Label Shift: Infer, Align and Iterate, ICCV2021](https://arxiv.org/abs/2107.13469)


[SENTRY: Selective Entropy Optimization via Committee Consistency for Unsupervised Domain Adaptation, ICCV2021](https://arxiv.org/abs/2012.11460) 


[Gradient Distribution Alignment Certificates Better Adversarial Domain
Adaptation, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Gao_Gradient_Distribution_Alignment_Certificates_Better_Adversarial_Domain_Adaptation_ICCV_2021_paper.pdf) [code](https://github.com/theNded/SGP)
* Improvement for MCD third step: Fix two classifier and update G by minimize divegence between prob output of two classifiers.
* The new divergence loss is: gradience discrepancy: Cosine-distance (gs,gt) where gs is the grad. of L_ce and gt is the weighted pseudo label loss. 
* New way to select PL: calculate target proto by weighted features where weights are from the softmax outputs. 

[Adaptive Adversarial Network for Source-free Domain Adaptation, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Xia_Adaptive_Adversarial_Network_for_Source-Free_Domain_Adaptation_ICCV_2021_paper.pdf) 

[STEM: An approach to Multi-source Domain Adaptation with Guarantees, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Nguyen_STEM_An_Approach_to_Multi-Source_Domain_Adaptation_With_Guarantees_ICCV_2021_paper.pdf) 

[Dynamic Transfer for Multi-Source Domain Adaptation, CVPR2021](https://arxiv.org/pdf/2103.10583.pdf) 





<a name="2"/>

## 2.Domain Generalization
[Confidence Calibration for Domain Generalization under Covariate Shift, ICCV2021](https://arxiv.org/abs/2104.00742) 


<a name="3"/>

## 3.Image Self-supervised Learning
[A Broad Study on the Transferability of Visual Representations With Contrastive Learning](https://arxiv.org/abs/2103.13517)<br>:star:[code](https://github.com/asrafulashiq/transfer_broad)
[With a Little Help From My Friends: Nearest-Neighbor Contrastive Learning of Visual Representations](https://arxiv.org/abs/2104.14548)
[On Feature Decorrelation in Self-Supervised Learning, ICCV2021](https://arxiv.org/abs/2105.00470) 

[Improving Contrastive Learning by Visualizing Feature Transformation](https://arxiv.org/abs/2108.02982)<br>:open_mouth:oral:star:[code](https://github.com/DTennant/CL-Visualizing-Feature-Transformation)

[ISD: Self-Supervised Learning by Iterative Similarity Distillation, ICCV2021](https://arxiv.org/pdf/2012.09259.pdf) [code](https://github.com/UMBCvision/ISD)

[Switchable K-class Hyperplanes for Noise-Robust Representation Learning, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Liu_Switchable_K-Class_Hyperplanes_for_Noise-Robust_Representation_Learning_ICCV_2021_paper.pdf) [code](https://github.com/liubx07/SKH.git)

[Solving Inefficiency of Self-supervised Representation Learning, ICCV2021](https://arxiv.org/pdf/2104.08760.pdf) [code](https://github.com/wanggrun/triplet)


[Self-supervised Motion Learning from Static Images, CVPR2021](https://arxiv.org/pdf/2104.00240.pdf)

[Joint Contrastive Learning with Infinite Possibilities, NIPS2020](https://arxiv.org/pdf/2009.14776.pdf)
* Extension for Moco where only single positive key is used while JCL pushes the num of positives to infinity and minimizes the upper bound of loss. E(log(X))<= log E(X)
* Key is to estimate the Gaussian distribution of positive keys N(mu, sigma)
* **Comments**: 类似 Semantic Aug，只是loss 从CE 换成了Contrastive Loss. 

[Contrastive Learning with Adversarial Examples, NIPS2020](https://arxiv.org/pdf/2010.12050.pdf) [code](https://github.com/chihhuiho/CLAE)
* 2-steps optimization: 1) Generate positive adv samples by maximizing CTloss. 2) Use Adv samples for CTLoss.

[Adversarial Self-Supervised Contrastive Learning, NIPS2020](https://arxiv.org/pdf/2006.07589.pdf) [code](https://github.com/Kim-Minseon/RoCL)
* **Comments:和上面那篇基本一样，但是citation更高

<a name="4"/>

## 4.Video Self-supervised Learning
[Contrast and Order Representations for Video Self-Supervised Learning, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Hu_Contrast_and_Order_Representations_for_Video_Self-Supervised_Learning_ICCV_2021_paper.pdf)
[Contrastive Learning of Image Representations With Cross-Video Cycle-Consistency](https://arxiv.org/abs/2105.06463)<br>:house:[project](https://happywu.github.io/cycle_contrast_video/)



<a name="5"/>

## 5.Semi-supervised Learning
  * [Trash to Treasure: Harvesting OOD Data with Cross-Modal Matching for Open-Set Semi-Supervised Learning](https://arxiv.org/abs/2108.05617)

  * [Semi-Supervised Active Learning for Semi-Supervised Models: Exploit Adversarial Examples With Graph-Based Virtual Labels](https://openaccess.thecvf.com/content/ICCV2021/papers/Guo_Semi-Supervised_Active_Learning_for_Semi-Supervised_Models_Exploit_Adversarial_Examples_With_ICCV_2021_paper.pdf)
  * [CoMatch: Semi-Supervised Learning With Contrastive Graph Regularization](https://arxiv.org/abs/2011.11183)<br>:star:[code](https://github.com/salesforce/CoMatch)
  * 
[Semi-Supervised Learning of Visual Features by Non-Parametrically Predicting View Assignments with Support Samples, ICCV2021](https://arxiv.org/pdf/2104.13963.pdf) [code](https://github.com/facebookresearch/suncet)

[Weakly Supervised Contrastive Learning, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Zheng_Weakly_Supervised_Contrastive_Learning_ICCV_2021_paper.pdf) [code](https://github.com/theNded/SGP)

[Weakly Supervised Representation Learning with Coarse Labels, ICCV2021](https://openaccess.thecvf.com/content/ICCV2021/papers/Xu_Weakly_Supervised_Representation_Learning_With_Coarse_Labels_ICCV_2021_paper.pdf) [code](https://github.com/theNded/SGP)


<a name="6"/>

## 6.Long-tailed Recognition

<a name="7"/>

## 7.Noisy-label learning


 
 <a name="8"/>

## 8.Data Augmentation
-[On Feature Normalization and Data Augmentation, CVPR2021](https://arxiv.org/pdf/2002.11102.pdf) [code](https://github.com/Boyiliee/MoEx.)
* ConvNets trained on ImageNet are biased towards textures instead of shapes. The moments (mean, variance) contains rich structure information and should not be discarded by normalization. 
* Swap the shape (or style) information of two images by swapping the moments after 1st layers. 
* Feature-level augmentation. 类似 cross-norm那篇paper.

-[SuperMix: Supervising the Mixing Data Augmentation, CVPR2021](https://arxiv.org/pdf/2002.11102.pdf) [code](https://github.com/Boyiliee/MoEx.)
* ConvNets trained on ImageNet are biased towards textures instead of shapes. The moments (mean, variance) contains rich structure information and should not be discarded by normalization. 
* Swap the shape (or style) information of two images by swapping the moments after 1st layers. 
* Feature-level augmentation


<a name="9"/>

## 9.Few-shots/Meta Learning



 <a name="10"/>
 
 ## 10.Metric Learning
* [Towards Interpretable Deep Metric Learning with Structural Matching](https://arxiv.org/abs/2108.05889)<br>:star:[code](https://github.com/wl-zhao/DIML)
* [Deep Relational Metric Learning](https://arxiv.org/abs/2108.10026)<br>:star:[code](https://github.com/zbr17/DRML)
* [LoOp: Looking for Optimal Hard Negative Embeddings for Deep Metric Learning](https://arxiv.org/abs/2108.09335)<br>:star:[code](https://github.com/puneesh00/LoOp)


<a name="11"/>

## 11.Adversarial Learning

<a name="12"/>

## 12.Image2Image Translation


<a name="13"/>

## 13.Transformer 



<a name="0"/>

## 0. Classification/Fine-grained
[Towards Learning Spatially Discriminative Feature Representations, ICCV2021](https://arxiv.org/pdf/2109.01359.pdf)<br>:open_mouth:oral:star:[code](xxx)
* propose CAM-loss to push CAAM and CAM to be close by l1 distance. 
* **Comments**: 1.CAAMs代表所有objects出现的地方的attention, CAM代表某个特定object的attention. 一般来说，非target objects会干扰分类，所以让CAAM去拉近CAM可以避免这个问题。2. 可以拓展到Knowledge distillation. 用teacher的CAM 去guide student的CAAMs.

