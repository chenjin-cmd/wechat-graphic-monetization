---
name: wechat-graphic-monetization
description: This skill should be used when the user wants to monetize WeChat "图文" (photo-text / 小绿书, the WeChat Official Account image-note format modeled on Xiaohongshu) via 达人带货 (affiliate-style product promotion) — including account/mode understanding, opening a video-channel showcase window (橱窗) and 联盟 (affiliate alliance), product selection, inserting product cards into 图文 posts, data review, commission withdrawal, and compliance/credit-score rules. Trigger on keywords like 小绿书, 图文带货, 公众号图文, 达人带货, 橱窗, 联盟商品, 选品, 带货, 图文变现, 佣金, 信用分.
agent_created: true
---

# 微信图文（小绿书）带货变现 Skill

> 本文件带 `name`/`description` 元数据，供支持 Skills 机制的 AI 工具（WorkBuddy、Claude Code 等）自动触发。**其他工具可直接使用等价的 `UNIVERSAL.md`**（纯文本、工具无关）。
> This file carries `name`/`description` metadata for auto-trigger in Skills-enabled AI tools (WorkBuddy, Claude Code, etc.). **Other tools can use the equivalent `UNIVERSAL.md`** (plain-text, tool-agnostic).

## Overview

本技能把「微信图文（小绿书）达人带货变现」的完整闭环，封装成 AI 助手可直接调用的程序化工作流。小绿书指公众号的图片 / 文字图文消息（对标小红书），其带货以**达人带货**为核心：不自己开店、不碰发货售后，只做「选品 → 图文带货 → 赚佣金」。

```
模式认知 (Mode) → 开通橱窗 (Window) → 选品 (Selection)
   → 图文带货 (Graphic selling) → 数据复盘 (Review) → 结算合规 (Settlement)
   → 图文创作 (Creation) → 限流与矩阵 (Traffic & Matrix)
```

当用户处于任一阶段，或要产出具体交付物（选品清单、图文带货文案、商品卡片插入步骤、合规自查）时，加载对应 `references/*.md`，并从 `assets/` 取模板。

## 五条不可逾越的底线（每次给建议都要遵守）

1. **平台规则会变。** 橱窗 / 联盟门槛、保证金、信用分规则、佣金比例都会变化，以当前微信视频号 / 公众号后台与官方规则为准；引用具体数字（如 100 粉丝、1% 手续费、信用分 12 分）时标注「以官方最新为准」。
2. **不承诺收益。** 佣金 1%–50% 只是选品中心参考区间，所有销量、佣金、案例只能作参考，绝不构成收益承诺或「保证结果」。
3. **对标 ≠ 搬运。** 带货图文属营销行为，搬运第三方未经授权内容容易被举报侵权；对标拆解是学思路，不是洗稿复制，必须加入自己的原创图文与表达。
4. **选品必须与内容强相关。** 货品要与图文内容高度相关、能解决读者痛点或满足爽点；同一账号建议稳定做一类货品（垂直），不追热点乱带无关商品。
5. **敏感信息不泄露。** 账号主体认证信息、提现银行卡信息、微信号 / 手机号等仅用于本人操作，不写进公开笔记、截图、代码仓库与分享文档。

## 决策树——加载哪个 reference

| 用户意图（信号） | 加载文件 |
| --- | --- |
| 小绿书是什么 / 达人带货 vs 小店 / 老号新号 / 能做吗 | `references/01-mode-overview.md` |
| 怎么开通橱窗 / 联盟 / 账号互绑 / 保证金 / 100 粉门槛 | `references/02-open-window.md` |
| 怎么选品 / 选品中心 / 佣金销量好评率 / 图书食品生鲜 | `references/03-product-selection.md` |
| 怎么插商品卡片 / 文案×货品结合 / 垂直 / 原创 | `references/04-graphic-selling.md` |
| 数据看板 / 销售额 vs 佣金 / 用户画像 / 复盘 | `references/05-data-review.md` |
| 提现 / 1% 手续费 / 信用分 12 分 / 违规情形 / 常见问题 | `references/06-settlement-compliance.md` |
| 封面/标题/正文怎么写爆款 / 二创 / AI 仿写 / 图片去重 | `references/07-graphic-creation.md` |
| 0 播 / 限流 / 矩阵放大 / RPA 自动化 | `references/08-traffic-matrix.md` |

跨阶段请求（如「帮我开通橱窗并选品」）可同时加载多个 reference。

## 复用资产（可直接复制到用户工作区）

- `assets/product-selection-checklist.md` — 选品自查清单（佣金 / 销量 / 好评率 / 服务项，可勾选）
- `assets/prompt-recipes.md` — 图文带货文案提示词库（痛点型 / 爽点型 / 场景型 / 对比型）
- `assets/graphic-structure-template.md` — 合格图文结构模板（封面→方案→产品→购买指南）
- `assets/title-formulas.md` — 标题公式库（保留关键词 + 换修饰）
- `assets/dedup-checklist.md` — 素材去重清单（手段 / 工具 / 版权红线）
- `assets/weekly-review-template.md` — 周复盘表
- `assets/account-matrix-template.md` — 账号矩阵规划表
- `assets/30-day-launch-calendar.md` — 30 天冷启动执行日历
- `assets/pre-publish-compliance.md` — 发布前合规自检清单

## 使用方式

1. 用决策树判断用户处于哪个阶段。
2. 加载对应 reference 获取详细方法、步骤与陷阱。
3. 用户要具体交付物时，从 `assets/` 取模板并填充其账号 / 商品信息。
4. 始终遵守五条底线，尤其是收益承诺、搬运侵权、选品相关性、敏感信息。
5. 给建议时先判断「老号还是新号」，因为开通路径不同（老号走视频号橱窗，新号电脑端还需另开联盟商品）。
