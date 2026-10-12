# ai-fullstack-learning

> AI 全栈工程师（Agent UI 方向）进阶学习仓库。
>
> 以「Agent 前端交互层」为核心，贯通 **协议层 → 流式渲染 → 组件体系 → BFF 与后端 Agent 服务 → 部署运维** 的完整学习路线与实践项目。
>
> 本仓库由一份「全栈AI Agent（UI方向）」岗位 JD 拆解而来，覆盖 JD 中的全部岗位职责、硬性要求与加分项——**目标不是"写页面"，而是定义人与 AI 协作的界面语言。**

---

## 目录

1. [项目定位](#1-项目定位)
2. [能力全景（JD → 学习模块）](#2-能力全景jd--学习模块)
3. [学习路线（分 7 个阶段）](#3-学习路线分-7-个阶段)
4. [实战项目清单](#4-实战项目清单)
5. [资源清单](#5-资源清单)
6. [学习进度追踪](#6-学习进度追踪)
7. [参考 JD 画像](#7-参考-jd-画像)
8. [License](#8-license)

---

## 1. 项目定位

- **前端主线**：TypeScript + React（Next.js / Vite），SSE/WebSocket 流式渲染，Agent 交互组件体系，设计系统
- **后端支线**：Python Agent 服务（LangGraph / LangChain）、BFF 契约设计
- **协议主线**：Function/Tool Calling、Structured Output、MCP、AG-UI/A2UI、A2A
- **工程主线**：Vibe Coding 工具链（Codex / Cursor / Claude Code）、Docker、CI/CD、可观测性
- **最终产出标准**：不是"功能完成了"，而是交互足够直觉——让用户在 Agent"思考—调用工具—返回结果"的全过程中可感知、可信任、可介入

---

## 2. 能力全景（JD → 学习模块）

- **模块 A｜Agent 交互层**
  - 将 Agent 输出通过 AG-UI / A2UI 协议渲染为原生交互组件（表单、卡片、数据面板、多步骤工作流界面），而非纯文本堆砌
  - 流式渲染（SSE/WebSocket）下的渐进式展示、实时解析与状态管理
- **模块 B｜前端 Harness 抽象层**
  - 定义 Agent 前端侧"运行时能力"：流式通信适配器、结构化输出解析器、UI 渲染协议适配、错误恢复机制
  - 让业务开发者可替换底层 Agent 框架，而交互体验保持一致
- **模块 C｜Vibe Coding 工具链**
  - 深度使用 Codex / Cursor / Claude Code，作为默认开发范式
  - 用自然语言驱动复杂交互逻辑生成，缩短"想法 → 可交互原型"路径
  - 建设 Agent 交互调试与预览工具链
- **模块 D｜前端架构与组件体系**
  - 面向 Agent 场景的组件目录（Component Catalog）：可扩展的声明式组件协议
  - Web 端及跨端（移动端 / 桌面端）渲染适配与性能（长对话、大数据量表格、多面板布局、虚拟列表）
  - 设计系统与设计语言，保证品牌一致性与审美品质
- **模块 E｜后端 Agent 服务与 BFF**
  - 参与 BFF 层设计，定义前端与后端 Python Agent 服务之间的契约
  - 完成 MCP / Tool Calling 等协议的前端集成与适配，确保工具调用状态在 UI 层正确表达
- **模块 F｜协议与架构认知**
  - Function Calling、Tool Calling、Structured Output 核心机制
  - MCP（Model Context Protocol）、AG-UI/A2UI、A2A 协议设计理念
  - Harness 概念：工具调用、记忆、权限、上下文组织如何被工程化
  - LangGraph / LangChain 前端侧集成或调用、SSE、Middleware 模式
- **模块 G｜部署运维与工程质量**
  - CI/CD 流水线、容器化部署、静态资源分发、环境隔离
  - 稳定性与可观测性（日志 / 指标 / 链路）
- **模块 H｜加分进阶**
  - 跨端技术方案（React Native / Electron / Tauri）生产级多端
  - 端侧 AI（Transformers.js / WebGPU）浏览器端模型部署
  - Mastra / Vercel AI SDK 等 Agent 框架
  - Agent IDE / 调试工具开发经验、GitHub 开源与社区输出

---

## 3. 学习路线（分 7 个阶段）

### Phase 0｜前置基础（约 1–2 周）

- 目标：补齐工程地基
- 关键内容
  - TypeScript 工程化与类型设计
  - React 生态：Next.js / Vite 构建与路由
  - 现代 CSS 与布局（多面板、响应式）
- 对应 JD：精通 TypeScript、熟练掌握 React 生态（Next.js / Vite）、复杂交互落地能力
- 建议产出：用 Vite 搭建一个带多面板布局的 TypeScript + React 应用

### Phase 1｜实时数据驱动 UI（约 2–3 周）

- 目标：吃透流式渲染
- 关键内容
  - SSE 与 WebSocket 原理、选型与边界
  - 流式响应解析（增量 chunk → 结构化数据）
  - 渐进式渲染与状态管理（思考中 / 工具调用中 / 结果返回）
  - 错误恢复、断线重连
- 对应 JD：有流式渲染 / SSE / WebSocket 实时数据驱动 UI 的实际项目经验
- 建议产出：LLM 对话流式打字机 demo，分阶段展示"思考 → 调用工具 → 返回结果"

### Phase 2｜Agent 协议与架构（约 3–4 周）

- 目标：建立 Agent 架构的系统性认知
- 关键内容
  - Function Calling / Tool Calling / Structured Output 机制
  - MCP（Model Context Protocol）客户端与协议
  - AG-UI / A2UI（Agent UI 协议）设计理念与集成
  - Harness 概念：工具调用、记忆、权限、上下文组织的工程化
  - Middleware 模式
  - A2A（Agent 间通信）基本模型
- 对应 JD：Agent 技术栈理解全部条目
- 建议产出：基于 MCP SDK 做一个工具调用状态可视化面板（前端解析 + 状态呈现）

### Phase 3｜Agent 前端交互层实战（约 4–6 周）

- 目标：从"能渲染"到"好用、可信任"
- 关键内容
  - AG-UI/A2UI 输出 → 原生组件映射（表单 / 卡片 / 数据面板 / 多步骤工作流）
  - 组件目录（Component Catalog）与声明式组件协议
  - 性能优化：虚拟列表、大数据量表格、多面板布局
  - 设计系统与 Storybook 实践
  - Agent 交互信任设计：用户如何理解 AI 在做什么、为什么这样做、何时介入
- 对应 JD：职责 1、职责 3、审美与体验敏感度
- 建议产出：封装一个 Agent 前端运行时（Harness 雏形），配套 Storybook 组件目录

### Phase 4｜后端 Agent 服务与 BFF（约 3–4 周）

- 目标：打通前后端全链路
- 关键内容
  - Python Agent 服务：LangGraph / LangChain 状态图与工具调用
  - BFF 层设计：前端与后端服务的契约（OpenAPI / 类型生成）
  - Tool Calling 服务端实现与流式转发
- 对应 JD：职责 4（BFF 与 MCP/Tool Calling 集成）、硬性要求 LangGraph / LangChain
- 建议产出：Python Agent 服务 + BFF + 前端流式界面全链路 demo

### Phase 5｜部署运维与工程质量（约 2–3 周）

- 目标：能上线、能观测
- 关键内容
  - Docker 容器化部署
  - CI/CD 流水线（GitHub Actions 等）
  - Nginx / CDN 静态资源分发
  - 环境隔离与配置管理
  - 可观测性：日志、指标、链路追踪
- 对应 JD：职责 4（运维部署与工程质量）
- 建议产出：为 Phase 4 项目配置 Dockerfile + CI/CD 流水线

### Phase 6｜进阶与加分项（持续进行）

- 目标：拉开差异化
- 关键内容
  - 跨端：React Native / Electron / Tauri 生产级多端项目
  - 端侧 AI：Transformers.js / WebGPU 浏览器端模型部署
  - Agent 框架：Mastra / Vercel AI SDK
  - Agent IDE / 调试工具开发
  - GitHub 开源项目与社区持续输出
- 对应 JD：全部加分项
- 建议产出：端侧小模型 demo，或一个跨端壳工程

### Phase 7｜综合实战（对标岗位产出标准）

- 目标：交付一个"功能完成 + 体验可信"的完整项目
- 建议项目：**餐饮商家 AI 助手**（对齐 JD 的餐饮行业场景）
  - 场景：高峰期接单、处理差评、人力调度——商家不是在"玩 AI"，交互必须足够直觉
  - 功能：流式可感知的 Agent 交互、工具调用状态清晰、多步骤工作流界面
- 验收标准
  - 思考 / 工具调用 / 返回结果全过程可感知、可信任、可介入
  - 跨端视觉与交互一致
  - 可部署、可观测

---

## 4. 实战项目清单

1. 流式对话界面（打字机 + 状态分阶段展示）— Phase 1
2. 工具调用状态可视化面板 — Phase 2
3. Agent 前端运行时 Harness + Storybook 组件目录 — Phase 3
4. Python Agent 服务 + BFF 全链路 demo — Phase 4
5. 容器化 + CI/CD 部署 — Phase 5
6. 端侧 AI / 跨端 demo — Phase 6
7. 餐饮商家 AI 助手（综合实战）— Phase 7

---

## 5. 资源清单

- TypeScript 官方文档：https://www.typescriptlang.org/
- React 官方文档：https://react.dev/
- Next.js：https://nextjs.org/
- Vite：https://vitejs.dev/
- SSE / WebSocket（MDN）：https://developer.mozilla.org/
- MCP（Model Context Protocol）：https://modelcontextprotocol.io/
- AG-UI 官方站点：https://ag-ui.com/
- A2A 协议：https://a2a-protocol.org/
- LangGraph 文档：https://langchain-ai.github.io/langgraph/
- Vercel AI SDK：https://sdk.vercel.ai/
- Storybook：https://storybook.js.org/
- Transformers.js：https://huggingface.co/docs/transformers.js/
- Docker：https://docs.docker.com/
- GitHub Actions：https://docs.github.com/actions

---

## 6. 学习进度追踪

- [ ] Phase 0｜前置基础（TS + React 工程化）
- [ ] Phase 1｜实时数据驱动 UI（SSE / WebSocket）
- [ ] Phase 2｜Agent 协议与架构（MCP / AG-UI / Harness）
- [ ] Phase 3｜Agent 前端交互层实战（Harness + 组件目录）
- [ ] Phase 4｜后端 Agent 服务与 BFF
- [ ] Phase 5｜部署运维与工程质量
- [ ] Phase 6｜进阶与加分项（跨端 / 端侧 AI）
- [ ] Phase 7｜综合实战（餐饮商家 AI 助手）

---

## 7. 参考 JD 画像

**岗位：全栈AI Agent（UI方向）**

- 岗位职责：Agent 交互层设计与实现；Vibe Coding 工具链团队落地；前端架构与组件体系；运维部署与工程质量；BFF 层与前后端契约
- 硬性要求
  - 3 年以上前端经验，精通 TypeScript + React 生态
  - 有流式渲染 / SSE / WebSocket 实战经验
  - 熟悉 Docker、CI/CD、Nginx/CDN、云服务
  - 系统认知 Function Calling、Tool Calling、Structured Output、MCP、AG-UI/A2UI、Harness
  - Vibe Coding 深度使用者，对 AI 生成边界有清醒认知
  - 有设计系统 / 组件库 / Storybook 实践，对 Agent 交互信任设计有思考
- 加分项：Agent IDE / 调试工具、跨端（RN/Electron/Tauri）、端侧 AI（Transformers.js/WebGPU）、LangGraph / Mastra / Vercel AI SDK、A2A、开源输出、餐饮行业真实兴趣
- 真正的挑战：不是"写页面"，而是**定义人与 AI 协作的界面语言**；产出标准不是"功能完成了"，而是交互足够直觉、不浪费用户稀缺的注意力

---

## 8. License

MIT
