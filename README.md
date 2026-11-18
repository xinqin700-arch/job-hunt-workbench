# Job Hunt Workbench（求职助手工作台 Skill）

一个面向 [WorkBuddy](https://www.workbuddy.cn) 的求职管理技能：基于单文件 HTML 模板生成离线可用的求职仪表盘，支持记录 BOSS直聘等渠道的打招呼沟通记录、投递进展、收藏岗位分类与面试安排。

## ✨ 特性

- **单文件、零依赖**：纯静态 HTML，数据存 localStorage，双击即用，无任何外部请求
- **今日概览**：打招呼/简历接收目标进度、按日汇总的「打招呼历史」表（累计沟通与投递转化率自动计算）
- **打招呼记录**：逐条沟通明细（送达/已读/已开聊/对方回复/简历已接收），分类筛选
- **收藏岗位**：分类 pills（出海投放·UA / AI产品·Agent / 增长 / 海外运营·发行 / 商业化·变现 / 游戏·短剧）+ 关键词搜索 + 5 组岗位搜索关键词库（出海市场、UA买量、Google/Meta/Facebook/TikTok 渠道等）
- **投递追踪**：投递状态看板 + 面试安排时间线 + 转化漏斗

## 📦 安装（WorkBuddy Skill）

把 `job-hunt-workbench/` 目录放到 `~/.workbuddy/skills/` 下即可，或使用打包好的 `job-hunt-workbench.zip`。

## 🚀 直接使用（不用 WorkBuddy）

直接打开 `job-hunt-workbench/assets/job-hunt-workbench-template.html`，就是一份可用的求职工作台。数据明文写在 HTML 内的 `records / days / savedJobs / jobs` 数组里，可手动编辑，改动自动存入 localStorage。

## 🧩 Skill 结构

```
job-hunt-workbench/
├── SKILL.md                                  # 技能说明（触发时机 + 工作流）
└── assets/
    └── job-hunt-workbench-template.html      # 工作台模板（单文件）
```

技能的核心工作流：识别招聘沟通截图 → 按「姓名+公司」去重 → 追加记录并同步全部计数 → 打招呼历史按天汇总 → 可选同步到资料库页面。

## 📄 License

MIT
