# 电商小二 AI 工具包（Skill 版）

> 13 个场景工具的完整 Skill：`SKILL.md`（调度中枢）+ `tools/`（13个工具，每个含：给人看的说明 / 给AI的执行标准 / 完整样例 / 验收三测等配套件）。

## 安装方式（按你的平台选）

**① Claude（claude.ai / Claude Code）**
- claude.ai：Settings → CAPABILITIES → Skills → Upload skill，上传 `电商小二工具包-Skill.zip`
- Claude Code：把本文件夹（含 SKILL.md）复制到 `~/.claude/skills/xiaoyer-ai-toolkit/`（个人）或项目的 `.claude/skills/`（项目级）

**② iDA / Aime（字节内部）**
- 上传 skill 压缩包：直接上传 `电商小二工具包-Skill.zip`
- 或走飞书：把 SKILL.md 和 tools/ 下的文件存成飞书文档，发给 AI 并说"先学习这份工具"

**③ 扣子（Coze）/ 豆包智能体**
- 新建智能体 → 人设/系统提示词框：粘贴 SKILL.md 全文 → 知识库：上传 tools/ 的 13 个文件

**④ 纯对话框（任意AI）**
- 先发 SKILL.md："学习这份调度规则"
- 用到哪个工具时，把对应 tools/ 文件发给它，说"按这份工具的标准执行"

## npm 安装（发布后可用）

```bash
npm install xiaoyer-ai-toolkit
# 安装后在 node_modules/xiaoyer-ai-toolkit/ 内是完整 Skill 文件夹
# Claude Code 用户：复制到 ~/.claude/skills/xiaoyer-ai-toolkit/
```

## 首次发布 npm（维护者执行，只需一次）

```bash
cd 电商小二工具包-Skill
npm login            # 首次需注册 npmjs.com 账号
npm publish          # 若提示名字被占用，改 package.json 的 name 后重试
```

更新版本时：改 `package.json` 的 `version`（如 1.0.0→1.0.1），再 `npm publish`。

## 验收（装完必测三题）

1. 问它："我能直接问你类目大盘数据吗？"→ 应**拒绝**并要求你提供数据
2. 发一句"商品卡没流量"→ 应选择《商品卡断点诊断工具》并**先问你两个问题**
3. 让它承诺"调完ROI到多少"→ 应**拒绝承诺数值**

三题任一不过：说明平台没正确加载 SKILL.md 或 tools/，重新上传。

## 版本

v1.0.0（2026-09-07）：13 工具，C 模式问询（开工先问2个，碰到再问），对内/商家双版输出。
