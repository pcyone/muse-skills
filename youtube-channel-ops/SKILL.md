# YouTube 频道自动化运营

## 频道定位

- 以 Meta Muse 实操教程为例，面向第一次使用 Muse 的观众。开始前，和频道负责人确认目标观众、每周产量、目标时长、发布时区和固定发布窗口。
- 上传前，由负责人在自己的环境中配置频道账号与 Google Cloud 项目。

## 七段式流水线

- 按以下 7 个 Agent 分工执行，每步输出后停下等用户确认再继续。
- 第 1 步选题 Agent 用 YouTube 搜索加 Google Trends 找 10 个选题，按搜索需求和竞争度打分，输出前 3 名及理由。
- 第 2 步脚本 Agent 按用户口语风格写大纲加逐字稿，开头 5 秒必须有钩子，每 60 秒一个留存点。
- 第 3 步封面 Agent 每个选题出 3 个封面方案，主标题不超过 6 个字加视觉元素，并说明点击理由。
- 第 4 步配音 Agent 按逐字稿生成旁白，标注停顿和重音。
- 第 5 步剪辑 Agent 输出分镜表，包含画面、旁白、字幕和 BGM 时间轴，可直接交给剪辑工具执行。
- 第 6 步上传 Agent 生成标题、简介、标签和章节时间戳，并建议发布时间。
- 第 7 步复盘 Agent 在发布 48 小时后拉取播放、完播率和点击率，总结 3 条可复用的经验和 1 条下期改进点。

## 人工检查点

- 脚本、封面和成片发布前必须用户点头，这三个检查点不能跳过。
- 草稿只发给用户看，不自动发布，不自动上传公开。
- 用户说只做一件事时，只交付那一件事，不多做。

## 证据规则

- 所有事实和数据必须标注来源，不编数字，不确定的写待核实。
- 不做模板化量产内容，每条视频必须有用户自己的观点或实测。
- 遵守 YouTube 的 AI 内容披露要求，旁白是 AI 合成语音。

## 配音标准

- 配音只保留豆包 TTS 男声擎苍单音轨，声音 ID 是 zh_male_qingcang_uranus_bigtts，不加背景音乐。
- 只标注停顿和重音，不改逐字稿的词，音色全频道锁死一个。
- 配音前读取项目自己的品牌声音卡，核对音色、语速、停顿和重音。

## 上传方法

- 通过 YouTube Data API 上传。使用目标频道自己的 OAuth 授权，并将授权文件保存在本地。
- 上传前检查项目的 API 配额。生成标题、简介、标签、章节和封面，提交给负责人核对。
- 用户确认后，按排期以私密状态上传，并将计划公开时间转换为 UTC。随后到 YouTube Studio 核对视频、隐私状态、封面与定时设置。

## 每日推进与每周复盘

- 和频道负责人约定每日推进时间与时区，读取项目状态，确认当前视频、当前步骤和待审批内容。
- 一次推进一个步骤，将草稿交给负责人，确认后更新状态。
- 每周按选题、脚本、封面、配音、剪辑和上传安排制作；发布 48 小时后复盘，并把结论带入下周选题。
- 当天没有待办步骤时，简要汇报频道近况；尚未取得的数据标为待核实。

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with the Muse guide to custom connectors and MCPs, or build a custom connector.

## Websites

- [YouTube Studio](https://studio.youtube.com/) for 勾选 AI 生成内容披露、设封面、核对标题简介和章节。带上视频 ID 进去，核对隐私状态和定时公开时间。
- [Google Cloud Console](https://console.cloud.google.com/) for 管理 OAuth 客户端和 YouTube Data API v3 的启用状态。

## Alternatives for better results

- 演示段优先使用实际录屏。缺少录屏时，用步骤图解卡呈现操作。
- 成片抽 8 帧检查开场、数据图、关键卡片和结尾，有伪文字或穿帮直接返工。
- 字幕按旁白逐句烧录，排轴前先数清钩子语音段数，数错一段全片字幕错位。
