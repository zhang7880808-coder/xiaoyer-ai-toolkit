# 电商小二 AI 工具包

面向抖音电商运营小二的 Agent Skills 合集：**5 个主题包、13 个场景技能**。符合 [agentskills.io](https://agentskills.io/specification) 规范。

## 快速开始

### 方式1 · npm（最简单）

```bash
npm install xiaoyer-ai-toolkit
```

装完后 `node_modules/xiaoyer-ai-toolkit/` 里有 `SKILL.md`（调度器）和 `references/`（13个技能文件），复制到你的 AI 工具的 skill 目录即可。

### 方式2 · 直接发给任何 AI

把下方内容复制、连同 `skills/xiaoyer-industry-benchmark/SKILL.md（任选一个主题包的SKILL.md）` 全文一起发给 AI：

```
请学习以下 Agent Skill 调度规则，按调度表读取对应技能文件执行任务：

（此处粘贴 SKILL.md 全文）

我发任务后，你按调度表选技能、读取 references/ 里的对应文件，按该技能的七节结构执行。
```

### 方式3 · 上传 zip 到平台

从 `skills/` 目录下载任一主题包，上传到支持 Skill 的平台：
- **iDA / Aime**：直接上传 zip
- **Claude**：Settings → Skills → Upload
- **扣子 / 豆包**：SKILL.md 粘贴进人设框，references/ 上传为知识库

## 包一览

| 包 | 内容 | 技能数 |
|---|---|---|
| `skills/xiaoyer-industry-benchmark` | 行业数据解读 · 商家对标诊断 · 载体效率体检 | 3 |
| `skills/xiaoyer-selling-point-test` | 卖点三层拆解与合规预检 · 跨渠道转译与单变量测试 | 2 |
| `skills/xiaoyer-hit-video-research` | 爆款样本筛选 · 视频逐秒拆解 · 共性验证 | 3 |
| `skills/xiaoyer-product-card-clinic` | 商品卡五关断点诊断 · 动作排序与方案生成 | 2 |
| `skills/xiaoyer-qianchuan-ads` | 千川术语速查 · 三病诊断 · 优化与止损线 | 3 |

npm 整合包：[npmjs.com/package/xiaoyer-ai-toolkit](https://www.npmjs.com/package/xiaoyer-ai-toolkit)

## 技能的统一结构（七节）

1. **岗位匹配**——对应小二哪项职责、什么场景、产出什么
2. **开工问询**——AI 先问 2 个关键问题（有默认值），答一次永久记忆
3. **拉数后怎么读**——逐遍读法 + "停下信号"（如增速含大促先剔除再读）
4. **界定标准**——判定规则链 + 常见误判表
5. **报告输出**——对内版 + 商家版双模板 + 完整虚构样例
6. **结论验证**——数据回指 → 交叉验证 → 反例检验 → 置信度标注
7. **配套件**——常见坑 / 验收三测 / 复盘指令 / 进阶钩子

## 装后验收（三题）

1. 问"能直接问你行业数据吗"→ 应**拒绝**
2. 说"商品卡没流量"→ 应路由到断点诊断并**先问你两个问题**
3. 让它承诺"ROI 到多少"→ 应**拒绝承诺数值**

## 设计原则

- **反幻觉**：数据从小二手里来，AI 只当分析师；缺数写"待补"禁编造
- **口径先行**：对比一律"同行同级"；不引用"行业平均"
- **止损文化**：方案必含"何时加码、何时认输"
- **渐进式加载**：SKILL.md 是调度器，重内容在 references/ 按需读取

---
v1.0.0 · 作者：张琪 · [npm](https://www.npmjs.com/package/xiaoyer-ai-toolkit)
