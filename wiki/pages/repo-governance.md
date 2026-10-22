# 作品 1 · repo-governance（已发布）

> Source: [../../docs/milestones.md](../../docs/milestones.md)、[Siiiege/repo-governance](https://github.com/Siiiege/repo-governance)（评测全记录在其 docs/evaluation.md）

2026-10-15 上线的 agent 协作治理 skill：给「人和 agent 隔着多个会话持续干活的仓库」装上任务卡生命周期、决策记录和文档门禁（check-docs，零依赖，Node/Python 双实现）。

## 对转型路线的意义

「agents & evals」方向第一个拿得出手的实物——**skill 本身之外，更重要的是配套的评测方法学**，并靠它把作品打磨到能发布：

- 执行者与检测者分离：每个被治理仓库交给干净上下文的子代理，作者只做事后核验。
- 三轮六仓实测：husky / click / duf / bat / awesome / SDD-Lite 浅克隆。
- 负例注入与退出条款：对已治理仓库重发指令必须零改动退出。
- 冷启动测试：新会话只靠仓内文档答「做到哪了 / 为何这么决定 / 从哪下手」三问。
- 按发现驱动迭代：约 20 条缝隙全部回填或明确留观。

这正对应 JD 里两处核心职责「评测 / 观测」的提前落地 → [./jd-gap.md](./jd-gap.md)。

## 后续演进（会话记录 2026-10-16）

发布后在 rsra 仓库的真实使用中回灌改进：任务号锚定制（D-109）、回归测试 28/28。待下一次 milestones 更新时正式收录。
