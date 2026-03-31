# 第一阶段：Python 数据科学基础

> 这是 AI 学习的地基，扎实的 Python 数据处理能力会让后续学习事半功倍。

## 📚 知识点总览

- [1.1 Python 基础语法回顾](#11-python-基础语法回顾)
- [1.2 NumPy 数值计算](#12-numpy-数值计算)
- [1.3 Pandas 数据处理](#13-pandas-数据处理)
- [1.4 Matplotlib 数据可视化](#14-matplotlib-数据可视化)
- [1.5 Seaborn 高级可视化](#15-seaborn-高级可视化)
- [1.6 Jupyter Notebook 使用](#16-jupyter-notebook-使用)
- [1.7 综合实战](#17-综合实战)

---

## 1.1 Python 基础语法回顾

### 核心知识点
- [ ] 数据类型：int、float、str、bool、None
- [ ] 数据结构：list、tuple、dict、set
- [ ] 列表推导式与字典推导式
- [ ] 函数定义、参数传递（*args, **kwargs）
- [ ] Lambda 表达式与高阶函数（map、filter、reduce）
- [ ] 面向对象编程：类、继承、魔术方法
- [ ] 异常处理：try/except/finally
- [ ] 文件读写：open、with 语句、csv/json 处理
- [ ] 迭代器与生成器（yield）
- [ ] 装饰器基础
- [ ] 类型提示（Type Hints）

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Python 官方教程（中文）](https://docs.python.org/zh-cn/3/tutorial/) | 文档 | 官方权威教程 |
| [莫烦 Python 基础教程](https://mofanpy.com/tutorials/python-basic/) | 视频+文档 | 简洁易懂的中文教程 |
| [Python Cookbook 中文版](https://python3-cookbook.readthedocs.io/zh-cn/latest/) | 书籍 | 进阶技巧参考 |

---

## 1.2 NumPy 数值计算

### 核心知识点
- [ ] ndarray 创建：array、zeros、ones、arange、linspace
- [ ] 数组属性：shape、dtype、ndim、size
- [ ] 数组索引与切片（一维、多维、布尔索引、花式索引）
- [ ] 数组形状操作：reshape、flatten、ravel、transpose
- [ ] 广播机制（Broadcasting）原理与规则
- [ ] 数学运算：加减乘除、矩阵乘法（dot、@）
- [ ] 统计函数：mean、std、var、min、max、sum、argmax
- [ ] 排序与搜索：sort、argsort、where
- [ ] 随机数生成：random 模块（seed、rand、randn、randint、choice）
- [ ] 线性代数：linalg 模块（inv、det、eig、svd）
- [ ] 数组拼接与分割：concatenate、stack、split
- [ ] 向量化运算 vs 循环的性能对比

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [NumPy 官方入门教程](https://numpy.org/doc/stable/user/absolute_beginners.html) | 文档 | 官方新手指南 |
| [莫烦 NumPy 教程](https://mofanpy.com/tutorials/data-manipulation/numpy/) | 视频 | 中文视频讲解 |
| [NumPy 100 题](https://github.com/rougier/numpy-100) | 练习 | 经典练习题集 |

---

## 1.3 Pandas 数据处理

### 核心知识点
- [ ] Series 与 DataFrame 创建与基本操作
- [ ] 数据读取：read_csv、read_excel、read_json、read_sql
- [ ] 数据查看：head、tail、info、describe、shape、dtypes
- [ ] 数据选择：loc（标签）、iloc（位置）、条件筛选
- [ ] 缺失值处理：isnull、dropna、fillna
- [ ] 重复值处理：duplicated、drop_duplicates
- [ ] 数据类型转换：astype、to_datetime、to_numeric
- [ ] 字符串操作：str 访问器（contains、replace、split、strip）
- [ ] 分组聚合：groupby、agg、transform、apply
- [ ] 数据合并：merge、join、concat
- [ ] 透视表：pivot_table、crosstab
- [ ] 排序：sort_values、sort_index
- [ ] 时间序列：DatetimeIndex、resample、shift、rolling
- [ ] 数据导出：to_csv、to_excel、to_json
- [ ] 链式操作与 pipe 方法
- [ ] 大数据量优化：分块读取（chunksize）、数据类型优化

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Pandas 官方入门教程](https://pandas.pydata.org/docs/getting_started/intro_tutorials/) | 文档 | 10 分钟入门 Pandas |
| [Joyful Pandas](https://datawhalechina.github.io/joyful-pandas/) | 教程 | Datawhale 出品的中文教程 |
| [Kaggle Pandas 课程](https://www.kaggle.com/learn/pandas) | 交互课程 | 免费实操练习 |
| [Pandas 练习题](https://github.com/guipsamora/pandas_exercises) | 练习 | 分主题练习 |

---

## 1.4 Matplotlib 数据可视化

### 核心知识点
- [ ] Figure 与 Axes 对象模型
- [ ] 基础图表：折线图（plot）、散点图（scatter）、柱状图（bar）
- [ ] 直方图（hist）、饼图（pie）、箱线图（boxplot）
- [ ] 图表装饰：标题（title）、标签（xlabel/ylabel）、图例（legend）
- [ ] 坐标轴设置：xlim/ylim、xticks/yticks、刻度格式化
- [ ] 子图布局：subplot、subplots、GridSpec
- [ ] 颜色与样式：colormap、linestyle、marker
- [ ] 文本标注：text、annotate
- [ ] 图片保存：savefig（分辨率、格式）
- [ ] 中文显示配置（解决乱码问题）
- [ ] 面向对象 API vs pyplot API 的区别

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Matplotlib 官方教程](https://matplotlib.org/stable/tutorials/index.html) | 文档 | 官方系统教程 |
| [Matplotlib 速查表](https://github.com/matplotlib/cheatsheets) | 参考 | 官方速查表 PDF |
| [莫烦 Matplotlib 教程](https://mofanpy.com/tutorials/data-manipulation/plt/) | 视频 | 中文视频讲解 |

---

## 1.5 Seaborn 高级可视化

### 核心知识点
- [ ] Seaborn 与 Matplotlib 的关系
- [ ] 分布图：histplot、kdeplot、rugplot
- [ ] 关系图：scatterplot、lineplot、relplot
- [ ] 分类图：boxplot、violinplot、swarmplot、barplot、countplot
- [ ] 热力图：heatmap（相关性矩阵可视化）
- [ ] 回归图：regplot、lmplot
- [ ] 多变量关系：pairplot、jointplot
- [ ] FacetGrid 分面绑定
- [ ] 主题与调色板：set_theme、set_palette

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Seaborn 官方教程](https://seaborn.pydata.org/tutorial.html) | 文档 | 官方教程与示例 |
| [Seaborn 图表画廊](https://seaborn.pydata.org/examples/index.html) | 示例 | 各类图表代码示例 |

---

## 1.6 Jupyter Notebook 使用

### 核心知识点
- [ ] Jupyter Notebook / JupyterLab 安装与启动
- [ ] Cell 类型：Code、Markdown、Raw
- [ ] 常用快捷键（运行、插入、删除、切换类型）
- [ ] Magic 命令：%timeit、%matplotlib inline、%%time、%who
- [ ] Shell 命令执行（!pip install）
- [ ] Markdown 语法在 Notebook 中的使用
- [ ] 变量检查与调试
- [ ] 导出格式：HTML、PDF、Python 脚本
- [ ] Google Colab 使用（免费 GPU）

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Jupyter 官方文档](https://jupyter.org/documentation) | 文档 | 官方使用指南 |
| [Google Colab](https://colab.research.google.com/) | 平台 | 免费在线 Notebook 环境 |
| [28 个 Jupyter 技巧](https://www.dataquest.io/blog/jupyter-notebook-tips-tricks-shortcuts/) | 文章 | 实用技巧合集 |

---

## 1.7 综合实战

### 练习项目
- [ ] 项目一：泰坦尼克号生存预测数据分析（Kaggle 经典数据集）
- [ ] 项目二：电影数据集探索性分析（IMDB / 豆瓣）
- [ ] 项目三：中国城市空气质量数据可视化

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Kaggle Titanic 数据集](https://www.kaggle.com/c/titanic) | 数据集 | 经典入门数据集 |
| [Kaggle 数据分析入门课](https://www.kaggle.com/learn/intro-to-machine-learning) | 课程 | 免费交互课程 |
| [天池数据集](https://tianchi.aliyun.com/dataset) | 平台 | 阿里云中文数据集平台 |

---

> ✅ 完成本阶段后，你应该能够熟练使用 Python 进行数据读取、清洗、分析和可视化。
>
> 👉 下一步：[02-机器学习](../02-machine-learning/README.md)
