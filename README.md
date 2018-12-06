# CV-paper-review
# General
* Group Normalization  [[paper](https://arxiv.org/abs/1803.08494 "悬停显示")] [[Comment](https://zhuanlan.zhihu.com/p/35005794)]
shuffle net
deformable network

*Spatial Transformer Networks [[Comment](https://zhuanlan.zhihu.com/p/41738716)] 
  *Localisation net 对feature map的输入输出，做出位置映射，从而得到 Grid generator. 然后，需要给feagure map输出的位置上赋值，采取bilinear interpolation, 让输出的feature map的score等于对应输入位置周围附近的score. 创建一个 position -> score的映射。这样，反向传导时可行 （dV/dU, dV/d theta= dV/dx dx/d theta）
  *This differentiable module can be inserted into existing convolutional architectures, giving neural networks the ability to actively spatially transform feature maps, conditional on the feature map itself, without any extra training supervision or modification to the optimisation process.

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
