# 术语表

> 遇到不认识的词就来这里查。按主题分组，每条都给大白话解释。

---

## 一、最基础的几个

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **人工智能** | AI | 让机器表现得聪明的总称，是个大筐 |
| **机器学习** | Machine Learning | 不给规则，给例子，让机器自己找规律 |
| **深度学习** | Deep Learning | 用多层神经网络找规律 |
| **大语言模型** | LLM | 专门处理语言的超大神经网络，如 GPT、Claude、Qwen |
| **生成式 AI** | Generative AI | 能"生成"新内容的 AI（写文章、画图），对应"做选择题"的判别式 AI |
| **多模态** | Multimodal | 能处理文字、图片、声音等多种类型 |

---

## 二、模型的组成

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **参数** | Parameters | 模型内部的"旋钮"，7B 就是 70 亿个旋钮 |
| **权重** | Weights | 参数的具体数值 |
| **神经网络** | Neural Network | 模仿大脑的多层计算结构 |
| **Transformer** | - | 现在所有主流大模型的底层结构 |
| **注意力机制** | Attention | 处理某个词时，决定该重点看句中哪些词 |
| **层** | Layer | 网络的一层处理，大模型有几十到上百层 |
| **MoE** | Mixture of Experts | 混合专家，只激活部分参数，省算力 |

---

## 三、文本处理

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **token** | - | 模型眼里的"字"，约半个词或 1–2 个汉字 |
| **分词** | Tokenization | 把文字切成 token 的过程 |
| **上下文窗口** | Context Window | 一次能看多少 token 的上限（如 128K） |
| **上下文** | Context | 这次对话模型能看到的全部内容 |
| **向量 / 嵌入** | Embedding | 把文字变成一串数字，用于比较语义相似度 |
| **语义相似度** | Semantic Similarity | 两段话意思像不像（用向量距离算） |

---

## 四、训练相关

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **预训练** | Pre-training | 读海量文本，学会语言规律（最贵的一步） |
| **微调** | Fine-tuning | 用你的数据再训练一遍，改变它的行为习惯 |
| **LoRA** | - | 一种省显存的微调方法，只训一小块"外挂" |
| **SFT** | Supervised Fine-Tuning | 用人类写的问答示范来训练 |
| **RLHF** | Reinforcement Learning from Human Feedback | 根据人类的"哪个回答更好"来调整 |
| **DPO** | Direct Preference Optimization | RLHF 的简化替代方案 |
| **对齐** | Alignment | 让 AI 的行为符合人类价值和意图 |
| **过拟合** | Overfitting | 死记硬背训练数据，换个场景就不行 |
| **基座模型** | Base Model | 只预训练过、还不会对话的原始模型 |
| **灾难性遗忘** | Catastrophic Forgetting | 微调后忘了原来的能力 |

---

## 五、推理相关

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **推理** | Inference | 用训练好的模型生成回答（日常用 AI 就是在推理） |
| **自回归** | Autoregressive | 一个词一个词地生成 |
| **温度** | Temperature | 控制随机性的旋钮，越低越稳 |
| **top_p** | - | 只在概率最高的那部分词里挑 |
| **KV Cache** | - | 缓存已经算过的内容，加速生成 |
| **思维链** | Chain-of-Thought | 让它先写出推理步骤再给答案 |
| **推理模型** | Reasoning Model | 专门优化了"先想很久再答"的模型 |
| **量化** | Quantization | 压缩模型精度，减小体积和显存 |

---

## 六、应用相关

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **提示词** | Prompt | 你输入给 AI 的话 |
| **系统提示** | System Prompt | 给 AI 的"总规则"，优先级较高 |
| **少样本** | Few-shot | 在提示词里给几个例子 |
| **RAG** | Retrieval-Augmented Generation | 先查资料再回答 |
| **切分** | Chunking | 把长文档切成小段落以便检索 |
| **重排** | Rerank | 对检索结果二次排序，提高精度 |
| **向量数据库** | Vector DB | 专门存向量并做相似度检索的数据库 |
| **Agent** | - | 能自己规划、调用工具、连续做多步的 AI |
| **工具调用** | Tool / Function Calling | 模型"申请"执行操作，由程序真正执行 |
| **MCP** | Model Context Protocol | 让工具能被任何 AI 应用使用的标准协议 |
| **多 Agent** | Multi-Agent | 多个 Agent 分工协作 |

---

## 七、成本与限制

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **输入 token** | Input tokens | 你发给模型的内容，按 token 收费 |
| **输出 token** | Output tokens | 模型生成的内容，通常更贵 |
| **速率限制** | Rate Limit | 单位时间内能调用多少次的上限 |
| **TPM / RPM** | Tokens / Requests Per Minute | 每分钟 token 数 / 请求数上限 |
| **缓存命中** | Prompt Caching | 相同前缀的内容可以打折计费 |
| **流式输出** | Streaming | 边生成边返回，像打字机 |

---

## 八、问题与风险

| 术语 | 英文 | 大白话 |
| --- | --- | --- |
| **幻觉** | Hallucination | 一本正经地编造不存在的内容 |
| **提示词注入** | Prompt Injection | 有人在资料里藏指令，骗 AI 去执行 |
| **越狱** | Jailbreak | 想办法让 AI 突破安全限制 |
| **护栏** | Guardrails | 检查输入输出的安全机制 |
| **人在回路** | Human-in-the-loop | 关键步骤需要人确认 |
| **沙箱** | Sandbox | 隔离的执行环境，搞坏了也影响不到外面 |

---

## 九、常见缩写

| 缩写 | 全称 | 意思 |
| --- | --- | --- |
| **LLM** | Large Language Model | 大语言模型 |
| **GPT** | Generative Pre-trained Transformer | 一类模型的名字 |
| **RAG** | Retrieval-Augmented Generation | 检索增强生成 |
| **SFT** | Supervised Fine-Tuning | 监督微调 |
| **RLHF** | Reinforcement Learning from Human Feedback | 人类反馈强化学习 |
| **CoT** | Chain-of-Thought | 思维链 |
| **MCP** | Model Context Protocol | 模型上下文协议 |
| **AGI** | Artificial General Intelligence | 通用人工智能（还不是现实） |

---

## 十、容易混淆的几组

| 容易混 | 区别 |
| --- | --- |
| 参数 vs 超参数 | 参数是机器自己学的；超参数是你手动设的（层数、学习速度） |
| 训练 vs 推理 | 训练是教它；推理是用它 |
| 提示词 vs 微调 | 前者不改模型；后者改参数 |
| RAG vs 微调 | RAG 加知识；微调改行为 |
| token vs 字 | token 是模型的处理单位，不是字也不是词 |
| 模型 vs 产品 | 模型是技术；ChatGPT、Claude 是用模型做的产品 |
| 开源 vs 闭源 | 开源可下载自建；闭源只能调 API |
| 幻觉 vs 说谎 | 它没有撒谎的意图，只是生成了像真的内容 |
| Agent vs RAG | RAG 只会查；Agent 能查+能做+能规划 |
| 上下文 vs 记忆 | 上下文是"这次能看到的"；记忆是"长期保留的"（模型本身没有） |
