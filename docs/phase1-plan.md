# AI 转型 · 第一阶段计划（12 周）

> 定位：在职前端开发者 → AI 应用工程师（AI 全栈方向）
> 每周预算：8~10 小时（视频跟敲 4h + 动手作业 4h + 笔记复盘 2h）
> 阶段完成标志：GitHub 上有 2 个手写实现 + 1 个微调作品 + 3 篇博客/长笔记
> 规则：验收标准没达成就顺延，不跳过；宁可慢一周，不糊弄一个验收。

## Week 0 · 启动 ✅（2026-10-13 完成）

- [x] 建 `ai-journey` 仓库，本计划入库
- [x] 目标 JD 分析（docs/jd-analysis.md）
- [ ] Profile README 发布（草稿在 profile-README.md，建 Siiiege/Siiiege 仓库后启用）
- [ ] Python venv + PyTorch 安装（本机 MX550 4GB 可跑 W1-9；W10 微调租 AutoDL）

## Week 1 · micrograd（上）

- 学：Karpathy《The spelled-out intro to neural networks and backpropagation》前半
- 做：跟敲 `Value` 类、加法/乘法节点的反向传播，每行自己敲
- 笔记：计算图 → 链式法则的对应关系画一张图
- 验收：能脱稿讲清"为什么加法节点的梯度是直通、乘法节点要交换偏导"

## Week 2 · micrograd（下）+ 自己的扩展

- 学：视频后半（neuron / MLP / 训练）
- 做：**自己的扩展**（和只看教程的人拉开差距的点）：把 tanh 换成 ReLU，手推梯度并实现；或加一个 `pow` / `exp` 算子
- 产出：笔记 1《手写反向传播》
- 验收：扩展算子的梯度能通过对拍（和 PyTorch autograd 对比数值）

## Week 3 · 第一个语言模型（makemore：bigram → MLP）

- 学：makemore part 1（bigram）+ part 2（Bengio 式 MLP）
- 按需补：softmax、交叉熵、embedding（遇到再查，不开数学课）
- 做：跟敲并训练，loss 曲线和生成样例截图进笔记
- 验收：能讲清"采样温度"和"训练 loss vs 验证 loss"分别说明什么

## Week 4 · 缓冲周 + Transformer 预习

- 学：makemore part 3（1.25 倍速，知道"为什么要初始化/归一化"即可）+ 通读 The Illustrated Transformer
- 做：补前三周欠账
- 验收：能用自己的话说清 self-attention 的 Q/K/V 各自在干什么

## Week 5 · Let's build GPT（上）：亲手写 attention

- 学：Karpathy《Let's build GPT: from scratch》前半
- 做：**先自己实现 single-head self-attention（不看视频），再对答案**——本阶段最值钱的练习
- 验收：白板写出 scaled dot-product attention 公式并解释为什么要除以 √d

## Week 6 · Let's build GPT（下）：完整的 GPT

- 学：视频后半（MultiHead、Block、生成采样）
- 做：全部代码敲进自己的仓库 `nanoGPT-mine`（**禁止复制粘贴**）
- 验收：`nanoGPT-mine` 有像样的 README（是什么/怎么跑/结构图）

## Week 7 · 训练 + 博客 2

- 做：char-level 莎士比亚语料训练出效果；README 放 loss 曲线 + 生成样例
- 写：博客 2《从零手写一个 GPT》
- 加分：跑通官方 nanoGPT，对比缺了什么（KV cache？优化器？）

## Week 8 · HuggingFace 速成 + 定微调任务

- 学：HF LLM Course 核心章节（pipeline / tokenizer / Trainer / datasets）
- 定任务（具体、可量化）：结构化抽取（自然语言 → 固定 JSON schema）或垂直短文本分类
- 做：baseline——不微调直接 prompt + 建一个 50~100 条评测集
- ⚠️ 不用公司敏感数据
- 验收：baseline 指标出来，评测集入库

## Week 9 · 数据工程周

- 做：构造/清洗训练集（几百~几千条）；train/eval 切分；评测脚本
- 验收：一条命令跑完"推理 + 打分"

## Week 10 · LoRA 微调

- 学：PEFT 文档（rank、alpha、target_modules）
- 做：AutoDL 租 GPU，LoRA 微调 Qwen 0.5B~1.5B；记录超参和 loss 曲线
- 验收：checkpoint + 训练日志入库（模型放 HF Hub）

## Week 11 · 对比实验 + README 打磨

- 做：baseline vs 微调对比表；**诚实分析失败案例**
- 做：作品 1 README 终稿
- 验收：陌生人 10 分钟能跑通你的项目

## Week 12 · 博客 3 + 复盘

- 写：博客 3《LoRA 微调实战：从数据到评测》
- 做：pinned 调整；复盘并排 Phase 2（RAG/Agent/Evals）计划

## 每周固定仪式

- 周日晚 30 分钟：笔记收尾、README 更新、写下周 3 件事
- 小步提交：有意义的最小单元一个 commit
- 仓库 README 模板：**是什么 / 为什么 / 效果（图+指标）/ 怎么跑 / 踩坑记录**
