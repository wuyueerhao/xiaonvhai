# Xiaonvhai

基于Hexo和Next主题的静态博客。

## 本地开发

```bash
# 安装依赖
npm install

# 清理缓存
npm run clean

# 本地预览
npm run server

# 生成静态文件
npm run build
```

## Cloudflare Pages 部署配置

### 1. 连接 GitHub 仓库

1. 登录 [Cloudflare Dashboard](https://dash.cloudflare.com/)
2. 进入 **Workers & Pages** > **Create application** > **Pages** > **Connect to Git**
3. 选择你的 GitHub 仓库：`wuyueerhao/xiaonvhai`

### 2. 构建配置

在 Cloudflare Pages 设置中使用以下配置：

- **Framework preset**: None (或选择 Hexo)
- **Build command**: `npm run build`
- **Build output directory**: `public`
- **Root directory**: `/` (默认)
- **Environment variables**:
  - `NODE_VERSION`: `24.10.0` (可选，已通过 .node-version 文件指定)

### 3. 部署

配置完成后，Cloudflare Pages 会自动：
- 每次推送到 main 分支时自动构建和部署
- 为每个 Pull Request 创建预览部署
- 提供全球 CDN 加速

## 技术栈

- [Hexo](https://hexo.io/) - 静态博客框架
- [Next Theme](https://github.com/next-theme/hexo-theme-next) - Hexo 主题
- Cloudflare Pages - 部署平台

## 主题配置

主题配置文件位于 `_config.next.yml`，可以在此文件中自定义主题样式、功能等。

## 写作

```bash
# 创建新文章
npx hexo new "文章标题"

# 创建新页面
npx hexo new page "页面名称"

# 创建草稿
npx hexo new draft "草稿标题"
```
