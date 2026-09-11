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

# Prompt Pack / 提示词正文

> **Copy the prompt below and use it directly.**  
> **下面的提示词可以直接复制使用。**

---

# 1) Local / Open Model
## Maximum Reference Fidelity
### 本地 / 开源模型版（最大化参考图忠实度）

适用于 FLUX、Qwen Image、SDXL、ComfyUI 等本地 / 开源工作流。  
这版优先保留参考图的构图、人物关系、动作、镜头方向和视觉重心。

### English Prompt

```text
Transform the provided reference image into a sophisticated mid-century modern editorial poster.

Preserve the important visual information of the reference image, including:

- number of subjects
- subject relationships
- recognizable pose and gesture
- camera angle
- framing
- visual hierarchy
- dominant color relationships
- major clothing silhouettes
- important props
- emotional tone
- spatial relationships between subjects

Do not simply apply a filter.

Reconstruct the entire image as a designed graphic poster.

VISUAL LANGUAGE

Use a combination of:

- mid-century modern poster design
- European editorial illustration
- vintage cinema poster design
- screen-print graphics
- risograph texture
- 1960s–1970s magazine illustration

CHARACTER RENDERING

Convert people into elegant graphic illustrations using:

- sharp geometric facial planes
- simplified anatomy
- elongated proportions
- strong silhouettes
- angular shadows
- large flat color areas
- restrained facial details
- expressive but controlled gestures

Maintain enough identifying visual characteristics for the subject to remain recognizable when appropriate.

Avoid photographic skin texture.

COLOR SYSTEM

Preserve the dominant color identity of the original image, but reinterpret it using a restricted poster palette.

Preferred palette structure:

- 1 dominant color
- 1 dark structural color
- 1 light paper color
- 1–2 optional accent colors

Common combinations:

- scarlet red / black / warm cream
- slate blue / charcoal / ivory
- dark green / burgundy / warm beige
- mustard / black / parchment

Avoid unnecessary gradients.

TYPOGRAPHY

Introduce oversized editorial typography into the composition.

Typography should behave as a graphic object rather than normal text.

Use:

- oversized serif or sans-serif letters
- cropped characters
- partially hidden letters
- vertical typography
- typography behind people
- typography overlapping architecture
- letters extending outside the canvas

Text may be abstract or derived from the image concept.

Do not overcrowd the poster with text.

COMPOSITION

Use bold asymmetrical composition.

Create strong foreground/background relationships.

Allow figures to overlap typography.

Use negative space aggressively.

Simplify secondary architecture, furniture and environment into geometric shapes.

Remove visual clutter that does not contribute to the composition.

TEXTURE

Add authentic analog printing imperfections:

- paper grain
- aged paper texture
- screen-print ink
- risograph texture
- subtle ink bleeding
- uneven ink density
- slight registration offset
- printed edge wear
- subtle halftone texture

The image should feel physically printed rather than digitally rendered.

FINAL LOOK

The finished result should feel like a collectible vintage film poster or editorial illustration produced by an elite graphic designer.

Elegant.
Minimal.
Cinematic.
Graphic.
Tactile.
Timeless.

Avoid:

- generic AI illustration
- glossy 3D rendering
- plastic skin
- over-detailed backgrounds
- excessive gradients
- neon cyberpunk colors
- random decorative elements
- unnecessary text
- modern advertising aesthetics
```

### 中文提示词

```text
将输入参考图片重新设计成一张高级的复古现代主义编辑海报。

尽可能保留原图重要的视觉信息，包括：

- 人物数量
- 人物之间的关系
- 主要动作和姿势
- 镜头角度
- 构图
- 视觉重心
- 主色关系
- 服装主要轮廓
- 关键道具
- 情绪
- 人物之间的空间关系

不要简单给原图套滤镜。

需要重新设计整张图片，使其真正成为一张平面设计海报。

【视觉语言】

融合：

- 20世纪中叶现代主义海报
- 欧洲编辑插画
- 复古电影海报
- 丝网印刷
- Risograph孔版印刷
- 1960–1970年代杂志插画

【人物绘制】

将人物重新绘制成高级平面插画：

- 锐利的几何面部切面
- 简化的人体结构
- 修长人物比例
- 强烈人物剪影
- 大块明暗关系
- 大面积平涂色块
- 克制的五官细节
- 有表现力但不夸张的动作

在适当情况下保留足够的人物识别特征。

避免真实摄影式皮肤纹理。

【配色】

尽可能保留原图的主要色彩关系，但重新归纳为有限色海报配色。

推荐结构：

- 1个主色
- 1个深色结构色
- 1个浅色纸张色
- 1–2个辅助色

例如：

- 朱红 / 黑 / 暖米白
- 灰蓝 / 炭黑 / 象牙白
- 深绿 / 酒红 / 暖米色
- 芥末黄 / 黑 / 旧纸色

避免不必要的渐变。

【字体】

加入具有编辑设计感的超大型字体。

字体不是普通信息文字，而应该作为画面中的图形元素。

可以使用：

- 超大衬线字体
- 超大无衬线字体
- 被画面裁切的字母
- 被人物遮挡的字体
- 竖排字体
- 位于人物后方的字体
- 与建筑发生重叠的字体
- 延伸到画布之外的字体

文字可以根据图片主题重新生成，也可以只作为抽象图形。

不要加入过多文字。

【构图】

采用大胆的非对称构图。

强调人物、文字、背景之间的前后关系。

允许人物覆盖字体。

大胆使用留白。

将次要建筑、家具和环境简化成几何剪影和色块。

删除不会增强画面表达的复杂背景元素。

【印刷质感】

加入真实模拟印刷效果：

- 纸张颗粒
- 老纸纹理
- 丝网印刷油墨
- Risograph颗粒
- 轻微油墨扩散
- 不均匀墨色
- 轻微套色偏移
- 印刷边缘磨损
- 轻微网点

画面应该像真实印刷品，而不是纯数字生成图片。

【最终效果】

最终作品应该像一张收藏级复古电影海报，或者高级杂志编辑插画。

高级。
克制。
电影感。
平面化。
有触感。
不过时。

避免：

- 普通AI插画感
- 塑料3D质感
- 假皮肤
- 过度复杂背景
- 大量渐变
- 赛博朋克霓虹色
- 随机装饰
- 无意义小字
- 廉价商业广告感
```

---

# 2) Hosted / Guardrail-Friendly
## Original Reinterpretation
### 托管平台版（原创重构）

适用于 ChatGPT、Gemini 等存在第三方相似性保护的平台。  
这版不是直接“照着原图改”，而是先提取高层信息，再原创重构。

### English Prompt

```text
Analyze the provided reference image only for its high-level visual structure.

Extract:

- number of subjects
- emotional relationship
- dominant mood
- broad pose direction
- camera orientation
- visual hierarchy
- dominant color relationships
- negative-space distribution
- general subject placement

Do not recreate the original artwork.

Create a completely new and original poster inspired only by these high-level characteristics.

If the reference contains recognizable actors, characters, movie posters, brands, logos, costumes, makeup, typography or protected visual identities, replace them with original equivalents.

Create new:

- faces
- hairstyles
- wardrobe details
- props
- background environment
- typography
- title
- graphic elements

while preserving the broad emotional and compositional logic.

Now reinterpret the scene using the CINEGRAPHIC visual system.

STYLE

- mid-century modern editorial poster
- European graphic illustration
- vintage cinema design
- screen-print aesthetics
- risograph texture
- 1960s–1970s editorial graphics

CHARACTERS

Use elegant geometric character rendering:

- sharp facial planes
- angular shadows
- simplified anatomy
- elongated proportions
- strong silhouettes
- large flat color fields

COLOR

Use a restricted 3–5 color palette.

Preserve the broad color relationship of the reference, not its exact colors.

Prefer:

- warm cream paper
- deep black or charcoal
- one strong dominant color
- one optional muted accent color

TYPOGRAPHY

Use newly generated oversized typography as an abstract graphic element.

Typography may appear:

- behind figures
- cropped by the canvas
- partially hidden
- vertically arranged
- overlapping architecture

Do not reproduce titles, logos or typography from the reference.

COMPOSITION

Preserve only the broad visual hierarchy.

Rebuild the layout from scratch.

Use:

- asymmetry
- large negative space
- foreground/background overlap
- simplified architecture
- bold geometric structure

TEXTURE

Add:

- paper grain
- screen-print ink
- risograph texture
- minor ink misregistration
- subtle wear
- uneven ink density

FINAL RESULT

The image should feel emotionally related to the reference, but visually independent from it.

It should look like an original collectible vintage editorial poster, not a recreation of an existing movie poster or artwork.
```

### 中文提示词

```text
首先只分析输入参考图片的高层视觉信息。

提取：

- 人物数量
- 人物之间的情绪关系
- 整体氛围
- 大致动作方向
- 镜头方向
- 视觉层级
- 主色关系
- 留白分布
- 主体在画面中的大致位置

不要直接重制原作品。

根据这些高层信息，从零设计一张完全原创的新海报。

如果参考图片包含：

- 演员
- 影视角色
- 电影海报
- 品牌
- Logo
- 标志性服装
- 标志性妆容
- 特殊字体
- 或其他容易识别的第三方视觉元素

请自动将其替换为原创设计。

重新设计：

- 人物面孔
- 发型
- 服装细节
- 道具
- 背景
- 字体
- 标题
- 图形元素

但尽可能保留原图：

- 情绪关系
- 人物数量
- 叙事逻辑
- 整体视觉重心

然后将整个场景重新设计为 CINEGRAPHIC / 电影图形主义风格。

【风格】

- 20世纪中叶现代主义编辑海报
- 欧洲平面插画
- 复古电影海报
- 丝网印刷
- Risograph孔版印刷
- 1960–1970年代编辑设计

【人物】

使用几何化高级人物插画：

- 锐利面部切面
- 大块阴影
- 简化人体结构
- 修长比例
- 强剪影
- 大面积平涂

【颜色】

使用3–5种限制性色彩。

只保留参考图的大致颜色关系，不要精确复制颜色。

推荐：

- 暖米白纸张
- 深黑或炭灰
- 一个强烈主色
- 一个可选的低饱和辅助色

【字体】

重新设计新的大型字体作为画面图形元素。

可以：

- 置于人物后方
- 被人物遮挡
- 被画布裁切
- 竖向排列
- 与建筑重叠

不要复制参考图片原本的：

- 片名
- Logo
- 字体设计
- 品牌信息

【构图】

只保留原图的大致视觉层级。

重新设计具体版式。

使用：

- 非对称构图
- 大量留白
- 人物与字体叠压
- 前后层次
- 几何建筑
- 简洁背景

【质感】

加入：

- 纸张颗粒
- 丝网油墨
- Risograph颗粒
- 轻微套印偏差
- 印刷磨损
- 不均匀墨色

【最终效果】

最终作品在情绪上可以让人联想到参考图，但视觉设计必须是一张独立的新作品。

它应该像：

- 收藏级复古电影海报
- 高级编辑插画
- 真正印刷出来的平面设计作品

而不是原电影海报的复制品。
```

---

## Notes / 使用备注

- 本地模型优先使用 **Local / Open Model** 版本。
- ChatGPT、Gemini 等托管平台优先使用 **Hosted / Guardrail-Friendly** 版本。
- 想保留更多原图构图时，img2img strength 可从 `0.35–0.55` 开始测试。
- 想要更强的风格转译时，可从 `0.55–0.75` 开始测试。
- 如果只是借参考图的情绪和关系做原创，可使用更高的重绘强度。

---

## Negative Prompt / 负面提示词

### English

```text
generic AI art,
3D render,
plastic skin,
photorealistic skin texture,
neon cyberpunk,
overly complex background,
excessive detail,
random typography,
cheap advertising,
glossy digital illustration,
oversaturated gradients,
cluttered composition,
floating decorative objects,
stock photo aesthetics
```

### 中文

```text
普通AI插画感，
3D渲染，
塑料皮肤，
摄影级皮肤纹理，
赛博朋克霓虹，
复杂背景，
过度细节，
随机字体，
廉价广告感，
光滑数字插画，
过饱和渐变，
杂乱构图，
随机漂浮装饰，
图库照片感
```
