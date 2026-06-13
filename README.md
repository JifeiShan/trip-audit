# 行前体检

你的 AI 行程，真的走得完吗？

这是一个可直接发布到 GitHub Pages 的静态网站草稿，用来承接“旅行路线体检/深度重排/创作者项目策划”的咨询需求。

## 服务

- 路线体检：找出原行程里最可能崩的风险点。
- 深度重排：把 3-7 天旅行重排到真实可执行。
- 创作者项目：把旅行变成图文、视频或拍摄项目。

## 页面

- `index.html`：落地页。
- `auditor.html`：行程审计器原型。
- `inquiry.html`：咨询问卷复制页。
- `privacy.html`：隐私与服务边界。

## 方法

- 交通核对
- 季节风险
- 住宿区域
- 体力边界
- 拍摄节奏
- 备选方案

## 本地预览

直接打开：

```bash
open index.html
```

或用任意静态服务器：

```bash
python3 -m http.server 8080
```

## 检查链接

从工作区根目录运行：

```bash
node money_research/scripts/check-site-links.mjs
```

## 设置正式站点 URL

拿到 GitHub Pages 地址后，从工作区根目录运行：

```bash
node money_research/scripts/set-site-url.mjs https://your-name.github.io/trip-audit
```

## GitHub Pages 发布方式

当前机器的 `gh` 登录态已失效，需要先重新登录：

```bash
gh auth login -h github.com
```

登录后可在 `money_research/site` 目录里创建仓库并发布：

```bash
git init
git add .
git commit -m "Launch trip audit landing page"
gh repo create trip-audit --public --source=. --remote=origin --push
gh api -X POST repos/:owner/trip-audit/pages -f source.branch=main -f source.path=/
```

如果默认分支是 `master`，把 `main` 改成实际分支名。

## 上线前补充

- 联系方式：微信、邮箱或表单链接。
- 真实案例：至少 3 个匿名诊断案例。
- 付款方式：先用人工确认后收款，不自动收款。
- 自定义域名与访问统计。
