# Chenhui Miao Blog

基于 Hexo 和 Fluid 主题的个人博客。

## 本地预览

```bash
npm install
npm run server
```

打开 `http://localhost:4000` 查看博客。

## 新建文章

```bash
npx hexo new "文章标题"
```

## 构建

```bash
npm run build
```

构建结果会生成到 `public/`。

## GitHub Pages 部署

这个项目已经配置了 GitHub Actions 自动部署。

1. 在 GitHub 创建一个新仓库。
2. 把本地项目推送到仓库的 `main` 分支。
3. 在仓库 `Settings -> Pages` 中，把 `Source` 设置为 `GitHub Actions`。
4. 当前发布地址是 `https://1519605664-hui.github.io/chenhui-miao.github.io/`。

## 已开启功能

- Fluid 主题
- 暗色模式
- 站内搜索
- 分类与标签
- RSS：`/atom.xml`
- 站点地图：`/sitemap.xml`
- GitHub Actions 自动部署
