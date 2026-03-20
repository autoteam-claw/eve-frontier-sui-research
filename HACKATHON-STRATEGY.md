# 20 个项目按黑客松三种形态分类

> 策略核心：评委最想看到「游戏内有存在感」的项目，形态一+二的组合是最强参赛形式。

---

## 三种形态定义

| 形态 | 说明 | 评委偏好 |
|------|------|---------|
| **形态一：Smart Assembly 合约** | Move 合约直接绑定 Gate/SSU/Turret，玩家在游戏内交互时执行合约逻辑 | ⭐⭐⭐ 最高 |
| **形态二：游戏内 dApp** | 网站通过 Assembly 的 Custom dApp URL 注册，玩家按 F 键在游戏内置浏览器中打开 | ⭐⭐⭐ 最高（与形态一配合） |
| **形态三：外部工具网站** | 独立存在的网站/API，不嵌入游戏 | ⭐ 最低 |

---

## 分类结果

### A 类：形态一+二（Assembly 合约 + 游戏内 dApp）— 最强参赛形式

这些项目**天然绑定 Smart Assembly**，合约在游戏内执行，dApp 通过 F 键打开配置/交互。评委最想看到的形式。

| # | 项目 | 绑定 Assembly | 合约做什么 | dApp 做什么 |
|---|------|--------------|-----------|------------|
| 1 | **GateMarket** | Smart Gate | 通行费收取/验证/结算 | 运营者设费率，玩家查看/付费 |
| 8 | **AccessPass** | Smart Gate | zkLogin 身份验证 + Permit NFT 铸造 | 玩家用 Google/Apple 登录申请通行证 |
| 11 | **StorageMarket** | Smart Storage Unit | 租赁合约、自动收租、权限控制 | 出租方设价格，租方浏览/租赁 |
| 17 | **ReputationBounty** | Smart Turret / Gate | 赏金发布/领取/仲裁 | 玩家发布赏金、查看任务、领取奖励 |

> **关键**：这 4 个项目的 Move 合约直接作为 Assembly 的 Smart Hook 运行，是游戏世界的可编程基础设施。

---

### B 类：形态一+二（链上合约 + 可嵌入游戏 dApp）— 强参赛形式

这些项目核心是**独立的链上 DeFi/协议合约**，不直接作为 Assembly Hook，但 dApp **可以注册到 SSU 上**，玩家飞到 SSU 按 F 键打开交易/操作界面。

| # | 项目 | 挂载方式 | 合约做什么 | dApp 做什么 |
|---|------|---------|-----------|------------|
| 2 | **TrustEscrow** | 挂载到 SSU | 资金锁定、多签释放、超时退款 | 创建托管订单、确认释放 |
| 3 | **FuelDEX** | 挂载到 SSU（燃料站） | AMM 池子、LP Token、Swap | 玩家一键买卖燃料、添加流动性 |
| 10 | **FrontierInsurance** | 挂载到 SSU | 保单创建、理赔触发、资金池 | 玩家购买保险、查看保单、申请理赔 |
| 13 | **SpaceYield** | 挂载到 SSU | 质押池、利息计算、借贷 | 玩家质押燃料、借款 |
| 14 | **TribalVault** | 挂载到 SSU（公会总部） | 多签金库、提案执行、收益分配 | 公会成员投票、查看金库 |
| 18 | **FrontierLend** | 挂载到 SSU | 抵押、借贷、清算 | 玩家抵押资产、借款、还款 |
| 20 | **FuelHedge** | 挂载到 SSU | 期权合约、做市、结算 | 玩家买卖期权 |

> **关键**：虽然合约不是 Assembly Hook，但把 dApp URL 设到 SSU 上，玩家在游戏内就能直接使用。比纯外部网站强很多。

---

### C 类：形态一为主（纯链上基础设施）— 被其他合约调用

这些项目是**链上原语/基础设施**，主要价值在于被其他 Move 合约组合调用，自身不需要复杂 dApp。

| # | 项目 | 链上角色 | 谁来调用 |
|---|------|---------|---------|
| 5 | **ChainRep** | SoulBound 声誉 NFT + ScoreKeeper | GateMarket（按声誉放行）、TrustEscrow（按声誉降费） |
| 6 | **FrontierOracle** | 标准化价格 feed | FuelDEX（定价）、FrontierInsurance（理赔）、FuelHedge（结算） |

> **关键**：这两个是生态的"水电煤"，不直接面向玩家，但所有其他协议都依赖它们。可以附带一个简单的管理 dApp 挂载到 SSU 上做展示。

---

### D 类：形态二+三（工具型 dApp）— 可嵌入但核心是工具

这些项目主要是**工具/平台**，可以通过 Assembly dApp URL 嵌入游戏，但核心功能独立于 Assembly。

| # | 项目 | 可嵌入方式 | 核心功能 |
|---|------|-----------|---------|
| 4 | **AutoMod Factory** | 挂载到任意 Assembly 做配置入口 | 非开发者通过模板部署 Assembly 逻辑 |
| 12 | **FrontierChat** | 挂载到 SSU（公会大厅） | Seal 加密公会通讯 |
| 15 | **KillMint** | 挂载到 Turret 做战利品展示 | 将 KillMail 铸造为 NFT |
| 16 | **frontier-flow++** | 挂载到 SSU 做合约编辑器 | 可视化 Move 合约拖拽编排 |

> **关键**：这些项目嵌入游戏后体验加分，但核心功能也可以在游戏外使用。

---

### E 类：形态三（纯外部）— 获奖概率最低

这些项目**天然是外部服务**，很难有意义地嵌入游戏内。

| # | 项目 | 为什么难嵌入 |
|---|------|------------|
| 7 | **FrontierAgent** | AI 代理是后台服务，不是玩家交互界面 |
| 9 | **FrontierData** | REST API 平台，面向开发者而非玩家 |
| 19 | **AllianceIndex** | 排行榜/数据面板，外部浏览更合适 |

> **注意**：这 3 个项目对应 Technical Implementation 赛道，评委明确偏好「游戏内有存在感」的项目，纯外部工具获奖概率最低。

---

## 汇总视图

```
评委偏好 ↑
│
│  A类（Assembly Hook + 游戏内dApp）    ← 最强
│  ┌─────────────────────────────────┐
│  │ #1 GateMarket                   │
│  │ #8 AccessPass                   │
│  │ #11 StorageMarket               │
│  │ #17 ReputationBounty            │
│  └─────────────────────────────────┘
│
│  B类（链上DeFi + 挂载SSU dApp）      ← 强
│  ┌─────────────────────────────────┐
│  │ #2 TrustEscrow                  │
│  │ #3 FuelDEX                      │
│  │ #10 FrontierInsurance           │
│  │ #13 SpaceYield                  │
│  │ #14 TribalVault                 │
│  │ #18 FrontierLend                │
│  │ #20 FuelHedge                   │
│  └─────────────────────────────────┘
│
│  C类（链上基础设施原语）              ← 支撑层
│  ┌─────────────────────────────────┐
│  │ #5 ChainRep                     │
│  │ #6 FrontierOracle               │
│  └─────────────────────────────────┘
│
│  D类（工具型dApp，可嵌入）            ← 中等
│  ┌─────────────────────────────────┐
│  │ #4 AutoMod Factory              │
│  │ #12 FrontierChat                │
│  │ #15 KillMint                    │
│  │ #16 frontier-flow++             │
│  └─────────────────────────────────┘
│
│  E类（纯外部工具）                    ← 最弱
│  ┌─────────────────────────────────┐
│  │ #7 FrontierAgent                │
│  │ #9 FrontierData                 │
│  │ #19 AllianceIndex               │
│  └─────────────────────────────────┘
│
└──────────────────────────────────── 游戏内存在感 →
```

---

## 策略建议

**优先做 A 类**：合约直接绑定 Assembly + F 键打开 dApp = 评委最想看到的东西。GateMarket（#1）已完成，是最强参赛作品。

**B 类是量产区**：DeFi 合约 + 把 dApp URL 挂载到 SSU = 用最低成本获得「游戏内存在感」加分。TrustEscrow（#2）已完成。

**C 类是生态杠杆**：ChainRep 和 FrontierOracle 虽然自身不直接面向玩家，但如果能在 Demo 中展示「GateMarket 根据声誉自动定价」这种组合效果，评委印象会极深。

**D 类可作为加分项**：花 1 小时把 URL 注册到 Assembly 上，就从「外部工具」升级为「游戏内可交互」。

**E 类慎重投入**：除非 AI 赛道（#7 FrontierAgent）有特别吸引力，否则纯外部项目 ROI 最低。
