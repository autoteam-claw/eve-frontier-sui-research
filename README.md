# EVE Frontier × Sui — 生态研究报告

## 研究时间
2026-03-20

## 生态现状

### Smart Assembly 三类可编程结构
- **Smart Gate** — 星门/通行控制，自定义通行规则
- **Smart Storage Unit** — 仓库/交易所，自定义存取规则  
- **Smart Turret** — 炮塔/防御，自定义打击目标
- 所有 Assembly 依赖 **Network Node** 供能，Network Node 需持续注入燃料

### 已有工具（竞争对手）
| 项目 | Stars | 功能 |
|------|-------|------|
| evefrontier-rs | 0 | 路径规划/地图 CLI |
| efctl | 2 | 本地开发环境一键启动 |
| FrontierSharp | 4 | C# API客户端 |
| frontier-flow | 0 | 可视化合约编排（草案）|
| EVEFrontier_TrustLocker | 0 | 托管协议（草案）|

### 空白市场
- 燃料链上交易所 ✅
- 玩家托管协议 ✅（只有草案）
- 声誉系统 ✅
- 链上保险 ✅
- Move合约模板市场 ✅
- 价格预言机 ✅
- 数据API平台 ✅

### DeepSurge 赛道
DeFi / Infra & Tooling / Culture & Entertainment / AI / Programmable Storage / Payments & Wallets / Explorations / Cryptography / Degen

### Sui 差异化能力
- **Seal** — 去中心化访问控制/密钥管理
- **Walrus** — 可编程链上存储
- **zkLogin** — Google/Apple → Sui钱包
- **Sponsored Tx** — Gas代付
- **Object模型** — 真实资产所有权
- **Move** — 与游戏合约直接组合

---

## 20个项目排名

| 排名 | 项目 | 综合得分 |
|------|------|---------|
| 1 | GateMarket — 星门通行费交易所 | 88 |
| 2 | TrustEscrow — 玩家去中心化托管 | 85 |
| 3 | FuelDEX — 燃料链上交易所 | 83 |
| 4 | AutoMod Factory — Move合约模板市场 | 82 |
| 5 | ChainRep — 链上声誉系统 | 80 |
| 6 | FrontierOracle — 游戏价格预言机 | 80 |
| 7 | FrontierAgent — AI自动化运营代理 | 78 |
| 8 | AccessPass — zkLogin身份门控 | 77 |
| 9 | FrontierData — 游戏数据API平台 | 77 |
| 10 | FrontierInsurance — 链上游戏保险 | 76 |
| 11 | StorageMarket — 仓储单元租赁市场 | 75 |
| 12 | FrontierChat — Seal加密族群通讯 | 75 |
| 13 | SpaceYield — 燃料质押生息 | 72 |
| 14 | TribalVault — 联盟链上金库 | 72 |
| 15 | KillMint — 链上战报NFT | 72 |
| 16 | frontier-flow++ — 可视化合约编排 | 70 |
| 17 | ReputationBounty — 链上赏金平台 | 70 |
| 18 | FrontierLend — 资产抵押借贷 | 69 |
| 19 | AllianceIndex — 联盟排行榜 | 68 |
| 20 | FuelHedge — 燃料价格期权 | 67 |

---

## 进度追踪

- [ ] P1: GateMarket
- [ ] P2: TrustEscrow
- [ ] P3: FuelDEX
- [ ] P4: AutoMod Factory
- [ ] P5: ChainRep

---

## 🔗 项目仓库

| 排名 | 项目 | 仓库 | 得分 |
|------|------|------|------|
| #1 | GateMarket — 星门通行费交易所 | [autoteam-claw/p1-gatemarket](https://github.com/autoteam-claw/p1-gatemarket) | 88 |
| #2 | TrustEscrow — 去中心化托管协议 | [autoteam-claw/p2-trustescrow](https://github.com/autoteam-claw/p2-trustescrow) | 85 |
| #3 | FuelDEX — 燃料 AMM 交易所 | [autoteam-claw/p3-fueldex](https://github.com/autoteam-claw/p3-fueldex) | 83 |
| #4 | AutoMod Factory — 合约模板市场 | [autoteam-claw/p4-automod-factory](https://github.com/autoteam-claw/p4-automod-factory) | 82 |
| #5 | ChainRep — 链上声誉系统 | [autoteam-claw/p5-chainrep](https://github.com/autoteam-claw/p5-chainrep) | 80 |

## 技术栈

- **链上**: Sui Move (EVE Frontier world-contracts 扩展)
- **前端**: Next.js 14 (App Router) + Tailwind CSS
- **数据库**: PostgreSQL + Prisma ORM
- **钱包**: @mysten/dapp-kit

## 开发进度

- ✅ P1 GateMarket — Move合约 + Next.js全栈 + Prisma（完整）
- ✅ P2 TrustEscrow — Move合约 + Next.js全栈 + Prisma（完整）
- 🔄 P3 FuelDEX — Move合约完整，Next.js全栈开发中
- 🔄 P4 AutoMod Factory — Move合约完整，Next.js全栈开发中
- 🔄 P5 ChainRep — Move合约完整，Next.js全栈开发中
