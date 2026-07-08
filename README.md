# 🎬 Awesome AI Video Production

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> A curated collection of tools, workflows, prompt systems, and resources for AI-powered video production — from script to screen.

**[中文版 README](README_CN.md)**

Whether you're creating short-form content, educational animations, advertising videos, or full narrative films with AI, this repo is your one-stop reference.

---

## Table of Contents

- [Why This Repo](#why-this-repo)
- [AI Video Generation](#ai-video-generation)
- [AI Image Generation](#ai-image-generation)
- [AI Audio & Music](#ai-audio--music)
- [AI Voice & TTS](#ai-voice--tts)
- [Workflow & Automation](#workflow--automation)
- [Prompt Engineering for Video](#prompt-engineering-for-video)
- [Storyboard & Script Tools](#storyboard--script-tools)
- [Post-Production & Editing](#post-production--editing)
- [Distribution Platforms](#distribution-platforms)
- [Tutorials & Case Studies](#tutorials--case-studies)
- [Production Pipeline Templates](#production-pipeline-templates)
- [Contributing](#contributing)

---

## Why This Repo

The AI video production space is exploding but fragmented. Creators waste hours evaluating scattered tools. This repo provides:

- **Tool comparisons** with real production experience, not just feature lists
- **End-to-end pipeline templates** from script → storyboard → assets → final video
- **Prompt engineering systems** specifically designed for visual content
- **Automation workflows** that turn manual processes into repeatable pipelines

Built by a practitioner running a full AI content production studio.

---

## AI Video Generation

Tools for generating video clips, animations, and footage from text or images.

| Tool | Best For | Pricing | Quality |
|------|----------|---------|---------|
| [Runway Gen-3/Gen-4](https://runwayml.com/) | General video gen, motion control | Paid tiers | ⭐⭐⭐⭐⭐ |
| [Kling AI](https://klingai.com/) | Realistic motion, long clips | Free tier + paid | ⭐⭐⭐⭐ |
| [Pika](https://pika.art/) | Quick iterations, stylized | Free tier + paid | ⭐⭐⭐⭐ |
| [Hailuo / MiniMax](https://hailuoai.video/) | Fast generation, good motion | Free tier | ⭐⭐⭐⭐ |
| [Vidu](https://www.vidu.studio/) | Chinese-style content | Free tier + paid | ⭐⭐⭐⭐ |
| [Sora](https://openai.com/sora) | Cinematic quality | ChatGPT Plus/Pro | ⭐⭐⭐⭐⭐ |
| [Wan (Alibaba)](https://github.com/Wan-Video/Wan2.1) | Open source, self-hosted | Free (open source) | ⭐⭐⭐⭐ |
| [Podframes](https://github.com/Jellypod-Inc/podframes) | Two-host AI podcast videos from one topic | Free (open source) | ⭐⭐⭐ |
| [LTX Video](https://www.ltx.studio/) | Full project management | Paid | ⭐⭐⭐⭐ |
| [PixVerse](https://pixverse.ai/) | Stylized, anime-friendly | Free tier + paid | ⭐⭐⭐½ |

### Tips from Production Experience

- **Runway** remains the most reliable for commercial work — consistent quality, good motion control, and the multi-motion brush is a game-changer for directing camera + subject independently.
- **Kling** is the best free option right now for realistic human motion.
- **Sora** produces stunning results but is unpredictable — great for hero shots, not for batch production.
- For **Chinese-style content** (古风, 国潮, ink wash), Vidu and Kling handle cultural aesthetics significantly better than Western tools.

---

## AI Image Generation

For creating keyframes, storyboard frames, backgrounds, and character assets.

| Tool | Best For | Style Strength |
|------|----------|---------------|
| [Midjourney v6/v7](https://midjourney.com/) | Photorealistic, cinematic frames | Cinematic, editorial |
| [Midjourney Niji](https://midjourney.com/) | Anime, illustration, 2D styles | Anime, manga, children's |
| [Stable Diffusion (SDXL)](https://stability.ai/) | Full control, custom models, batch | Any (with LoRA/ControlNet) |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI) | Node-based SD workflows | Pipeline automation |
| [FLUX](https://blackforestlabs.ai/) | Text rendering, photorealism | Photorealistic, text-heavy |
| [Ideogram](https://ideogram.ai/) | Text in images, logos | Graphic design, typography |
| [Recraft](https://www.recraft.ai/) | Vector art, brand assets | Illustration, icons |

### Image-to-Video Workflow

The most effective pipeline for consistent AI video production:

```
Script → Shot List → Image Prompts → Generate Keyframes → Video Gen (img2vid) → Edit
```

Why image-first beats text-to-video:
1. **Consistency** — You control character/scene appearance across shots
2. **Iteration speed** — Fix the frame before spending video credits
3. **Style lock** — Maintain visual coherence across an entire episode

---

## AI Audio & Music

| Tool | Best For | Notes |
|------|----------|-------|
| [Suno](https://suno.com/) | Full songs, BGM generation | Best for quick music with vocals |
| [Udio](https://www.udio.com/) | High-quality music gen | Better audio fidelity than Suno |
| [Stable Audio](https://stableaudio.com/) | Sound effects, ambient | Good for SFX layers |
| [ElevenLabs Sound Effects](https://elevenlabs.io/) | SFX generation | Text-to-SFX |

### Music Production Tips

- Generate 3-5 variations per scene, then pick. AI music is cheap — use volume to find quality.
- For children's content: Suno with cheerful prompts + tempo 120-140 BPM works consistently.
- Always generate instrumental versions separately for under-narration use.

---

## AI Voice & TTS

| Tool | Best For | Language Support |
|------|----------|-----------------|
| [ElevenLabs](https://elevenlabs.io/) | Realistic voice cloning, multilingual | 29+ languages |
| [HeyGen](https://heygen.com/) | Talking avatar + lip sync | Multilingual |
| [Fish Audio](https://fish.audio/) | Chinese TTS, voice cloning | Excellent Chinese |
| [ChatTTS](https://github.com/2noise/ChatTTS) | Open source, natural Chinese | Chinese-focused |
| [CosyVoice](https://github.com/FunAudioLLM/CosyVoice) | Open source TTS | Chinese + multilingual |
| [Azure TTS](https://azure.microsoft.com/en-us/products/ai-services/text-to-speech) | Production-grade, SSML control | 100+ languages |

### Voice Direction Tips

- For educational content: slightly slower speed (0.85-0.9x), warm tone, clear enunciation.
- For advertising: energetic, slightly compressed, higher pitch.
- Always generate at highest quality, then compress in post — you can't upscale voice quality.

---

## Workflow & Automation

| Tool | Type | Best For |
|------|------|----------|
| [n8n](https://n8n.io/) | Visual automation | Multi-step pipelines, API chaining |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI) | Image gen pipeline | Batch image generation workflows |
| [Dify](https://dify.ai/) | AI app builder | Custom AI agents for content |
| [飞书/Feishu Bitable](https://www.feishu.cn/) | Spreadsheet + automation | Content tracking, scheduling |
| [Airtable](https://airtable.com/) | Database + automation | Project management, asset tracking |
| Chrome CDP + Playwright 双轨浏览器自动化 | 浏览器自动化 | Chrome MCP 截图/导航/读取 + Playwright CDP JS执行/网络拦截，双轨互补。已知限制：chrome_javascript 返回 undefined |
| 抖音视频 CDP WebSocket 直连下载 | 视频下载 | Chrome CDP WebSocket 拦截播放请求，sessionid + sid_guard 两个 Cookie 获取 1080p 无水印视频 |
| 钉钉机器人加签推送 | 自动化推送 | Python hashlib 签名需 UTF-8 encode 后再 base64/hexdigest，与 Golang 实现对齐 |

### Example: Automated Content Pipeline

```
┌─────────┐    ┌───────────┐    ┌──────────┐    ┌───────────┐    ┌──────────┐
│  Script  │───▶│ Storyboard│───▶│  Prompts │───▶│  Assets   │───▶│  Video   │
│ (AI Gen) │    │ (AI Gen)  │    │ (Template)│   │ (MJ/SD)   │    │ (Runway) │
└─────────┘    └───────────┘    └──────────┘    └───────────┘    └──────────┘
                                                                       │
                                                                       ▼
                                                                 ┌──────────┐
                                                                 │  Publish  │
                                                                 │(Multi-plat)│
                                                                 └──────────┘
```

Each step can be templated, automated, and run in batch. See [/templates](/templates) for ready-to-use pipeline configs.

---

## Prompt Engineering for Video

### Image Prompt Structure (6-Module System)

For maximum quality and consistency, structure every image prompt with these 6 modules:

1. **Stage Environment** — Overall setting, time of day, atmosphere
2. **Foreground Detail** — Close objects, textures, interactive elements
3. **Midground Subject** — Main character/object, pose, expression, clothing
4. **Background Structure** — Architecture, landscape, depth layers
5. **Dynamic Elements** — Particles, weather, movement, energy
6. **Technical Stack** — Lighting, camera, lens, render style, resolution

### Video Prompt Structure

When writing prompts for video generation (Runway, Kling, etc.):

```
[Subject Action] + [Camera Movement] + [Atmosphere/FX] + [Lighting Mood]
```

Example:
> A young girl in Tang dynasty hanfu slowly turns to face the camera, cherry blossoms drifting past her face. Slow dolly-in, shallow depth of field, golden hour rim lighting, cinematic 24fps, film grain.

### Negative Prompt Stack (Universal)

```
watermark, QR code, text overlay, subtitle, logo, blurry, distorted face,
extra fingers, deformed hands, low quality, pixelated, oversaturated,
cartoon style (unless intended), stock photo watermark
```

---

## Storyboard & Script Tools

| Tool | Best For |
|------|----------|
| [Claude](https://claude.ai/) | Script writing, prompt generation, storyboard logic |
| [ChatGPT](https://chat.openai.com/) | Quick ideation, outline generation |
| [Boords](https://boords.com/) | Visual storyboard creation |
| [Canva](https://canva.com/) | Quick storyboard layouts |
| [FrameForge](https://www.frameforge.com/) | Professional previz |

### Shot Numbering Convention

For consistent production tracking:

```
Shot 0  — Cover shot (3-4s)
Shot 1-N — Content shots (3-6s each)
Shot T  — Title card (6s) — format: 「Title｜Dynasty · Author」
Shot E  — End card (5s)
```

---

## Post-Production & Editing

| Tool | Best For | Price |
|------|----------|-------|
| [CapCut](https://www.capcut.com/) | Quick edits, subtitles, effects | Free + Pro |
| [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve) | Professional editing + color | Free + Studio |
| [Premiere Pro](https://www.adobe.com/products/premiere.html) | Industry standard editing | Subscription |
| [After Effects](https://www.adobe.com/products/aftereffects.html) | Motion graphics, VFX | Subscription |
| [Cinema 4D](https://www.maxon.net/en/cinema-4d) | 3D assets, product viz | Subscription |
| [Toon Boom Harmony](https://www.toonboom.com/products/harmony) | Traditional + digital animation | Subscription |

---

## Distribution Platforms

### Chinese Platforms

| Platform | Content Type | Monetization |
|----------|-------------|--------------|
| 抖音 (Douyin) | Short video, vertical | Ad revenue, e-commerce, tips |
| 小红书 (Xiaohongshu) | Lifestyle, tutorials | Brand deals, affiliate |
| 视频号 (WeChat Video) | Short + mid video | Tips, e-commerce |
| B站 (Bilibili) | Long-form, educational | Ad revenue, membership |

### International Platforms

| Platform | Content Type | Monetization |
|----------|-------------|--------------|
| YouTube | All formats | AdSense, membership, sponsorship |
| TikTok | Short vertical | Creator fund, brand deals |
| Instagram Reels | Short vertical | Brand deals |

### Multi-Platform Strategy

- Produce in **landscape 16:9** as master, then crop to **9:16** for vertical platforms.
- Or produce natively in each format if quality matters more than speed.
- Use platform-specific hooks: Douyin needs a strong first 3 seconds, YouTube needs strong thumbnails.

---

## Tutorials & Case Studies

- [How to Build an AI Animation Series from Zero](/tutorials/ai-animation-series.md) *(coming soon)*
- [Prompt Engineering for Chinese Historical Content](/tutorials/chinese-historical-prompts.md) *(coming soon)*
- [Automating a 30-Episode Content Pipeline](/tutorials/automation-pipeline.md) *(coming soon)*

---

## Production Pipeline Templates

Ready-to-use templates in the `/templates` directory:

- [Children's Educational Animation Pipeline](/templates/children-education.md) *(coming soon)*
- [Historical Biography Series Pipeline](/templates/historical-biography.md) *(coming soon)*
- [Product Advertisement Pipeline](/templates/product-ad.md) *(coming soon)*
- [Shot Master Prompt Template](/templates/shot-master-prompt.md) *(coming soon)*

---

## Contributing

We welcome contributions! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Areas where help is especially welcome:
- Adding new tools with real production experience
- Sharing workflow templates and pipeline configs
- Translating content between English and Chinese
- Case studies from your own AI video projects

---

## License

[MIT](LICENSE) © 2025-2026

---

## Star History

If this repo helps your AI video production work, please ⭐ star it — it helps others discover these resources!
