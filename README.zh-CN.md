# 架构图设计器

[English](README.md) | **简体中文**

将系统描述、技术文档、组件清单或视觉参考转化为语义准确、视觉精致的架构图图片。

![同一套经典架构应用七种内置视觉风格](showcase/classic-agent-system/style-overview.png)

## 为什么需要这个 Skill

架构图不是普通流程图。一张有效的架构图必须准确表达系统边界、关系方向、信任区域、反馈回路和抽象层级。这个 Skill 会先选择与系统语义匹配的架构拓扑，再应用视觉风格。

## 核心能力

1. 提取真实的参与者、组件、边界和关系类型。
2. 根据系统结构选择合适的架构拓扑，而不是强行使用通用流程图。
3. 用户未指定风格时，推荐三种差异明显的候选风格。
4. 默认直接生成一张独立的架构图图片。
5. 可以学习参考图的视觉语言，同时独立判断架构拓扑，不机械照搬布局。

支持系统上下文图、分层架构图、组件图、数据流、事件驱动架构、中心辐射式控制平面、部署视图、信任区域、生态系统和反馈回路。

## 快速开始

```text
使用 $architecture-diagram-designer，为一个包含编排器、LLM、工具、记忆、
策略护栏、评估和可观测性的 Agent 平台生成架构图。
```

直接指定内置风格：

```text
使用 $architecture-diagram-designer 和 Dark Blueprint 风格，展示下面这个
多地域事件驱动平台：……
```

跳过风格讨论并立即生成：

```text
使用 $architecture-diagram-designer，自动选择最合适的风格，并根据下面的
技术文档直接生成架构图：……
```

## 内置风格

下面所有预览均使用同一套 **Agent System Architecture — From Intent to Trusted Execution** 拓扑和标签，只改变视觉语言，方便直接比较风格差异。

| 风格 | 预览 | 适用场景 |
|---|---|---|
| Editorial Tech | [查看](showcase/classic-agent-system/editorial-tech.png) | AI 系统、技术战略、技术报告 |
| Dark Blueprint | [查看](showcase/classic-agent-system/dark-blueprint.png) | 基础设施、运行时、网络系统 |
| Swiss Signal | [查看](showcase/classic-agent-system/swiss-signal.png) | 框架、规范、GitHub 项目发布 |
| Product Minimal | [查看](showcase/classic-agent-system/product-minimal.png) | SaaS、开发者体验、产品文档 |
| Neo Brutalist | [查看](showcase/classic-agent-system/neo-brutalist.png) | 创意开发工具、开源项目 |
| Executive Dark | [查看](showcase/classic-agent-system/executive-dark.png) | 管理层沟通、治理、企业战略 |
| Soft Data Canvas | [查看](showcase/classic-agent-system/soft-data-canvas.png) | 数据产品、易理解的 AI 系统、教育 |

## 风格选择

- 指定某个内置风格时，直接使用该风格。
- 提供视觉参考时，提取其配色、字体、节点和连线语言，但仍独立选择架构拓扑。
- 未指定风格时，先推荐三种差异明显的候选风格。
- 用户说“自动选择”或“直接生成”时，自动选择最合适的风格并继续生成，不暂停询问。

## 推荐运行环境

为了获得最佳效果，建议在**已启用图像生成能力的 Codex** 中使用本 Skill，并在可用时优先选择 **[GPT Image 2（`gpt-image-2`）](https://developers.openai.com/api/docs/models/gpt-image-2)**。GPT Image 2 面向高质量图像生成和编辑，更适合输出完成度较高的架构图图片。

本 Skill 本身不捆绑图像模型。其他 Agent 仍然可以使用其中的拓扑选择、语义分析、风格系统和提示词编译能力；但如果 Agent 没有图像生成工具，只会输出一份完整、可转交给图像模型的生成提示词，不会直接生成最终图片。本项目不会加入 SVG、Mermaid、Graphviz 或代码渲染器作为替代链路。

## 输出方式

默认产物是直接生成的架构图图片。如果明确要求“只输出提示词”，Skill 会返回简洁的架构图策略和完整、可直接交给图像模型的生成提示词。

可编辑 Mermaid、Graphviz、SVG、PowerPoint 和普通插画不属于本 Skill 的目标产物。

## 安装

将本目录复制到兼容 Codex 的 Skill 目录：

```bash
cp -R architecture-diagram-designer ~/.agents/skills/architecture-diagram-designer
```

如果 Skill 列表没有立即刷新，请重启 Codex 或新建一个任务。

## 设计原则

> 先保证架构拓扑语义正确，再决定视觉风格。
