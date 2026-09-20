# Skills

一组经过精简和重构的 AI agent skills，用于需求澄清、规格沉淀、项目文档、
原型验证、测试驱动开发、架构评审和交互式学习。

这些 skills 可以独立使用，也可以根据任务需要自由组合。它们不是一套必须完整执行的固定工作流。

## Skills

| Skill | 用途 |
| --- | --- |
| [`grill-me`](./skills/grill-me/SKILL.md) | 发现隐含决定，完整澄清想法并确认共同理解。 |
| [`to-spec`](./skills/to-spec/SKILL.md) | 将当前已确认的功能讨论沉淀为可交接的任务规格。 |
| [`project-docs`](./skills/project-docs/SKILL.md) | 审计项目文档需求，并按确认范围补齐基础文档。 |
| [`prototype`](./skills/prototype/SKILL.md) | 用可丢弃原型验证交互、状态或设计方向。 |
| [`tdd`](./skills/tdd/SKILL.md) | 对规则明确的行为执行精简的红灯、绿灯、重构循环。 |
| [`architecture-review`](./skills/architecture-review/SKILL.md) | 输出有证据支撑的中文架构优化报告。 |
| [`teach`](./skills/teach/SKILL.md) | 通过结构化课程和学习记录交互式学习技术主题。 |

## 安装

通过交互式安装器选择 skill、目标 agent 和安装范围：

```bash
npx skills@latest add <owner>/skills
```

只查看可用的 skills：

```bash
npx skills@latest add <owner>/skills --list
```

将全部 skills 全局安装到 Claude Code：

```bash
npx skills@latest add <owner>/skills --skill '*' --agent claude-code --global
```

将全部 skills 全局安装到 Codex：

```bash
npx skills@latest add <owner>/skills --skill '*' --agent codex --global
```

更新已安装的 skills：

```bash
npx skills@latest update
```

将 `<owner>` 替换为本仓库发布后的 GitHub 用户名。

## 致谢

本仓库中的部分 skills 复制或改编自 [Matt Pocock's skills](https://github.com/mattpocock/skills)。
感谢 Matt Pocock 分享高质量的 skill 设计、工作流思想和原始实现。

原始内容依照 MIT License 使用。具体来源和改编关系见 [NOTICE.md](./NOTICE.md)。
