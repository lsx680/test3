# 赛题 6 · Scheduler-定时任务抓取与分析 GitHub 热门

本作品基于 `analyze-github-trending` 技能与码道 IDE 定时任务能力，按日自动抓取 GitHub Trending 榜单，补充 README 语义信息，生成中文分析日报，并同步输出可离线打开的 dashboard 页面，全流程无需人工干预。

## 定时任务

- 调度：`0 8 * * *`（每日 08:00，本地时区）
- 执行：`node scripts/run-analysis.mjs --period daily`
- 输出：Markdown 日报、结构化缓存、dashboard 页面与历史快照

## 本期产物（2026-10-30）

- `reports/github-trending/2026-10-30-daily.md`：中文日报，含整体趋势分析与 11 个项目解读
- `reports/github-trending/dashboard/index.html`：dashboard 页面，内嵌数据，可直接通过 `file://` 打开
- `reports/github-trending/dashboard/history/2026-10-30.html`：当日静态历史快照
- `reports/github-trending/cache/2026-10-30/`：抓取与富化后的结构化数据

## 页面预览

直接用浏览器打开 `reports/github-trending/dashboard/index.html`。dashboard 支持日 / ISO 周 / 自然月三种时间桶切换，并与 Markdown 报告保持同一分析口径。

## 数据来源

- 榜单：[GitHub Trending](https://github.com/trending)
- 抓取日期：2026-10-30