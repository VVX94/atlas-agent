<p align="center">
<img align="center" src="doc/imgs/logo.png" width="1600" alt="Atlas Agent 标题图">
</p>

--------------------------------------------------------------------------------

[English](./README.md) | 简体中文

[![GitHub Stars](https://img.shields.io/github/stars/VVX94/atlas-agent)](https://github.com/VVX94/atlas-agent/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/VVX94/atlas-agent)](https://github.com/VVX94/atlas-agent/issues)
[![License](https://img.shields.io/github/license/VVX94/atlas-agent)](https://github.com/VVX94/atlas-agent/blob/main/LICENSE)
[![Last Commit](https://img.shields.io/github/last-commit/VVX94/atlas-agent)](https://github.com/VVX94/atlas-agent/commits/main)
[![Stage](https://img.shields.io/badge/%E9%98%B6%E6%AE%B5-%E8%A7%84%E5%88%92%E5%AE%8C%E6%88%90%E4%B8%8E%E4%BB%93%E5%BA%93%E5%88%9D%E5%A7%8B%E5%8C%96-1f6feb)](https://github.com/VVX94/atlas-agent)

欢迎来到 Atlas Agent GitHub 仓库。

**一个面向笔记、PDF 和网页摘录的个人知识 Agent。** Atlas Agent 是一个以 CLI 为优先入口的知识管理系统，目标是把零散资料转化为一个可检索、可引用、可复用的工作知识库。它不是一个简单的聊天壳子，而是按照真实工程项目来构建，强调真实的 Agent 主循环、结构化工具、持久化状态和可观测执行过程。

项目将支持托管 API 或 OpenAI 兼容接口。核心设计目标不是绑定某一个模型供应商，而是把知识导入、检索、笔记操作、会话记忆和运行 tracing 组织成一个完整的 Agent 工作流。

<table>
<tr><td><b>真实的 Agent 主循环</b></td><td>通过工具调用完成搜索、笔记操作、摘要与基于证据的回答，而不是停留在单轮聊天壳层。</td></tr>
<tr><td><b>带引用的知识检索</b></td><td>导入 Markdown、PDF 和网页摘录后，基于检索结果回答问题，并返回明确引用。</td></tr>
<tr><td><b>Session 记忆</b></td><td>支持会话持久化、历史检索与上下文压缩，面向真正的多轮知识工作流。</td></tr>
<tr><td><b>笔记操作能力</b></td><td>通过结构化工具创建、更新和整理笔记，让 Agent 不只会读，还能对知识库做实际操作。</td></tr>
<tr><td><b>可追踪执行</b></td><td>模型调用、工具使用、耗时、重试和失败都应可被记录与检查，便于调试和评测。</td></tr>
<tr><td><b>安全防护</b></td><td>参数校验、超时控制和基础 Prompt Injection 防护将作为核心设计的一部分，而不是补丁。</td></tr>
</table>

---

## 项目进度

Atlas Agent 当前处于 **规划完成与仓库初始化** 阶段。

目前仓库中已经具备：

- 面向公开展示的中英双语 README
- 初始化后的公开仓库结构
- 保留的项目许可证
- 一套明确的架构方向与实现路线，供后续开发使用

核心运行时、检索链路、会话存储和工具实现 **尚未开始编码**。下一阶段的目标是打通第一个可运行的工作流，覆盖导入、检索、笔记操作和会话持久化。

---

## 项目是什么

Atlas Agent 是一个面向以下场景的知识 Agent：

- 个人研究
- 笔记整理
- 基于文档证据的问答
- 长周期知识工作流

它的目标不是支持零散 prompt，而是支持真实知识工作的全过程。系统需要能够检索证据、管理笔记、在多次会话之间保留上下文，并让自身行为可以被检查和持续改进。

## 架构方向

项目将围绕几个边界清晰、职责明确的子系统展开：

- 面向本地工作流的 CLI 入口层
- 负责编排与工具调用循环的 Agent Runtime
- 向模型暴露结构化能力的工具注册表
- 面向知识处理的导入与检索层
- 负责会话、记忆、笔记和 trace 数据的持久化层
- 负责评测、观测与运行控制的可观测性和安全层

这种设计可以让系统建立在明确接口之上，使后续的调试、评测和扩展更可控。

## 主要工作面

仓库后续将围绕这些工作域展开：

- Agent 主循环设计与工具分发
- RAG 导入、切分、索引与检索
- Session memory、历史检索与上下文压缩
- 笔记生命周期管理
- tracing 与评测工作流
- 安全防护与失败处理

## 为什么做这个项目

很多知识类 AI 演示只停留在“能检索”。Atlas Agent 想进一步把知识工作视为一个端到端的 Agent 问题来处理：导入信息、检索证据、操作笔记、在多次会话之间保留有价值的上下文，并把系统自身的执行过程暴露出来，便于检查和迭代。

长期目标是构建一个边界清晰、工程上站得住、并且具备持续扩展空间的个人知识管理 Agent。
