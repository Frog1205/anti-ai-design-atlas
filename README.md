# AI 味设计图鉴

线上地址：https://anti-ai-design-atlas.pages.dev

五十种让网页看起来“像 AI 做的”的设计习惯，每条写清怎么认出来、问题在哪、怎么改。原样示意用红笔批注；“改后”统一用虚构产品「落账」（一款给夜市摊和小卖部用的记账 App）来画。

- `site/index.html`：部署用的完整页面，单文件，无构建步骤
- `index.html`：同一页面的源文件（不含 `<html>`/`<head>` 外壳）

## 部署

推送到 `main` 且改动了 `site/` 时，GitHub Actions（`.github/workflows/deploy.yml`）会自动部署到 Cloudflare Pages 项目 `anti-ai-design-atlas`。也可以在 Actions 页面手动运行 “Deploy to Cloudflare Pages”。

需要在仓库 Settings → Secrets and variables → Actions 里添加两个 secret：

- `CLOUDFLARE_API_TOKEN`：Cloudflare API Token，权限至少包含 Account → Cloudflare Pages → Edit
- `CLOUDFLARE_ACCOUNT_ID`：Cloudflare 账号 ID

注意：部署的是 `site/index.html`。改页面时请改这个文件（根目录的 `index.html` 是不含 `<html>`/`<head>` 外壳的源稿）。

本地手动部署：

```bash
npx wrangler pages deploy site --project-name anti-ai-design-atlas --branch main
```
