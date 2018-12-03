# CV-paper-review
# General
* Group Normalization  [[paper](https://arxiv.org/abs/1803.08494 "悬停显示")] [[Comment](https://zhuanlan.zhihu.com/p/35005794)]

# Face recognition
* Schroff F, Kalenichenko D, Philbin J. Facenet: A unified embedding for face recognition and clustering,CVPR, 2015
>Hightlight: Triple Loss

* Liu W, Wen Y, Yu Z, et al. Large-Margin Softmax Loss for Convolutional Neural Networks [C]// ICML, 2016.
> Large-Margin Softmax Loss,是large margin系列的开创算法，首先联合FC + Softmax + Cross-entropy重新并给出了Softmax loss的表达式. 加强分类条件，强制让对应类别的W和x夹角增加到原来的m倍

* Liu W, Wen Y, Yu Z, et al. SphereFace: Deep Hypersphere Embedding for Face Recognition [C]// CVPR. 2017.
> angular softmax loss. 归一化了权值W，让训练更加集中在优化深度特征映射和特征向量角度上，降低样本数量不均衡问题

* Wen Y, Zhang K, Li Z, et al. A discriminative feature learning approach for deep face recognition [C]// ECCV, 2016.
> 为每个类别学习一个中心，并将每个类别的所有特征向量拉向对应类别中心，联合Softmax一起使用

* Jiankang Deng, Jia Guo, Stefanos Zafeiriou. ArcFace: Additive Angular Margin Loss for Deep Face Recognition [J]. arXiv:1801.07698. (Submitted to IJCV)

* 特征归一化的重要性
> 从最新方法来看，权值W和特征f(或x)归一化已经成为了标配，而且都给归一化特征乘以尺度因子s进行放大，目前主流都采用固定尺度因子s的方法(看来自适应训练没那么重要)；
> 权值和特征归一化使得CNN更加集中在优化夹角上，得到的深度人脸特征更加分离；
> 特征归一化后，特征向量都固定映射到半径为1的超球上，便于理解和优化；但这样也会压缩特征表达的空间；乘尺度因子s，相当于将超球的半径放大到s，超球变大，特征表达的空间也更大（简单理解：半径越大球的表面积越大）；
> 特征归一化后，人脸识别计算特征向量相似度，L2距离和cos距离意义等价，计算量也相同，我们再也不用纠结到底用L2距离还会用cos距离：


large magin是显式的类内夹角约束，目标是让同一类的所有特征向量都拉向该类别的权值向量。

# Detection
* An Analysis of Scale Invariance in Object Detection – SNIP
* Single-Shot Refinement Neural Network for Object Detection
* Cascade R-CNN: Delving into High Quality Object Detection

# Attention
* attention is all you need  [[paper](https://arxiv.org/pdf/1711.07971.pdf "悬停显示")] [[Comment](https://zhuanlan.zhihu.com/p/34781297)]

* Non-local Neural Networks  [[paper](https://arxiv.org/abs/1711.07971 "悬停显示")] [[Comment](https://zhuanlan.zhihu.com/p/33345791)]



# Transfer Learning
* Disentangling Task Transfer Learning, CVPR18 [[paper](http://taskonomy.stanford.edu/taskonomy_CVPR2018.pdf "悬停显示")] [[Comment](https://zhuanlan.zhihu.com/p/38425434)]  

>Goal: 目标是着眼于一组任务，并利用任务之间的关联性减少总体数据使用量. 量化视觉任务的关联性，并基于求得的affinity matrix最优化得到如何分配任务监督数据量。选择一些任务从零学习，剩下的任务用少量数据进行迁移学习，具体迁移学习的策略由subgraph中的edge来决定
