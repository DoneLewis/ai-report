# Agent Harness 工程软件文档库

围绕市面上主流大模型厂商推出的 harness 工程软件（Codex、Claude Code、DeepSeek Harness、OpenCode 等），逐家拆解其 **agent loop** 的设计与实现：循环如何运转、工具如何编排、上下文如何管理、权限如何控制，以及背后的产品理念。

## 文档库结构

| 章节 | 内容 |
| --- | --- |
| [首页](index.html) | 导航、概念总览、覆盖产品一览、阅读指南 |
| [01 · OpenAI Codex](01-codex.html) | 双层循环（外层任务 + 内层工具）、App Server/SDK、沙箱与审批、Memories、AGENTS.md |
| [02 · Claude Code](02-claude-code.html) | 单层循环 + 权限检查点、CLAUDE.md、auto-compact、权限模式、hooks、Task 子代理 |
| [03 · DeepSeek Harness](03-deepseek-harness.html) | 「Everything is a plugin」Cordis 内核，loop 本身可插拔、append-only session log |
| [04 · OpenCode](04-opencode.html) | 流式响应 + 工具回灌、LSP 深度集成、模型无关、plan/build 双模式 |
| [05 · 开源生态补充](05-open-source.html) | Cline、Aider、OpenHands、Goose、Roo Code |
| [06 · 商业生态补充](06-commercial.html) | Cursor、Windsurf、Devin、Gemini CLI、Copilot |
| [07 · 横向对比](07-comparison.html) | Mermaid loop 架构图、ECharts 雷达图、六维对比表、演进趋势 |

## 核心结论

所有 harness 共享「plan → act → observe → repeat」底层循环，但每家做了不同的工程取舍：

- **Codex**：双层循环分离任务/工具粒度
- **Claude Code**：把权限检查点做进循环
- **DeepSeek Harness**：把 loop 本身插件化
- **OpenCode**：流式 + 回灌保持循环透明

安全哲学从「默认信任」（OpenCode）到「默认沙箱」（Gemini CLI）展开；上下文工程分压缩/检索/文件三派。

## 使用方式

直接打开 `index.html` 即可浏览全部内容，页面间通过顶部导航互相跳转。所有事实均标注来源链接，信息截止 2026-08。

## 说明

本文档库为研究性资料汇编，内容基于公开来源整理，版权归各厂商所有；事实以官方文档为准。
