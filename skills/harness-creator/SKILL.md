---
name: harness-creator
description: "为当前仓库搭建 AI 协作 harness：AGENTS.md、CLAUDE.md、README.md、PROGRESS.md、docs/PRODUCT.md、docs/ARCHITECTURE.md。新项目开工前运行一次。"
disable-model-invocation: true
---

# Harness Creator

模板在 [templates/](./templates/)：

| 模板 | 写到 |
|---|---|
| `templates/AGENTS.md` | `AGENTS.md` |
| `templates/CLAUDE.md` | `CLAUDE.md` |
| `templates/README.md` | `README.md` |
| `templates/PROGRESS.md` | `PROGRESS.md` |
| `templates/PRODUCT.md` | `docs/PRODUCT.md` |
| `templates/ARCHITECTURE.md` | `docs/ARCHITECTURE.md` |

## 流程

1. **检查**：当前目录是否为 git 仓库；上表目标文件是否存在。
2. **建议 git**（仅非 git 仓库时）：强烈建议先运行 `git init`，原因：每个任务完成后要提交，便于回滚和追溯。征得用户同意后再执行；用户不同意则跳过，继续后续步骤。
3. **创建**：不存在的按模板创建；已存在的不动。
4. **输出结果**：用表格列出每个文件及状态（新建 / 已存在）；如未初始化 git，在表格下再提醒一次。
5. **给出建议**：按下面要点，用自己的话给出简洁的下一步建议（几行即可，不照抄）。

## 建议要点

按顺序：

1. 确定功能需求：可用 `/grill-me-docs` 讨论
2. 技术预研：调研相关技术、开源项目、行业方案，摸清能力边界；有技术风险的提前验证
3. 确定架构设计：架构、模块职责、接口写入 `docs/ARCHITECTURE.md`
4. 拆分任务：按功能在 `PROGRESS.md` 拆出任务和验收标准
5. MVP 开发：先搭骨架，跑通一条核心链路
6. 测试迭代：验证 MVP 解决了核心问题，再逐步补功能
