# AI Coding Standard

A reusable, human-led and project-adaptive AI Coding framework for specification-driven development, incremental delivery, quality assurance, and full-lifecycle engineering.

AI Coding Standard v1.0.0 是一套面向 Codex 的中文开发规范，覆盖项目初始化、接管、开发、修复、审查、部署与复盘。人类负责关键决策和验收，AI 协助调研、实现和验证。项目可按规模与风险调整流程。

## 快速开始

克隆仓库以查看插件源码和规范。

```shell
git clone https://github.com/yuyuxianxian74-debug/ai-coding-standard.git
```

在已安装此插件的 Codex 中打开要工作的项目，说明目标、当前状态和验收条件。例如：

- **初始化**：「按 AI Coding Standard 梳理这个项目的目标、MVP 和验收条件，再起草项目专属规范。」
- **接管**：「按 AI Coding Standard 检查现有代码、Git 状态、依赖与运行方式，汇报风险和下一步。」
- **开发或修复**：「按项目规范完成这项任务，运行相关测试并审查 Git diff，汇报验证结果。」

也可以直接把[项目专属规范模板](skills/ai-coding-standard/references/PROJECT_STANDARD_TEMPLATE.md)复制到自己的项目，按实际情况填写并在 `AGENTS.md` 中引用。

## 工作方式

1. 阅读全局规范、项目文档和相关代码，优先复用已有实现。
2. 按任务规模确定规格、实现计划和验收方式。复杂需求可分别维护 `SPEC.md`、`PLAN.md` 和 `TASKS.md`。
3. 按可独立验证的任务增量开发，运行适用的测试和构建，审查差异并更新相关文档。
4. 交付时记录实际验证结果。重大架构、数据、权限和生产变更交由人类确认。

## 仓库文件

| 文件 | 用途 |
| --- | --- |
| [`plugin.json`](plugin.json) | Agent Plugins 清单，定义插件版本和界面元数据。 |
| [`.codex-plugin/plugin.json`](.codex-plugin/plugin.json) | Codex 清单，声明技能目录和展示信息。 |
| [`SKILL.md`](skills/ai-coding-standard/SKILL.md) | 定义技能入口和各阶段的工作流程。 |
| [`GLOBAL_STANDARD.md`](skills/ai-coding-standard/references/GLOBAL_STANDARD.md) | 项目可复用的全局开发规范。 |
| [`PROJECT_STANDARD_TEMPLATE.md`](skills/ai-coding-standard/references/PROJECT_STANDARD_TEMPLATE.md) | 用于起草项目自己的架构、质量、安全和发布规则。 |
| [`TASK_CHECKLIST.md`](skills/ai-coding-standard/references/TASK_CHECKLIST.md) | 用于任务准备、交付和完成检查。 |
