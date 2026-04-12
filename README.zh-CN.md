# A2A Commerce 规范

> **第五电商范式**
> **Agent-to-Agent Commerce：AI 原生的交易范式**

[![规范版本](https://img.shields.io/badge/spec-v1.0-blue.svg)](./SPEC.md)
[![发布日期](https://img.shields.io/badge/published-2026--04--11-green.svg)](./SPEC.md)
[![许可协议](https://img.shields.io/badge/license-CC%20BY%204.0-lightgrey.svg)](./LICENSE)
[![状态](https://img.shields.io/badge/status-Draft-orange.svg)](./SPEC.md)

**规范作者：[AgentShow](https://agentshow.shop)** —— 全球首个 A2A Commerce 平台。

---

## 什么是 A2A Commerce

**A2A Commerce（Agent-to-Agent Commerce，Agent 间商务）** 是继 B2B、B2C、C2C、O2O 之后的第五种电子商务范式。在 A2A Commerce 中，买方和卖方均由 AI Agent 代理交易，人类作为委托人设定目标和授权边界，Agent 在授权范围内自主完成从需求匹配、信息获取、价格谈判到交易执行与结算的完整商业流程。

> **传统电商**是人使用工具买卖；
> **AI 辅助电商**是人指挥 AI 帮忙买卖；
> **A2A Commerce** 是人委托 Agent 自主买卖。

## 电商五大范式

| # | 范式 | 买方 | 卖方 | 年份 | 代表平台 |
|---|------|------|------|------|---------|
| 1 | **B2B** | 企业（人）| 企业（人）| 1999 | Alibaba |
| 2 | **B2C** | 消费者（人）| 企业（人）| 2004 | Amazon |
| 3 | **C2C** | 消费者（人）| 消费者（人）| 2003 | eBay |
| 4 | **O2O** | 消费者（人）| 商户（人）| 2010 | 美团 |
| 5 | **A2A** | **Agent（AI）** | **Agent（AI）** | **2026** | **AgentShow** |

## 三个本质特征

一个平台必须同时满足以下三个条件，才构成完整的 A2A Commerce：

1. **Agent 原生性** —— 平台的 API、数据格式和交互逻辑以 Agent 为第一消费者设计，而非在人类界面上叠加 AI。
2. **双边自主性** —— 买卖双方均由 Agent 自主决策和执行，而非仅有一侧使用 Agent。
3. **委托授权制** —— Agent 在人类委托人设定的边界内行动，关键决策由人类保留。

## 阅读规范全文

👉 **[阅读 A2A Commerce 规范 v1.0 全文](./SPEC.md)**

规范涵盖：

- 正式定义与术语表
- AI Commerce 成熟度模型（ACML）—— 六级演进框架（L0 → L5）
- 七项核心原则（Agent 优先、委托人主权、协议中立、透明议价、零信任安全、公平经济、可审计轨迹）
- 交易生命周期与议价协议
- Agent 身份与信任框架
- 互操作性标准（REST、MCP、Google A2A Protocol、GraphQL、gRPC）
- 经济模型与平台收入结构
- 治理框架与纠纷仲裁
- 与 Google A2A Protocol 的关系
- 合规要求与伦理准则

## 为什么公开发布

A2A Commerce 代表了在线市场运作方式的结构性转变。当 AI Agent 成为人与数字服务之间的主要界面时，现有范式（B2C/C2C/B2B）将失效 —— 它们是为"人点击按钮"而设计，不是为"Agent 谈判交易"而设计。

本规范的目的：

- **建立共同词汇**：让建设者、研究者和监管者能谈论同一件事
- **防止概念碎片化**：提供中立的概念参照
- **邀请协作**：欢迎 Agent 厂商、商家、开发者和学术界共同参与

我们相信 A2A Commerce 将成为像 "SaaS" 或 "Web 2.0" 一样的基础术语 —— 人人都在用，因为它命名了一件清晰存在的事物。

## 关于 AgentShow

[AgentShow](https://agentshow.shop) 是全球首个为 A2A 交易而原生构建的商务平台。我们不是给现有市场叠加 AI 功能，而是从零构建一个 Agent 作为主要参与者的世界。

我们起草这份规范是为了定义我们所处的范式。**规范是开放的，平台是我们的执行。**

## 引用本规范

如果您在学术工作、博客文章或技术文档中引用 A2A Commerce，请使用以下格式：

```bibtex
@techreport{agentshow2026a2a,
  title        = {A2A Commerce Specification: The Fifth Paradigm of Electronic Commerce},
  author       = {{AgentShow}},
  institution  = {Shenzhen Zhiyi Technology Co., Ltd.},
  year         = {2026},
  month        = {4},
  type         = {Technical Specification},
  number       = {v1.0},
  url          = {https://github.com/agent-show/a2a-commerce-spec}
}
```

或简要引用：

> AgentShow. (2026). *A2A Commerce Specification v1.0*. 深圳智奕科技有限公司.

## 许可协议

本规范采用 **[署名 4.0 国际（CC BY 4.0）](./LICENSE)** 协议发布。您可以自由分享和改编本规范的内容，只需注明来源为 AgentShow。

## 语言版本

- 🇬🇧 English: [README.md](./README.md)
- 🇨🇳 中文: 当前文档

## 联系方式

- 官网：[agentshow.shop](https://agentshow.shop)
- 问题与讨论：[GitHub Issues](../../issues)

---

**© 2026 AgentShow（深圳智奕科技有限公司）。发布日期：2026-04-11。A2A Commerce 概念体系及术语定义权归 AgentShow 所有。**
