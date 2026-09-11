# Cinegraphic / 电影图形主义

> **Not a filter. A visual system.**  
> **不是滤镜，是一套视觉系统。**

Cinegraphic is a reusable image-to-poster prompting system that transforms reference images into cinematic, editorial, mid-century-inspired graphic posters.

Cinegraphic 是一套可复用的图像转海报提示词系统：把普通照片、人物图和参考构图重新设计成具有电影海报感、编辑插画感与复古印刷质感的现代主义作品。

<p align="center">
  <img src="assets/reference-grid-horizontal.svg" width="100%" alt="Cinegraphic reference comparisons">
</p>

<p align="center"><sub>Noir / Temporal / Romance · three source-to-Cinegraphic transformations</sub></p>

---

<table>
<tr>
<td width="50%" valign="top">

### Visual grammar / 视觉语言

- Mid-century modern composition
- Editorial illustration
- Vintage cinema poster design
- Restricted 3–5 color palettes
- Geometric facial & body planes
- Oversized typography
- Strong negative space
- Screen-print / Risograph texture

</td>
<td width="50%" valign="top">

### What it does / 它做什么

- 保留人物关系与视觉重心
- 压缩复杂配色为有限色体系
- 把人物重构成几何块面
- 用大字参与构图，而不是简单贴字
- 简化建筑和环境噪音
- 加入纸张、油墨、套印偏差等印刷质感

</td>
</tr>
</table>

> The objective is not to make an image look old. The objective is to make it look **designed**.  
> 目标不是把图片简单“做旧”，而是让它看起来像真的被设计过。

---

## Choose your mode / 选择版本

<table>
<tr>
<td width="50%" valign="top">

### Local / Open Model
**Maximum Reference Fidelity**

适合 FLUX、Qwen Image、SDXL、ComfyUI 等本地 / 开源工作流。

优先保留：
- 构图
- 人物关系
- 动作
- 镜头方向
- 主色关系
- 关键道具

**[English + 中文 Prompt →](prompts/local-reference-faithful.md)**

</td>
<td width="50%" valign="top">

### Hosted / Guardrail-Friendly
**Original Reinterpretation**

适合 ChatGPT、Gemini 等可能存在第三方相似性保护的平台。

工作流：
- 提取高层情绪与构图
- 去掉可识别第三方身份细节
- 从零重构原创人物与版式
- 再套用 Cinegraphic 视觉系统

**[English + 中文 Prompt →](prompts/hosted-original-reinterpretation.md)**

</td>
</tr>
</table>

---

<table>
<tr>
<td width="50%" valign="top">

### Recommended ratios / 推荐比例

| Use | Ratio |
|---|---|
| Social cover | `3:4` |
| Classic poster | `2:3` |
| Editorial | `4:5` |
| Landscape key art | `16:9` |

</td>
<td width="50%" valign="top">

### Local img2img strength / 本地图生图强度

| Strength | Result |
|---|---|
| `0.35–0.55` | 更多保留原构图 |
| `0.55–0.75` | 更明显风格转译 |
| `0.75+` | 更自由重新设计 |

</td>
</tr>
</table>

---

## Skill file

For agent / skill-based workflows, use **[SKILL.md](SKILL.md)**.

用于 Agent / Skill 工作流时，直接读取 **[SKILL.md](SKILL.md)**。

## Author

**Bryce Yu**

## License

Prompt text and documentation are released under the MIT License. Third-party source imagery shown in the comparison examples is for visual study/reference only and is not included in the MIT license.
