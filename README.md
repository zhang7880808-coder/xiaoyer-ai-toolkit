# 电商小二 AI 工具包

面向抖音电商运营小二的 Agent Skills 合集：**6 个主题包、15 个场景技能**。符合 [agentskills.io](https://agentskills.io/specification) 规范。

## 快速开始

### 方式1 · npm
```bash
npm install xiaoyer-ai-toolkit
```
装完后 `node_modules/xiaoyer-ai-toolkit/` 里有 `SKILL.md` 和 `references/`（15个技能文件）。

### 方式2 · 发给任何 AI
把任一主题包的 `SKILL.md` 全文发给 AI，说"学习这份调度规则"，然后正常交任务。

### 方式3 · 上传 zip 到平台
从 `skills/` 下载任一主题包 zip，上传到 iDA/Aime/Claude/扣子。

## 包一览

| 包 | 内容 | 技能数 |
|---|---|---|
| `skills/xiaoyer-industry-benchmark` | 行业数据解读 · 商家对标诊断 · 载体效率体检 | 3 |
| `skills/xiaoyer-selling-point-test` | 卖点拆解与合规预检 · 跨渠道转译与测试 | 2 |
| `skills/xiaoyer-hit-video-research` | 爆款样本筛选 · 视频逐秒拆解 · 共性验证 | 3 |
| `skills/xiaoyer-product-card-clinic` | 商品卡断点诊断 · 动作排序与方案生成 | 2 |
| `skills/xiaoyer-qianchuan-ads` | 千川术语速查 · 三病诊断 · 优化与止损线 | 3 |
| `skills/xiaoyer-live-clinic` | 直播间断点诊断 · 体验分与违规治理 | 2 |

npm: [npmjs.com/package/xiaoyer-ai-toolkit](https://www.npmjs.com/package/xiaoyer-ai-toolkit)

## 技能结构（七节）

岗位匹配 → 开工问询（首次8+专属问，永久零问）→ 读数方法 → 界定标准（含基准三级链）→ 报告输出（对内+商家双版）→ 结论验证（四步+置信度）→ 配套件

## 装后验收

1. 问"能直接问你行业数据吗"→ 应拒绝
2. 说"商品卡没流量"→ 应路由到断点诊断并先问你问题
3. 让它承诺"ROI到多少"→ 应拒绝承诺数值

## 设计原则

反幻觉（数据从小二来，AI只当分析师）| 口径先行（基准三级链：同级中位→自身历史→定性）| 全程自动（问完配置零参与）| 止损文化（何时加码何时认输）| 建议三标签（成本/周期/可逆性）

---
v1.2.0 · 作者：张琪 · [npm](https://www.npmjs.com/package/xiaoyer-ai-toolkit)
