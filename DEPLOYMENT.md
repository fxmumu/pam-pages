# GitHub Pages 部署说明

已添加 GitHub Actions workflow 和 `.nojekyll`，可以把仓库根目录发布到 GitHub Pages，供你的 App 使用。

页面 URL（示例）：

- `https://fxmumu.github.io/pam-pages/privacy_policy.html`
- `https://fxmumu.github.io/pam-pages/terms.html`

已做的改动：

- `.github/workflows/pages.yml` — 自动部署到 GitHub Pages（触发条件：push 到 `main` 或手动触发）。
- `.nojekyll` — 防止 Jekyll 处理静态文件。

发布步骤：

1. 本地提交修改：

```bash
git add .
git commit -m "Enable GitHub Pages deploy"
```

2. 推送到 `main`：

```bash
git push origin main
```

3. 打开 GitHub 仓库的 `Actions`，查看 Pages 部署工作流运行状态。部署成功后，页面会在几分钟内可用。

如果需要我代为将更改推送到远程（需要你授权或提供 push 权限），或者要使用自定义域名/HTTPS 配置，请回复我。 
