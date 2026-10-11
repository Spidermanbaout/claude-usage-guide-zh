# Claude 使用教程：从第一次提问到 Projects、Artifacts 与 GitHub

> 面向刚开始使用 Claude 的中文用户。本文介绍 Claude.ai 网页版的常见工作流，不等同于 Claude Code 命令行工具教程。界面和可用功能可能因套餐、地区及产品更新而变化。  
> 最后核对：2026-10-11

## 目录

- [1. Claude 适合做什么](#1-claude-适合做什么)
- [2. 写清楚需求，让回答更好用](#2-写清楚需求让回答更好用)
- [3. 上传文件并围绕材料提问](#3-上传文件并围绕材料提问)
- [4. 用 Projects 管理长期任务](#4-用-projects-管理长期任务)
- [5. 用 Artifacts 生成可编辑成果](#5-用-artifacts-生成可编辑成果)
- [6. 设置回答风格](#6-设置回答风格)
- [7. 连接 GitHub 阅读代码库](#7-连接-github-阅读代码库)
- [8. 一个可以直接复用的工作流程](#8-一个可以直接复用的工作流程)
- [官方资料](#官方资料)

## 1. Claude 适合做什么

Claude 是 Anthropic 的 AI 助手。你可以用自然语言让它解释概念、整理材料、起草和修改文字、分析文件、梳理代码，或把想法做成可查看和继续修改的内容。

把 Claude 当作协作助手来用：给它目标和必要背景，再检查它的结论。涉及最新事实、专业判断或重要决定时，要求它说明依据，并自行核对关键内容。

## 2. 写清楚需求，让回答更好用

一个好用的提示词通常会交代五件事：

1. **目标**：这次要完成什么？
2. **背景**：读者是谁，内容用在哪里？
3. **材料**：应该依据哪些文件、链接或已知信息？
4. **约束**：篇幅、语气、语言、不能做的事是什么？
5. **交付格式**：要清单、表格、邮件、代码，还是分步骤说明？

可以直接套用这个模板：

```text
目标：请帮我……
背景：……
材料：只依据我提供的……
要求：使用……语气，控制在……字以内；遇到材料没有说明的内容请标出来，不要猜测。
格式：请按……格式输出。
```

**示例：**

```text
请把下面的会议记录整理成发给团队的行动清单。
按“事项、负责人、截止时间、待确认问题”四列输出。
只提取记录中明确出现的信息；没有写负责人的事项标注“待确认”，不要推断。
```

如果结果不合适，不必从头重写提示词。直接指出要改的部分，例如：“保留原来的结论，把语气改得更简洁，并把建议和已确认事实分开。”

## 3. 上传文件并围绕材料提问

你可以在对话中上传文档，让 Claude 总结、比较、提取信息或回答有关文件的问题。官方帮助中心列出的常见文档格式包括 PDF、DOCX、CSV、TXT、HTML、ODT、RTF、EPUB 和 JSON；启用分析工具时也支持 XLSX。文件大小、每次对话数量和功能可用性可能调整，上传时以产品界面提示为准。

建议按“定位—分析—核对”来提问：

1. 先让 Claude 说明文件内容和结构。
2. 再提出具体问题，限定它依据哪些文件或章节。
3. 要求它标记找不到依据的地方，并给出页码、章节或原文短句，方便你回查。

**示例：**

```text
请先阅读我上传的两份方案。
比较它们在目标用户、价格、上线时间和风险上的差异。
用表格呈现，每项附上对应文件中的页码或章节。
材料没有提到的内容写“未说明”，不要自行补全。
```

文件包含机密、个人信息或尚未公开内容时，上传前先确认自己有权将它提供给该服务，并按需要删去不必要的信息。

## 4. 用 Projects 管理长期任务

Projects 适合持续进行的工作，例如课程研究、写作项目、产品资料整理或代码库分析。你可以为项目添加相关资料，并设置项目专属指令，让同一项目里的对话有共同背景。

**建议这样设置：**

- 项目名称写清楚用途，例如“客户访谈分析”。
- 只放当前项目需要的资料，并清理过时版本。
- 在项目指令里说明目标、受众、术语和输出偏好。
- 开始新聊天时，仍要在问题里说明本次任务；不同聊天之间的对话上下文不会自动全部共享，放进项目知识库的信息才可供项目内聊天参考。

Anthropic 帮助中心目前将 Projects 列为付费方案功能；实际套餐、额度和界面可能变化，请查看你的账户页面及[官方 Projects 说明](https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects)。

## 5. 用 Artifacts 生成可编辑成果

当你希望结果以独立内容呈现时，可以让 Claude 创建 Artifact。常见成果包括文档、图表、流程图、SVG、网页或交互式小工具。你可以继续对话要求调整，再复制或下载结果；可用的编辑和发布方式会因 Artifact 类型而异。

**可以这样开始：**

```text
请把这份调研结论做成一个单页网页。
受众是第一次了解这个主题的同事。
页面包含结论摘要、三条关键发现和一个对比表格，布局适合手机阅读。
先生成初稿，我确认内容后再调整视觉风格。
```

分享前要特别检查内容：发布的 Artifact 可能通过链接被任何拿到链接的人访问。不要把密钥、内部资料、个人信息或其他不应公开的内容放进将要分享的 Artifact。可以在[官方 Artifacts 说明](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them)中查看当前能力与可用范围。

## 6. 设置回答风格

如果 Claude 的回答总是太长、太正式或解释不足，可以调整风格。官方说明提到的选项包括 Normal、Concise、Formal、Explanatory，也可以创建自定义写作风格。你也可以在单次提示词里临时说明语气和结构。

**自定义风格示例：**

```text
使用简体中文。先给结论，再列依据和下一步。
句子尽量短；术语第一次出现时用一句话解释。
不确定时明确说不确定，不要编造来源。
```

设置入口和选项可能随产品界面更新，参考[官方 Styles 说明](https://support.anthropic.com/en/articles/10181068-configuring-and-using-styles)及[个性化功能说明](https://support.anthropic.com/en/articles/10185728-understanding-claude-s-personalization-features)。

## 7. 连接 GitHub 阅读代码库

Claude 的 GitHub 集成可以让你选择仓库中的文件或文件夹作为阅读材料，帮助解释项目结构、查找相关实现或总结代码。连接后，按任务选择相关目录，并明确告诉 Claude 要关注的内容。

**示例：**

```text
请先梳理这个仓库的目录结构。
找出登录流程涉及的前端页面、API 调用和服务端处理位置。
先提供文件路径和各自职责，不要修改代码。
如果无法从已连接的文件确认某个环节，请说明还缺少什么。
```

连接步骤及可读取范围请查看[官方 GitHub 集成指南](https://support.anthropic.com/en/articles/10167454-using-the-github-integration)。在让 AI 分析代码前，检查连接的仓库和文件范围，并避免提供不必要的机密。

## 8. 一个可以直接复用的工作流程

1. **先给任务和材料**：说明目标、背景以及可用资料。
2. **让 Claude 先复述计划**：确认它理解了问题和限制。
3. **分步完成**：把复杂任务拆成调研、草稿、修改和最终整理。
4. **让结论可核查**：要求区分事实、推断和建议；对材料分析给出出处。
5. **自己检查关键内容**：尤其是数字、引文、最新信息和重要决定。
6. **分享前做隐私检查**：确认文件、Artifact 和代码库里没有不该公开的资料。

## 官方资料

- [Claude Projects：创建和管理项目](https://support.anthropic.com/en/articles/9519177-how-can-i-create-and-manage-projects)
- [Claude Artifacts：功能和使用方法](https://support.anthropic.com/en/articles/9487310-what-are-artifacts-and-how-do-i-use-them)
- [Artifacts：创建 AI 应用和可视化内容](https://support.anthropic.com/articles/11649427-use-artifacts-to-visualize-and-create-ai-apps-without-ever-writing-a-line-of-code)
- [Styles：配置和使用回答风格](https://support.anthropic.com/en/articles/10181068-configuring-and-using-styles)
- [个性化功能](https://support.anthropic.com/en/articles/10185728-understanding-claude-s-personalization-features)
- [GitHub 集成](https://support.anthropic.com/en/articles/10167454-using-the-github-integration)
- [可上传的文档类型](https://support.anthropic.com/en/articles/8241126-what-kinds-of-documents-can-i-upload-to-claude-ai)
