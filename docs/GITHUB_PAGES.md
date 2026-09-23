# GitHub Pages 发布说明

## 推荐：分支根目录发布

本项目的 HTML 就是发布产物。没有 npm、Jekyll、编译器或自定义 GitHub Actions 工作流需要运行。保留根目录 `.nojekyll` 文件。

1. 新建一个可用 GitHub Pages 的仓库；公开仓库是最简单的选择。仓库名可用 `arthur-research`。
2. 上传项目内容，确认仓库根目录直接包含 `index.html` 和 `assets/`。图形界面上传时容易漏掉隐藏文件；可在 GitHub 的 Add file → Create new file 创建空的 `.nojekyll`，或使用下面的 Git 方式上传全部文件。
3. Settings → Pages → Build and deployment → Source 选择 **Deploy from a branch**。
4. 选择 **main** 和 **/ (root)**，Save。
5. 查看 Actions 中 GitHub 自动生成的 Pages 任务。成功后以 Settings → Pages 给出的地址为准。
6. 检查首页、八个导航链接、直接打开 `questions.html#rq1`、刷新子页、窄屏阅读和模板下载。

官方说明：
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site

## 可选：Git 上传

在此项目文件夹中执行。替换 YOUR_USERNAME 为你的 GitHub 用户名；先在 GitHub 创建空仓库。以下命令由维护者主动执行，本次交付没有替你执行 push。

```sh
git init -b main
git add .
git commit -m "Create Arthur Research static website"
git remote add origin https://github.com/YOUR_USERNAME/arthur-research.git
git push -u origin main
```

已有 Git 仓库时，不要重复初始化或盲目替换 origin；使用现有仓库流程。

## 地址和子路径

普通项目仓库在绑定域名前可通过 `https://YOUR_USERNAME.github.io/arthur-research/` 访问。

本项目已经在根目录提供 `CNAME`，内容为：

```text
research.arthur-k.uk
```

发布后，在 **Settings → Pages → Custom domain** 确认 `research.arthur-k.uk`。Cloudflare DNS 中为 `research` 建立 CNAME，目标指向你的 GitHub Pages 主机名（通常为 `YOUR_USERNAME.github.io`）。建议先让 DNS 解析生效，再启用 GitHub Pages 的 **Enforce HTTPS**。

内部链接采用 `questions.html`、`assets/style.css` 等相对路径。不要加成 `/assets/style.css`，否则在项目子路径下会指向错误位置。改仓库名无需改当前相对链接。

## 常见问题

- **404**：确认发布分支是 main、目录是根目录、根目录有 index.html、Pages 任务已完成。
- **首页能看，样式缺失**：确认 assets 文件夹也已上传，文件大小写未改，地址包含项目路径。
- **更新没出现**：确认最新提交已成功发布，稍后刷新或硬刷新。
- **找不到 Pages 设置或选项不可用**：检查仓库管理权限及账户对该仓库可见性对应的 Pages 支持。
- **别把“文件已上传”当成“已发布”**：最终以任务成功和公开 URL 实际可访问为准。

仓库发布范围内的 README、docs 和 templates 也应视作公开内容。当前项目不含私密原始记录。后续证据整理请遵循 CONTENT_GUIDE.md。
