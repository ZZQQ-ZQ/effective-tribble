---
name: 构图技能
description: 电影画面构图法则速查系统。20种构图技法（三分法/引导线/对称/框架/负空间/对角线/三角形/黄金比例/景深层次等）+场景→构图匹配表+情绪→构图映射+AI提示词构图关键词。触发：(1) 写分镜时需要构图参考 (2) 导演问构图/画面布局/怎么排 (3) 不确定某个场景用什么构图 (4) 需要把构图指令写入Seedance提示词。
---

# 构图技能

> 景别决定框多大，构图决定框里怎么排。镜头逻辑性选景别→构图技能排画面→运镜术语定动法。
> 创建：2026-07-05 | 全网调研后导演指定

---

## 🔴 核心原则

**构图=画面元素排列。目的三个：**
1. 引导观众视线 → 看到导演想让他们看的
2. 传递情绪信息 → 稳定/不安/压迫/自由
3. 服务叙事 → 构图是视觉语法，不是装饰

**写每镜前先过三问：**
- 主体在画面哪个区域？（三分交叉点？中心？对角线上？）
- 观众视线怎么走？（有引导线吗？前中后景有层次吗？）
- 这个构图的情绪是什么？（平衡=稳定 / 不平衡=紧张 / 留白=孤独）

---

## 一、20种构图法则速查

### A. 基础必用（5种，覆盖80%场景）

| # | 构图法 | 怎么写进提示词 | 适用 |
|---|--------|--------------|------|
| 1 | **三分法** | `subject positioned on left third of frame` / `eyes on upper third line` | 万能基础，人像/风景/对话 |
| 2 | **中心构图** | `centered in frame` / `symmetrical central composition` | 威严/神圣/产品/对称建筑 |
| 3 | **引导线** | `leading lines draw the eye toward [主体]` / `road/path/railings converge on subject` | 纵深/叙事推进/公路/走廊 |
| 4 | **框架构图** | `framed by doorway/archway/window` / `foreground branches frame the subject` | 层次感/偷窥感/聚焦 |
| 5 | **负空间** | `ample negative space around subject` / `isolated against vast empty background` | 孤独/极简/呼吸感 |

### B. 进阶技法（5种，增强视觉张力）

| # | 构图法 | 怎么写进提示词 | 适用 |
|---|--------|--------------|------|
| 6 | **对称构图** | `perfectly symmetrical composition` / `mirrored left and right` | 秩序/仪式感/压迫/库布里克风 |
| 7 | **对角线** | `diagonal composition` / `subject aligned along diagonal axis` | 动感/不稳定/活力/冲突前兆 |
| 8 | **三角形** | `triangular composition, three figures form a triangle` | 稳定/多人/权力结构/对峙 |
| 9 | **黄金比例** | `golden ratio composition, spiral leads to subject` | 自然和谐/高级感/史诗 |
| 10 | **S型曲线** | `S-curve composition, winding path leads through frame` | 韵律/优雅/深远/河流道路 |

### C. 空间层次（3种，构建深度）

| # | 构图法 | 怎么写进提示词 | 适用 |
|---|--------|--------------|------|
| 11 | **前景虚化** | `out-of-focus foreground element, subject sharp in midground` | 空间深度/氛围/遮挡窥视 |
| 12 | **前中后三层** | `distinct foreground, midground, and background planes` | 大景深/史诗/全景交代 |
| 13 | **主体分离** | `shallow depth of field, subject isolated against blurred background` | 特写/情绪聚焦 |

### D. 情绪构图（7种，传递特定感受）

| # | 构图法 | 情绪 | 怎么写进提示词 |
|---|--------|------|--------------|
| 14 | **填充画面** | 压迫/亲密 | `subject fills the entire frame` / `tight close-up filling screen` |
| 15 | **并置对比** | 对立/冲突 | `juxtaposed in frame, contrasting scales` / `tiny figure against colossal structure` |
| 16 | **运动空间** | 动感/方向 | `lead room ahead of moving subject` / `space in direction of movement` |
| 17 | **头顶空间** | 渺小/压迫 | `minimal headroom, cramped framing` / `generous headroom, small in frame` |
| 18 | **图案纹理** | 秩序/催眠 | `repeating pattern fills the frame` / `textured surface composition` |
| 19 | **奇数法则** | 自然和谐 | `three subjects arranged in frame` |
| 20 | **色彩构图** | 情绪引导 | `complementary color composition, warm subject against cool background` |

---

## 二、场景→构图速配表

| 场景类型 | 推荐构图（优先级从高到低） | 为什么 |
|---------|--------------------------|--------|
| 单人特写/近景 | 填充画面 > 中心 > 三分法 | 面部情绪优先，别让环境抢戏 |
| 单人全景/中景 | 三分法 > 引导线 > 负空间 | 人物+环境关系，画面透气 |
| 双人对话（平等） | 三分法（各占一侧） > 对称 > 三角形 | OTS时肩在画框一角，主体在另一侧三分处 |
| 双人对峙（冲突） | 对角线 > 并置对比 > 三角形 | 不稳定感传递火药味 |
| 多人场景（3+人） | 三角形 > 奇数法则 > 三层景深 | 三角稳定结构避免散乱 |
| 人物登场 | 中心构图 > 引导线 > 框架构图 | 宣告式登场，气场最大化 |
| 打斗/动作 | 对角线 > 运动空间 > 引导线 | 动态张力+运动方向留空 |
| 追逐/奔跑 | 运动空间 > 引导线 > 对角线 | 运动方向前方必须有空间 |
| 孤独/离别 | 负空间 > 远景三分 > 前景虚化 | 大环境小人物，留白即情绪 |
| 压迫/被困 | 填充画面 > 头空极小 > 框架构图 | 画面逼仄，没有出路感 |
| 史诗/宏大 | 对称 > 黄金比例 > 前中后三层 | 秩序感+空间纵深 |
| 回忆/梦境 | 前景虚化 > 框架构图 > S型曲线 | 朦胧+画中画的距离感 |
| 建筑/场景空镜 | 对称 > 引导线 > 图案纹理 | 展示空间结构和质感 |

---

## 三、情绪→构图映射

| 想要观众感受 | 构图选择 |
|-------------|---------|
| 稳定/平静/安全 | 对称、三分法、三角形 |
| 紧张/不安/冲突 | 对角线、倾斜、头空极小、并置对比 |
| 孤独/渺小/无力 | 负空间、远景、俯拍+留白 |
| 压迫/被困/窒息 | 填充画面、框架构图（封闭框）、头空极小 |
| 自由/开阔/希望 | 运动空间（前方留空）、引导线（通向远方）、负空间 |
| 威严/权力/支配 | 中心构图、仰拍+对称、三角形（顶点在上） |
| 亲密/脆弱/柔软 | 填充画面（近景特写）、前景虚化、浅景深分离 |
| 神秘/悬疑/未知 | 框架构图（窥视）、前景遮挡、负空间+暗部 |
| 动感/能量/爆发 | 对角线、运动空间、引导线（曲线加速） |

---

## 四、构图+角度+景别三合一决策

写任何一镜时，按这个顺序敲定：

```
1. 先定景别（镜头逻辑性技能）→ 画面框多大
2. 再选构图（本技能）→ 框里怎么排
3. 最后定角度（运镜术语库）→ 从哪个方向拍
```

**三合一速查示例：**

| 场景 | 景别 | 构图 | 角度 | 效果 |
|------|------|------|------|------|
| 英雄登场 | 全景→中景缓推 | 中心构图 | 仰拍低角度 | 气场最大化 |
| 恋人告别 | 近景 | 三分法（偏画左/右） | 平视 | 留白一侧给离去方向 |
| BOSS压迫 | 全景 | 并置对比（BOSS大→角色小） | 低角度仰拍BOSS | 悬殊感 |
| 混战开打 | 全景→中景 | 对角线（动态张力） | 手摇跟拍 | 紧张混乱 |
| 独白回忆 | 近景 | 前景虚化+三分法 | 平视 | 朦胧距离感 |
| 决战一击 | 特写 | 填充画面 | 低角度 | 冲击力爆发 |

---

## 五、构图关键词速查（直接粘进提示词）

```
# 基础
rule of thirds composition
center framed, symmetrical
golden ratio composition
diagonal composition
triangular composition

# 视线引导
leading lines guide the eye toward [subject]
converging lines drawn to focal point
line of sight leads viewer across frame

# 空间层次
distinct foreground, midground, background layers
shallow depth of field, [subject] sharp against blurred background
deep depth of field, everything in focus
out-of-focus foreground frames the scene

# 框架
frame within a frame
viewed through [doorway / archway / window]
foreground [branches / curtains / silhouette] frame the subject
natural frame created by surrounding architecture

# 负空间
generous negative space around [subject]
isolated against vast empty [sky / wall / landscape]
breathing room in composition

# 运动/方向
lead room ahead of moving subject
space in direction of gaze
[subject] positioned on [left/right] third, facing into frame

# 比例/压迫
[subject] fills the frame completely
tight cramped framing, minimal headroom
tiny figure dwarfed by colossal [structure / environment]
juxtaposed scales, [small] against [enormous]
```

---

## 🔴 铁律

1. **构图服务于情绪，不是反过来** — 先确定这段要什么情绪，再选构图
2. **运动方向必须有空间** — 人物朝右看→放画左；人物朝左跑→前方留空
3. **单人对话永远近景/特写，构图用三分法或中心** — 别在对话镜头里搞复杂构图
4. **打架不走中心构图** — 打架=不稳定，中心构图=稳定，两者冲突
5. **俯拍人→负空间情绪** — 俯拍天然削弱人物，别同时用中心构图，矛盾
6. **一段15秒内不要换超过2种构图逻辑** — 构图跳来跳去观众头晕
