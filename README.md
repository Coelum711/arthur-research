# Arthur Research

Arthur Research 是一个可直接发布到 GitHub Pages 的匿名研究档案站，预设自定义域名 `research.arthur-k.uk`。网页正文使用英文；没有构建步骤、后台、分析服务或外部字体。Related Work 星图使用少量纯前端 JavaScript，仅用于本地筛选与 SVG 交互。

研究主问题：

> How can a canon-grounded persistent character remain recognisably itself while genuinely changing through open-ended lived experience?

## 隐私范围

公开站点刻意不包含：

- 研究者真实姓名、学校/单位、邮箱、地理位置或其他现实身份信息；
- 私人对话、关系信息、地点历史、内部日记、原始行为记录或可识别的角色生活细节；
- runtime credentials、raw logs、production prompts 或 production source code。

站点只保留抽象研究问题、概念框架、公开级 study directions、related work 与证据规范。项目名称 `Arthur Research` 和公开域名仅用于标识研究档案本身。

## 预览

直接打开 `index.html`，或在仓库根目录运行：

```sh
python3 -m http.server 8080
```

## GitHub Pages

1. 将此目录内容提交到仓库 `main` 根目录。
2. `Settings → Pages → Build and deployment`。
3. Source 选 `Deploy from a branch`；Branch 选 `main`；目录选 `/ (root)`。
4. 自定义域名使用 `research.arthur-k.uk`；根目录已包含 `CNAME`。

详细步骤见 `docs/GITHUB_PAGES.md`。

## 内容状态

当前公开版包含完整 research question、三层 persistence、研究地图、三条高层 study directions、related work 与匿名化的 framework changelog。可执行 protocol、阈值、样本设计与分析细节在正式 preregistration / preprint / paper 之前不公开。没有发布自然运行中的私人 longitudinal trace，也没有报告完成的 controlled result。

## Related-work atlas

The related-work page combines a current foreground set with a broader 82-work background map and later additions. Its constellation is descriptive research positioning, not a quality ranking.
