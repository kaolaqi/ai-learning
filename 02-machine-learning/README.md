# 第二阶段：机器学习

> 理解经典算法的原理与应用场景，学会用 Scikit-learn 解决实际问题。

## 📚 知识点总览

- [2.1 机器学习概述](#21-机器学习概述)
- [2.2 数据预处理](#22-数据预处理)
- [2.3 线性回归](#23-线性回归)
- [2.4 逻辑回归](#24-逻辑回归)
- [2.5 决策树与随机森林](#25-决策树与随机森林)
- [2.6 支持向量机 SVM](#26-支持向量机-svm)
- [2.7 K 近邻 KNN](#27-k-近邻-knn)
- [2.8 朴素贝叶斯](#28-朴素贝叶斯)
- [2.9 聚类算法](#29-聚类算法)
- [2.10 降维技术](#210-降维技术)
- [2.11 模型评估与调参](#211-模型评估与调参)
- [2.12 集成学习](#212-集成学习)
- [2.13 综合实战](#213-综合实战)

---

## 2.1 机器学习概述

### 核心知识点
- [ ] 什么是机器学习：从数据中学习规律
- [ ] 监督学习 vs 无监督学习 vs 半监督学习 vs 强化学习
- [ ] 分类问题 vs 回归问题
- [ ] 训练集、验证集、测试集的划分
- [ ] 过拟合与欠拟合
- [ ] 偏差-方差权衡（Bias-Variance Tradeoff）
- [ ] 没有免费午餐定理（No Free Lunch）
- [ ] 机器学习工作流程：数据收集 → 预处理 → 特征工程 → 建模 → 评估 → 部署

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [吴恩达机器学习课程](https://www.coursera.org/learn/machine-learning) | 视频课程 | 最经典的入门课程 |
| [StatQuest 机器学习系列](https://www.youtube.com/playlist?list=PLblh5JKOoLUICTaGLRoHQDuF_7q2GfuJF) | 视频 | 直观易懂的可视化讲解 |
| [动手学机器学习](https://zh.d2l.ai/) | 书籍 | 李沐老师中文教程 |

---

## 2.2 数据预处理

### 核心知识点
- [ ] 特征缩放：StandardScaler（标准化）、MinMaxScaler（归一化）
- [ ] 类别特征编码：LabelEncoder、OneHotEncoder、OrdinalEncoder
- [ ] 缺失值处理策略：均值/中位数/众数填充、删除、插值
- [ ] 异常值检测与处理：IQR 方法、Z-Score
- [ ] 特征选择：方差阈值、相关性分析、互信息
- [ ] 特征工程：多项式特征、交叉特征、分箱
- [ ] Pipeline 管道：将预处理和模型串联
- [ ] ColumnTransformer：对不同列应用不同变换

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Scikit-learn 预处理文档](https://scikit-learn.org/stable/modules/preprocessing.html) | 文档 | 官方预处理指南 |
| [Kaggle 特征工程课程](https://www.kaggle.com/learn/feature-engineering) | 交互课程 | 免费实操课程 |

---

## 2.3 线性回归

### 核心知识点
- [ ] 线性回归原理：y = wx + b
- [ ] 损失函数：均方误差（MSE）
- [ ] 最小二乘法（解析解）
- [ ] 梯度下降法：批量梯度下降、随机梯度下降、小批量梯度下降
- [ ] 学习率的选择与影响
- [ ] 多元线性回归
- [ ] 正则化：Ridge（L2）、Lasso（L1）、ElasticNet
- [ ] 评估指标：MSE、RMSE、MAE、R²

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: 线性回归](https://www.youtube.com/watch?v=nk2CQITm_eo) | 视频 | 直观讲解线性回归 |
| [3Blue1Brown: 梯度下降](https://www.youtube.com/watch?v=IHZwWFHWa-w) | 视频 | 梯度下降可视化 |

---

## 2.4 逻辑回归

### 核心知识点
- [ ] 逻辑回归原理：Sigmoid 函数将线性输出映射到概率
- [ ] 决策边界
- [ ] 损失函数：交叉熵损失（Cross-Entropy Loss）
- [ ] 多分类：One-vs-Rest（OvR）、Softmax 回归
- [ ] 正则化在逻辑回归中的应用
- [ ] 评估指标：准确率、精确率、召回率、F1-Score
- [ ] 混淆矩阵
- [ ] ROC 曲线与 AUC

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: 逻辑回归](https://www.youtube.com/watch?v=yIYKR4sgzI8) | 视频 | 清晰讲解逻辑回归 |
| [Scikit-learn 逻辑回归文档](https://scikit-learn.org/stable/modules/linear_model.html#logistic-regression) | 文档 | 官方使用指南 |

---

## 2.5 决策树与随机森林

### 核心知识点
- [ ] 决策树原理：信息增益、基尼系数
- [ ] ID3、C4.5、CART 算法区别
- [ ] 树的剪枝：预剪枝、后剪枝
- [ ] 决策树的可视化
- [ ] 随机森林：Bagging + 随机特征选择
- [ ] 特征重要性（feature_importances_）
- [ ] 超参数：max_depth、min_samples_split、n_estimators

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: 决策树](https://www.youtube.com/watch?v=_L39rN6gz7Y) | 视频 | 决策树可视化讲解 |
| [StatQuest: 随机森林](https://www.youtube.com/watch?v=J4Wdy0Wc_xQ) | 视频 | 随机森林原理 |

---

## 2.6 支持向量机 SVM

### 核心知识点
- [ ] SVM 原理：最大间隔分类器
- [ ] 支持向量的概念
- [ ] 软间隔与 C 参数
- [ ] 核函数：线性核、多项式核、RBF 核
- [ ] 核技巧（Kernel Trick）：低维到高维映射
- [ ] SVM 用于回归（SVR）
- [ ] gamma 参数的影响

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: SVM](https://www.youtube.com/watch?v=efR1C6CvhmE) | 视频 | SVM 直观讲解 |
| [MIT SVM 讲座](https://www.youtube.com/watch?v=_PwhiWxHK8o) | 视频 | 深入数学推导 |

---

## 2.7 K 近邻 KNN

### 核心知识点
- [ ] KNN 原理：基于距离的懒惰学习
- [ ] 距离度量：欧氏距离、曼哈顿距离、闵可夫斯基距离
- [ ] K 值选择对结果的影响
- [ ] 特征缩放对 KNN 的重要性
- [ ] KNN 用于分类和回归
- [ ] KD-Tree 加速搜索
- [ ] 维度灾难

---

## 2.8 朴素贝叶斯

### 核心知识点
- [ ] 贝叶斯定理：P(A|B) = P(B|A) * P(A) / P(B)
- [ ] 朴素假设：特征条件独立
- [ ] 高斯朴素贝叶斯（连续特征）
- [ ] 多项式朴素贝叶斯（文本分类）
- [ ] 伯努利朴素贝叶斯（二值特征）
- [ ] 拉普拉斯平滑
- [ ] 文本分类实战：垃圾邮件检测

---

## 2.9 聚类算法

### 核心知识点
- [ ] K-Means 算法原理与步骤
- [ ] K 值选择：肘部法则（Elbow Method）
- [ ] 轮廓系数（Silhouette Score）
- [ ] K-Means 的局限性
- [ ] DBSCAN：基于密度的聚类
- [ ] 层次聚类（Hierarchical Clustering）
- [ ] 聚类结果可视化

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: K-Means](https://www.youtube.com/watch?v=4b5d3muPQmA) | 视频 | K-Means 可视化讲解 |
| [Scikit-learn 聚类文档](https://scikit-learn.org/stable/modules/clustering.html) | 文档 | 各种聚类算法对比 |

---

## 2.10 降维技术

### 核心知识点
- [ ] 为什么需要降维：维度灾难、可视化、去噪
- [ ] PCA 主成分分析原理
- [ ] 方差解释比（explained_variance_ratio_）
- [ ] 选择主成分数量
- [ ] t-SNE：非线性降维可视化
- [ ] UMAP：更快的非线性降维
- [ ] PCA vs t-SNE vs UMAP 对比

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: PCA](https://www.youtube.com/watch?v=FgakZw6K1QQ) | 视频 | PCA 原理讲解 |
| [StatQuest: t-SNE](https://www.youtube.com/watch?v=NEaUSP4YerM) | 视频 | t-SNE 可视化讲解 |

---

## 2.11 模型评估与调参

### 核心知识点
- [ ] 交叉验证：K-Fold、Stratified K-Fold、Leave-One-Out
- [ ] 分类指标：Accuracy、Precision、Recall、F1、AUC-ROC
- [ ] 回归指标：MSE、RMSE、MAE、R²、MAPE
- [ ] 混淆矩阵详解
- [ ] 分类报告（classification_report）
- [ ] 学习曲线（Learning Curve）分析
- [ ] 验证曲线（Validation Curve）分析
- [ ] 网格搜索（GridSearchCV）
- [ ] 随机搜索（RandomizedSearchCV）
- [ ] 贝叶斯优化（Optuna）
- [ ] 过拟合诊断与解决方案

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Scikit-learn 模型评估文档](https://scikit-learn.org/stable/modules/model_evaluation.html) | 文档 | 官方评估指南 |
| [Kaggle 模型验证课程](https://www.kaggle.com/learn/intro-to-machine-learning) | 课程 | 免费实操课程 |

---

## 2.12 集成学习

### 核心知识点
- [ ] 集成学习思想：三个臭皮匠顶个诸葛亮
- [ ] Bagging：Bootstrap Aggregating
- [ ] Boosting：序列化提升
- [ ] AdaBoost 原理
- [ ] Gradient Boosting 原理
- [ ] XGBoost：高效梯度提升
- [ ] LightGBM：更快的梯度提升
- [ ] CatBoost：处理类别特征
- [ ] Stacking 模型堆叠
- [ ] Voting 投票集成

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [StatQuest: AdaBoost](https://www.youtube.com/watch?v=LsK-xG1cLYA) | 视频 | AdaBoost 讲解 |
| [StatQuest: XGBoost](https://www.youtube.com/watch?v=OtD8wVaFm6E) | 视频 | XGBoost 系列 |
| [XGBoost 官方文档](https://xgboost.readthedocs.io/) | 文档 | 官方使用指南 |

---

## 2.13 综合实战

### 练习项目
- [ ] 项目一：泰坦尼克号生存预测（Kaggle 入门赛）
- [ ] 项目二：房价预测（回归问题）
- [ ] 项目三：信用卡欺诈检测（不平衡数据）
- [ ] 项目四：客户分群（聚类应用）

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Kaggle Titanic](https://www.kaggle.com/c/titanic) | 竞赛 | 经典入门竞赛 |
| [Kaggle House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) | 竞赛 | 回归入门竞赛 |
| [Scikit-learn 官方示例](https://scikit-learn.org/stable/auto_examples/) | 示例 | 各算法代码示例 |

---

> ✅ 完成本阶段后，你应该能够针对常见的分类和回归问题，选择合适的算法并完成建模。
>
> 👉 下一步：[03-深度学习](../03-deep-learning/README.md)
