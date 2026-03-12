# 🎬 Awesome AI 视频制作

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> 精选 AI 视频制作工具、工作流、Prompt 系统与实战资源——从脚本到成片的全链路参考手册。

**[English README](README.md)**

无论你是做短视频、教育动画、广告片还是叙事影片，这个 repo 都是你的一站式参考。

---

## 目录

- [为什么做这个 Repo](#为什么做这个-repo)
- [AI 视频生成](#ai-视频生成)
- [AI 图像生成](#ai-图像生成)
- [AI 音频与音乐](#ai-音频与音乐)
- [AI 配音与 TTS](#ai-配音与-tts)
- [工作流与自动化](#工作流与自动化)
- [视频 Prompt 工程](#视频-prompt-工程)
- [分镜与脚本工具](#分镜与脚本工具)
- [后期制作与剪辑](#后期制作与剪辑)
- [分发平台](#分发平台)
- [教程与案例](#教程与案例)
- [生产管线模板](#生产管线模板)
- [参与贡献](#参与贡献)

---

## 为什么做这个 Repo

AI 视频制作领域正在爆发式增长，但信息极度碎片化。创作者在评估散落各处的工具上浪费大量时间。本 repo 提供：

- **基于真实生产经验的工具对比**，不是简单的功能罗列
- **端到端管线模板**：脚本 → 分镜 → 素材 → 成片的完整流程
- **专为视觉内容设计的 Prompt 工程体系**
- **自动化工作流方案**，将手动流程变成可复用的管线

由一位运营全栈 AI 内容制作工作室的实战从业者维护。

---

## AI 视频生成

| 工具 | 最适合 | 定价 | 质量 |
|------|--------|------|------|
| [Runway Gen-3/Gen-4](https://runwayml.com/) | 通用视频生成、运动控制 | 付费 | ⭐⭐⭐⭐⭐ |
| [可灵 Kling AI](https://klingai.com/) | 真实感运动、长片段 | 免费+付费 | ⭐⭐⭐⭐ |
| [Pika](https://pika.art/) | 快速迭代、风格化 | 免费+付费 | ⭐⭐⭐⭐ |
| [海螺 Hailuo](https://hailuoai.video/) | 快速生成、运动效果好 | 免费 | ⭐⭐⭐⭐ |
| [Vidu](https://www.vidu.studio/) | 中国风内容 | 免费+付费 | ⭐⭐⭐⭐ |
| [Sora](https://openai.com/sora) | 电影级质感 | ChatGPT Plus/Pro | ⭐⭐⭐⭐⭐ |
| [Wan 万相 (阿里)](https://github.com/Wan-Video/Wan2.1) | 开源、可本地部署 | 免费开源 | ⭐⭐⭐⭐ |
| [PixVerse](https://pixverse.ai/) | 风格化、动漫风 | 免费+付费 | ⭐⭐⭐½ |

### 生产实战经验

- **Runway** 仍然是商业项目最可靠的选择——质量稳定，运动控制好，multi-motion brush 是镜头+主体独立控制的利器。
- **可灵** 是目前免费工具中真实人物运动做得最好的。
- **Sora** 出片惊艳但不可控——适合做主视觉大片，不适合批量生产。
- 做**中国风内容**（古风、国潮、水墨），Vidu 和可灵对文化美学的理解远超西方工具。

---

## AI 图像生成

| 工具 | 最适合 | 风格优势 |
|------|--------|----------|
| [Midjourney v6/v7](https://midjourney.com/) | 写实、电影感画面 | 电影、编辑风 |
| [Midjourney Niji](https://midjourney.com/) | 动漫、插画、2D | 动漫、漫画、儿童 |
| [Stable Diffusion (SDXL)](https://stability.ai/) | 完全可控、自定义模型、批量 | 任意（LoRA/ControlNet） |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI) | 节点式 SD 工作流 | 管线自动化 |
| [FLUX](https://blackforestlabs.ai/) | 文字渲染、写实 | 写实、文字密集 |
| [Ideogram](https://ideogram.ai/) | 图中文字、Logo | 平面设计、排版 |

### 图生视频工作流（推荐）

最有效的 AI 视频一致性生产方式：

```
脚本 → 镜头列表 → 图像 Prompt → 生成关键帧 → 图生视频（img2vid）→ 剪辑
```

为什么先出图再生视频比直接文生视频好：
1. **一致性** — 你能控制角色/场景在各镜头间的外观统一
2. **迭代效率** — 先修好画面再消耗视频额度
3. **风格锁定** — 整集保持视觉连贯性

---

## AI 音频与音乐

| 工具 | 最适合 | 说明 |
|------|--------|------|
| [Suno](https://suno.com/) | 完整歌曲、BGM 生成 | 带人声音乐速出最佳 |
| [Udio](https://www.udio.com/) | 高品质音乐生成 | 音质比 Suno 更好 |
| [Stable Audio](https://stableaudio.com/) | 音效、环境音 | 适合 SFX 层 |
| [ElevenLabs 音效](https://elevenlabs.io/) | 音效生成 | 文字转音效 |

---

## AI 配音与 TTS

| 工具 | 最适合 | 语言支持 |
|------|--------|----------|
| [ElevenLabs](https://elevenlabs.io/) | 逼真声音克隆、多语言 | 29+ 语言 |
| [HeyGen](https://heygen.com/) | 数字人 + 口型同步 | 多语言 |
| [Fish Audio](https://fish.audio/) | 中文 TTS、声音克隆 | 中文极佳 |
| [ChatTTS](https://github.com/2noise/ChatTTS) | 开源、自然中文 | 中文为主 |
| [CosyVoice](https://github.com/FunAudioLLM/CosyVoice) | 开源 TTS | 中文+多语言 |

---

## 工作流与自动化

| 工具 | 类型 | 最适合 |
|------|------|--------|
| [n8n](https://n8n.io/) | 可视化自动化 | 多步管线、API 串联 |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI) | 图像生成管线 | 批量图像生成工作流 |
| [Dify](https://dify.ai/) | AI 应用构建器 | 定制内容 AI Agent |
| [飞书多维表格](https://www.feishu.cn/) | 表格+自动化 | 内容排期、资产追踪 |

### 自动化内容管线示例

```
┌──────┐   ┌──────┐   ┌───────┐   ┌──────┐   ┌──────┐   ┌──────┐
│ 脚本 │──▶│ 分镜 │──▶│Prompt │──▶│ 素材 │──▶│ 视频 │──▶│ 发布 │
│AI生成│   │AI生成│   │ 模板  │   │MJ/SD │   │Runway│   │多平台│
└──────┘   └──────┘   └───────┘   └──────┘   └──────┘   └──────┘
```

每个环节都可以模板化、自动化、批量运行。详见 [/templates](/templates) 目录。

---

## 视频 Prompt 工程

### 图像 Prompt 六模块结构

为确保最高质量和跨镜头一致性，每条图像 Prompt 遵循以下 6 个模块：

1. **舞台环境** — 整体场景、时间、氛围
2. **前景细节** — 近处物体、质感、交互元素
3. **中景主体** — 主角/主体，姿态、表情、服饰
4. **背景结构** — 建筑、景观、纵深层次
5. **动态元素** — 粒子、天气、运动、能量
6. **技术栈** — 灯光、机位、镜头、渲染风格、分辨率

### 视频 Prompt 结构

```
[主体动作] + [镜头运动] + [氛围/特效] + [光影情绪]
```

示例：
> 一位身着唐代汉服的少女缓缓转身面向镜头，樱花花瓣从脸侧飘过。慢速推镜，浅景深，黄金时段逆光轮廓光，电影感24fps，胶片颗粒。

### 通用负向提示词栈

```
watermark, QR code, text overlay, subtitle, logo, blurry, distorted face,
extra fingers, deformed hands, low quality, pixelated, oversaturated,
cartoon style (unless intended), stock photo watermark
```

---

## 分镜与脚本工具

| 工具 | 最适合 |
|------|--------|
| [Claude](https://claude.ai/) | 脚本撰写、Prompt 生成、分镜逻辑 |
| [ChatGPT](https://chat.openai.com/) | 快速构思、大纲生成 |
| [Boords](https://boords.com/) | 可视化分镜制作 |
| [Canva](https://canva.com/) | 快速分镜排版 |

### 镜号规范

```
Shot 0  — 封面镜头（3-4s）
Shot 1-N — 内容镜头（每镜3-6s）
Shot T  — 标题卡（6s）— 格式：「诗题｜朝代 · 作者」
Shot E  — 尾镜（5s）
```

---

## 分发平台

### 国内平台

| 平台 | 内容类型 | 变现方式 |
|------|----------|----------|
| 抖音 | 短视频、竖屏 | 广告分成、电商、打赏 |
| 小红书 | 生活方式、教程 | 品牌合作、带货 |
| 视频号 | 短+中视频 | 打赏、电商 |
| B站 | 长视频、知识类 | 广告分成、大会员 |

### 国际平台

| 平台 | 内容类型 | 变现方式 |
|------|----------|----------|
| YouTube | 全格式 | AdSense、会员、赞助 |
| TikTok | 短竖屏 | 创作者基金、品牌合作 |
| Instagram Reels | 短竖屏 | 品牌合作 |

---

## 教程与案例

- [从零搭建 AI 动画系列](/tutorials/ai-animation-series.md) *(即将上线)*
- [中国历史内容 Prompt 工程](/tutorials/chinese-historical-prompts.md) *(即将上线)*
- [30集内容管线自动化实战](/tutorials/automation-pipeline.md) *(即将上线)*

---

## 生产管线模板

`/templates` 目录下的即用模板：

- [少儿教育动画管线](/templates/children-education.md) *(即将上线)*
- [历史人物传记系列管线](/templates/historical-biography.md) *(即将上线)*
- [产品广告管线](/templates/product-ad.md) *(即将上线)*
- [Shot Master Prompt 模板](/templates/shot-master-prompt.md) *(即将上线)*

---

## 参与贡献

欢迎贡献！请阅读 [CONTRIBUTING.md](CONTRIBUTING.md) 了解贡献指南。

特别欢迎以下方向的贡献：
- 补充基于真实生产经验的工具评测
- 分享工作流模板和管线配置
- 中英双语内容翻译
- 你自己的 AI 视频项目案例

---

## 许可证

[MIT](LICENSE) © 2025-2026

---

如果这个 repo 对你的 AI 视频制作有帮助，请点 ⭐ Star——帮助更多人发现这些资源！
