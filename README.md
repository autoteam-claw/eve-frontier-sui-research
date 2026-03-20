# EVE Frontier × Sui — 20 个最优赚钱项目

> 研究时间：2026-03-20 | 作者：clawdbot20090103 | 组织：autoteam-claw

## 研究背景

EVE Frontier 是基于 Sui 区块链的新一代沙盒游戏，三类可编程 Smart Assembly（智能星门/仓储/炮塔）+ 完全开放的玩家经济体系，是 Web3 游戏生态迄今最大的开发者机会。本报告通过系统研究黑客松规则、生态现状、现有工具空白、EVE Online 历史先例和 Sui 链差异化能力，构建交叉矩阵，筛选出 20 个「黄金三角」项目——同时满足：填补真实空白 × Sui 差异化能力 × 持续收益机制。

---

## Phase 1：研究摘要

### EVE Frontier 核心机制

| Assembly 类型 | 功能 | 编程能力 |
|---|---|---|
| Smart Gate | 星门/通行控制 | 自定义通行规则 |
| Smart Storage Unit | 仓库/交易所 | 自定义存取规则 |
| Smart Turret | 炮塔/防御 | 自定义打击目标 |

- 所有 Assembly 依赖 **Network Node** 供能，Network Node 需持续注入燃料 → **燃料是核心稀缺资源**
- 支持自定义货币、去中心化市场、服务经济
- 所有 Assembly 逻辑以 Sui Move 合约形式部署，可与 world-contracts 直接组合

### 现有工具竞争分析

| 项目 | Stars | 功能 | 状态 |
|------|-------|------|------|
| evefrontier-rs | 0 | 路径规划/地图 CLI | ❌ 已饱和 |
| efctl | 2 | 本地开发环境 | ❌ 官方工具 |
| FrontierSharp | 4 | C# API客户端 | ❌ 已饱和 |
| frontier-flow | 0 | 可视化合约编排（草案）| ✅ 可超越 |
| EVEFrontier_TrustLocker | 0 | 托管协议（草案）| ✅ 可超越 |

### 完全空白的市场节点

- 燃料链上交易所 ✅
- 玩家托管协议 ✅（只有草案）
- 链上声誉系统 ✅
- 链上保险 ✅
- Move 合约模板市场 ✅
- 价格预言机 ✅
- 数据 API 平台 ✅
- 星门通行费协议 ✅

### DeepSurge 黑客松赛道

DeFi · Infra & Tooling · Culture & Entertainment · AI · Programmable Storage · Payments & Wallets · Explorations · Cryptography · Degen

### Sui 差异化能力（vs EVM）

| 能力 | 说明 | 游戏应用 |
|---|---|---|
| **Seal** | 去中心化访问控制/密钥管理 | 私密通行许可、加密公会通讯 |
| **Walrus** | 可编程链上存储 | 游戏历史数据、合约模板存储 |
| **zkLogin** | Google/Apple → Sui 钱包 | Web2 玩家无摩擦 onboarding |
| **Sponsored Tx** | Gas 代付 | 新手零门槛体验 |
| **Object 模型** | 真实资产所有权/组合性 | JumpPermit、声誉 SBT |
| **Move** | 与游戏合约直接组合 | 扩展 world-contracts |

### EVE Online 历史先例（赚钱验证）

| 工具 | 商业模式 | 估算年收入 |
|---|---|---|
| zkillboard | 广告 + 会员订阅 | $50K+ |
| evepraisal | 价格查询 + API 授权 | $30K+ |
| dotlan | 地图工具 + 广告 + 订阅 | $20K+ |
| eve-marketeer | 市场数据 API | $10K+ |

---

## Phase 2：黄金三角筛选条件

必须同时满足：
- ✅ 填补了 EVE Frontier 的真实需求空白
- ✅ 用到了 Sui 的差异化能力（不是用 EVM 也能做的）
- ✅ 有持续性收益机制（每笔交互抽佣 / 协议税 / NFT royalty）

强制排除：
- ❌ 地图 / 路线规划 / 战报面板（已饱和）
- ❌ 纯链下工具（无 Sui 集成）
- ❌ 一次性奖励结构

---

## Phase 3：评分模型

| 维度 | 权重 | 说明 |
|------|------|------|
| 💰 持续收益能力 | 30% | 有清晰的收益飞轮 |
| 🏆 黑客松获奖概率 | 25% | 差异化 × 赛道契合 × Demo 可视化 |
| 🔒 生态护城河 | 25% | 占据核心节点 × 先发优势 |
| ⚡ Solo 实现速度 | 20% | 2 周内能否出可演示 MVP |

**综合得分 = 0.30×收益 + 0.25×获奖 + 0.25×护城河 + 0.20×速度**

---

## Phase 4：20 个项目

### 🥇 1. GateMarket / 星门通行费交易所

**核心概念**：EVE Frontier 首个链上星门通行费协议，把 Smart Gate 通行费变成可配置的链上收入流。

**赚钱机制**：
- 主要收入来源：协议手续费 1% + 竞价手续费 0.5%
- 每笔通行费均值：0.01~0.1 SUI
- 日活 100 玩家 × 每人 5 次通行 × 1% = 月收入约 $300~3000（随 SUI 价格浮动）
- 收益飞轮：更多玩家 → 更多星门接入 → 流量节点价值增加 → 协议费增加

**Sui 集成方式**：
- Move 合约：TollRegistry Object + OperatorCap（绑定具体 gate_id）
- Sponsored Tx：普通玩家无 Gas 体验
- 链上存储：通行记录、费率配置
- 为什么必须 Sui：Smart Gate 本身是 Sui Move 合约，必须同链交互

**黑客松角度**：
- 目标赛道：DeFi + Culture & Entertainment
- 差异化：第一个把游戏内基础设施变成 DeFi 可交易资产
- 90 秒 Demo：运营者设置通行费 → 玩家付费 → 链上自动结算 → 星门跳转

**护城河**：
- 占据星门流量节点（宇宙交通命脉）
- 通行量历史数据 → 定价权
- LP 锁仓形成流动性护城河

**MVP 路径（Solo，14 天）**：
- Day 1-3：理解 Smart Gate API，设计 TollGate Move 合约
- Day 4-7：实现通行费设置、代付、链上记录
- Day 8-14：Next.js 前端（运营者 + 玩家双面板）+ Demo

**评分**：持续收益 9/10 · 获奖概率 9/10 · 护城河 10/10 · 速度 7/10
**综合得分：88/100** 🥇

**仓库**：[autoteam-claw/p1-gatemarket](https://github.com/autoteam-claw/p1-gatemarket)

---

### 🥈 2. TrustEscrow / 玩家去中心化托管协议

**核心概念**：解决玩家大额交易信任问题，资金锁定在链上，双方确认释放，超时自动退款，争议触发仲裁。

**赚钱机制**：
- 主要收入来源：每笔托管 0.5% 协议费
- 仲裁费：0.1 SUI/次
- 大额交易均值 $100+，月 100 笔 × 0.5% = $500+
- 收益飞轮：声誉数据积累 → 成为社区标准协议 → 无法绕过

**Sui 集成方式**：
- Move 合约：EscrowOrder Object（时间锁 + 多签释放）
- Seal：敏感协议条款加密存储
- Walrus：合约历史记录永久存档
- Sponsored Tx：新手零门槛

**黑客松角度**：
- 目标赛道：Infra & Tooling
- 差异化：EVE 生态首个完整链上托管，比 TrustLocker 草案功能完善 10 倍
- Demo：两个钱包完成一笔托管，资金自动释放

**护城河**：
- 托管历史数据 → 声誉护城河
- 社区标准化后网络效应巨大
- 仲裁记录不可篡改

**评分**：持续收益 8/10 · 获奖概率 8/10 · 护城河 9/10 · 速度 9/10
**综合得分：85/100** 🥈

**仓库**：[autoteam-claw/p2-trustescrow](https://github.com/autoteam-claw/p2-trustescrow)

---

### 🥉 3. FuelDEX / 燃料链上交易所

**核心概念**：专为 EVE Frontier 燃料设计的 AMM 交易所，基于恒积公式（x·y=k），支持 Fuel/SUI 双向兑换。

**赚钱机制**：
- 主要收入来源：交易手续费 0.3%（LP 0.25% + 协议 0.05%）
- 每笔均值燃料交易量 $5~50
- 日活 100 玩家 × 日均 3 笔 × 0.05% × $20 均值 = 月收入约 $90（仅协议份额）
- 收益飞轮：更多 Network Node → 更大燃料需求 → 更多流量 → LP 收益高 → 更多 LP

**Sui 集成方式**：
- Move 合约：AMM Pool Object（LP Token 发行）+ Supply 管理
- 游戏燃料本身是 Sui Object，必须同链撮合
- Walrus：历史价格数据存储

**黑客松角度**：
- 目标赛道：DeFi
- 差异化：第一个游戏内专用燃料 DEX，比通用 DEX 有更好的 UX 和定制化
- Demo：Network Node 运营者一键补充燃料，价格从 DEX 实时获取

**护城河**：
- 占据燃料流转节点（所有 Network Node 必经之路）
- 历史价格数据 → 定价权威
- LP 锁仓形成流动性护城河

**评分**：持续收益 9/10 · 获奖概率 8/10 · 护城河 8/10 · 速度 7/10
**综合得分：83/100** 🥉

**仓库**：[autoteam-claw/p3-fueldex](https://github.com/autoteam-claw/p3-fueldex)

---

### 4. AutoMod Factory / Move 合约模板市场

**核心概念**：让非开发者玩家通过"填参数"而非"写代码"部署自定义 Smart Assembly 逻辑，类似 Shopify 模板市场。

**赚钱机制**：
- 模板部署费：0.1 SUI/次
- 高级模板订阅：$10/月
- 模板开发者分润：70/30
- 月活 100 玩家 × $10 = $1000/月基础收益
- 收益飞轮：越多玩家使用 → 越多模板开发者 → 更丰富模板 → 更多用户

**Sui 集成方式**：
- Move 合约：TemplateRegistry Object + 动态字段参数化
- Walrus：模板代码存储（内容引用 blob ID）
- zkLogin：Web2 友好登录

**黑客松角度**：
- 目标赛道：Infra & Tooling
- 差异化：极大降低 Smart Assembly 编程门槛
- Demo：非技术玩家 3 分钟完成定制星门策略部署

**评分**：持续收益 8/10 · 获奖概率 9/10 · 护城河 8/10 · 速度 7/10
**综合得分：82/100**

**仓库**：[autoteam-claw/p4-automod-factory](https://github.com/autoteam-claw/p4-automod-factory)

---

### 5. ChainRep / 链上声誉系统

**核心概念**：基于链上行为自动积累的 SoulBound 声誉 NFT，其他协议可直接读取声誉分数，构建信任基础设施。

**赚钱机制**：
- 声誉查询 API：$5/月订阅
- 企业集成授权：$50/月
- 声誉 NFT mint 费：0.05 SUI
- 收益飞轮：声誉数据越多 → API 价值越高 → 更多集成 → 更多数据输入

**Sui 集成方式**：
- Move 合约：ReputationProfile（SoulBound Token，不可转让）+ ScoreKeeper 权限系统
- Seal：私密声誉维度门控（仅授权方可查）
- 与 GateMarket、TrustEscrow 无缝集成

**5 个声誉等级**：Unknown → Newcomer（50+）→ Trusted（200+）→ Veteran（500+）→ Elite（800+）

**黑客松角度**：
- 目标赛道：Infra & Tooling
- 差异化：Sui SBT + Seal 组合在游戏声誉场景无先例
- Demo：声誉分实时更新 → 星门根据声誉自动拒绝低信用玩家

**评分**：持续收益 7/10 · 获奖概率 8/10 · 护城河 9/10 · 速度 8/10
**综合得分：80/100**

**仓库**：[autoteam-claw/p5-chainrep](https://github.com/autoteam-claw/p5-chainrep)

---

### 6. FrontierOracle / 游戏内价格预言机

**核心概念**：聚合全服交易数据，提供标准化价格 feed，供其他 Move 合约（交易所、保险、贷款）引用。

**赚钱机制**：
- 链上引用费：0.001 SUI/次
- 开发者订阅：$10/月
- 收益飞轮：越多合约引用 → 数据更权威 → 更多订阅

**Sui 集成**：OracleRegistry Object + 价格更新权限 · Walrus 历史价格序列永久存储

**评分**：持续收益 8/10 · 获奖概率 7/10 · 护城河 9/10 · 速度 8/10
**综合得分：80/100**

---

### 7. FrontierAgent / AI 自动化运营代理

**核心概念**：AI 代理自动管理玩家的 Network Node（补充燃料、监控状态、触发告警、执行策略）。

**赚钱机制**：
- 代理订阅：$15/月
- 高级策略包：$30/月
- 收益分润：代理创造收益的 5%
- 收益飞轮：越多数据 → 策略越优 → 收益越高 → 更多用户

**Sui 集成**：AgentPermission Object（授权代理操作）· Walrus 策略历史记录 · Sponsored Tx 代理 Gas 代付

**黑客松角度**：目标赛道 **AI**（DeepSurge 有专门 AI 赛道！）

**评分**：持续收益 8/10 · 获奖概率 9/10 · 护城河 7/10 · 速度 7/10
**综合得分：78/100**

---

### 8. AccessPass / zkLogin 身份门控

**核心概念**：用 Google/Apple 登录创建游戏身份，绑定链上声誉，实现 Web2 玩家无摩擦进入 EVE Frontier 生态。

**赚钱机制**：
- 高级身份验证：$5/月
- B2B：为其他 dApp 提供身份验证 $50/月/应用

**Sui 集成**：zkLogin（Sui 原生，EVM 无法复制）· Seal 身份数据加密 · Sponsored Tx 新手 Gas 代付

**评分**：持续收益 7/10 · 获奖概率 8/10 · 护城河 8/10 · 速度 8/10
**综合得分：77/100**

---

### 9. FrontierData / 游戏数据 API 平台

**核心概念**：将链上游戏数据（KillMail、交易记录、燃料价格、玩家行为）打包成开发者友好的 REST API。

**赚钱机制**：
- 免费版 100 次/天 · 基础版 $9/月 · 专业版 $29/月无限制
- 先例：evepraisal 年收入估算 $30K+

**Sui 集成**：Walrus 历史数据存档 · Sui Pay 链上订阅支付 · zkLogin 开发者注册

**评分**：持续收益 8/10 · 获奖概率 6/10 · 护城河 8/10 · 速度 9/10
**综合得分：77/100**

---

### 10. FrontierInsurance / 链上游戏保险

**核心概念**：玩家为 Network Node、装备、货物购买保险，PvP 损失由链上资金池赔付。

**赚钱机制**：
- 保费收入（预计占赔付额 20% 利润）
- 资金池 LP 收益
- 收益飞轮：资金池规模大 → 可承保更大额 → 更多用户

**Sui 集成**：PolicyObject + ClaimObject（时间锁定）· 直接读取链上 KillMail 自动理赔

**评分**：持续收益 9/10 · 获奖概率 8/10 · 护城河 8/10 · 速度 5/10
**综合得分：76/100**

---

### 11. StorageMarket / 仓储单元租赁市场

**核心概念**：玩家将闲置的 Smart Storage Unit 出租给其他玩家/公会，链上自动收租。

**赚钱机制**：租金抽成 5% · 闪租 0.01 SUI/小时

**评分**：持续收益 7/10 · 获奖概率 8/10 · 护城河 7/10 · 速度 8/10
**综合得分：75/100**

---

### 12. FrontierChat / Seal 加密族群通讯

**核心概念**：基于 Seal 的端到端加密公会通讯，只有持有特定 NFT/声誉的玩家可访问频道。

**赚钱机制**：高级加密频道 $3/月 · 企业公会包 $20/月

**Sui 集成**：Seal（核心！门控加密通讯，EVM 无 Seal）· Walrus 消息历史存储

**评分**：持续收益 7/10 · 获奖概率 9/10 · 护城河 7/10 · 速度 7/10
**综合得分：75/100**

---

### 13. SpaceYield / 燃料质押生息

**核心概念**：持有闲置燃料可质押获得收益，借款方（需要燃料的运营者）付利息。

**赚钱机制**：利差 2~5% · 协议费 10% 利息收入

**评分**：持续收益 8/10 · 获奖概率 7/10 · 护城河 7/10 · 速度 6/10
**综合得分：72/100**

---

### 14. TribalVault / 联盟链上金库

**核心概念**：公会/联盟共享金库，多签控制，自动按贡献度分配收益。

**赚钱机制**：金库管理费 0.5%/年 · 提案执行手续费 0.01 SUI/次

**评分**：持续收益 7/10 · 获奖概率 7/10 · 护城河 7/10 · 速度 8/10
**综合得分：72/100**

---

### 15. KillMint / 链上战报 NFT

**核心概念**：将 KillMail 自动铸造为 NFT，配上链上战报渲染图，胜利者纪念品。

**赚钱机制**：Mint 费 0.05 SUI · 精选战报 Premium 0.5 SUI · 广告位 $100/周

**评分**：持续收益 6/10 · 获奖概率 8/10 · 护城河 6/10 · 速度 9/10
**综合得分：72/100**

---

### 16. frontier-flow++ / 可视化合约编排

**核心概念**：在现有 frontier-flow（0⭐）基础上，做成真正可用的可视化 Move 合约生成工具。

**赚钱机制**：导出模板 0.1 SUI/次 · 高级节点库 $10/月

**评分**：持续收益 6/10 · 获奖概率 8/10 · 护城河 6/10 · 速度 8/10
**综合得分：70/100**

---

### 17. ReputationBounty / 链上赏金平台

**核心概念**：玩家发布链上赏金（击杀某目标、完成某任务），完成者自动领取。

**赚钱机制**：赏金发布费 2% · 仲裁费 0.1 SUI/次

**评分**：持续收益 6/10 · 获奖概率 8/10 · 护城河 6/10 · 速度 8/10
**综合得分：70/100**

---

### 18. FrontierLend / 游戏资产抵押借贷

**核心概念**：用游戏内资产（稀有装备 NFT）作为抵押，借出游戏货币或 SUI。

**赚钱机制**：协议费 0.5%/贷款 · 清算奖励 5%

**评分**：持续收益 8/10 · 获奖概率 7/10 · 护城河 7/10 · 速度 5/10
**综合得分：69/100**

---

### 19. AllianceIndex / 联盟竞争力排行榜

**核心概念**：综合链上数据计算联盟综合实力排行，配新闻订阅。

**赚钱机制**：排行 API $5/月 · 联盟高级报告 $20/月

**评分**：持续收益 5/10 · 获奖概率 7/10 · 护城河 7/10 · 速度 9/10
**综合得分：68/100**

---

### 20. FuelHedge / 燃料价格期权

**核心概念**：玩家可买入燃料价格看涨/看跌期权，对冲运营成本。

**赚钱机制**：期权费收入 · 做市商价差

**评分**：持续收益 8/10 · 获奖概率 7/10 · 护城河 6/10 · 速度 5/10
**综合得分：67/100**

---

## 完整排名

| 排名 | 项目 | 综合得分 | 仓库 |
|------|------|---------|------|
| 🥇 1 | GateMarket — 星门通行费交易所 | **88** | [p1-gatemarket](https://github.com/autoteam-claw/p1-gatemarket) |
| 🥈 2 | TrustEscrow — 玩家去中心化托管 | **85** | [p2-trustescrow](https://github.com/autoteam-claw/p2-trustescrow) |
| 🥉 3 | FuelDEX — 燃料 AMM 交易所 | **83** | [p3-fueldex](https://github.com/autoteam-claw/p3-fueldex) |
| 4 | AutoMod Factory — Move 合约模板市场 | **82** | [p4-automod-factory](https://github.com/autoteam-claw/p4-automod-factory) |
| 5 | ChainRep — 链上声誉系统 | **80** | [p5-chainrep](https://github.com/autoteam-claw/p5-chainrep) |
| 6 | FrontierOracle — 价格预言机 | **80** | — |
| 7 | FrontierAgent — AI 自动化运营代理 | **78** | — |
| 8 | AccessPass — zkLogin 身份门控 | **77** | — |
| 9 | FrontierData — 游戏数据 API 平台 | **77** | — |
| 10 | FrontierInsurance — 链上游戏保险 | **76** | — |
| 11 | StorageMarket — 仓储单元租赁 | **75** | — |
| 12 | FrontierChat — Seal 加密通讯 | **75** | — |
| 13 | SpaceYield — 燃料质押生息 | **72** | — |
| 14 | TribalVault — 联盟链上金库 | **72** | — |
| 15 | KillMint — 链上战报 NFT | **72** | — |
| 16 | frontier-flow++ — 可视化合约编排 | **70** | — |
| 17 | ReputationBounty — 链上赏金平台 | **70** | — |
| 18 | FrontierLend — 资产抵押借贷 | **69** | — |
| 19 | AllianceIndex — 联盟排行榜 | **68** | — |
| 20 | FuelHedge — 燃料价格期权 | **67** | — |

---

## Phase 5：战略总结

### ① Top 3 必做项目

**#1 GateMarket**（首选）
占据星门流量节点——这是整个宇宙的交通命脉，每个玩家无法绕过。先发者建立协议标准后护城河极深。Demo 最直观，评委秒懂。

**#2 TrustEscrow**（必做）
解决玩家大额交易最真实痛点，有 TrustLocker 参赛草案证明需求真实存在——但对方只有草案，我们做完整实现。2 周内 Solo 可完成，获奖概率高。

**#3 FrontierAgent + AI 赛道**（弯道超车）
DeepSurge 有专门的 AI 赛道，而其他参赛者几乎都在做 DeFi/工具。AI 代理自动管理 Network Node 既解决真实痛点，又天然击中 AI 赛道评委偏好。

### ② 最佳组合套件（5 项目共享代码）

推荐组合：**GateMarket + TrustEscrow + ChainRep + FrontierOracle + FrontierData**

```
packages/
  frontier-core/        # 共享 Move 合约基础库
    - identity.move     # 玩家身份/声誉基础
    - payment.move      # 统一支付原语
    - oracle.move       # 价格预言机接口
  frontier-sdk/         # 共享 TypeScript SDK
    - client.ts         # Sui RPC 封装
    - events.ts         # 链上事件监听
  frontier-ui/          # 共享 React 组件
    - WalletConnect     # zkLogin + 传统钱包
    - TxStatus          # 交易状态展示
```

为什么 1+1>2：
- ChainRep 声誉 → GateMarket 用声誉决定通行权
- FrontierOracle 价格 → GateMarket 动态定价
- TrustEscrow + ChainRep → 高声誉享受更低托管费
- FrontierData API → 对外变现整套基础设施数据

### ③ 最快赚到第一笔钱的路径

**第 1 天**：KillMint 上线，每笔 Mint 0.05 SUI，社区免费宣传

**第 3-5 天**：FrontierData API 公测，第 7 天推出付费订阅，预计 $50~200

**第 7-14 天**：GateMarket Beta，早鸟 0.1% 费率，建立使用数据 → 黑客松 Demo 更有说服力

### ④ 生态控制地图

```
EVE Frontier 经济价值流转

[燃料生产] → [Network Node燃料市场] → FuelDEX ✅
                     ↓
[Assembly运营] → [星门通行] → GateMarket ✅
                     ↓
[玩家交易] → [信任托管] → TrustEscrow ✅
                     ↓
[价格发现] → FrontierOracle ✅
                     ↓
[数据消费] → FrontierData API ✅
```

**已被占据节点**：地图/路线（弱竞争）· 开发工具（官方友好）

**空白核心节点**：燃料流转 · 星门控制 · 信任基础 · 数据层

**制霸 3 节点最强组合**：GateMarket + FuelDEX + FrontierOracle
- 控制交通 + 控制能源 + 控制定价权
- 任何新进入者都要依赖你的基础设施

---

## 技术栈

- **链上**：Sui Move（EVE Frontier world-contracts 扩展模式）
- **前端**：Next.js 14 (App Router) + Tailwind CSS
- **数据库**：PostgreSQL + Prisma ORM
- **钱包**：@mysten/dapp-kit
- **数据存储**：Walrus（链上历史数据）
- **访问控制**：Seal（私密数据门控）

## 开发进度

| 项目 | Move 合约 | Next.js 全栈 | 状态 |
|------|-----------|-------------|------|
| P1 GateMarket | ✅ 完整 | ✅ 完整 | 完成 |
| P2 TrustEscrow | ✅ 完整 | ✅ 完整 | 完成 |
| P3 FuelDEX | ✅ 完整 | 🔄 开发中 | 进行中 |
| P4 AutoMod Factory | ✅ 完整 | 🔄 开发中 | 进行中 |
| P5 ChainRep | ✅ 完整 | 🔄 开发中 | 进行中 |

---

*by clawdbot20090103 · autoteam-claw · 2026-03-20*
