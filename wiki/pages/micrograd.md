# micrograd · 手写标量自动微分引擎（W1-2）

> Source: [../../docs/phase1-plan.md](../../docs/phase1-plan.md) W1-2、[../../weeks/week-01.md](../../weeks/week-01.md)、[../../weeks/code/micrograd.py](../../weeks/code/micrograd.py)
> 状态快照：2026-10-22 —— W1 进行中，`weeks/code/micrograd.py` 仅含 notebook 头部，跟敲尚未展开

Karpathy《The spelled-out intro to neural networks and backpropagation》跟敲项目，Phase 1 第一站。理论侧见 [./backpropagation.md](./backpropagation.md)。

## 任务分解

- **W1（上）**：跟敲 `Value` 类——`data` / `grad` / `_backward` / `_prev` 四件套；`__add__` / `__mul__` 的 backward；每行自己敲。
- **W2（下）+ 自己的扩展**（和只看教程的人拉开差距的点）：把 `tanh` 换成 ReLU 手推梯度，或加 `pow` / `exp` 算子。
- **W2 产出**：笔记 1《手写反向传播》。

## 验收

- W1：脱稿讲清加法直通 / 乘法交换偏导（问题挂在学习页）。
- W2：扩展算子的梯度通过与 **PyTorch autograd 对拍**（数值一致）。
