# 原始语料索引

本文件负责把任务路由到可复查的第一方字幕、动态、作者回复和社区评论。不要只凭
`SKILL.md` 中的抽象表达 DNA 完成角色模拟或仿写。

## 使用原则

1. 先确定输出形态：视频长评、评分卡短评、标题、社区解码或现实争议分析。
2. 创作者本人字幕和动态是角色声音来源；评论区只用于理解受众，不得混入作者口吻。
3. 常规动漫角色模拟不得默认读取液体喵事件语料。该语料只服务于事件分析或用户明确要求的现实争议模式。
4. AI 字幕和 ASR 可用于句式、节奏和结构检索；精确引用、专有名词和事实主张必须回听或重新核验。
5. 提炼结构后重新组织内容，不连续复制原文，也不把角色台词升级为本人真实立场。

## 任务路由

| 任务 | 必读语料 | 最小采样 | 不要混入 |
|---|---|---:|---|
| 视频长评角色模拟 | 本索引 + 同类主题字幕 + 一条结构对照字幕 | 2条；超过200字时3条 | 评论区口癖、现实争议性羞辱 |
| 评分卡/动态单句 | 87条动态原始数据中的评分卡动态 | 同类对象5条 | 视频长评的完整开场和评分收尾 |
| 标题仿写 | 15条公开视频标题 + 相关字幕开头 | 6个标题，必要时再读2条字幕 | 随机堆叠宏大词 |
| 内容机制分析 | 对应研究文件 + 至少1条第一方原文 | 1至3条 | 只引用研究结论不看原文 |
| 社区黑话与解码 | `04-community-decoding.md` + 对应 rpid 原文 | 3条评论 | 把评论写成本人观点 |
| 液体喵事件分析 | `07-liquid-miao-event.md` + 事件原始 JSON/转写 | 2个独立节点 | 把切片、截图或发誓当独立实锤 |
| 现实争议角色模拟 | 仅在用户明确要求时读取事件语料 | 2条第一方片段 | 私密录音、性羞辱、健康或违法指控 |

角色模拟时，在内部先形成一个三项风格计划：开场姿态、核心偷换动作、收尾方式。
三项分别锚定到已读取语料，再开始生成。

## 本人视频字幕

目录 `sources/creator-video-subtitles/` 保存14条站内 AI 中文字幕。
`BV1PMq6YnEtf` 无站内字幕，使用 `sources/BV1PMq6YnEtf-transcript.txt` 的本地 ASR。

| BVID | 日期 | 适合提取 | 风格位置 | 文件 |
|---|---|---|---|---|
| `BV13BaCeUEDc` | 2024-08-07 | 观众降级、教育姿态、十分制收尾 | 早期原型 | `sources/creator-video-subtitles/BV13BaCeUEDc.txt` |
| `BV1K3zmY7E1A` | 2024-12-03 | 大是大非、清算语汇、自我受迫害开场 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV1K3zmY7E1A.txt` |
| `BV1K8iUY5Ess` | 2024-12-04 | 传统文化套壳、伪冷知识、短篇评分 | 经典短格式 | `sources/creator-video-subtitles/BV1K8iUY5Ess.txt` |
| `BV1PMq6YnEtf` | 2024-12-10 | 胜利宣告、技术政治化、连续阵营指控 | 高密度短篇，ASR | `sources/BV1PMq6YnEtf-transcript.txt` |
| `BV1PzqoYPEbh` | 2024-12-15 | 权威榜单、观众阶层降级、产业论证 | “太刻意”反例 | `sources/creator-video-subtitles/BV1PzqoYPEbh.txt` |
| `BV16MkGY5EcK` | 2024-12-16 | 封建/阶级套壳、理想国倒置、评分收尾 | 经典闭环 | `sources/creator-video-subtitles/BV16MkGY5EcK.txt` |
| `BV11pCYYEEvM` | 2024-12-25 | 道德恐慌、资本因果链、伪古训 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV11pCYYEEvM.txt` |
| `BV1tL6WYHECB` | 2024-12-28 | “答案是否定的”、强者逻辑、综上评分 | 最典型闭环 | `sources/creator-video-subtitles/BV1tL6WYHECB.txt` |
| `BV1f3z4BTE1s` | 2026-01-25 | 常识碎片转资本罪名、教育式劝告 | 现实议题套壳 | `sources/creator-video-subtitles/BV1f3z4BTE1s.txt` |
| `BV1WhFNzqEoA` | 2026-02-02 | 反人类争议倒置、道德身份反打、荒谬补论 | 多段式闭环 | `sources/creator-video-subtitles/BV1WhFNzqEoA.txt` |
| `BV1RncbzsEGD` | 2026-02-11 | 可喜可贺、技术替代、敌人反对即正确 | 胜利宣告型 | `sources/creator-video-subtitles/BV1RncbzsEGD.txt` |
| `BV1RQZ4ByEz1` | 2026-02-15 | 晚年思想家、同行者动摇、最后斗争 | 自我史诗专用 | `sources/creator-video-subtitles/BV1RQZ4ByEz1.txt` |
| `BV1T1QuBNE3Y` | 2026-04-14 | 连续反问、定义偷换、结果论证 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV1T1QuBNE3Y.txt` |
| `BV1eCoxBMETS` | 2026-04-23 | 逐场景改写、黑马观众开场、伪剧情梗概 | 电影解说变体 | `sources/creator-video-subtitles/BV1eCoxBMETS.txt` |
| `BV1Nk516GEd9` | 2026-05-13 | 骇人听闻、事实碎片、替天行道式收束 | 高风险样本，只取结构 | `sources/creator-video-subtitles/BV1Nk516GEd9.txt` |

优先组合：

- 普通动漫锐评：`BV1tL6WYHECB` + `BV16MkGY5EcK`，再按主题补一条。
- 技术或产业话题：`BV1RncbzsEGD` + `BV1PMq6YnEtf`。
- 自我史诗：`BV1RQZ4ByEz1` + 一条普通锐评作结构对照。
- 电影剧情重写：`BV1eCoxBMETS` + `BV1WhFNzqEoA`。
- 判断“串得太刻意”：对照 `BV1PzqoYPEbh` 与 `BV1tL6WYHECB`。

## 本人动态

原始文件：`sources/liquid-miao-event-accounts-2026-06-12.json`

关键 JSON 路径：

- 视频目录：`accounts.dishang_dongman.videos.videos`
- 87条动态：`accounts.dishang_dongman.dynamics.dynamics`
- 评分卡类型：`type == "UNKNOWN_COMMON_SQUARE"`
- 动态原文：`text_content`
- 动态锚点：`dynamic_id`

评分卡代表锚点：

- 一星共识倒置：`1016109320049262595`、`1151828005935382535`、`1196380006639468545`
- 反常五星：`1152786612579467318`、`1152027812122591234`、`1205302358833102853`
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

经典15条视频的评论结论目前以研究文件中的 rpid 锚点保存，未单独落盘完整原始 JSON。
需要逐字引用、复查上下文或分析新评论时，重新用 BiliStalker 获取对应评论，不从研究摘要反推原话。

## 液体喵事件语料

该部分是独立语域，不得作为普通动漫锐评的默认角色语料。

| 用途 | 文件 |
|---|---|
| 事件时间线与证据分层 | `research/07-liquid-miao-event.md` |
| 账号、视频与87条动态 | `sources/liquid-miao-event-accounts-2026-06-12.json` |
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
