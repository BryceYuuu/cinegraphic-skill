# Cinegraphic / 电影图形主义

> **Not a filter. A visual system.**  
> **不是滤镜，是一套视觉系统。**

Cinegraphic is a reusable image-to-poster prompting system that transforms reference images into cinematic, editorial, mid-century-inspired graphic posters.

Cinegraphic 是一套可复用的图像转海报提示词系统：把普通照片、人物图和参考构图重新设计成具有电影海报感、编辑插画感与复古印刷质感的现代主义作品。

![Cinegraphic reference grid](assets/reference-grid.jpg)

## Core visual grammar / 核心视觉语言

- Mid-century modern poster composition / 20 世纪中叶现代主义构图
- Editorial illustration / 编辑插画
- Vintage cinema poster design / 复古电影海报
- Restricted 3–5 color palettes / 3–5 色限制色体系
- Geometric facial and body planes / 人物几何切面
- Oversized typography as composition / 巨型字体参与构图
- Strong negative space and asymmetric hierarchy / 大面积留白与非对称层级
- Screen-print, Risograph and paper grain / 丝网印刷、Risograph 与纸张颗粒
- Simplified architecture and environmental silhouettes / 建筑与环境几何化

The objective is not to make an image simply look old. The objective is to make it look **designed**.

目标不是把图片简单“做旧”，而是让它看起来像真的被设计过。

## Prompt versions / 提示词版本

### Local / Open Model — Maximum Reference Fidelity
适用于本地/开源工作流，如 FLUX、Qwen Image、SDXL、ComfyUI。优先保留参考图构图、人物关系、动作和视觉层级。

- [English + 中文](prompts/local-reference-faithful.md)

### Hosted / Guardrail-Friendly — Original Reinterpretation
适用于 ChatGPT、Gemini 等可能存在第三方相似性保护的平台。先提取高层视觉结构，再从零重构原创海报。

- [English + 中文](prompts/hosted-original-reinterpretation.md)

## Recommended ratios / 推荐比例

- `3:4` — social cover / 社交封面
- `2:3` — classic poster / 经典电影海报
- `4:5` — editorial / 编辑视觉
- `16:9` — landscape key art / 横版主视觉

## Local image-to-image strength / 本地图生图强度参考

- `0.35–0.55` — preserve more composition / 更多保留原构图
- `0.55–0.75` — stronger Cinegraphic transformation / 更明显风格转译
- `0.75+` — loose reinterpretation / 更自由重新设计

## Author

Bryce Yu

## License

Prompt text and documentation are released under the MIT License. Third-party source imagery shown in the comparison grid is for visual study/reference only and is not included in the MIT license.
