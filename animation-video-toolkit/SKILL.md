---
name: animation-video-toolkit
description: Animation and video toolchain for Muse — 18 free open-source GitHub tools covering the full pipeline from brief to render. Use when the user asks to make, animate, or export a video or animation, or asks which tool fits a motion task. Picks the right tool per stage instead of defaulting to one library.
---

# 动画与视频工具箱（18 个开源工具）

本指南按制作阶段整理动画工具。需要 Remotion 工作流时，在项目中安装相应的官方技能。

## 总路由

- 做视频（React + 代码出片、字幕、渲染）：先读 `remotion-best-practices`，按具体任务选择相关 Remotion 技能。
- 只做一个动效、不要整套视频管线：按下面分工挑库。

## 流程分工：指示 → 制作 → 动起来 → 修改 → 导出

| 阶段 | 工具 | 一句话 |
|---|---|---|
| 指示/脚手架 | Remotion `remotion-create` | 新建 Remotion 项目/Composition：`bun create video` 或 `npx create-video` |
| 制作：写画面 | `remotion-markup` | 写 Composition、排版、字体、媒体、音频、时序的最佳实践 |
| 制作：图解动画 | Motion Canvas | 代码驱动的 2D 讲解动画（TypeScript，适合示意图、流程、数据变化） |
| 制作：数学动画 | Manim | Python 数学/公式/图形动画（3Blue1Brown 同款），`pip install manim`，需 ffmpeg；数学排版需 LaTeX |
| 制作：2D 矢量 | Two.js | 与渲染器无关的 2D 绘图 API（SVG/Canvas/WebGL 同一套代码） |
| 制作：交互画布 | Konva | HTML5 Canvas 交互图形：设计编辑器、白板、可拖拽画布 |
| 制作：3D 场景 | Three.js | JS 3D 库，生态最广；Babylon.js 是带游戏/渲染管线的引擎；LUME 是用 HTML 标签写 3D（`<lume-box>`），适合轻量 3D 嵌入 |
| 制作：3D/角色 | Blender | 绑定与角色动画、建模渲染（桌面软件，非 npm：blender.org 下载；GPL） |
| 制作：游戏动画 | Godot | 2D/3D 游戏引擎，做游戏内动画与交互场景（桌面引擎，godotengine.org 下载；MIT） |
| 动起来：通用动效 | Motion | React/JS 现代动画库（手势、布局动画、滚动触发），`npm i motion` |
| 动起来：时间线 | Anime.js | JS 动画引擎，时间线、错峰（stagger）、SVG/属性动画 |
| 动起来：顺序补间 | TweenJS | CreateJS 套件，按顺序把对象动起来 |
| 动起来：缓动 | Shifty | 轻量快速的 TypeScript 补间引擎 |
| 动起来：数值平滑 | Ola | 让数值平滑变动（插值），适合仪表盘、计数、实时数据 |
| 动起来：粒子 | Proton | JS 粒子动画库（爆炸、烟雾、星空等粒子效果） |
| 动起来：播放 AE 动画 | Lottie Web | 轻量播放 After Effects 导出的矢量动画（JSON），Web/Android/iOS |
| 修改/预览 | `remotion-studio`、`remotion-interactivity` | Studio 预览；让图层在 Studio 里可点选编辑 |
| 导出：视频/静帧 | `remotion-render` | 渲染成视频或静帧 |
| 导出：字幕 | `remotion-captions` | 转录、展示、动画化字幕 |
| 导出：GIF | gifenc | 快速 GIF 编码，`npm i gifenc` |
| 导出：音视频处理 | `remotion-multimedia` | Mediabunny：浏览器内读写音视频元数据、转码 |
| 文档/升级/许可 | `remotion-docs`、`remotion-upgrade`、`remotion-license` | 查 Remotion 文档、升级、许可证问答 |

## 选型速查

- 讲解/科普动画（公式、图表、流程）：Manim（数学）或 Motion Canvas（通用图解）。
- 网页里的动效：Motion（React）或 Anime.js（通用）；数值滚动用 Ola；粒子用 Proton。
- 已有 AE 成品要放网页/App：Lottie Web。
- 完整短视频（旁白+字幕+多镜）：Remotion 全套。
- 3D 产品演示：Three.js；要游戏级渲染管线：Babylon.js；要 HTML 里嵌 3D：LUME。
- 交互白板/编辑器：Konva；2D 绘图抽象层：Two.js。
- 角色动画/影视级：Blender；游戏：Godot。

## 安装命令

```bash
npm i remotion @remotion/cli
npm i motion
npm i @motion-canvas/core
npm i animejs
npm i shifty
npm i ola
npm i two.js
npm i lottie-web
npm i @createjs/tweenjs
npm i @lume/element
npm i gifenc
npm i konva
npm i three
npm i @babylonjs/core
npm i proton-js
pip install manim                   # Python，需 ffmpeg
```

Blender、Godot 不走 npm，去官网下载。Remotion 新项目用 `bun create video`（会提示加装官方技能）。

## 工具仓库

- [remotion-dev/skills](https://github.com/remotion-dev/skills)
- [motion-canvas/motion-canvas](https://github.com/motion-canvas/motion-canvas)
- [motiondivision/motion](https://github.com/motiondivision/motion)
- [franciscop/ola](https://github.com/franciscop/ola)
- [juliangarnier/anime](https://github.com/juliangarnier/anime)
- [ManimCommunity/manim](https://github.com/ManimCommunity/manim)
- [jeremyckahn/shifty](https://github.com/jeremyckahn/shifty)
- [jonobr1/two.js](https://github.com/jonobr1/two.js)
- [airbnb/lottie-web](https://github.com/airbnb/lottie-web)
- [CreateJS/TweenJS](https://github.com/CreateJS/TweenJS)
- [lume/lume](https://github.com/lume/lume)
- [mattdesl/gifenc](https://github.com/mattdesl/gifenc)
- [konvajs/konva](https://github.com/konvajs/konva)
- [blender/blender](https://github.com/blender/blender)
- [mrdoob/three.js](https://github.com/mrdoob/three.js)
- [godotengine/godot](https://github.com/godotengine/godot)
- [BabylonJS/Babylon.js](https://github.com/BabylonJS/Babylon.js)
- [drawcall/Proton](https://github.com/drawcall/Proton)

## 移植到其他 Agent

将本技能目录复制到目标工具支持的技能目录。项目若引用 Remotion 配套技能，另行安装相应依赖。

## 注意

- 别把“开源权重/开源技能”和“零成本”混为一谈：Remotion 免费版可商用有条件，许可证问题读 `remotion-license`。
- 动效库只解决“动起来”，长视频的脚手架、字幕、渲染仍走 Remotion；不要为一个小动效搭整套视频管线。
- 做视频前先确认用途（抖音竖屏/推文方形/教程横屏），再选工具，不要先装一堆库。

## 进阶动效与媒体处理

| 用途 | 工具 | 使用要点 |
| --- | --- | --- |
| 动作设计 | motion-design、GSAP | 前者用于节奏和缓动设计，后者编排时间线。 |
| 线稿与结构图解 | hairline-create、hairline-adopt、anatomy、anatomy-reveal | 从草图或 SVG 生成等距图解。导出分解展示视频前，检查 FFmpeg 和 ImageMagick 依赖。 |
| 3D 物理与特效 | @react-three/rapier、@react-three/postprocessing、three.quarks | 分别处理物理、后期和粒子。安装前核对 React Three Fiber 的兼容版本。 |
| 数据、交互与创意编程 | D3、Matter.js、PixiJS、p5.js、Tweakpane、@react-spring/web | 按需选择数据图、2D 物理、画布渲染、参数调节或弹簧动画。使用 DOM 的库在浏览器中预览。 |
| 声音与节奏 | Openverse、Tone.js、librosa、MusicGen | 分别用于寻找素材、合成音频、检测节拍和生成音乐。使用素材时核对许可及署名条件。 |
| 字幕对齐 | WhisperX、whisper.cpp | 先转录旁白，再用带时间戳的结果与成片核对。 |
| 三维渲染与补帧 | Blender、RIFE、FFmpeg | 无 GPU 时可尝试 Cycles CPU。补帧后检查帧率、时长和音轨同步。 |
