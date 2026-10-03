# wechat-graphic-monetization · Universal (tool-agnostic) guide

> 微信图文（小绿书）达人带货变现的**工具无关方法论**。
> 本文件供任意支持「项目上下文 / 系统指令」的 AI 工具使用——Cursor、Claude、Claude Code、Cline、通义灵码、CodeBuddy、ChatGPT 自定义指令、WorkBuddy 等，不绑定任何单一工具。

## 这是什么

把「微信图文（小绿书）带货」的实战经验，整理成一份给 AI 助手看的程序化工作流。小绿书是公众号的图片 / 文字图文消息（对标小红书），其主流变现方式是**达人带货**：不自己开店、不碰发货售后，只做「选品 → 图文带货 → 赚佣金」。

它覆盖一个图文账号从开通带货能力到结算合规的全生命周期：

**模式认知 → 开通橱窗 → 选品 → 图文带货 → 数据复盘 → 结算合规**

配套文件：
- `references/` 按阶段拆分的详细方法论（本文件只做索引与决策）
- `assets/` 可直接复制的交付物模板（选品清单、文案提示词）
- `SKILL.md` 带 `name`/`description` 元数据的入口（供支持 Skills 机制的 AI 工具自动触发，如 WorkBuddy / Claude Code；内容与本文等价）

## 怎么用（任意 AI 工具都行）

把本仓库作为**项目上下文 / 系统指令**提供给你的 AI，然后告诉它读哪些文件。例如：

> 先读 `UNIVERSAL.md` 和 `references/03-product-selection.md`，帮我按「高佣金 + 七天无理由 + 好评率高」筛一批适合图书类图文带货的商品。

AI 会按下面的决策树自动加载对应阶段的方法论。无需安装插件，也无需特定平台。

## 决策树：该读哪一份

| 你的目标 | 读这份 |
|---|---|
| 搞懂小绿书带货是什么 / 达人带货 vs 小店 / 老号新号 | `references/01-mode-overview.md` |
| 开通橱窗 / 联盟 / 账号互绑 / 保证金 | `references/02-open-window.md` |
| 选品 / 佣金销量好评率 / 图书食品生鲜 | `references/03-product-selection.md` |
| 插入商品卡片 / 文案与货品结合 / 垂直 / 原创 | `references/04-graphic-selling.md` |
| 看数据 / 销售额 vs 佣金 / 复盘 | `references/05-data-review.md` |
| 提现 / 手续费 / 信用分 / 违规 / 常见问题 | `references/06-settlement-compliance.md` |
| 封面/标题/正文怎么写爆款 / 二创 / AI 仿写 / 图片去重 | `references/07-graphic-creation.md` |
| 0 播 / 限流 / 矩阵放大 / RPA 自动化 | `references/08-traffic-matrix.md` |

## 五条底线（合规）

1. **平台规则会变**：橱窗 / 联盟门槛、保证金、信用分、佣金比例以微信官方最新规则为准，引用数字标注「以官方最新为准」。
2. **不承诺收益**：佣金 1%–50% 只是参考区间，所有销量 / 佣金 / 案例不作收益承诺。
3. **对标 ≠ 搬运**：带货图文属营销行为，搬运第三方内容易被举报侵权；学思路，不洗稿复制，坚持原创图文。
4. **选品强相关**：货品要与内容高度相关、解决痛点或满足爽点；同账号建议稳定做一类货品（垂直）。
5. **敏感信息不外泄**：认证主体、提现银行卡、微信号 / 手机号不写进公开仓库。

## 阶段概览

1. **模式认知** `references/01-mode-overview.md`：达人带货 vs 微信小店、老号 / 新号、7 大特点、橱窗 vs 短视频 vs 直播门槛。
2. **开通橱窗** `references/02-open-window.md`：视频号实名 → 创建橱窗 → 开通带货权限 → 账号互绑 → 开通联盟商品。
3. **选品** `references/03-product-selection.md`：手机 / 电脑选品中心、筛选原则、佣金·销量·好评率、图书与食品生鲜。
4. **图文带货** `references/04-graphic-selling.md`：插入商品卡片（电脑 / 手机端）、文案×货品结合、垂直与原创。
5. **数据复盘** `references/05-data-review.md`：数据看板、销售额 vs 佣金、成交 / 商品 / 用户画像。
6. **结算合规** `references/06-settlement-compliance.md`：提现 1% 手续费、信用分 12 分制、7 类违规、FAQ。
7. **图文创作** `references/07-graphic-creation.md`：封面/标题/正文、模块化心法、AI 仿写提示词、图片去重。
8. **限流与矩阵** `references/08-traffic-matrix.md`：0 播应对、商品入口多样化、矩阵放大、RPA 自动化。

## 可直接复制的模板

- `assets/product-selection-checklist.md` — 选品自查清单（可勾选）
- `assets/prompt-recipes.md` — 图文带货文案提示词库
- `assets/graphic-structure-template.md` — 合格图文结构模板
- `assets/title-formulas.md` — 标题公式库
- `assets/dedup-checklist.md` — 素材去重清单
- `assets/weekly-review-template.md` — 周复盘表
- `assets/account-matrix-template.md` — 账号矩阵规划表
- `assets/30-day-launch-calendar.md` — 30 天冷启动日历
- `assets/pre-publish-compliance.md` — 发布前合规自检

---

MIT License。
