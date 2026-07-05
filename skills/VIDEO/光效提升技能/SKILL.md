---
name: 光效提升技能
description: 全维度光效增强与画面质感提升。覆盖人物/道具/服装/背景/镜头的光效设计、31种打光系统、电影感氛围塑造、镜头光学特性、色彩温度控制、空气介质效果。触发条件：(1) 导演要求提升画面光效/质感/氛围 (2) 写提示词时光影描述不够 (3) 需要特定打光风格参考 (4) 新场景需要光效设计 (5) 导演问"有什么光效/灯光/氛围提升技巧"。
---

# 光效提升技能 — 全维度光效增强与电影感塑造

> **创建日期**：2026-06-30
> **来源**：全网搜索整合（即梦Seedance官方/AbleGPT 31种打光/TrueFan 8点镜头语法/AI视频质感提升教程/影视布光6大技巧/阿里云Prompt指南/Midjourney打光体系）
> **与现有体系关系**：本技能与「场景质感增强技能」互补——后者管场景材质真实感（纹理/磨损/凹凸），本技能管全维度光效设计（灯光方向/光质/色彩温度/镜头光学/空气介质）。场景质感 §光影模块 涵盖体积光/阴影层次，本技能进一步扩展为 31种打光系统+景别×光效+色彩温度+空气介质。

---

## 一、画质基准关键词（实测有效·四类）

> 关键词位置影响作用范围：句末→全局质感基线；紧跟物体→仅作用于该物体。

### ① 全局画质
- `电影级画质` > `8K`（8K 在部分模型训练数据中关联过度锐化商业素材→引入塑料感）
- `自然的细节层次` — 比 8K 更柔和耐看
- `超高精度细节` `大师级摄影` `专业电影摄影`

### ② 光影质感
- `电影灯光` `体积光` `柔和阴影` `自然光照明`
- **写法模板**：`[光源方向] + [光源性质] + [空间效果]`
  - ✅ `午后暖金色阳光从左侧树冠缝隙穿透，在空气中形成数道光柱，浮尘粒子缓慢飘动`
  - ❌ `光影好看，灯光很美`（模型听不懂）

### ③ 材质纹理
- `纹理清晰` `哑光质感` `光泽表面` `面料肌理`
- 紧贴物体写：`丝绸高光通透，皮革哑光微磨，金属表面微划痕反射环境光`

### ④ 镜头光学
- `35mm胶片感` `变形宽银幕` `浅景深bokeh` `镜头光晕`
- `anamorphic lens flare` `subtle chromatic aberration` `black pro-mist filter`

---

## 二、31种打光系统（全模板·按场景速查）

### 📐 方向光（8种）

| # | 名称 | 光位 | 效果 | 提示词片段 |
|---|------|------|------|-----------|
| 1 | 正面光 | 镜头同方向正前 | 均匀照亮，无阴影 | `flat frontal lighting, evenly lit face` |
| 2 | 顶光 | 正上方垂直下 | 眼窝/鼻下阴影，压迫感 | `top-down harsh light casting deep eye socket shadows` |
| 3 | 底光 | 下方往上打 | 反派光，诡异/恐怖 | `under-lighting from below, unsettling shadows rising up the face` |
| 4 | 侧光 | 侧面90°打 | 半明半暗，戏剧冲突 | `side lighting splitting the face into lit and shadow halves` |
| 5 | 轮廓光/边缘光 | 后方斜侧 | 人物边缘高亮，与背景分离 | `rim light outlining the figure's edge, separating from the dark background` |
| 6 | 伦勃朗光 | 侧上45° | 一侧脸颊三角光斑 | `Rembrandt lighting with a triangular patch of light under the shadow-side eye` |
| 7 | 蝴蝶光 | 前上45° | 鼻下蝴蝶形阴影，时尚 | `butterfly lighting casting a butterfly-shaped shadow beneath the nose` |
| 8 | 分割光 | 侧面90° | 面部精确一半亮一半暗 | `split lighting, exactly half the face illuminated half in deep shadow` |

### 🌤 氛围光（7种）

| # | 名称 | 色温 | 氛围 | 提示词片段 |
|---|------|------|------|-----------|
| 1 | 金色时刻 | 3200-4000K | 日落前暖金低角度，长影 | `golden hour, warm amber sunlight raking across the landscape, long dramatic shadows` |
| 2 | 蓝色时刻 | 8000-10000K | 日落后冷蓝，静谧 | `blue hour, cool twilight tones, deep indigo sky gradient` |
| 3 | 阴天漫射 | 5500-6500K | 柔和均匀，无硬阴影 | `overcast diffused light, soft shadowless illumination, even tonal range` |
| 4 | 斑驳树影 | 4500-5500K | 阳光透过树叶，光斑跳动 | `dappled sunlight filtering through tree canopy, shifting light patches` |
| 5 | 月光 | 4000-5000K | 冷白银色，夜寂静谧 | `moonlight, cool silvery-blue illumination, pale highlights` |
| 6 | 霓虹双色 | 混合 | 赛博朋克 | `dual-tone neon lighting, warm magenta key + cool cyan rim` |
| 7 | 烛光 | 1800-2200K | 暖橙跳动 | `candlelight, warm flickering amber glow, intimate illumination` |

### 🎬 电影光（6种）

| # | 名称 | 特点 | 提示词片段 |
|---|------|------|-----------|
| 1 | 三点布光 | key+fill+rim，标准电影光 | `three-point lighting setup, key light defining form, fill controlling shadows, rim for separation` |
| 2 | 高调光 | 明亮干净，商业广告 | `high-key lighting, bright clean illumination, minimal shadows` |
| 3 | 低调光 | 暗部主导，悬疑氛围 | `low-key lighting, deep shadows dominating the frame, dramatic contrast` |
| 4 | 明暗对照 | 强对比光影，经典油画感 | `chiaroscuro lighting, dramatic light-shadow contrast, sculptural illumination` |
| 5 | 有源光 | 光有明确来源（窗/灯/火） | `motivated lighting from a visible window source, naturalistic illumination` |
| 6 | 实景光源 | 画面内可见光源 | `practical light visible in frame, diegetic light source illuminating the scene` |

### ✨ 特殊效果光（5种）

| # | 名称 | 特点 | 提示词片段 |
|---|------|------|-----------|
| 1 | 硬光 | 边缘锐利，强对比 | `hard directional light, crisp defined shadows with sharp edges` |
| 2 | 柔光 | 大光源漫射，过渡柔和 | `soft diffused lighting, gentle shadow falloff, smooth tonal transitions` |
| 3 | 体积光/上帝光 | 空气中可见光柱 | `volumetric lighting, visible light beams cutting through the air, god rays` |
| 4 | 轮廓背光 | 人物边缘发亮 | `strong rim backlight outlining the subject, hair catching the edge light` |
| 5 | 发际光 | 发丝背光勾勒 | `hair light creating a luminous halo around the head from behind` |

### 🌫 环境特效光（5种）

| # | 名称 | 效果 | 提示词片段 |
|---|------|------|-----------|
| 1 | 雾霭 | 空气透视，远处朦胧 | `atmospheric haze softening distant details, layered depth through fog` |
| 2 | 浮尘粒子 | 光束中可见微尘 | `dust motes suspended in light beams, particles drifting slowly through the air` |
| 3 | 漏光 | 胶片意外曝光效果 | `film light leak, warm amber streaks bleeding into the frame edges` |
| 4 | 镜头光晕 | 光源直射镜头 | `lens flare, multi-element anamorphic flare streaks across the frame` |
| 5 | 高光溢出 | 亮部柔光扩散 | `bloom effect, highlights softly bleeding into surrounding areas` |

---

## 三、景别 × 光效匹配表

| 景别 | 光效重点 | 写入提示词的关键要素 |
|------|---------|-------------------|
| 极特写 ECU | 虹膜高光/皮肤毛孔/光影过渡 | `iris catchlight, pore-level texture, single soft source` |
| 特写 CU | 面部单侧柔光/伦勃朗三角/发丝背光 | `one-sided soft key, Rembrandt triangle, hair backlight halo` |
| 近景 MCU | 三点布光完整可见 | `three-point visible, key direction clear, fill controlling shadow density` |
| 中景 MS | 人物+环境光影统一/体积光显形 | `subject and environment lit as one, volumetric beams visible` |
| 全景 LS | 丁达尔光柱/大气透视/阴影层次 | `god rays through openings, atmospheric depth, layered shadow planes` |
| 大全景 ELS | 全局光影基调/天空梯度/远景衰减 | `global light direction establishing mood, sky gradient, distant color falloff` |

---

## 四、电影感质感公式

### 核心公式
```
主体 + 场景 + 动作
+ 材质质感（皮肤毛孔/面料肌理/金属反光/物体表面）
+ 光线质感（方向/色温/软硬/体积光/阴影层次）
+ 色彩质感（橙青/褪色胶片/冷暖对比/饱和度层次）
+ 空气质感（雾/尘/大气透视/景深衰减）
+ 镜头运动（固定/跟拍/环绕/推拉/手持）
+ 情绪氛围（宁静/压迫/温暖/冷寂/紧张）
```

### 快速套用模板
```
电影级画质，[XXmm]镜头，[XX光]从[方向]打向[主体]，
在[背景]中形成[光影效果]，空气中有[粒子/雾/尘]缓慢飘动，
[材质]表面反射[光色]，[色彩风格]，浅景深背景虚化，
镜头[运镜方式]，[情绪氛围]
```

### 示例（中级地图户外场景）
```
电影级画质，24mm广角，正午暖金色阳光从左侧树冠缝隙穿透，
在草地上形成斜向丁达尔光柱，光雾中浮尘粒子缓慢上升，
战士铠甲表面反射碎金高光，刀身刃面映出环境碎片，
暖金与翠绿双色对比，浅景深远景森林虚化在光雾中，宁静中带着空旷孤寂
```

---

## 五、分维度光效增强速查

### 🧑 人物
- 皮肤：`保留毛孔纹理` `不磨皮` `自然血色透出` `面部单侧柔光` `伦勃朗三角光斑`
- 眼睛：`虹膜高光点闪烁` `眼神灵动` `缓慢自然眨眼` `眼球轻微转动` `catchlight反射`
- 头发：`根根分明发丝` `粗细错落` `环境反光` `发丝背光高亮` `不结块无团块`
- 微表情：`眉部微弱起伏` `嘴角肌肉微动` `光影塑造面部立体感`
- 光影：`面部固定单侧柔光` `光影稳定不跳动` `明暗塑造五官立体`

### ⚔️ 道具
- 金属武器：`刃面映出环境碎片` `刃缘高光碎斑` `刀身宽厚重量感`
- 金属甲胄：`表面微划痕反射环境光` `磨砂哑光/镜面高光区域对比`
- 系统面板：`半透明蓝色面板` `边框光脉流动` `金字逐行浮现` `辉光映在握刀手背`
- 发光道具：`边缘高亮核心` `光晕向外衰减` `投射光斑到周围表面`

### 👘 服装
- 布料：`面料肌理清晰` `褶皱层次丰富` `光线塑造布料体积` `色彩冷暖层次`
- 丝绸：`高光通透` `光泽流动` `随动作反光位置变化`
- 皮革：`哑光微磨` `边缘磨损露出底色`
- 薄纱：`半透质感` `层叠光影` `透出下层衣料色彩`

### 🏞 背景
- 空气：`大气透视远景色偏蓝` `暖金色光雾` `丁达尔光束斜射`
- 植物：`草叶随机朝向` `叶片正反面双色反光` `露珠微棱镜`
- 地面：`地面纹理不重复` `碎石散落不规则` `泥土微凸凹在光下显阴影`
- 远景：`远树轮廓模糊在光雾中` `色彩饱和度随距离衰减` `天空从暖金到冷蓝梯度`
- 天空：`薄云边缘镀金` `太阳位置决定整体光向` `云隙光`

### 📷 镜头
- 广角(14-24mm)：`人物放大前景开阔` `远景点透视压缩` `边角色散轻微`
- 标准(35-50mm)：`自然透视` `电影感` `浅景深bokeh`
- 长焦(85-135mm)：`背景强力虚化` `空间压缩` `主体与背景分离`
- 变形宽银幕：`水平光晕拉丝` `椭圆bokeh` `独特炫光`
- 滤镜：`黑柔滤镜柔化高光` `ND减光保留天空层次`

---

## 六、色彩温度控制

| 光源 | 色温 (K) | 色调 | 场景 |
|------|---------|------|------|
| 烛光 | 1800-2200 | 暖橙 | 古堡/山洞/夜晚室内 |
| 日出日落 | 2500-3500 | 金橙 | 金色时刻/浪漫/怀旧 |
| 正午阳光 | 5000-5500 | 白 | 晴天户外 |
| 阴天 | 6000-6500 | 微冷 | 柔和漫射 |
| 蓝天阴影 | 7000-8000 | 冷蓝 | 阴影区 |
| 月光 | 4000-5000 | 冷银 | 夜景 |
| 霓虹灯 | 混合 | 多色 | 赛博朋克/都市夜 |

**色彩对比公式**：
- `暖色主体 + 冷色背景` → 人物突出
- `橙肤色 + 青阴影` → 好莱坞橙青调
- `高饱和高光 + 低饱和阴影` → 立体层次
- `单一色温 + 互补色点缀` → 氛围统一但不过分单调

---

## 七、快速检查清单

写出光影描述后，逐条勾：

```
[ ] 光源方向是否明确？（左/右/上/下/前/后 斜侧？）
[ ] 光源色温是否合理？（日/夜/室内/烛光 对应 K 值？）
[ ] 光质是硬是柔？（点光源→硬，大面光源→柔）
[ ] 有没有体积光？（树冠/窗/门缝→光柱）
[ ] 有没有空气介质？（雾/尘/烟→可见光路）
[ ] 人物身上有没有对应光影？（受光面+阴影面+轮廓光）
[ ] 道具表面有没有环境反光？（金属→反射，布料→吸收）
[ ] 景别与光效匹配吗？（特写→面部光影，全景→全局光向）
[ ] 阴影层次清晰吗？（近深远浅，不糊成一团黑）
[ ] 有没有镜头光学质感？（光晕/bokeh/色散/柔焦？）
```

---

## 八、组合增效（与其他技能协作）

| 搭配技能 | 协同方式 |
|---------|---------|
| 场景质感增强技能 | 本技能管光，场景质掌管材质纹理→光打在材质上才好看 |
| 人物服装增强技能 | 本技能管全局光影，人物服装管皮肤/眼睛/头发/布料→光影＋材质=人物逼真 |
| camera-terminology | 本技能提供光效，运镜术语提供镜头运动→光和镜头一起设计 |
| 场景一致性保持技能 | 本技能提供光效锚定词→连续镜头中光效一致 |
| 打斗设计技能 | 本技能提供碰撞光效/能量光效/脏镜弧线→战斗场面光效设计 |

---

## 九、即梦/Seedance 光效提示词实例

### 户外森林场景
```
电影级画质，35mm变形宽银幕，正午暖金色阳光从左侧高大树冠缝隙穿透，
在草地上投下斜向丁达尔光柱，光雾中浮尘粒子缓慢上升飘动，
战士铠甲表面反射碎金高光，刀身刃面映出环境碎片，
暖金阳光与翠绿草地形成强烈色彩对比，浅景深远景森林虚化在光雾中，
地平线处天空从暖金过渡到淡蓝，宁静中带着空旷孤寂
```

### 战斗场景
```
电影级画质，手持跟拍，侧逆硬光从画右上方斜射战场，
体积光穿透扬起的尘土形成分层光幕，铠甲反光随动作闪烁跳跃，
刀刃碰撞瞬间产生碎芒四溅，火星在高光区拖出短弧线，
暖橙火花与冷蓝刀光双色交织，镜头脏镜弧线划过画面
```

### 室内人物特写
```
电影级画质，85mm长焦镜头，单侧柔光从右侧窗斜射人物面部，
形成伦勃朗三角光斑在左侧颧骨下，眼窝阴影深邃眼神有光，
发丝背光勾勒金色轮廓，皮肤毛孔纹理在亮面保留暗面柔和过渡，
背景虚化为暖色bokeh光斑，浅景深，f/1.8
```

---

## 十二、深度美学约束（GitHub MapleShaw 补充 · 2026-07-01）

> **来源**：MapleShaw/seedance2.0-prompt-skill aesthetic-constraints.md
> **核心理念**：让每一帧都对标 Octane/V-Ray/Arnold 级别渲染品质。

### 渲染品质三档

**基础版（20字）**：`Octane渲染品质，全局光照，材质细节真实，物理正确光影`

**进阶版（50字）**：`Octane render quality, GI, physically accurate lighting, SSS skin detail, micro-surface imperfections, anisotropic highlights, volumetric atmosphere, cinematic lens flare`

**极致版（80字）**：`对标Octane/V-Ray渲染品质，GI全局光照，物理正确光线衰减，皮肤次表面散射，金属各向异性高光微划痕，体积光丁达尔效应，真实焦散，ACEScg色彩空间，运动模糊物理准确，景深散景真实光学模拟`

### 六组冷暖色调

| 色调 | 冷色(暗部) | 暖色(亮部) | 情绪 | 场景 |
|------|-----------|-----------|------|------|
| 赛博霓虹 | 深空蓝+电光紫 | 霓虹红+能量橙 | 紧张→爆发 | 科技/夜间 |
| 极简白金 | 苹果白+铂金灰 | 金色+炭黑 | 宁静→聚焦 | 奢侈品 |
| 冰火对冲 | 深海蓝+钴蓝 | 烈焰红+橙黄 | 对峙→冲突 | 对决/竞技 |
| 赛博冷调 | GitHub暗+碳灰 | 冰蓝+矩阵绿 | 冷静→渗透 | 黑客 |
| 暮光渐变 | 暮紫+深青 | 落霞粉+暮金 | 舒缓→回味 | 情感/MV |
| 极简黑白 | 纯黑 | 纯白+点缀色 | 克制→冲击 | 先锋艺术 |

### 材质微观（6种）

- **金属**：各向异性高光+微划痕+真实反射
- **皮肤**：毛孔+次表面散射SSS+微血管
- **玻璃**：色散彩虹+焦散+折射率IOR 1.52
- **织物**：纤维级编织+绒毛+光散射
- **液体**：弯月面+粘度+飞溅物理
- **塑料/树脂**：多层涂层+底层颗粒+清漆反射

### 极简构图五法则

1. **减法优先**：画面元素≤3个
2. **强对比分割**：冷暖色温分割叙事节奏
3. **呼吸留白**：至少30%负空间
4. **几何锚点**：对角线或几何中心锚定重心
5. **层次递进**：前景(虚)→中景(实)→背景(虚)

### 垂直场景美学速查

| 项目 | 渲染 | 色调 | 构图 | 材质 |
|------|------|------|------|------|
| 科技产品 | Octane极致 | 赛博霓虹/极简白金 | 减法+几何锚点 | 金属/玻璃 |
| 品牌故事 | V-Ray进阶 | 暮光渐变/极简黑白 | 留白+层次 | 皮肤/织物 |
| 游戏角色 | Octane极致 | 冰火对冲/赛博霓虹 | 对比分割+对角线 | 金属甲/SSS |
| 时尚奢侈 | V-Ray极致 | 极简白金/黑白 | 减法+30%留白 | 织物/液体 |
| 赛博MV | Octane极致 | 冷调+霓虹 | 强对比分割 | 金属/玻璃 |
| 情感短片 | Arnold进阶 | 暮光渐变 | 留白+层次 | 皮肤/自然 |

### 光影三层叠加法

`[光源] + [光行为] + [色调]`

例：`夕阳侧逆光 + 穿透树叶形成丁达尔光束 + 暖金色调暗部深橄榄绿冷色`
