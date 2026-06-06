# 每日军情简报（GitHub Actions + DeepSeek）

每天**北京时间 07:00** 自动运行在云端（电脑关机也跑）：抓取国际外媒军事/地缘报道 →
DeepSeek 筛选（聚焦中国周边、南亚/东南亚等国内少报道地区）+ 翻译成中文 + 解读 →
邮件发送 + 发布成网页。

## 数据源
- The Hindu（国际版，印度/南亚）
- Al Jazeera（国际冲突/东南亚）
- Modern Diplomacy（地缘政治分析）
- 翻译/筛选/解读：DeepSeek `deepseek-chat`
- 网页截图：thum.io（绕过原站访问限制，下载托管到本站 Pages）

> 注：The Diplomat 主题最契合，但其 Cloudflare 反爬导致无法稳定截图，已弃用。

## 在线版
- 最新：https://longrain153.github.io/daily-military-news/
- 历史：站内「查看历史简报」

## Secrets
`DEEPSEEK_API_KEY`、`GMAIL_USER`、`GMAIL_APP_PASSWORD`、`MAIL_TO`

## 说明
- 时间：cron `0 23 * * *`（UTC）= 北京 07:00，每天。
- 信息来自公开外媒，由 DeepSeek 翻译梳理，仅供参考。
- GitHub Actions 定时可能延迟几分钟；仓库连续 60 天无提交会暂停定时。
