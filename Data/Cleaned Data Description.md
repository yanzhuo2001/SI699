# **Steam 数据集说明**

## **1. Users.csv（根据Recommendations.csv更新后调整用户ID的用户信息表）**
| 字段名 | 含义 |
|--------|------|
| `user_id` | 用户的唯一 ID（匿名化） |
| `products` | 用户在 Steam 上购买的游戏数量 |
| `reviews` | 用户发布的游戏评论数量 |

---
## **2. Recommendations.csv（根据Games.csv更新后调整游戏ID的游戏评论表）**
| 字段名 | 含义 |
|--------|------|
| `app_id` | 游戏的唯一 ID（与 `games.csv` 对应） |
| `helpful` | 该评论被认为有帮助的次数 |
| `funny` | 该评论被认为有趣的次数 |
| `date` | 用户评论的发布时间 |
| `is_recommended` | 该用户是否推荐此游戏（`true` 或 `false`） |
| `hours` | 用户在该游戏上的游玩时长（小时） |
| `user_id` | 发表评论的用户 ID（与 `user.csv` 对应） |
| `review_id` | 该评论的唯一 ID |

---
## **3. Games.csv（根据最少游戏ID的csv合并后的游戏信息表）**
| 字段名 | 含义 |
|--------|------|
| `app_id` | 游戏的唯一 ID（与 `recommendation.csv` 及 `games_metadata.csv` 对应） |
| `title` | 游戏名称 |
| `date_release` | 游戏的发行日期 |
| `win` | 该游戏是否支持 Windows（`true`/`false`） |
| `mac` | 该游戏是否支持 Mac（`true`/`false`） |
| `linux` | 该游戏是否支持 Linux（`true`/`false`） |
| `rating` | 游戏的总体评价（如 "Very Positive", "Mixed"） |
| `positive_ratio` | 游戏的好评率（0-100） |
| `user_reviews` | 该游戏的总评论数量 |
| `price_final` | 游戏的最终价格（折扣后价格，单位：美元） |
| `price_original` | 游戏的原价（未折扣前价格，单位：美元） |
| `discount` | 游戏的折扣百分比 |
| `steam_deck` | 游戏是否支持 Steam Deck（`true`/`false`） |
| `description` | 游戏的详细描述 |
| `tags` | 该游戏的分类标签（如 "Action", "RPG"，多个标签用 `,` 号分隔） |
| `detailed_description` | 该游戏的详细介绍（用于 Steam 页面） |
| `about_the_game` | 该游戏的简介（Steam 页面 "About This Game" 部分） |
| `short_description` | 该游戏的简要介绍（通常是一句话总结） |
| `header_image` | 该游戏的封面图片 URL |
| `screenshots` | 该游戏的截图 JSON（包含多个缩略图和全尺寸图片） |
| `background` | 该游戏的背景图片 URL |
| `movies` | 该游戏的宣传视频（目前数据为空，但可能存储视频链接） |
