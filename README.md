# Cloudflare Pages 部署说明

本目录包含 PicSeek 隐私政策的 Cloudflare Pages 部署文件。

## 📁 文件说明

- `index.html` - 隐私政策网页（支持深色模式，移动端优化）
- `_redirects` - URL 重定向规则（可选）
- `README.md` - 本说明文件

## 🚀 部署步骤

### 1. 登录 Cloudflare
访问 [dash.cloudflare.com](https://dash.cloudflare.com) 并登录（如果没有账户，免费注册）

### 2. 创建 Pages 项目

1. 点击左侧菜单 **Pages**
2. 点击 **Create a project**
3. 选择 **Connect to Git**
4. 授权 Cloudflare 访问你的 GitHub 账户
5. 选择 **PhotoAlbumManager** 仓库

### 3. 配置构建设置

在项目设置页面填写：

```
Project name: picseek-privacy (或你喜欢的名字)
Production branch: main (或 feat/privacy-policy-deploy)
Build settings:
  - Framework preset: None
  - Build command: (留空)
  - Build output directory: Tools/cloudflare-pages
```

### 4. 部署

点击 **Save and Deploy**，几秒钟后部署完成。

### 5. 获取 URL

部署成功后，你会得到类似这样的 URL：
```
https://picseek-privacy.pages.dev
```

## 🔧 自定义域名（可选）

如果你有自己的域名（如 `privacy.picseek.app`）：

1. 在 Pages 项目中点击 **Custom domains**
2. 点击 **Set up a custom domain**
3. 输入你的域名
4. 按照提示在域名注册商处添加 CNAME 记录

## 📱 在 App Store Connect 中使用

1. 登录 [App Store Connect](https://appstoreconnect.apple.com)
2. 选择你的 App → **App Privacy**
3. 在 **Privacy Policy URL** 填入你的 Cloudflare Pages URL
4. 示例：`https://picseek-privacy.pages.dev`

## 🔄 更新隐私政策

当你需要更新隐私政策时：

1. 修改 `index.html` 中的内容
2. 更新 "Last Updated" 日期
3. 提交并推送到 GitHub
4. Cloudflare Pages 会自动重新部署（约 30-60 秒）

## ✅ 验证部署

访问你的 URL，确认：
- ✅ 页面正常显示
- ✅ 深色模式工作正常（系统切换深色模式测试）
- ✅ 移动端布局正常
- ✅ 联系邮箱链接可点击

## 🔒 安全性

- ✅ 自动 HTTPS（Cloudflare 提供 SSL 证书）
- ✅ DDoS 防护
- ✅ 全球 CDN 加速
- ✅ 私有仓库支持

## 💰 成本

**完全免费** - Cloudflare Pages 免费计划包括：
- 无限静态请求
- 无限带宽
- 500 次构建/月（远超你的需求）
- 1 次并发构建

## 📞 支持

如果遇到问题：
- Cloudflare 文档: https://developers.cloudflare.com/pages/
- Cloudflare 社区: https://community.cloudflare.com/

---

**创建日期**: 2025-11-17  
**维护者**: HU GongLin
