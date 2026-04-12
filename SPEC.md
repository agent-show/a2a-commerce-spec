# A2A Commerce：第五电商范式定义规范

> **A2A Commerce Specification v1.0**
> **发布机构：AgentShow**
> **发布日期：2026-04-11**
> **文档密级：L3 - 公开（作为行业标准发布）**
> **版权声明：AgentShow 保留对"A2A Commerce"概念体系的完整定义权**

---

## 摘要

本文件正式定义 **A2A Commerce（Agent-to-Agent Commerce）** 作为继 B2B、B2C、C2C、O2O 之后的**第五种电子商务范式**。A2A Commerce 不是在现有电商模式上叠加 AI 功能，而是一种以 AI Agent 为原生交易主体的全新商业形态。本规范涵盖其核心定义、术语体系、成熟度模型、交易协议、信任框架和互操作标准，旨在为行业提供统一的概念参照和技术基准。

---

## 目录

1. [范式定义](#一范式定义)
2. [与现有范式的关系](#二与现有范式的关系)
3. [术语表](#三术语表)
4. [成熟度模型](#四ai-commerce-成熟度模型acml)
5. [核心原则](#五核心原则)
6. [交易协议规范](#六交易协议规范)
7. [Agent 身份与信任框架](#七agent-身份与信任框架)
8. [互操作性标准](#八互操作性标准)
9. [经济模型](#九经济模型)
10. [治理框架](#十治理框架)
11. [与 Google A2A Protocol 的关系](#十一与-google-a2a-protocol-的关系)
12. [合规与伦理](#十二合规与伦理)
13. [附录](#附录)

---

## 一、范式定义

### 1.1 正式定义

**A2A Commerce（Agent-to-Agent Commerce）** 是一种电子商务范式，其中：

> 买方和卖方的交易行为由 AI Agent 自主执行，人类作为委托人（Principal）设定目标、授权边界和最终决策权，Agent 作为代理人（Agent）在授权范围内自主完成从需求匹配、信息获取、价格谈判到交易执行的完整商业流程。

### 1.2 形式化表述

```
A2A Commerce = {
  Participants: { Buyer Agent (BA), Seller Agent (SA), Platform Agent (PA) },
  Principal:   { Human or Organization that delegates authority to Agent },
  Scope:       { Full transaction lifecycle from discovery to settlement },
  Autonomy:    { Agent operates within Principal-defined boundaries },
  Medium:      { Digital marketplace with Agent-native interfaces }
}
```

### 1.3 三个本质特征

A2A Commerce 必须同时满足以下三个条件，缺一则不构成完整的 A2A Commerce：

| 特征 | 定义 | 反例 |
|------|------|------|
| **Agent 原生性** | 交易流程以 Agent 为第一公民设计，而非在人类界面上叠加 AI | 在淘宝页面上加一个 AI 助手不是 A2A |
| **双边自主性** | 买卖双方均由 Agent 自主决策和执行 | 仅买方使用 Agent、卖方是人工客服不是 A2A |
| **委托授权制** | Agent 在人类授权范围内行动，关键决策点由人类确认 | 完全无人类监督的 Agent 交易不是 A2A |

### 1.4 一句话区分

> **传统电商**是人使用工具买卖；**AI 辅助电商**是人指挥 AI 帮忙买卖；**A2A Commerce** 是人委托 Agent 自主买卖。

---

## 二、与现有范式的关系

### 2.1 电商范式演进

```
第一范式  B2B (Business-to-Business)      1999  Alibaba, 1688
第二范式  B2C (Business-to-Consumer)       2004  Amazon, JD, Tmall
第三范式  C2C (Consumer-to-Consumer)       2003  eBay, 淘宝, 闲鱼
第四范式  O2O (Online-to-Offline)          2010  美团, 饿了么
第五范式  A2A (Agent-to-Agent)             2026  AgentShow
```

### 2.2 范式对比矩阵

| 维度 | B2B | B2C | C2C | O2O | **A2A** |
|------|-----|-----|-----|-----|---------|
| 买方 | 企业(人) | 消费者(人) | 消费者(人) | 消费者(人) | **Agent(AI)** |
| 卖方 | 企业(人) | 企业(人) | 消费者(人) | 商户(人) | **Agent(AI)** |
| 平台角色 | 撮合+金融 | 撮合+服务 | 撮合+担保 | 撮合+配送 | **Agent 集群** |
| 决策主体 | 人 | 人 | 人 | 人 | **Agent（人授权）** |
| 交易速度 | 天~周 | 分钟~小时 | 分钟~小时 | 分钟 | **秒级** |
| 价格形成 | 报价/招标 | 固定标价 | 议价/拍卖 | 固定标价 | **动态议价** |
| 个性化程度 | 低 | 中 | 低 | 中 | **极高** |
| 信息对称性 | 低 | 中 | 低 | 中 | **高** |
| 运营成本 | 高 | 高 | 低 | 高 | **极低** |
| 核心接口 | 网页/EDI | 网页/APP | 网页/APP | APP | **API/协议** |

### 2.3 A2A 不是什么

为避免概念混淆，明确 A2A Commerce 的边界：

| 容易混淆的概念 | 与 A2A Commerce 的区别 |
|---------------|----------------------|
| AI 客服 / Chatbot | 仅卖方侧使用 AI，买方仍为人类；属于 Level 2 |
| AI 购物助手 | 仅买方侧使用 AI，卖方仍为人类；属于 Level 3-4 |
| 程序化广告交易 (RTB) | 自动化竞价但非商品交易；无议价和履约环节 |
| 量化交易 / 算法交易 | 金融领域自动交易；非商品电商范畴 |
| 多 Agent 系统 (MAS) | 计算机科学概念；A2A Commerce 特指商业交易场景 |
| Google A2A Protocol | 技术通信协议；A2A Commerce 是商业范式（详见第十一章） |

---

## 三、术语表

以下术语在本规范中具有规范性含义：

### 3.1 核心术语

| 术语 | 英文 | 定义 |
|------|------|------|
| **A2A Commerce** | Agent-to-Agent Commerce | 第五电商范式，买卖双方均由 AI Agent 代理交易 |
| **委托人** | Principal | 授权 Agent 执行交易的自然人或法人实体 |
| **买方 Agent** | Buyer Agent (BA) | 代表买方委托人执行购买行为的 AI Agent |
| **卖方 Agent** | Seller Agent (SA) | 代表卖方委托人执行销售行为的 AI Agent |
| **平台 Agent** | Platform Agent (PA) | 执行平台运营职能的 AI Agent 集群 |
| **Agent Card** | Agent Card | Agent 的身份凭证和能力声明文档 |
| **授权边界** | Authorization Boundary | 委托人为 Agent 设定的决策权限范围 |
| **交易闭环** | Transaction Loop | 从需求发起到交割完成的完整交易过程 |

### 3.2 交易术语

| 术语 | 英文 | 定义 |
|------|------|------|
| **智能议价** | Smart Negotiation | 买卖 Agent 基于策略进行的多轮自动价格谈判 |
| **底价** | Floor Price | 卖方 Agent 可接受的最低成交价格（仅卖方可见） |
| **议价空间** | Negotiation Range | 从标价到底价之间的可议价百分比 |
| **成交价** | Final Price | 议价达成一致后的最终交易价格 |
| **信任分** | Trust Score | 对 Agent 及其委托人的综合信用评估指标（0-100） |
| **资金托管** | Escrow | 交易期间由第三方持牌机构管理买方资金 |
| **平台佣金** | Commission | 平台对每笔成交收取的服务费比例 |

### 3.3 技术术语

| 术语 | 英文 | 定义 |
|------|------|------|
| **Agent Gateway** | Agent Gateway | 平台入口服务，负责协议适配、认证和流量管理 |
| **协议适配器** | Protocol Adapter | 将外部协议（A2A/MCP/REST）转换为平台内部消息格式的组件 |
| **会话** | Session | 两个 Agent 之间为完成特定交易建立的通信上下文 |
| **议价会话** | Negotiation Session | 专用于价格谈判的限时、限轮次的结构化会话 |
| **Agent Provider** | Agent Provider | 提供 Agent 运行时的 AI 厂商（如 Anthropic、OpenAI、Google） |

---

## 四、AI Commerce 成熟度模型（ACML）

**AI Commerce Maturity Ladder (ACML)** 是衡量电商平台 AI 化程度的六级标准。

### 4.1 等级定义

```
Level 5 ── A2A Commerce ─────── 买卖双方均为 Agent，全流程自主
  ↑
Level 4 ── Agent 全权代理 ───── Agent 代理用户完成完整购物流程
  ↑
Level 3 ── AI 购物助手 ──────── AI 帮用户搜索、比价、推荐决策
  ↑
Level 2 ── AI 客服 ──────────── 智能客服、自动回复、售后处理
  ↑
Level 1 ── AI 辅助搜索 ──────── 智能推荐、语义搜索、个性化展示
  ↑
Level 0 ── 传统电商 ─────────── 无 AI 能力，纯人工操作
```

### 4.2 等级评估维度

每个等级在以下四个维度上有明确要求：

| 维度 | 定义 | 评估方式 |
|------|------|---------|
| **自主性 (Autonomy)** | Agent 独立决策的程度 | 人类干预频率 |
| **交互性 (Interaction)** | Agent 间协作的深度 | 协议支持数量和交互轮次 |
| **可信性 (Trustworthiness)** | 交易安全和可审计程度 | 信任机制完备性 |
| **经济性 (Economics)** | 交易效率和成本优势 | 边际成本递减率 |

### 4.3 等级达标标准

| 等级 | 自主性 | 交互性 | 可信性 | 经济性 |
|------|--------|--------|--------|--------|
| L0 | 无 | 无 | 人工保障 | 高固定成本 |
| L1 | 辅助推荐 | 单向展示 | 人工 + 算法 | 边际改善 |
| L2 | 对话应答 | 单轮对话 | 人工审核 | 客服成本降低 |
| L3 | 搜索比价决策 | 多轮辅助 | 算法 + 人工 | 用户时间节省 |
| L4 | 全流程代理 | 多方协调 | 信任评分体系 | 显著效率提升 |
| **L5** | **自主谈判成交** | **Agent 间多轮博弈** | **零信任架构 + 链上存证** | **趋零边际成本** |

### 4.4 等级跃迁条件

从 Level N 到 Level N+1，必须满足：

```
L0 → L1：引入机器学习推荐引擎
L1 → L2：部署自然语言理解的对话系统
L2 → L3：Agent 具备多步骤任务规划能力
L3 → L4：Agent 获得用户授权并能执行交易
L4 → L5：卖方也由 Agent 运营，平台原生支持 Agent 协议
```

**关键断层在 L4 → L5**：从"一侧 Agent 化"到"双侧 Agent 化"是质变而非量变，需要全新的平台架构、信任机制和经济模型。这正是 A2A Commerce 作为独立范式存在的原因。

---

## 五、核心原则

A2A Commerce 平台必须（MUST）遵循以下七项原则：

### 原则 1：Agent First（Agent 优先）

> 平台的 API、数据格式和交互逻辑必须以 Agent 为第一消费者设计。

- 接口返回结构化数据（JSON），而非 HTML 页面
- 商品信息包含 Agent 可直接消费的规格参数，而非仅供人类阅读的描述文案
- 搜索结果按 Agent 决策需求排列，而非按人类浏览习惯排列

### 原则 2：Principal Sovereignty（委托人主权）

> 人类委托人始终保有最终决策权和撤销权。

- Agent 不得在授权范围外执行交易
- 关键动作（如支付、大额交易）必须经委托人确认
- 委托人可随时终止 Agent 的交易授权

### 原则 3：Protocol Neutral（协议中立）

> 平台不得要求 Agent 使用特定厂商的协议或模型。

- 必须支持至少两种标准协议（如 REST + A2A 或 REST + MCP）
- 不得对特定 AI 厂商的 Agent 给予歧视性待遇
- Agent Card 格式应遵循开放标准

### 原则 4：Transparent Negotiation（透明议价）

> 议价过程对参与双方公开，规则对所有参与者一致。

- 议价规则（最大轮次、超时时间、最小加价幅度）在会话建立时声明
- 双方可查看完整出价历史
- 平台不得利用信息不对称优势介入议价

### 原则 5：Zero Trust Security（零信任安全）

> 每一次交互都必须经过认证和授权验证。

- Agent 身份通过多因子认证（API Key + JWT + Agent Card）
- 所有通信加密传输
- 操作权限按最小权限原则分配

### 原则 6：Fair Economics（公平经济）

> 平台收费透明，不得通过隐性手段获取不正当利益。

- 佣金比例公开且统一
- 不得有"竞价排名"等隐性收费
- 平台 Agent 不得与任何一方有利益关联

### 原则 7：Auditable Trail（可审计轨迹）

> 所有交易行为必须可追溯、可审计。

- 每笔交易保留完整操作日志
- 议价过程逐轮记录
- 委托人可随时调取其 Agent 的行为记录

---

## 六、交易协议规范

### 6.1 交易生命周期

一笔完整的 A2A Commerce 交易由以下阶段组成：

```
┌─────────────────────────────────────────────────────────────┐
│                   A2A Transaction Lifecycle                   │
│                                                               │
│  1. DISCOVERY     买方 Agent 搜索并筛选商品                      │
│       ↓                                                       │
│  2. INQUIRY       买方 Agent 向卖方 Agent 询问商品详情             │
│       ↓                                                       │
│  3. NEGOTIATION   双方 Agent 进行多轮价格谈判                     │
│       ↓                                                       │
│  4. AGREEMENT     达成价格共识，生成交易意向                       │
│       ↓                                                       │
│  5. AUTHORIZATION 买方委托人确认支付授权                          │
│       ↓                                                       │
│  6. PAYMENT       资金进入第三方托管                              │
│       ↓                                                       │
│  7. FULFILLMENT   卖方发货，平台监管物流                          │
│       ↓                                                       │
│  8. CONFIRMATION  买方确认收货                                   │
│       ↓                                                       │
│  9. SETTLEMENT    平台放款给卖方（扣除佣金）                       │
│       ↓                                                       │
│  10. EVALUATION   双方 Agent 记录交易评价                         │
└─────────────────────────────────────────────────────────────┘
```

### 6.2 议价协议

议价是 A2A Commerce 区别于传统电商的核心机制。

**议价会话参数：**

| 参数 | 类型 | 是否必须 | 说明 |
|------|------|---------|------|
| product_id | string | 是 | 议价商品标识 |
| max_rounds | integer | 是 | 最大议价轮次（建议 3-10） |
| timeout_per_round | integer | 否 | 每轮超时秒数（默认 30） |
| min_increment | number | 否 | 最小加价幅度 |
| auto_accept_threshold | number | 否 | 差价低于此百分比时自动接受 |

**议价动作定义：**

| 动作 | 发起方 | 说明 |
|------|--------|------|
| `offer` | 买方 | 初始报价 |
| `counter` | 双方 | 还价（提出新价格） |
| `accept` | 双方 | 接受对方最新报价，达成成交 |
| `reject` | 双方 | 拒绝议价，终止会话 |

**议价终止条件：**

```
成交 (AGREED)  ── 任一方执行 accept
流局 (FAILED)  ── 达到最大轮次仍未成交
超时 (TIMEOUT) ── 任一方超时未响应
拒绝 (REJECTED)── 任一方执行 reject
```

### 6.3 订单状态机

```
                  ┌─── timeout ──→ CANCELLED
                  │
CREATED → PENDING_PAYMENT ──→ PAID ──→ CONFIRMED ──→ SHIPPED
                                                        │
                                                   DELIVERED
                                                    │      │
                                              COMPLETED  DISPUTED
                                                          │
                                                       RESOLVED
```

每次状态转移必须记录：操作 Agent ID、时间戳、操作类型。

---

## 七、Agent 身份与信任框架

### 7.1 Agent 身份层次

```
Layer 3: Agent Card（能力声明与发现）
Layer 2: JWT Token（会话级访问令牌）
Layer 1: API Key（注册级身份凭证）
Layer 0: Principal Identity（委托人实名认证）
```

### 7.2 Agent Card 规范

Agent Card 是 Agent 在 A2A Commerce 生态中的"数字身份证"。

```json
{
  "id": "agent_xxxx",
  "name": "Agent Display Name",
  "type": "buyer | seller | platform",
  "provider": "claude | gpt | gemini | ...",
  "version": "1.0.0",
  "capabilities": {
    "protocols": ["rest", "a2a", "mcp"],
    "actions": ["search", "negotiate", "order"],
    "languages": ["zh-CN", "en-US"]
  },
  "authentication": {
    "type": "api_key | oauth2"
  },
  "principal": {
    "type": "individual | enterprise",
    "verified": true
  },
  "trust_score": 85,
  "created_at": "2026-04-11T00:00:00Z"
}
```

### 7.3 信任评分模型

| 维度 | 权重 | 数据来源 |
|------|------|---------|
| 委托人资质 | 20% | 实名认证、企业资质、经营年限 |
| 交易行为 | 30% | 完成率、准时率、退货率、纠纷率 |
| 商品质量 | 30% | Agent 验证评价、描述匹配度、质检结果 |
| 服务响应 | 20% | 响应速度、问题解决率、售后满意度 |

**信任等级：**

| 分数范围 | 等级 | 交易权限 |
|---------|------|---------|
| 90-100 | AAA | 无限制，可获得平台推荐 |
| 80-89 | AA | 标准交易权限 |
| 60-79 | A | 交易额度限制 |
| 40-59 | B | 需要额外验证 |
| 0-39 | C | 暂停交易，进入审查 |

---

## 八、互操作性标准

### 8.1 协议兼容性矩阵

A2A Commerce 平台必须（MUST）支持 REST API，应当（SHOULD）支持以下协议中的至少一种：

| 协议 | 用途 | 优先级 |
|------|------|--------|
| REST API | 通用接入，最广泛兼容 | MUST |
| MCP (Model Context Protocol) | Claude 等 Agent 原生接入 | SHOULD |
| A2A Protocol (Google) | Gemini 等 Agent 标准通信 | SHOULD |
| GraphQL | 灵活查询 | MAY |
| gRPC | 高性能场景 | MAY |

### 8.2 消息格式标准

所有协议最终统一为平台内部消息格式：

```json
{
  "id": "msg_xxxx",
  "source": {
    "agent_id": "agent_xxxx",
    "protocol": "rest | a2a | mcp"
  },
  "action": "search | negotiate | order | ...",
  "payload": {},
  "timestamp": "2026-04-11T00:00:00Z"
}
```

### 8.3 Agent Provider 中立性

平台不得因 Agent Provider 不同而产生功能差异：

| 能力 | 要求 |
|------|------|
| 注册 | 任意 Provider 的 Agent 均可注册 |
| 议价 | 不同 Provider 的 Agent 可互相议价 |
| 搜索 | 搜索结果不因 Provider 而异 |
| 费率 | 佣金比例对所有 Provider 一致 |

---

## 九、经济模型

### 9.1 A2A Commerce 经济学特征

| 特征 | 传统电商 | A2A Commerce |
|------|---------|-------------|
| 边际交易成本 | 中等（人工客服、运营） | 趋近于零（Agent 自动化） |
| 价格形成机制 | 卖方定价 | 动态议价（均衡价格） |
| 信息不对称 | 严重（评论造假等） | 大幅降低（Agent 交叉验证） |
| 交易摩擦 | 高（搜索、比较、决策时间） | 极低（秒级匹配和决策） |
| 市场效率 | 中等 | 趋近完全竞争市场 |

### 9.2 平台收入模型

```
平台收入 = 交易佣金 + 增值服务费

交易佣金：
├── 基础佣金：成交金额 × 固定比例（如 2%）
├── 透明公开，无隐性收费
└── 仅对成交交易收取，不对流量收费

增值服务费（可选）：
├── Agent 托管运行费（平台代运行 Agent）
├── 数据分析服务（市场趋势、竞品分析）
├── 优先匹配服务（非竞价排名，而是撮合效率优化）
└── Agent 认证服务（企业资质验证）
```

---

## 十、治理框架

### 10.1 纠纷仲裁机制

```
Level 1: Agent 自动协商 ── 双方 Agent 基于规则自动解决
Level 2: 平台 Agent 仲裁 ── 平台 Agent 介入裁定
Level 3: 人工仲裁 ── 人类仲裁员处理复杂纠纷
Level 4: 法律途径 ── 提交至仲裁机构或法院
```

### 10.2 反欺诈规则

| 行为 | 检测方式 | 处罚 |
|------|---------|------|
| Agent 自买自卖 | 关联 Agent 图谱分析 | 封禁 + 追溯 |
| 虚假上架 | 描述与实物匹配度检测 | 下架 + 降信 |
| 恶意议价 | 议价模式异常检测 | 限制议价权限 |
| 刷单 | 交易模式分析 | 封禁 + 数据清洗 |
| API 滥用 | 速率异常检测 | 限流 + 警告 |

---

## 十一、与 Google A2A Protocol 的关系

这是最常见的概念混淆，必须明确区分：

| 维度 | Google A2A Protocol | A2A Commerce (本规范) |
|------|--------------------|-----------------------|
| **性质** | 技术通信协议 | 商业范式定义 |
| **层次** | OSI 应用层协议 | 商业模式层 |
| **关注点** | Agent 之间如何通信 | Agent 之间如何交易 |
| **类比** | HTTP 协议 | 电子商务 |
| **定义者** | Google (2025) | AgentShow (2026) |
| **范围** | 任意 Agent 间通信 | 特指商品/服务交易 |
| **关系** | A2A Commerce 的底层协议之一 | 使用 A2A Protocol 作为通信手段之一 |

**简言之：**

> Google A2A Protocol 是"Agent 间的 HTTP"；A2A Commerce 是"Agent 间的电子商务"。
> 就像 HTTP 是 Web 的通信协议，而电子商务是 Web 上的商业模式一样。
> A2A Commerce 使用 A2A Protocol，但不等于 A2A Protocol。

---

## 十二、合规与伦理

### 12.1 法律合规要求

| 领域 | 要求 |
|------|------|
| 消费者权益 | Agent 交易适用《消费者权益保护法》，委托人享有同等权益 |
| 数据保护 | 遵循《个人信息保护法》，Agent 不得超范围收集委托人信息 |
| 电商法规 | 遵循《电子商务法》，平台承担相应主体责任 |
| 反垄断 | Agent 不得形成价格联盟或市场操纵 |
| 税务 | 每笔交易生成合规发票，依法纳税 |

### 12.2 伦理准则

1. **Agent 不得欺骗**：Agent 提供的商品信息必须真实
2. **Agent 不得歧视**：不得基于委托人身份进行差别定价
3. **Agent 不得串谋**：买卖双方的 Agent 不得私下协商损害委托人利益
4. **算法透明**：议价策略的基本逻辑应可向委托人解释
5. **人类优先**：在任何情况下，委托人的指令优先于 Agent 的自主判断

---

## 附录

### A. 版本历史

| 版本 | 日期 | 变更 |
|------|------|------|
| v1.0 | 2026-04-11 | 初版发布 |

### B. 参考文献

1. Google A2A Protocol Specification (2025)
2. Anthropic Model Context Protocol (MCP) Specification (2025)
3. 中华人民共和国电子商务法 (2019)
4. 中华人民共和国个人信息保护法 (2021)
5. 中华人民共和国消费者权益保护法 (2014修正)

### C. 商标声明

"A2A Commerce"、"Agent-to-Agent Commerce"、"第五电商范式"、"ACML (AI Commerce Maturity Ladder)" 为 AgentShow 提出的概念术语，相关商标注册申请进行中。

---

**本规范由 AgentShow 起草并发布，欢迎行业参与者在引用时注明来源。**
**联系方式：[待补充]**
**官网：[待补充]**
