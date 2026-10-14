# The Talking Leaves

纯 HTML + CSS 静态杂志文章。正文直接写在 `index.html`，关闭 JavaScript 仍可完整阅读。

## 修改
- 正文：编辑 `index.html` 中带 `data-original` 的标题及段落。该属性仅用于逐段校验，网页不会显示它。
- 样式：编辑 `styles.css`。按后续要求，背景已改为旧报纸浅黄 `#e8ddb6`，标题为深绿 `#173f32`。
- 图片：位于 `images/`。替换时保留文件名，或同步修改 HTML 的 `src`、尺寸、alt 和图注。
- `script.js` 目前只有注释，无必需脚本。
- 根据后续要求，已删除 Sources & Further Reading 及其以下全部内容，同时移除页顶对应入口；正文 16 个来源链接保留。

## 图片说明
- `cherokee-syllabary-comparison.png`：用户提供，位于 D/Ꭰ 段后。
- `cherokee-phoenix-1828.jpg`：真正的 1828 年 2 月 21 日创刊号，来自 Wikimedia Commons / American Antiquarian Society，公有领域。用户提供截图实际上是 5 月 21 日第 13 期，因此未使用该截图。
- `royce-1884-cherokee-cessions.png`：用户提供的全幅标注地图，保持原 PNG 格式，位于 land / power 段后。
- 视频以 Further Viewing 外链呈现，无 iframe、无自动播放。视频缩略图下载超时，当前使用简洁播放符号及标题，不使用损坏图片占位。

## 本地预览
可直接双击 `index.html`。也可在此文件夹运行：

```sh
python -m http.server 8765
```

浏览器打开 http://localhost:8765。

## GitHub Pages 部署
计划使用 GitHub Pages，目标账号为用户指定的 `258967406-spec`。截至本说明生成时，尚未完成仓库创建和公网部署，等待浏览器账号登录稳定。
1. 创建 public 仓库 `talking-leaves`。
2. 将此文件夹中的 `index.html`、`styles.css`、`script.js`、`README.md`、`.nojekyll` 及 `images/` 上传到仓库根目录。
3. Settings → Pages → Deploy from a branch → main → /(root) → Save。
4. 等待部署完成，实际打开 GitHub 返回的网址确认无需登录访问。

Cloudflare Pages 备用：上传相同文件，选择静态 HTML，无框架、无构建命令。

## 以后更新正文
直接修改 `index.html`，保持内联链接及段落顺序；提交到 main 后 Pages 会重新部署。若需严格对照新的最终稿，应重新逐字校验，不要仅凭页面目测。

## 已完成检查
- 39 个原稿文本块与 DOCX 逐字一致（只删除引用标号）。
- 16 个内联链接 URL 与用户指定完全一致，全部新标签页打开并带安全 rel。
- 没有残留引用标号；深色引文仅出现一次。
- 三张图片位置正确；图片均有 alt。
- 375px 手机视口无横向溢出。
- 16 个来源均已通过 HTTP 请求或网页检索识别到对应页面／文档；部分站点对本机自动请求返回 403、406、超时或证书链错误，不能保证所有网络和地区都能直接访问。
- 公网访问测试尚待实际部署后完成。
