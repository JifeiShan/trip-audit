# 行前体检

你的 AI 行程，真的走得完吗？

这是一个已经发布到 GitHub Pages 的静态网站，用来承接“旅行路线体检/深度重排/创作者项目策划”的咨询需求。

## 入口

- 网站：https://jifeishan.github.io/trip-audit/
- 咨询入口：https://jifeishan.github.io/trip-audit/contact.html
- 行程审计器：https://jifeishan.github.io/trip-audit/auditor.html
- 20 问清单：https://jifeishan.github.io/trip-audit/checklist.html
- 服务与报价：https://jifeishan.github.io/trip-audit/offers.html
- 原创资料包：https://jifeishan.github.io/trip-audit/products.html
- AI 行程自查 50 问：https://jifeishan.github.io/trip-audit/product-ai-itinerary-self-check.html
- 购买意向：https://jifeishan.github.io/trip-audit/order.html
- GitHub Issues：https://github.com/JifeiShan/trip-audit/issues
- 启动日志：[LAUNCH_LOG.md](LAUNCH_LOG.md)
- 运营手册：[OPERATIONS.md](OPERATIONS.md)

## 服务

- 路线体检：找出原行程里最可能崩的风险点。
- 深度重排：把 3-7 天旅行重排到真实可执行。
- 创作者项目：把旅行变成图文、视频或拍摄项目。

## 公开路线图

这个项目不是一次性网页。它会继续沉淀：

- 行程审计规则。
- 匿名路线案例。
- 内容选题。
- 资料包。
- 开源小工具。

详细路线图见 [ROADMAP.md](ROADMAP.md)。

## 页面

- `index.html`：落地页。
- `auditor.html`：行程审计器原型。
- `checklist.html`：AI 日本行程出发前 20 问。
- `offers.html`：服务与报价决策页。
- `products.html`：原创资料包和低价数字产品页。
- `product-ai-itinerary-self-check.html`：AI 行程自查 50 问详情和样章页。
- `order.html`：测试期购买意向复制页。
- `inquiry.html`：咨询问卷复制页。
- `contact.html`：咨询入口和接单边界。
- `privacy.html`：隐私与服务边界。
- `OPERATIONS.md`：公开运营循环、报价梯度和接单边界。

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

## 设置咨询入口

发布前把占位联系方式替换成真实入口：

```bash
node money_research/scripts/set-contact.mjs 微信 your_wechat_id "填完问卷后发送纯文本，不要发送证件号、订单号或银行卡信息。"
```

## GitHub Pages 发布方式

本仓库已发布到 GitHub Pages。后续更新流程：

```bash
git add .
git commit -m "Update site"
git push origin main
```

## 运营补充

- GitHub Issues 只接匿名样例和非隐私问题。
- 真实联系方式可用 `set-contact.mjs` 替换。
- 付款方式先人工确认，不自动收款。
- 后续需要补充自定义域名与访问统计。
