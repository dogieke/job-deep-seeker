# 工具样本库（Toolbox）

> **作用**：agent 需要工具时，先看这里找「同类工具该找什么」。**链接失效也没关系**——样本告诉你找哪类项目，用 web_search 搜同类即可。**务必选真实、star 数高的开源项目**（用 web_search 确认）。

> **原则**：本目录是参考样本，不是强制要求。你的环境可能有更好的选择。

## ① 求职岗位采集（JobHunter 类）

**目标**：批量获取岗位信息（含投递方式），无需登录。

- **jobhunt-cli** — 大厂官网招聘 API 聚合 CLI
- **boss-agent-cli** — BOSS直聘双端 CLI（职位搜索、投递、流水线追踪）
- **Auto-JobHunter** — 多平台抓取→清洗→LLM评估→自动投递管线
- 搜索关键词：`job board CLI` / `careers API aggregator` / `招聘信息聚合命令行`

## ② 浏览器自动化（操作社交平台/网页）

**目标**：打开网页、搜索、滚动、截图、点击。用于登录态平台。

- **Playwright** — 跨平台（Mac/Win/Linux），Python/Node，截图+点击+滚动
- **Selenium** — 经典跨平台浏览器自动化
- 搜索关键词：`browser automation CLI` / `headless browser 截图`

## ③ 视觉多模态模型（反爬页面截图转写）

**目标**：把截图转写成结构化文字（标题/正文/邮箱/投递方式）。**反爬网站的正确采集方式**：截图 + 视觉模型，不爬取。

- **OpenRouter**（聚合 API）— 一个 key 调多家视觉模型
- 各家官方 API：OpenAI / Anthropic / Google / 国产（通义/豆包/智谱）
- 搜索关键词：`vision model API OCR` / `multimodal API 截图识别`

## ④ 邮件发送

**目标**：发带附件的邮件。按平台选。

- **macOS**：本机邮件客户端（Apple Mail）→ 系统自动化驱动
- **跨平台**：Python `smtplib`（标准库，需授权码）/ msmtp / mutt
- **零配置**：浏览器操作网页邮箱
- **API**：Resend / SendGrid（需注册）

## ⑤ 简历 HTML → PDF

**目标**：HTML 转单页 A4 PDF。

- **puppeteer-core**（Node）/ Playwright（跨平台）
- **weasyprint**（Python，纯本地）
- **wkhtmltopdf**（老牌 CLI）
- 搜索关键词：`html to pdf A4 CLI`

## 案例示范格式

每个样本记录格式（可追加新样本到对应分类）：
```markdown
- **{工具名}** — {一句话说明}
  - 搜索关键词：{用于 web_search 的查询词}
  - 平台：{Mac/Win/Linux/跨平台}
  - 用途：{对应哪个阶段目标}
```

## 维护

- 找到更好用的工具 → 追加到对应分类
- 链接失效 → 保留描述（作为"找同类"的样本），更新搜索关键词
