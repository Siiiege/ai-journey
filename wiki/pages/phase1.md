# Phase 1 · 十二周计划概览

> Source: [../../docs/phase1-plan.md](../../docs/phase1-plan.md)（打勾追踪在那里，本页只做概览与快照）
> 状态快照：2026-10-22 —— W0 完成；W1 进行中（跟敲刚起步，`weeks/code/micrograd.py` 尚未展开）

## 阶段骨架

| 周 | 主题 | 关键验收 |
|---|---|---|
| W0 | 启动 | ✅ 仓库 + JD 分析完成 |
| W1-2 | micrograd：手写反向传播 | W2 扩展算子（ReLU/pow/exp）梯度与 PyTorch autograd **对拍** |
| W3-4 | makemore：bigram → MLP 语言模型 | 能讲清采样温度、train/val loss |
| W5-6 | Let's build GPT | **先不看视频自己实现 single-head attention 再对答案**；`nanoGPT-mine` 禁止复制粘贴 |
| W7 | 训练 + 博客 2 | 莎士比亚语料出效果，README 放 loss 曲线与生成样例 |
| W8-9 | HuggingFace 速成 + 定微调任务 + 数据工程 | baseline 指标 + 50~100 条评测集入库；一条命令跑完「推理 + 打分」 |
| W10 | LoRA 微调（AutoDL 租 GPU，Qwen 0.5B~1.5B） | checkpoint + 训练日志入库，模型上 HF Hub |
| W11-12 | 对比实验 + 博客 3 + 复盘排 Phase 2 | baseline vs 微调对比表，诚实分析失败案例 |

## 运行规则（提炼）

- 每周预算 8~10 小时（视频跟敲 4h + 作业 4h + 笔记复盘 2h）。
- **验收没达成顺延，不跳过**——宁可慢一周，不糊弄一个验收。
- 阶段完成标志：2 个手写实现 + 1 个微调作品 + 3 篇博客/长笔记。
- 每周日晚 30 分钟仪式：笔记收尾、README 更新、写下周 3 件事（wiki 的 INGEST/LINT 挂在这个仪式上，见 [../AGENTS.md](../AGENTS.md)）。

相关页：[./micrograd.md](./micrograd.md)、[./backpropagation.md](./backpropagation.md)、[./goal.md](./goal.md)
