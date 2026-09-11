# Cinegraphic / 电影图形主义

> **Not a filter. A visual system.**  
> **不是滤镜，是一套视觉系统。**

Cinegraphic is a reusable image-to-poster prompting system that transforms reference images into cinematic, editorial, mid-century-inspired graphic posters.

Cinegraphic 是一套可复用的图像转海报提示词系统：把普通照片、人物图和参考构图重新设计成具有电影海报感、编辑插画感与复古印刷质感的现代主义作品。

## Reference transformations / 参考效果

<table>
<tr>
<td width="33.33%" align="center" valign="top">
<img src="https://raw.githubusercontent.com/BryceYuuu/cinegraphic-skill/main/assets/noir.jpg" width="100%" alt="Cinegraphic Noir comparison"><br>
<sub><b>Noir</b></sub>
</td>
<td width="33.33%" align="center" valign="top">
<img src="https://raw.githubusercontent.com/BryceYuuu/cinegraphic-skill/main/assets/temporal.jpg" width="100%" alt="Cinegraphic Temporal comparison"><br>
<sub><b>Temporal</b></sub>
</td>
<td width="33.33%" align="center" valign="top">
<img src="https://raw.githubusercontent.com/BryceYuuu/cinegraphic-skill/main/assets/romance.jpg" width="100%" alt="Cinegraphic Romance comparison"><br>
<sub><b>Romance</b></sub>
</td>
</tr>
</table>

<p align="center"><sub>Three source-to-Cinegraphic transformations · 三组原图 → Cinegraphic 风格转译</sub></p>

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

优先保留：构图、人物关系、动作、镜头方向、主色关系、关键道具。

**[Standalone prompt file →](prompts/local-reference-faithful.md)**

</td>
<td width="50%" valign="top">

### Hosted / Guardrail-Friendly
**Original Reinterpretation**

适合 ChatGPT、Gemini 等可能存在第三方相似性保护的平台。

工作流：提取高层情绪与构图 → 去掉可识别第三方身份细节 → 从零重构 → 应用 Cinegraphic。

**[Standalone prompt file →](prompts/hosted-original-reinterpretation.md)**

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

# Prompt Pack / 提示词正文

> **Click to expand. English on the left · 中文在右侧。**  
> 两列使用原生 Markdown 表格渲染，中间会有明确分隔线，不再使用会把右栏挤出屏幕的代码块。

<details>
<summary><b>1) Local / Open Model — Maximum Reference Fidelity / 本地开源模型版</b></summary>
<br>

| English | 中文 |
|---|---|
| **CORE INSTRUCTION**<br><br>Transform the provided reference image into a sophisticated mid-century modern editorial poster.<br><br>Do not simply apply a filter. Reconstruct the entire image as a designed graphic poster. | **核心指令**<br><br>将输入参考图片重新设计成一张高级的复古现代主义编辑海报。<br><br>不要简单给原图套滤镜，需要重新设计整张图片，使其真正成为一张平面设计海报。 |
| **PRESERVE FROM THE REFERENCE**<br><br>• number of subjects<br>• subject relationships<br>• recognizable pose and gesture<br>• camera angle and framing<br>• visual hierarchy<br>• dominant color relationships<br>• major clothing silhouettes<br>• important props<br>• emotional tone<br>• spatial relationships between subjects | **从参考图保留**<br><br>• 人物数量<br>• 人物之间的关系<br>• 主要动作和姿势<br>• 镜头角度与取景<br>• 视觉重心<br>• 主色关系<br>• 服装主要轮廓<br>• 关键道具<br>• 情绪<br>• 人物之间的空间关系 |
| **VISUAL LANGUAGE**<br><br>Combine mid-century modern poster design, European editorial illustration, vintage cinema poster design, screen-print graphics, Risograph texture, and 1960s–1970s magazine illustration. | **视觉语言**<br><br>融合 20 世纪中叶现代主义海报、欧洲编辑插画、复古电影海报、丝网印刷、Risograph 孔版印刷，以及 1960–1970 年代杂志插画。 |
| **CHARACTER RENDERING**<br><br>Use sharp geometric facial planes, simplified anatomy, elongated proportions, strong silhouettes, angular shadows, large flat color areas, restrained facial details, and expressive but controlled gestures.<br><br>Maintain enough identifying characteristics for the subject to remain recognizable when appropriate. Avoid photographic skin texture. | **人物绘制**<br><br>使用锐利的几何面部切面、简化人体结构、修长比例、强烈剪影、大块明暗、大面积平涂色块、克制五官细节，以及有表现力但不过度夸张的动作。<br><br>在适当情况下保留足够的人物识别特征，避免摄影式真实皮肤纹理。 |
| **COLOR SYSTEM**<br><br>Preserve the dominant color identity of the original image, then compress it into a restricted 3–5 color poster palette.<br><br>Preferred structure:<br>• 1 dominant color<br>• 1 dark structural color<br>• 1 light paper color<br>• 1–2 optional accent colors<br><br>Examples:<br>• scarlet / black / warm cream<br>• slate blue / charcoal / ivory<br>• dark green / burgundy / warm beige<br>• mustard / black / parchment<br><br>Avoid unnecessary gradients. | **配色**<br><br>尽可能保留原图主要色彩身份，再压缩成 3–5 色的限制色海报体系。<br><br>推荐结构：<br>• 1 个主色<br>• 1 个深色结构色<br>• 1 个浅色纸张色<br>• 1–2 个辅助色<br><br>例如：<br>• 朱红 / 黑 / 暖米白<br>• 灰蓝 / 炭黑 / 象牙白<br>• 深绿 / 酒红 / 暖米色<br>• 芥末黄 / 黑 / 旧纸色<br><br>避免不必要的渐变。 |
| **TYPOGRAPHY**<br><br>Introduce oversized editorial typography as a structural graphic element rather than ordinary text.<br><br>It may be cropped, partially hidden, vertical, placed behind people, overlapped by architecture, or extended beyond the canvas.<br><br>Text may be abstract or concept-derived. Do not overcrowd the poster. | **字体**<br><br>加入超大型编辑字体，让字体成为构图结构的一部分，而不是普通信息文字。<br><br>可以被画布裁切、被人物遮挡、竖向排列、置于人物后方、与建筑重叠，或延伸到画布之外。<br><br>文字可以是抽象字母或根据主题生成，但不要塞入过量文案。 |
| **COMPOSITION**<br><br>Use bold asymmetrical composition. Create strong foreground/background relationships. Allow figures to overlap typography. Use negative space aggressively. Simplify architecture, furniture, and environment into geometric shapes. Remove visual clutter that does not strengthen the composition. | **构图**<br><br>采用大胆的非对称构图，强调前景与背景的层次。允许人物覆盖字体，大胆使用留白。将建筑、家具和环境简化成几何剪影与色块，并删除不会增强画面表达的复杂元素。 |
| **TEXTURE**<br><br>Add paper grain, aged paper texture, screen-print ink, Risograph grain, subtle ink bleeding, uneven ink density, slight registration offset, printed-edge wear, and restrained halftone texture.<br><br>The result should feel physically printed rather than digitally glossy. | **印刷质感**<br><br>加入纸张颗粒、老纸纹理、丝网印刷油墨、Risograph 颗粒、轻微油墨扩散、不均匀墨色、轻微套色偏移、印刷边缘磨损和克制网点。<br><br>画面应该像真实印刷品，而不是光滑的数字渲染图。 |
| **FINAL LOOK**<br><br>The finished result should feel like a collectible vintage film poster or elite editorial illustration.<br><br>Elegant. Minimal. Cinematic. Graphic. Tactile. Timeless.<br><br>**Avoid:** generic AI illustration, glossy 3D rendering, plastic skin, over-detailed backgrounds, excessive gradients, neon cyberpunk colors, random decorative elements, unnecessary text, modern advertising aesthetics. | **最终效果**<br><br>最终作品应该像收藏级复古电影海报或高级杂志编辑插画。<br><br>高级、克制、电影感、平面化、有触感、不过时。<br><br>**避免：**普通 AI 插画感、光滑 3D 渲染、塑料皮肤、复杂背景、大量渐变、赛博朋克霓虹、随机装饰、无意义小字、廉价商业广告感。 |

**Copy-ready full prompt / 可直接复制完整版：** [Local prompt file](prompts/local-reference-faithful.md)

</details>

<br>

<details>
<summary><b>2) Hosted / Guardrail-Friendly — Original Reinterpretation / 托管平台原创重构版</b></summary>
<br>

| English | 中文 |
|---|---|
| **ANALYZE FIRST**<br><br>Analyze the provided reference image only for its high-level visual structure.<br><br>Extract:<br>• number of subjects<br>• emotional relationship<br>• dominant mood<br>• broad pose direction<br>• camera orientation<br>• visual hierarchy<br>• dominant color relationships<br>• negative-space distribution<br>• general subject placement | **先分析高层信息**<br><br>首先只分析输入参考图片的高层视觉信息。<br><br>提取：<br>• 人物数量<br>• 人物之间的情绪关系<br>• 整体氛围<br>• 大致动作方向<br>• 镜头方向<br>• 视觉层级<br>• 主色关系<br>• 留白分布<br>• 主体在画面中的大致位置 |
| **ORIGINAL REINTERPRETATION**<br><br>Do not recreate the original artwork. Create a completely new and original poster inspired only by these high-level characteristics.<br><br>If the reference contains recognizable actors, characters, movie posters, brands, logos, costumes, makeup, typography, or other protected visual identities, replace them with original equivalents. | **原创重构**<br><br>不要直接重制原作品。根据这些高层信息，从零设计一张完全原创的新海报。<br><br>如果参考图片包含可识别的演员、影视角色、电影海报、品牌、Logo、标志性服装、妆容、字体或其他第三方视觉身份，请自动替换为原创设计。 |
| **CREATE NEW**<br><br>Create new faces, hairstyles, wardrobe details, props, background environment, typography, title, and graphic elements while preserving only the broad emotional and compositional logic. | **重新设计**<br><br>重新设计人物面孔、发型、服装细节、道具、背景、字体、标题和图形元素，只保留原图的大致情绪关系、人物数量、叙事逻辑和整体视觉重心。 |
| **STYLE**<br><br>Reinterpret the scene using the Cinegraphic visual system: mid-century modern editorial poster, European graphic illustration, vintage cinema design, screen-print aesthetics, Risograph texture, and 1960s–1970s editorial graphics. | **风格**<br><br>将场景重新设计为 Cinegraphic / 电影图形主义：20 世纪中叶现代主义编辑海报、欧洲平面插画、复古电影海报、丝网印刷、Risograph 孔版印刷和 1960–1970 年代编辑设计。 |
| **CHARACTERS**<br><br>Use sharp facial planes, angular shadows, simplified anatomy, elongated proportions, strong silhouettes, and large flat color fields. | **人物**<br><br>使用锐利面部切面、大块阴影、简化人体结构、修长比例、强剪影和大面积平涂。 |
| **COLOR**<br><br>Use a restricted 3–5 color palette. Preserve only the broad color relationship of the reference, not its exact colors.<br><br>Prefer warm cream paper, deep black or charcoal, one strong dominant color, and one optional muted accent color. | **颜色**<br><br>使用 3–5 种限制性色彩，只保留参考图的大致颜色关系，不要精确复制颜色。<br><br>推荐暖米白纸张、深黑或炭灰、一个强烈主色，以及一个可选的低饱和辅助色。 |
| **TYPOGRAPHY**<br><br>Generate new oversized typography as an abstract graphic element. It may sit behind figures, be cropped by the canvas, partially hidden, vertically arranged, or overlap architecture.<br><br>Do not reproduce titles, logos, or typography from the reference. | **字体**<br><br>重新生成新的超大型字体，把它作为抽象图形元素参与构图。可以置于人物后方、被人物遮挡、被画布裁切、竖向排列，或与建筑重叠。<br><br>不要复制参考图原本的片名、Logo、字体设计或品牌信息。 |
| **COMPOSITION**<br><br>Preserve only the broad visual hierarchy. Rebuild the layout from scratch using asymmetry, large negative space, foreground/background overlap, simplified architecture, and bold geometric structure. | **构图**<br><br>只保留原图的大致视觉层级，具体版式从零重新设计。使用非对称构图、大量留白、人物与字体叠压、前后层次、几何建筑和简洁背景。 |
| **TEXTURE**<br><br>Add paper grain, screen-print ink, Risograph texture, minor ink misregistration, subtle wear, and uneven ink density. | **质感**<br><br>加入纸张颗粒、丝网油墨、Risograph 颗粒、轻微套印偏差、印刷磨损和不均匀墨色。 |
| **FINAL RESULT**<br><br>The image should feel emotionally related to the reference but visually independent from it. It should look like an original collectible vintage editorial poster, not a recreation of an existing movie poster or artwork. | **最终效果**<br><br>最终作品在情绪上可以让人联想到参考图，但视觉设计必须独立。它应该像原创的收藏级复古电影海报或高级编辑插画，而不是原电影海报或作品的复制品。 |

**Copy-ready full prompt / 可直接复制完整版：** [Hosted prompt file](prompts/hosted-original-reinterpretation.md)

</details>

---

## Notes / 使用备注

- 本地模型优先使用 **Local / Open Model** 版本。
- ChatGPT、Gemini 等托管平台优先使用 **Hosted / Guardrail-Friendly** 版本。
- 想保留更多原图构图时，img2img strength 可从 `0.35–0.55` 开始测试。
- 想要更强的风格转译时，可从 `0.55–0.75` 开始测试。
- 如果只是借参考图的情绪和关系做原创，可使用更高的重绘强度。

<details>
<summary><b>Negative Prompt / 负面提示词</b></summary>
<br>

| English | 中文 |
|---|---|
| generic AI art<br>3D render<br>plastic skin<br>photorealistic skin texture<br>neon cyberpunk<br>overly complex background<br>excessive detail<br>random typography<br>cheap advertising<br>glossy digital illustration<br>oversaturated gradients<br>cluttered composition<br>floating decorative objects<br>stock photo aesthetics | 普通AI插画感<br>3D渲染<br>塑料皮肤<br>摄影级皮肤纹理<br>赛博朋克霓虹<br>复杂背景<br>过度细节<br>随机字体<br>廉价广告感<br>光滑数字插画<br>过饱和渐变<br>杂乱构图<br>随机漂浮装饰<br>图库照片感 |

</details>
