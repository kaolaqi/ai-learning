# 第四阶段：大语言模型（LLM）

> 理解 LLM 的原理与能力边界，掌握 Prompt Engineering，能基于 LLM API 开发应用，了解 RAG 和微调技术。

## 📚 知识点总览

- [4.1 LLM 基础概念](#41-llm-基础概念)
- [4.2 Tokenization 分词](#42-tokenization-分词)
- [4.3 预训练与微调范式](#43-预训练与微调范式)
- [4.4 Prompt Engineering](#44-prompt-engineering)
- [4.5 LLM API 调用与应用开发](#45-llm-api-调用与应用开发)
- [4.6 Embedding 与向量数据库](#46-embedding-与向量数据库)
- [4.7 RAG 检索增强生成](#47-rag-检索增强生成)
- [4.8 微调技术](#48-微调技术)
- [4.9 模型评估与对齐](#49-模型评估与对齐)
- [4.10 开源模型生态](#410-开源模型生态)
- [4.11 综合实战](#411-综合实战)

---

## 4.1 LLM 基础概念

### 核心知识点
- [ ] 什么是大语言模型：基于 Transformer 的自回归语言模型
- [ ] LLM 的发展历程：GPT → GPT-2 → GPT-3 → ChatGPT → GPT-4
- [ ] 涌现能力（Emergent Abilities）：规模带来的质变
- [ ] 上下文窗口（Context Window）的概念与限制
- [ ] Temperature 与 Top-p 采样策略
- [ ] Token 与计费方式
- [ ] 幻觉问题（Hallucination）
- [ ] LLM 的能力边界：擅长什么、不擅长什么
- [ ] 主流模型对比：GPT-4、Claude、Gemini、Llama、Qwen、DeepSeek

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [State of GPT（Andrej Karpathy）](https://www.youtube.com/watch?v=bZQun8Y4L2A) | 视频 | LLM 训练全流程讲解 |
| [Intro to LLMs（Andrej Karpathy）](https://www.youtube.com/watch?v=zjkBMFhNj_g) | 视频 | 1小时LLM入门 |
| [李宏毅：ChatGPT 原理](https://www.youtube.com/watch?v=yiY4nPOzJEg) | 视频 | 中文讲解 ChatGPT 原理 |

---

## 4.2 Tokenization 分词

### 核心知识点
- [ ] 什么是 Token：文本的最小处理单元
- [ ] 字符级 vs 词级 vs 子词级分词
- [ ] BPE（Byte Pair Encoding）算法
- [ ] WordPiece 算法（BERT 使用）
- [ ] SentencePiece（多语言支持）
- [ ] tiktoken（OpenAI 的分词器）
- [ ] 中文分词的特殊性
- [ ] Token 数量与成本、上下文长度的关系
- [ ] 如何计算 Token 数量

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Andrej Karpathy: Tokenization](https://www.youtube.com/watch?v=zduSFxRajkE) | 视频 | 深入讲解 Tokenization |
| [OpenAI Tokenizer](https://platform.openai.com/tokenizer) | 工具 | 在线 Token 计算工具 |
| [Hugging Face Tokenizers 文档](https://huggingface.co/docs/tokenizers/) | 文档 | 分词器库文档 |

---

## 4.3 预训练与微调范式

### 核心知识点
- [ ] 预训练（Pre-training）：在大规模语料上学习语言知识
- [ ] 自监督学习：下一个 Token 预测（GPT）、掩码语言模型（BERT）
- [ ] 监督微调（SFT, Supervised Fine-Tuning）
- [ ] RLHF（基于人类反馈的强化学习）
  - [ ] 奖励模型（Reward Model）
  - [ ] PPO 算法
- [ ] DPO（Direct Preference Optimization）：RLHF 的简化替代
- [ ] 指令微调（Instruction Tuning）
- [ ] 对话格式训练
- [ ] 预训练 → SFT → RLHF 的完整流程

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [InstructGPT 论文解读](https://www.youtube.com/watch?v=VPRSBzXzavo) | 视频 | RLHF 原始论文讲解 |
| [Chip Huyen: RLHF 详解](https://huyenchip.com/2023/05/02/rlhf.html) | 文章 | RLHF 全面解析 |
| [李宏毅：RLHF 讲解](https://www.youtube.com/watch?v=73_2V2mGYKI) | 视频 | 中文 RLHF 讲解 |

---

## 4.4 Prompt Engineering

### 核心知识点
- [ ] Prompt 的基本结构：指令、上下文、输入、输出格式
- [ ] Zero-shot Prompting：零样本提示
- [ ] Few-shot Prompting：少样本提示
- [ ] Chain-of-Thought（CoT）：思维链提示
- [ ] Self-Consistency：自一致性
- [ ] Tree of Thoughts（ToT）：思维树
- [ ] ReAct：推理+行动
- [ ] 角色设定（System Prompt）
- [ ] 输出格式控制：JSON、Markdown、XML
- [ ] 提示词注入攻击与防御
- [ ] 提示词模板化与版本管理
- [ ] 多轮对话中的上下文管理
- [ ] 提示词调试与迭代技巧

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Prompt Engineering Guide（中文）](https://www.promptingguide.ai/zh) | 教程 | 最全面的提示工程指南 |
| [OpenAI Prompt Engineering 指南](https://platform.openai.com/docs/guides/prompt-engineering) | 文档 | 官方最佳实践 |
| [吴恩达: ChatGPT Prompt Engineering](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/) | 课程 | 免费短课程 |
| [Learn Prompting](https://learnprompting.org/zh-Hans/docs/intro) | 教程 | 系统化学习提示工程 |

---

## 4.5 LLM API 调用与应用开发

### 核心知识点
- [ ] OpenAI API 调用：Chat Completions API
- [ ] Claude API 调用：Messages API
- [ ] 国内模型 API：通义千问、文心一言、DeepSeek、智谱
- [ ] API 参数详解：model、messages、temperature、max_tokens、stop
- [ ] 流式输出（Streaming）
- [ ] Function Calling / Tool Use
- [ ] 多模态输入：图片、音频
- [ ] 结构化输出（Structured Output / JSON Mode）
- [ ] 错误处理与重试策略
- [ ] Token 用量优化与成本控制
- [ ] API Key 安全管理
- [ ] 速率限制（Rate Limiting）处理

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [OpenAI API 文档](https://platform.openai.com/docs/api-reference) | 文档 | 官方 API 参考 |
| [Anthropic Claude API 文档](https://docs.anthropic.com/) | 文档 | Claude API 参考 |
| [吴恩达: Building Systems with ChatGPT](https://www.deeplearning.ai/short-courses/building-systems-with-chatgpt/) | 课程 | 构建 LLM 应用 |

---

## 4.6 Embedding 与向量数据库

### 核心知识点
- [ ] 什么是文本 Embedding：将文本映射为稠密向量
- [ ] Word2Vec：词向量的开创性工作
- [ ] Sentence Embedding：句子级别的向量表示
- [ ] OpenAI Embedding API
- [ ] 开源 Embedding 模型：BGE、E5、GTE
- [ ] 向量相似度计算：余弦相似度、欧氏距离、点积
- [ ] 向量数据库概念与选型
  - [ ] Chroma：轻量级本地向量数据库
  - [ ] Pinecone：云端托管向量数据库
  - [ ] Milvus：开源分布式向量数据库
  - [ ] Weaviate：带语义搜索的向量数据库
  - [ ] FAISS：Facebook 的向量检索库
- [ ] 向量索引类型：Flat、IVF、HNSW
- [ ] 元数据过滤
- [ ] 混合搜索：向量搜索 + 关键词搜索

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Pinecone 学习中心](https://www.pinecone.io/learn/) | 教程 | 向量数据库系统教程 |
| [吴恩达: Vector Databases](https://www.deeplearning.ai/short-courses/vector-databases-embeddings-applications/) | 课程 | 向量数据库短课程 |
| [MTEB 排行榜](https://huggingface.co/spaces/mteb/leaderboard) | 排行榜 | Embedding 模型评测 |

---

## 4.7 RAG 检索增强生成

### 核心知识点
- [ ] RAG 的核心思想：检索 + 生成
- [ ] RAG 解决的问题：知识时效性、幻觉、领域知识
- [ ] RAG 基本流程：文档加载 → 分块 → Embedding → 存储 → 检索 → 生成
- [ ] 文档加载：PDF、Word、HTML、Markdown 解析
- [ ] 文本分块策略
  - [ ] 固定大小分块
  - [ ] 按语义分块
  - [ ] 递归字符分块
  - [ ] 重叠（Overlap）的作用
- [ ] 检索策略
  - [ ] 相似度检索
  - [ ] MMR（最大边际相关性）
  - [ ] 重排序（Reranking）
  - [ ] 混合检索
- [ ] 上下文压缩
- [ ] 多轮对话中的 RAG
- [ ] RAG 评估：检索质量、生成质量
- [ ] 高级 RAG 技术
  - [ ] 查询改写（Query Rewriting）
  - [ ] HyDE（假设文档嵌入）
  - [ ] Self-RAG
  - [ ] Graph RAG

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [吴恩达: Building RAG Agents](https://www.deeplearning.ai/short-courses/building-agentic-rag-with-llamaindex/) | 课程 | RAG Agent 短课程 |
| [LangChain RAG 教程](https://python.langchain.com/docs/tutorials/rag/) | 教程 | 官方 RAG 教程 |
| [RAG 论文原文](https://arxiv.org/abs/2005.11401) | 论文 | RAG 原始论文 |

---

## 4.8 微调技术

### 核心知识点
- [ ] 全参数微调（Full Fine-tuning）
- [ ] 参数高效微调（PEFT）概述
- [ ] LoRA（Low-Rank Adaptation）
  - [ ] 低秩分解原理
  - [ ] rank 参数选择
  - [ ] alpha 参数
  - [ ] 目标模块选择
- [ ] QLoRA：量化 + LoRA
- [ ] Adapter Tuning
- [ ] Prefix Tuning / P-Tuning
- [ ] 微调数据准备
  - [ ] 指令数据格式：instruction / input / output
  - [ ] 对话数据格式
  - [ ] 数据质量 > 数据数量
- [ ] 微调工具
  - [ ] Hugging Face Transformers + PEFT
  - [ ] LLaMA-Factory
  - [ ] Axolotl
- [ ] 微调评估与过拟合检测
- [ ] 模型合并（Model Merging）
- [ ] 量化部署：GPTQ、AWQ、GGUF

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Hugging Face PEFT 文档](https://huggingface.co/docs/peft) | 文档 | 官方 PEFT 库文档 |
| [吴恩达: Finetuning LLMs](https://www.deeplearning.ai/short-courses/finetuning-large-language-models/) | 课程 | 微调短课程 |
| [LoRA 论文](https://arxiv.org/abs/2106.09685) | 论文 | LoRA 原始论文 |
| [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) | 工具 | 一站式微调框架 |

---

## 4.9 模型评估与对齐

### 核心知识点
- [ ] 困惑度（Perplexity）
- [ ] BLEU、ROUGE 评分
- [ ] 人工评估 vs 自动评估
- [ ] LLM-as-Judge：用 LLM 评估 LLM
- [ ] 基准测试：MMLU、HumanEval、GSM8K、MT-Bench
- [ ] 安全对齐（Safety Alignment）
- [ ] 红队测试（Red Teaming）
- [ ] 宪法 AI（Constitutional AI）
- [ ] 开放排行榜：Open LLM Leaderboard、Chatbot Arena

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Chatbot Arena](https://chat.lmsys.org/) | 平台 | LLM 对战排行榜 |
| [Open LLM Leaderboard](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard) | 排行榜 | 开源模型评测 |

---

## 4.10 开源模型生态

### 核心知识点
- [ ] Llama 系列（Meta）：Llama 2 → Llama 3
- [ ] Qwen 系列（阿里）：通义千问开源模型
- [ ] DeepSeek 系列：DeepSeek-V2、DeepSeek-Coder
- [ ] ChatGLM 系列（智谱）
- [ ] Mistral / Mixtral（Mistral AI）
- [ ] Yi 系列（零一万物）
- [ ] Phi 系列（Microsoft）：小模型大能力
- [ ] 模型下载与使用：Hugging Face Hub
- [ ] 本地部署工具
  - [ ] Ollama：一键本地运行
  - [ ] llama.cpp：CPU 推理
  - [ ] vLLM：高性能推理服务
  - [ ] Text Generation Inference（TGI）
- [ ] 模型量化：4bit、8bit、GGUF 格式

### 推荐资源
| 资源 | 类型 | 说明 |
|------|------|------|
| [Hugging Face Hub](https://huggingface.co/models) | 平台 | 模型下载与分享 |
| [Ollama](https://ollama.ai/) | 工具 | 本地运行 LLM |
| [vLLM 文档](https://docs.vllm.ai/) | 文档 | 高性能推理框架 |

---

## 4.11 综合实战

### 练习项目
- [ ] 项目一：基于 OpenAI API 构建命令行聊天机器人
- [ ] 项目二：构建 RAG 知识库问答系统
- [ ] 项目三：使用 LoRA 微调一个中文对话模型
- [ ] 项目四：搭建本地 LLM 服务（Ollama + Open WebUI）
- [ ] 项目五：多文档 RAG 系统（支持 PDF、Markdown）

---

> ✅ 完成本阶段后，你应该能够使用 LLM API 开发应用，构建 RAG 系统，并了解微调的基本流程。
>
> 👉 下一步：[05-AI Agent](../05-ai-agent/README.md)
