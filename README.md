# 简读 · 在线阅读站

本仓库只放**构建产物**，是 [Shaksper/jianyue](https://github.com/Shaksper/jianyue) 的静态导出版本，供 GitHub Pages 托管。

- 在线阅读：https://shaksper.github.io/jianyue-site/
- `index.html` 是完整的单页阅读器（书架 + 阅读页 + 字号/主题 + 进度记忆 + Markdown 导出），数据以内联方式注入，无后端依赖
- `404.html` 是同一份阅读器，用于深链接兜底
- `.nojekyll` 关闭 Jekyll 处理，避免静态资源被过滤

## 不要在这里手改

内容由业务系统生成、发布后导出：

```bash
# 在 jianyue 仓库里
npm run build:static     # data/db.json -> docs/
# 再把 docs/ 的三个文件同步到本仓库
```

只导出 `status=published` 的导读，草稿与下架版本不会出现在站点上。
