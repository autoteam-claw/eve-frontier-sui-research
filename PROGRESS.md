# EVE Frontier × Sui — 开发进度

## 更新时间
2026-03-20

## 项目状态

### ✅ P1: GateMarket — 星门通行费交易所 (88分)
**路径：** `~/Desktop/eve/p1-gatemarket/`

**已完成：**
- `gatemarket/sources/config.move` — TollGateAuth 见证类型
- `gatemarket/sources/toll_gate.move` — 核心付费逻辑（TollRegistry + OperatorCap + buy_jump_permit）
- `gatemarket/tests/toll_gate_tests.move` — 单元测试
- `ts-scripts/register-gate.ts` — 运营者注册星门
- `ts-scripts/buy-jump-permit.ts` — 玩家付费通行
- `ts-scripts/withdraw-revenue.ts` — 提取收益
- `frontend/src/App.tsx` — 完整前端（运营者+玩家双面板）

**待完成（部署后）：**
- [ ] `sui client publish` 部署到 testnet
- [ ] 更新 .env 中的合约地址
- [ ] 授权 TollGateAuth 到目标星门
- [ ] 前端 `npm install && npm run dev` 测试

---

### ✅ P2: TrustEscrow — 玩家去中心化托管 (85分)
**路径：** `~/Desktop/eve/p2-trustescrow/`

**已完成：**
- `trustescrow/sources/escrow.move` — 完整托管协议
  - create_escrow / claim_refund / confirm_completion
  - raise_dispute / resolve_dispute
  - 协议费 0.5% + 仲裁费 0.1 SUI
- `frontend/src/App.tsx` — 创建托管 + 操作界面

---

### ✅ P3: FuelDEX — 燃料 AMM 交易所 (83分)
**路径：** `~/Desktop/eve/p3-fueldex/`

**已完成：**
- `fueldex/sources/pool.move` — 恒积 AMM（x*y=k）
  - add_liquidity / remove_liquidity
  - swap_fuel_for_sui / swap_sui_for_fuel
  - LP Token 发行
  - 手续费 0.3%（LP 0.25% + 协议 0.05%）

---

### ✅ P4: AutoMod Factory — Move 合约模板市场 (82分)
**路径：** `~/Desktop/eve/p4-automod/`

**已完成：**
- `automod/sources/registry.move` — 模板注册表
  - publish_template（开发者发布）
  - deploy_mod（玩家部署，0.1 SUI）
  - 收益分账：开发者70% / 协议30%
  - VecMap 参数 schema 系统

---

### ✅ P5: ChainRep — 链上声誉系统 (80分)
**路径：** `~/Desktop/eve/p5-chainrep/`

**已完成：**
- `chainrep/sources/reputation.move` — SoulBound 声誉 Token
  - 5个维度：交易/托管/星门/仲裁/PvP
  - ScoreKeeper 权限系统（其他协议可写入）
  - reputation_tier 等级（Unknown/Newcomer/Trusted/Veteran/Elite）
  - 与 GateMarket、TrustEscrow 可无缝集成

---

## 文件统计
- Move 合约：7个文件，共约 3,500 行
- TypeScript 脚本：4个文件
- React 前端：2个完整前端

## 下一步
1. 安装 Sui CLI + builder-scaffold 环境
2. `sui client publish` 部署到 testnet（Stillness/Utopia）
3. 完成前端 npm install + 测试
4. 录制 Demo 视频
5. 准备黑客松提交材料
