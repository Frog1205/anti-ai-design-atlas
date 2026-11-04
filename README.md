# AI 味设计图鉴

线上地址：https://anti-ai-design-atlas.pages.dev

五十种让网页看起来“像 AI 做的”的设计习惯，每条写清怎么认出来、问题在哪、怎么改。原样示意用红笔批注；“改后”统一用虚构产品「落账」（一款给夜市摊和小卖部用的记账 App）来画。

- `site/index.html`：部署用的完整页面，单文件，无构建步骤
- `index.html`：同一页面的源文件（不含 `<html>`/`<head>` 外壳）

## 部署

Cloudflare Pages（直接上传）：

```bash
npx wrangler pages deploy site --project-name anti-ai-design-atlas --branch main
```
