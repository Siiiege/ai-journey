# 里程碑记录

## 2026-10-15 · 发布 repo-governance

第一个正式作品上线：[Siiiege/repo-governance](https://github.com/Siiiege/repo-governance)——
一个 agent 协作治理 skill，给「人和 agent 隔着多个会话持续干活的仓库」装上任务卡
生命周期、决策记录和文档门禁（check-docs，零依赖，Node/Python 双实现）。

它的规则来自我自己仓库里的真实翻车：索引腐烂、文档双写漂移、agent 自述完成、
peer 依赖误删。成形后没有直接发布，而是先做了实测——三个轮次、六个真实开源仓库
（husky / click / duf / bat / awesome / SDD-Lite 的浅克隆），每个仓库交给一个干净
上下文的子代理去治理，我只做事后核验；另外单测了退出条款（对已治理仓库重发指令
必须零改动退出）和冷启动（新会话只靠仓内文档答「做到哪了 / 为何这么决定 / 从哪
下手」三问）。约 20 条缝隙全部回填或明确留观，完整记录在仓库的
[docs/evaluation.md](https://github.com/Siiiege/repo-governance/blob/main/docs/evaluation.md)。

对转型路线的意义：这是「agents & evals」方向第一个拿得出手的实物——写了一个
skill 之外，更重要的是给它搭了评测方法学（执行者与检测者分离、负例注入、按发现
驱动迭代），并靠这套方法把它打磨到能发布的程度。
