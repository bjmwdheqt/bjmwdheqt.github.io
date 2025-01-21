机器之心编辑部

Meta 开源的大模型系列 LLaMA 的评测结果出炉。尽管与 ChatGPT 仍有差距，但其性能表现和潜力引发了广泛关注。

## LLaMA模型亮点与初步评测

Meta 最近发布了 LLaMA（Large Language Model Meta AI）系列模型，参数量从 70 亿到 650 亿不等。相比 GPT-3 等大模型，LLaMA 参数量更少但性能更优。例如，130 亿参数的 LLaMA 模型在大多数基准测试中胜过 1750 亿参数的 GPT-3，并且可以在单块 V100 GPU 上运行。最大的 650 亿参数版本甚至可以媲美谷歌的 Chinchilla-70B 和 PaLM-540B。

然而，LLaMA 的实际表现是否如论文所述？研究者们对其进行了多项测试，包括笑话解释、零样本分类和代码生成。

### 笑话解释任务

在笑话解释任务中，LLaMA 的表现不尽如人意。尽管 LLaMA-33B 和 ChatGPT 在某些情况下能够捕捉到笑点，但生成的文本大多缺乏逻辑性。总体来看，这些模型在该任务上的表现与谷歌 PaLM 相差甚远。

### 零样本分类任务

在标题党分类任务中，LLaMA-33B 是唯一能够遵循所有请求格式（yes/no）的模型，且预测结果较为合理。相比之下，ChatGPT 的预测有时不够准确，格式也存在错误。较小的 LLaMA 模型（7B/13B）在该任务中表现较差。

### 代码生成任务

在代码生成任务中，LLaMA 的表现逊色于 ChatGPT。尽管 LLaMA 能够生成 SQL 查询，但其准确性和实用性不如 ChatGPT。

## LLaMA的优化与ChatLLaMA的出现

为了弥补 LLaMA 的短板，初创公司 Nebuly AI 开源了基于 RLHF（强化学习与人类反馈）的 ChatLLaMA 训练方法。ChatLLaMA 的训练过程类似于 ChatGPT，支持所有 LLaMA 模型架构（7B、13B、33B、65B），并且训练速度更快、成本更低。

### ChatLLaMA的优势

1. **完整开源**：允许用户基于预训练的 LLaMA 模型构建 ChatGPT 风格的服务。
2. **高效训练**：支持 DeepSpeed ZERO 加速微调过程，单 GPU 推理速度更快。
3. **灵活架构**：支持多种模型架构，用户可根据需求选择适合的模型。

研究者表示，ChatLLaMA 的训练速度最高可比 ChatGPT 快 15 倍，但这一说法尚需进一步验证。

### 如何使用 ChatLLaMA？

以下是 ChatLLaMA 的基本使用步骤：

1. 安装软件包：
   bash
   pip install chatllama-py
   
2. 克隆 LLaMA 模型：
   bash
   git clone https://github.com/facebookresearch/llama.git
   cd llama
   pip install -r requirements.txt
   pip install -e .
   
3. 运行训练示例：项目中提供了 ChatLLaMA 7B 的训练示例，感兴趣的用户可以参考原项目。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)

## 总结

LLaMA 的发布为大模型研究带来了新的可能性。尽管其在某些任务上的表现仍不及 ChatGPT，但通过引入 RLHF 等优化方法，LLaMA 的潜力正在逐步释放。未来，随着更多研究者的加入，LLaMA 有望成为更高效、更开放的 AI 助手。

👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)