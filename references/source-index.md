# 原始语料索引

本文件负责把任务路由到可复查的第一方字幕、动态、作者回复和社区评论。不要只凭
`SKILL.md` 中的抽象表达 DNA 完成角色模拟或仿写。

## 使用原则

1. 先确定输出形态：视频长评、评分卡短评、标题、社区解码或现实争议分析。
2. 创作者本人字幕和动态是角色声音来源；评论区只用于理解受众，不得混入作者口吻。
3. 常规动漫角色模拟不得默认读取液体喵事件语料。该语料只服务于事件分析或用户明确要求的现实争议模式。
4. AI 字幕和 ASR 可用于句式、节奏和结构检索；精确引用、专有名词和事实主张必须回听或重新核验。
5. 提炼结构后重新组织内容，不连续复制原文，也不把角色台词升级为本人真实立场。
6. 研究文件中的机制名、公式、证据标签和社区分类只服务于内部规划，不得直接进入角色成稿。
7. 角色成稿只保留用户请求的正文形态；来源锚点、检索过程和引用说明应放在正文之外。

## 任务路由

| 任务 | 必读语料 | 最小采样 | 不要混入 |
|---|---|---:|---|
| 视频长评角色模拟 | 本索引 + 同类主题字幕 + 一条结构对照字幕 | 2条；超过200字时3条 | 研究术语、评论区口癖、评分卡包装、现实争议性羞辱 |
| 评分卡/动态单句 | 90条当前可见动态中的60条文本星级评分卡 | 同类对象5条 | 视频长评的完整开场、十分制收尾、栏目标题和解释段 |
| 标题仿写 | 当前公开视频标题 + 相关字幕开头 | 6个标题，必要时再读2条字幕 | 随机堆叠宏大词 |
| 内容机制分析 | 对应研究文件 + 至少1条第一方原文 | 1至3条 | 只引用研究结论不看原文 |
| 社区黑话与解码 | `04-community-decoding.md` + 对应 rpid 原文 | 3条评论 | 把评论写成本人观点 |
| 真实人物公开内容锐评 | 被评内容原文 + 普通锐评字幕 | 被评内容1条，风格对照2条 | 无关私生活、旧争议、法律状态、人格或动机猜测 |
| 液体喵事件分析 | `07-liquid-miao-event.md` + 事件原始 JSON/转写 | 2个独立节点 | 把切片、截图或发誓当独立实锤 |
| 现实争议角色模拟 | 仅在用户明确要求时读取事件语料 | 2条第一方片段 | 私密录音、性羞辱、健康或违法指控 |

角色模拟时，在内部先形成三个锚点：目标素材里的不可替换事实、同类语料里可借用的推进方式、结尾语气。
锚点分别来自已读取语料，但不是成稿大纲，也不按固定顺序填空。

成稿前执行一次语域与特异性清理：

- 普通视频锐评默认写成约300至650个汉字的连续口播；逐场景剧情改写约600至900字。
- 评分卡只输出星级和一句裁决，通常不超过80个汉字。
- 不输出“评分卡、锐评文案、一句话裁决、一/二/三”等外部编辑结构。
- 不输出机制名、公式名、研究标签、置信度、BVID、动态ID、链接或引用标记。
- `鱼`、`老粉/新粉`、`串味`、`一星密码`等社区语言不得自动转成作者口癖。
- 问候、固定口癖、评分和宣言都是可选语气件；从同类样本中择少数使用，不把所有高频词塞进同一篇。
- 如果删掉作品名、人物名或事件名后正文仍能套给其他对象，回到原文补目标独有细节；补不出就向用户要素材。
- 连续输出多个版本时，更换事实接点或推进方式，不批量复用同一个开头和收尾。
- 评价真实人物时只使用当前公开内容中可核验的主张，不自动调用无关争议或推断其人格和动机。
- 用户需要来源时，先完成纯净成稿，再由普通助手在成稿之后单列风格样本和事实来源；依据说明也不展示机制名或内部计划。

## 本人视频字幕

目录 `sources/creator-video-subtitles/` 保存17条站内 AI 中文字幕。
`BV1PMq6YnEtf` 无站内字幕，使用 `sources/BV1PMq6YnEtf-transcript.txt` 的本地 ASR。

| BVID | 日期 | 适合提取 | 风格位置 | 文件 |
|---|---|---|---|---|
| `BV1WM7F6UEVs` | 2026-06-21 | 道歉、承认造谣/抹黑、要求停止传播 | 现实争议止损边界，不进入普通动漫锐评语料 | `sources/creator-video-subtitles/BV1WM7F6UEVs.txt` |
| `BV1Wujt6ZEpL` | 2026-06-21 | 动漫解说/云小鬼、观看方式倒置、资本与效率套壳 | 普通动漫/评论生态锐评，可作新近结构样本 | `sources/creator-video-subtitles/BV1Wujt6ZEpL.txt` |
| `BV1ZPJL6WETe` | 2026-06-13 | 正式回应、保存提示、直播验证、法律责任、分段悬念 | 现实争议专用，不进入普通动漫锐评语料 | `sources/creator-video-subtitles/BV1ZPJL6WETe.txt` |
| `BV13BaCeUEDc` | 2024-08-07 | 观众降级、教育姿态、十分制收尾 | 早期原型 | `sources/creator-video-subtitles/BV13BaCeUEDc.txt` |
| `BV1K3zmY7E1A` | 2024-12-03 | 大是大非、清算语汇、自我受迫害开场 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV1K3zmY7E1A.txt` |
| `BV1K8iUY5Ess` | 2024-12-04 | 传统文化套壳、伪冷知识、短篇评分 | 经典短格式 | `sources/creator-video-subtitles/BV1K8iUY5Ess.txt` |
| `BV1PMq6YnEtf` | 2024-12-10 | 胜利宣告、技术政治化、连续阵营指控 | 高密度短篇，ASR | `sources/BV1PMq6YnEtf-transcript.txt` |
| `BV1PzqoYPEbh` | 2024-12-15 | 权威榜单、观众阶层降级、产业论证 | “太刻意”反例 | `sources/creator-video-subtitles/BV1PzqoYPEbh.txt` |
| `BV16MkGY5EcK` | 2024-12-16 | 封建/阶级套壳、理想国倒置、评分收尾 | 经典闭环 | `sources/creator-video-subtitles/BV16MkGY5EcK.txt` |
| `BV11pCYYEEvM` | 2024-12-25 | 道德恐慌、资本因果链、伪古训 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV11pCYYEEvM.txt` |
| `BV1tL6WYHECB` | 2024-12-28 | “答案是否定的”、结论先行、综上评分 | 高风险样本，只取结构，不复刻性强迫合理化内容 | `sources/creator-video-subtitles/BV1tL6WYHECB.txt` |
| `BV1f3z4BTE1s` | 2026-01-25 | 常识碎片转资本罪名、教育式劝告 | 现实议题套壳 | `sources/creator-video-subtitles/BV1f3z4BTE1s.txt` |
| `BV1WhFNzqEoA` | 2026-02-02 | 反人类争议倒置、道德身份反打、荒谬补论 | 多段式闭环 | `sources/creator-video-subtitles/BV1WhFNzqEoA.txt` |
| `BV1RncbzsEGD` | 2026-02-11 | 可喜可贺、技术替代、敌人反对即正确 | 胜利宣告型 | `sources/creator-video-subtitles/BV1RncbzsEGD.txt` |
| `BV1RQZ4ByEz1` | 2026-02-15 | 晚年思想家、同行者动摇、最后斗争 | 自我史诗专用 | `sources/creator-video-subtitles/BV1RQZ4ByEz1.txt` |
| `BV1T1QuBNE3Y` | 2026-04-14 | 连续反问、定义偷换、结果论证 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV1T1QuBNE3Y.txt` |
| `BV1eCoxBMETS` | 2026-04-23 | 逐场景改写、黑马观众开场、伪剧情梗概 | 电影解说变体 | `sources/creator-video-subtitles/BV1eCoxBMETS.txt` |
| `BV1Nk516GEd9` | 2026-05-13 | 骇人听闻、事实碎片、替天行道式收束 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV1Nk516GEd9.txt` |

优先组合：

- 普通动漫锐评：`BV16MkGY5EcK` + `BV1K8iUY5Ess`，再按主题补一条；涉及动漫解说、云小鬼或观看方式争议时可补 `BV1Wujt6ZEpL`；需要“答案是否定的”结构时才参考`BV1tL6WYHECB`。
- 技术或产业话题：`BV1RncbzsEGD` + `BV1PMq6YnEtf`。
- 自我史诗：`BV1RQZ4ByEz1` + 一条普通锐评作结构对照。
- 电影剧情重写：`BV1eCoxBMETS` + `BV1WhFNzqEoA`。
- 判断“串得太刻意”：对照 `BV1PzqoYPEbh` 与 `BV1tL6WYHECB`。

## 本人动态

旧原始文件：`sources/liquid-miao-event-accounts-2026-06-12.json`
最新增量文件：`sources/dishang-dongman-new-public-data-2026-06-25.json`、`sources/dishang-dongman-all-raw-dynamics-2026-06-25.json`、`sources/dishang-dongman-raw-dynamics-first-page-2026-06-25.json`

关键 JSON 路径：

- 视频目录：`accounts.dishang_dongman.videos.videos`
- 90条当前可见动态：`sources/dishang-dongman-all-raw-dynamics-2026-06-25.json`
- 评分卡类型：`type == "UNKNOWN_COMMON_SQUARE"`
- 动态原文：`text_content`
- 动态锚点：`dynamic_id`

评分卡代表锚点：

- 一星共识倒置：`1016109320049262595`、`1151828005935382535`、`1196380006639468545`
- 反常五星：`1152786612579467318`、`1152027812122591234`、`1205302358833102853`
- 2026-06-25新增一星：`1217843044865277969`（《散华礼弥》）、`1217842821522784264`（《小林家的龙女仆》）
- 宏大话语短评：`1013862661284167682`、`1013863052128288773`
- 自我神化与生活叙事：`1013705753235554308`、`1212145680581132311`

`UNKNOWN_COMMON_SQUARE` 的对象名称不在当前稳定字段中。需要确认作品名时，先查
`research/01-account-map.md` 和 `research/02-content-mechanics.md` 中已经核对的映射；
没有映射就只描述动态文本，不猜作品对象。

检索示例：

```powershell
rg -n '"dynamic_id": "1151828005935382535"|\[星\]|还真是' references/sources
rg -n '答案是否定的|综上所述|哈基米|真正看懂' references/sources/creator-video-subtitles
```

## 社区与作者回复

- 社区机制总表：`research/04-community-decoding.md`
- 液体喵事件动态评论：`sources/liquid-miao-event-dynamic-comments-2026-06-12.json`
- 液体喵事件视频评论：`sources/liquid-miao-event-videos-comments-2026-06-12.json`
- 作者回复锚点：`rpid:302198271793`、`rpid:302201740225`、`rpid:302205104257`

早期经典视频的评论结论目前以研究文件中的 rpid 锚点保存，未单独落盘完整原始 JSON。
需要逐字引用、复查上下文或分析新评论时，重新用 BiliStalker 获取对应评论，不从研究摘要反推原话。

## 液体喵事件语料

该部分是独立语域，不得作为普通动漫锐评的默认角色语料。

| 用途 | 文件 |
|---|---|
| 事件时间线与证据分层 | `research/07-liquid-miao-event.md` |
| 2026-06-21本人道歉视频、两条新增视频、两条新增评分卡及评论 | `sources/dishang-dongman-new-public-data-2026-06-25.json` |
| 2026-06-25当前90条ALL_RAW动态 | `sources/dishang-dongman-all-raw-dynamics-2026-06-25.json` |
| 2026-06-25原始动态首页，用于核对评分卡作品名 | `sources/dishang-dongman-raw-dynamics-first-page-2026-06-25.json` |
| 2026-06-13本人正式回应详情、字幕与评论 | `sources/BV1ZPJL6WETe-bilistalker-2026-06-13.json` |
| 账号、视频与旧87条动态 | `sources/liquid-miao-event-accounts-2026-06-12.json` |
| 搜索候选与筛选结果 | `sources/liquid-miao-event-search-index-2026-06-12.json` |
| 关键视频详情与字幕 | `sources/liquid-miao-event-extra-videos-2026-06-12.json` |
| 视频评论 | `sources/liquid-miao-event-videos-comments-2026-06-12.json` |
| 动态评论与楼中楼 | `sources/liquid-miao-event-dynamic-comments-2026-06-12.json` |
| 本地ASR | `sources/BV1foRjBSEvk-transcript.txt`、`sources/BV19d5E6mEpK-transcript.txt`、`sources/BV1aHE16hELD-transcript.txt` |

事件语料中包含未经独立核验的关系、健康、违法和私密内容。只可用于分析公开叙事结构、
证据秀和传播机制，不得据此生成现实指控或复刻羞辱。

## 研究文件导航

| 问题 | 文件 |
|---|---|
| 账号阶段、视频和动态覆盖 | `research/01-account-map.md` |
| 选题与论证机制 | `research/02-content-mechanics.md` |
| 标题、句式、开场和人设 | `research/03-expression-performance.md` |
| 黑话、受众分层和评论续写 | `research/04-community-decoding.md` |
| 引流、争议和传播循环 | `research/05-traffic-controversy.md` |
| 人设演化、立场置信度和留出测试 | `research/06-evolution-boundaries.md` |
| 液体喵事件专项 | `research/07-liquid-miao-event.md` |
