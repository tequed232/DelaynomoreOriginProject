# 第一章：从 AI 到 Agent 工作流

> 本章介绍如何从普通 AI 对话走向可执行的 Agent 工作流，并以 DeepSeekHarness、腾讯 WorkBuddy、插件、Skills 和 GitHub MCP 为实践主线。

## 本章讲什么？

本章不重复项目导言。导言由项目维护者单独编写；本章从“AI 是否正在代替人思考”这一问题切入，讨论如何正确使用 AI，再进入实际工具配置和工作流搭建。

本章的重点不是鼓励用户把思考完全交给 AI，而是帮助用户理解：哪些工作可以交给 AI，哪些判断必须由人负责，以及如何通过 Harness、插件、Skills 和 MCP 建立可控的协作流程。

## 章节范围

1. **AI 代替思考，还是辅助思考？**  
   讨论自动化与人的判断责任、验证意识和过度依赖风险。
2. **使用 DeepSeekHarness**  
   认识项目、运行环境、基本配置和工作区。
3. **在腾讯 WorkBuddy 中导入 API**  
   配置兼容的模型服务，理解 API Key、Base URL、模型标识和兼容性。
4. **安装与使用 Plugins**  
   以 `dsh-bot` 和 `dsh-whale-widget` 为例，说明插件的作用、安装、配置、调用与排错。
5. **制作 Skills**  
   结合用户提供的 Claude 提示词材料，将稳定、可复用的工作方法整理成 Skill。
6. **接入 GitHub MCP**  
   让 Agent 在授权范围内读取仓库信息、Issue、Pull Request 等资源，并理解权限边界。

## 建议学习顺序

| 顺序 | 文档 | 学习结果 |
|---|---|---|
| 01 | `01-ai-and-thinking.md` | 建立 AI 辅助思考与验证意识 |
| 02 | `02-deepseekharness-introduction.md` | 认识并启动 DeepSeekHarness |
| 03 | `03-workbuddy-api-setup.md` | 在 WorkBuddy 中配置模型 API |
| 04 | `04-plugins-dsh-bot-and-whale-widget.md` | 理解并使用两个示例插件 |
| 05 | `05-create-skills-from-prompts.md` | 将提示词整理为可复用 Skill |
| 06 | `06-connect-github-mcp.md` | 配置 GitHub MCP 并进行受控操作 |
| 07 | `07-complete-workflow.md` | 串联完整工作流 |

## 适合谁？

- 使用过 DeepSeek、Claude、ChatGPT 等 AI 工具，但不了解 Agent 工程体系的用户。
- 希望把 AI 接入自己的开发工作流的初学者。
- 想学习插件、Skills、MCP 与 GitHub 协作的开发者。

## 前置条件

- 能够安装和运行 DeepSeekHarness（具体系统要求以项目当前版本为准）。
- 拥有可用的模型 API 服务及其合法使用权限。
- 能够使用腾讯 WorkBuddy；具体功能以当前客户端版本和账号权限为准。
- 有 GitHub 账号；接入 GitHub MCP 时应使用最小必要权限。
- 具备基本文件管理能力。遇到命令行操作时，教程会逐步解释。

## 重要说明

- `dsh-bot`、`dsh-whale-widget` 的实际安装方式、配置字段和能力，应以对应仓库的当前代码与 README 为准；未完成核对前不应把示例写成确定步骤。
- WorkBuddy 的 API 接入能力、支持的协议格式和界面入口可能随版本变化。教程发布前必须实测并记录版本。
- Skills 不等于简单地把一段长提示词复制到文件里。教程需要解释 Skill 的触发条件、输入输出、步骤、限制和验证方法。
- GitHub MCP 的授权范围必须遵循最小权限原则；演示阶段优先只读，写入、合并和删除操作需要明确确认。
- 不要把 API Key、GitHub Token 或其他密钥提交到 GitHub。

## 教程状态

本目录目前是第一版内容草稿。带有“待验证”标记的产品操作步骤，在正式发布前必须使用实际软件版本完成复现。

## 文件索引

- [AI 代替思考，还是辅助思考？](01-ai-and-thinking.md)
- [使用 DeepSeekHarness](02-deepseekharness-introduction.md)
- [在腾讯 WorkBuddy 中导入 API](03-workbuddy-api-setup.md)
- [Plugins：以 dsh-bot 和 dsh-whale-widget 为例](04-plugins-dsh-bot-and-whale-widget.md)
- [从 Claude 提示词制作 Skills](05-create-skills-from-prompts.md)
- [接入 GitHub MCP](06-connect-github-mcp.md)
- [完整工作流实战](07-complete-workflow.md)
- [第一章视频脚本](videos/episode-01-script.md)
