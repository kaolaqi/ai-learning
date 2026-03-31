# 第三阶段：深度学习

> 从神经网络基础到主流架构，掌握用 PyTorch 搭建和训练模型的能力。

## 📚 知识点总览

- [3.1 神经网络基础](#31-神经网络基础)
- [3.2 激活函数](#32-激活函数)
- [3.3 损失函数与优化器](#33-损失函数与优化器)
- [3.4 反向传播与梯度](#34-反向传播与梯度)
- [3.5 PyTorch 基础](#35-pytorch-基础)
- [3.6 卷积神经网络 CNN](#36-卷积神经网络-cnn)
- [3.7 循环神经网络 RNN](#37-循环神经网络-rnn)
- [3.8 Transformer 架构](#38-transformer-架构)
- [3.9 正则化与训练技巧](#39-正则化与训练技巧)
- [3.10 迁移学习](#310-迁移学习)
- [3.11 生成模型基础](#311-生成模型基础)
- [3.12 综合实战](#312-综合实战)

---

## 3.1 神经网络基础

### 核心知识点
- [ ] 感知机模型：单层神经元
- [ ] 多层感知机（MLP）：输入层、隐藏层、输出层
- [ ] 前向传播过程
- [ ] 权重与偏置的作用
- [ ] 万能近似定理
- [ ] 深度 vs 宽度的影响
- [ ] 批量大小（Batch Size）的选择
- [ ] Epoch 与 Iteration 的区别

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [3Blue1Brown: 神经网络](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) | 视频 | 最佳神经网络可视化系列 |
| [动手学深度学习（李沐）](https://zh.d2l.ai/) | 书籍+视频 | 中文深度学习经典教程 |
| [李沐 B站深度学习课程](https://space.bilibili.com/1567748478) | 视频 | B站免费中文课程 |

---

## 3.2 激活函数

### 核心知识点
- [ ] 为什么需要激活函数：引入非线性
- [ ] Sigmoid：公式、特点、梯度消失问题
- [ ] Tanh：与 Sigmoid 的对比
- [ ] ReLU：最常用的激活函数
- [ ] Leaky ReLU / PReLU：解决 ReLU 死亡问题
- [ ] ELU 与 SELU
- [ ] GELU：Transformer 中常用
- [ ] Swish / SiLU
- [ ] Softmax：多分类输出层
- [ ] 如何选择激活函数

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [激活函数可视化对比](https://dashee87.github.io/deep%20learning/visualising-activation-functions-in-neural-networks/) | 文章 | 各激活函数图形对比 |

---

## 3.3 损失函数与优化器

### 核心知识点

#### 损失函数
- [ ] 均方误差（MSE）：回归任务
- [ ] 交叉熵损失（Cross-Entropy）：分类任务
- [ ] 二元交叉熵（BCE）：二分类
- [ ] 负对数似然（NLLLoss）
- [ ] Focal Loss：处理类别不平衡
- [ ] 对比损失 / 三元组损失：度量学习

#### 优化器
- [ ] SGD：随机梯度下降
- [ ] SGD + Momentum：动量加速
- [ ] Adagrad：自适应学习率
- [ ] RMSprop：改进 Adagrad
- [ ] Adam：最常用的优化器
- [ ] AdamW：带权重衰减的 Adam
- [ ] 学习率调度：StepLR、CosineAnnealingLR、ReduceLROnPlateau、Warmup

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [优化器可视化对比](https://www.youtube.com/watch?v=mdKjMPmcWjY) | 视频 | 各优化器动画对比 |
| [Sebastian Ruder: 优化器综述](https://ruder.io/optimizing-gradient-descent/) | 文章 | 经典优化器综述 |

---

## 3.4 反向传播与梯度

### 核心知识点
- [ ] 链式法则（Chain Rule）
- [ ] 计算图（Computational Graph）
- [ ] 反向传播算法步骤
- [ ] 梯度消失问题与解决方案
- [ ] 梯度爆炸问题与梯度裁剪（Gradient Clipping）
- [ ] 自动微分（Autograd）原理
- [ ] 数值梯度检验

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [3Blue1Brown: 反向传播](https://www.youtube.com/watch?v=Ilg3gGewQ5U) | 视频 | 反向传播可视化 |
| [Andrej Karpathy: micrograd](https://www.youtube.com/watch?v=VMj-3S1tku0) | 视频 | 从零实现自动微分引擎 |

---

## 3.5 PyTorch 基础

### 核心知识点
- [ ] Tensor 创建与操作
- [ ] Tensor 与 NumPy 的互转
- [ ] GPU 加速：.to(device)、.cuda()
- [ ] 自动求导：requires_grad、backward()、grad
- [ ] nn.Module：自定义模型
- [ ] nn.Sequential：快速搭建模型
- [ ] nn.Linear、nn.Conv2d、nn.LSTM 等常用层
- [ ] Dataset 与 DataLoader
- [ ] 训练循环：forward → loss → backward → step
- [ ] 模型保存与加载：save、load_state_dict
- [ ] torchvision：数据集、预训练模型、图像变换
- [ ] TensorBoard 可视化训练过程

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [PyTorch 官方教程](https://pytorch.org/tutorials/) | 文档 | 官方入门教程 |
| [PyTorch 60分钟入门](https://pytorch.org/tutorials/beginner/deep_learning_60min_blitz.html) | 教程 | 快速上手 |
| [莫烦 PyTorch 教程](https://mofanpy.com/tutorials/machine-learning/torch/) | 视频 | 中文视频教程 |
| [李沐 PyTorch 动手学深度学习](https://zh.d2l.ai/chapter_installation/index.html) | 书籍 | 配套 PyTorch 代码 |

---

## 3.6 卷积神经网络 CNN

### 核心知识点
- [ ] 卷积操作原理：卷积核、步长（stride）、填充（padding）
- [ ] 特征图（Feature Map）
- [ ] 池化层：最大池化、平均池化
- [ ] 感受野（Receptive Field）
- [ ] 经典架构演进：
  - [ ] LeNet-5：手写数字识别
  - [ ] AlexNet：深度学习的突破
  - [ ] VGGNet：更深的网络
  - [ ] GoogLeNet / Inception：多尺度特征
  - [ ] ResNet：残差连接解决退化问题
  - [ ] DenseNet：密集连接
  - [ ] EfficientNet：复合缩放
- [ ] 1x1 卷积的作用
- [ ] 批归一化（Batch Normalization）
- [ ] 全局平均池化（GAP）
- [ ] 数据增强：翻转、旋转、裁剪、颜色变换
- [ ] 图像分类实战：CIFAR-10 / ImageNet

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [CS231n: CNN 课程](https://cs231n.stanford.edu/) | 课程 | 斯坦福经典计算机视觉课 |
| [CNN Explainer 可视化](https://poloclub.github.io/cnn-explainer/) | 工具 | 交互式 CNN 可视化 |
| [李沐: ResNet 论文精读](https://www.youtube.com/watch?v=pWMnzCX4cwQ) | 视频 | 经典论文讲解 |

---

## 3.7 循环神经网络 RNN

### 核心知识点
- [ ] RNN 基本结构：隐藏状态的时间传递
- [ ] RNN 的梯度消失与梯度爆炸
- [ ] LSTM：长短期记忆网络
  - [ ] 遗忘门、输入门、输出门
  - [ ] 细胞状态（Cell State）
- [ ] GRU：门控循环单元（LSTM 的简化版）
- [ ] 双向 RNN（Bidirectional RNN）
- [ ] 多层 RNN（Stacked RNN）
- [ ] Seq2Seq 模型：编码器-解码器架构
- [ ] 注意力机制的引入（Attention）
- [ ] 文本生成与序列预测实战

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [colah: 理解 LSTM](https://colah.github.io/posts/2015-08-Understanding-LSTMs/) | 文章 | 最经典的 LSTM 图解 |
| [李沐: RNN 讲解](https://zh.d2l.ai/chapter_recurrent-neural-networks/) | 书籍 | 动手学深度学习 RNN 章节 |

---

## 3.8 Transformer 架构

### 核心知识点
- [ ] Attention Is All You Need 论文核心思想
- [ ] 自注意力机制（Self-Attention）
- [ ] Query、Key、Value 的含义
- [ ] 缩放点积注意力（Scaled Dot-Product Attention）
- [ ] 多头注意力（Multi-Head Attention）
- [ ] 位置编码（Positional Encoding）
- [ ] 编码器结构：Multi-Head Attention + FFN + LayerNorm + 残差连接
- [ ] 解码器结构：Masked Attention + Cross Attention
- [ ] Transformer 的并行化优势
- [ ] BERT：双向编码器预训练
- [ ] GPT：自回归解码器预训练
- [ ] Vision Transformer（ViT）：Transformer 用于图像

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) | 文章 | 最佳 Transformer 图解 |
| [李沐: Transformer 论文精读](https://www.youtube.com/watch?v=nzqlFIcCSWQ) | 视频 | 逐段讲解原始论文 |
| [Andrej Karpathy: GPT from scratch](https://www.youtube.com/watch?v=kCc8FmEb1nY) | 视频 | 从零实现 GPT |
| [The Illustrated GPT-2](https://jalammar.github.io/illustrated-gpt2/) | 文章 | GPT-2 图解 |
| [The Illustrated BERT](https://jalammar.github.io/illustrated-bert/) | 文章 | BERT 图解 |
| [Hugging Face Transformers 教程](https://huggingface.co/learn/nlp-course) | 课程 | 免费 NLP 实操课程 |

---

## 3.9 正则化与训练技巧

### 核心知识点
- [ ] Dropout：随机丢弃神经元
- [ ] L1 / L2 正则化（权重衰减）
- [ ] 批归一化（Batch Normalization）
- [ ] 层归一化（Layer Normalization）
- [ ] 组归一化（Group Normalization）
- [ ] 早停法（Early Stopping）
- [ ] 数据增强策略
- [ ] 标签平滑（Label Smoothing）
- [ ] 混合精度训练（Mixed Precision Training）
- [ ] 梯度累积（Gradient Accumulation）
- [ ] 权重初始化：Xavier、He、Kaiming
- [ ] 学习率预热（Warmup）

---

## 3.10 迁移学习

### 核心知识点
- [ ] 迁移学习的概念与动机
- [ ] 预训练模型（Pretrained Models）
- [ ] 特征提取（Feature Extraction）：冻结预训练层
- [ ] 微调（Fine-tuning）：解冻部分层训练
- [ ] torchvision.models 预训练模型使用
- [ ] Hugging Face 预训练模型使用
- [ ] 领域适应（Domain Adaptation）
- [ ] 何时使用迁移学习

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [PyTorch 迁移学习教程](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html) | 教程 | 官方迁移学习指南 |
| [Hugging Face 模型库](https://huggingface.co/models) | 平台 | 海量预训练模型 |

---

## 3.11 生成模型基础

### 核心知识点
- [ ] 生成模型 vs 判别模型
- [ ] 自编码器（Autoencoder）
- [ ] 变分自编码器（VAE）
- [ ] 生成对抗网络（GAN）基本原理
  - [ ] 生成器与判别器的对抗训练
  - [ ] DCGAN：卷积 GAN
  - [ ] GAN 训练的不稳定性与技巧
- [ ] 扩散模型（Diffusion Model）基本概念
- [ ] Stable Diffusion 简介

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [李宏毅: GAN 课程](https://www.youtube.com/watch?v=DQNNMiAP5lw) | 视频 | 中文 GAN 讲解 |
| [The Illustrated Stable Diffusion](https://jalammar.github.io/illustrated-stable-diffusion/) | 文章 | Stable Diffusion 图解 |

---

## 3.12 综合实战

### 练习项目
- [ ] 项目一：MNIST / CIFAR-10 图像分类（CNN）
- [ ] 项目二：文本情感分类（RNN / LSTM）
- [ ] 项目三：使用预训练 ResNet 做图像分类（迁移学习）
- [ ] 项目四：从零实现一个简单的 Transformer
- [ ] 项目五：使用 Hugging Face 做文本分类

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [PyTorch 官方示例](https://github.com/pytorch/examples) | 代码 | 各种任务的示例代码 |
| [Papers With Code](https://paperswithcode.com/) | 平台 | 论文+代码+排行榜 |
| [Kaggle 深度学习竞赛](https://www.kaggle.com/competitions) | 竞赛 | 实战练手 |

---

> ✅ 完成本阶段后，你应该能够用 PyTorch 搭建 CNN、RNN、Transformer 模型，并理解深度学习的核心训练技巧。
>
> 👉 下一步：[04-大语言模型](../04-llm/README.md)
