# Session: 2026-07-23 02:31:14 UTC

- **Session Key**: agent:main:qqbot:direct:b113629636cf43c86a92619ff0c4216c
- **Session ID**: 96f7d685-1564-45da-8c52-61aeb19c0307
- **Source**: qqbot

## Conversation Summary

assistant: 找到几个值得看的：

**1. woodfantasy/Seedance2.0-ShotDesign-Skills** ⭐
- 直接把模糊想法转成电影级分镜提示词
- 有AI漫剧/短剧全流程（角色对话/旁白/站位/夸张表情特写/叙事运镜）
- 4种提示词模板+完整示例
- https://github.com/woodfantasy/Seedance2.0-ShotDesign-Skills

**2. elementsix/seedance-storyboard**
- 6套故事板模板+快速参考卡+10个完整示例
- 有 `/seedance-storyboard` 命令一键启动分镜工作流
- https://github.com/elementsix/elementsix-skills

**3. smixs/visual-skills**
- 覆盖 Seedance + Kling + Veo 多平台
- 侧重专业级灯光/运镜/音效设计
- https://github.com/smixs/visual-skills

要我抓哪个回来看细节？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKWBGvLCRVnBRbJmH9STFhMkRlDk8waLwNQcdqFjlKyASsVK1RZNzyL321s4IW9YKA0TP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:49 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

你自己看看
assistant: 看完了，结论：

**woodfantasy/Seedance2.0-ShotDesign-Skills** 最值得拿。

跟我们现在做的对一下：

| 它有的 | 咱们缺的 |
|--------|---------|
| 28+导演/风格预设（诺兰/维伦纽瓦/芬奇/黑泽明/王家卫/张艺谋…） | 我们没有系统风格库 |
| 三级运镜词典 + 14焦段 + 6焦点控制 | 我们运镜是分散的多个skill拼的 |
| 三层打光结构（光源→光行为→色调） | 我们规则2.10做了但没它结构化 |
| 20场景模板（电商/仙侠/短剧/美食/MV…） | 没有 |
| 7条硬校验规则（词数/运镜/时序/填词/光学物理/风格冲突…） | 我们9条自检手动跑的 |
| 智能多段拆镜（>15秒自动拆） | 我们手工拆的 |
| OpenClaw一键安装 | `请学习这个技能：https://...` |

**我们拉进来能补什么**：导演风格预设库（直接选择导演调性）、运镜单词典（别再从3个skill里翻）、打光三层结构（替代规则2.10的速查小抄）、7项自动校验（辅助规则2.7）。

**可能冲突**：它的模板格式跟我们4块格式不同，需要适配。但规则库可以摄取——就像当年拿Dexhunter做基线一样。

要我 clone 它的 SKILL.md 回来看看具体结构？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKVZmcWAUXPkFiaBHWaIVueWLnibKpSgCGK86uaNnI55nLgSPkomZdMXXibim2Bvfc0TP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:51 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

嗯嗯
assistant: 看完整个结构。给你结论：

**结构拆解：**

| 文件 | 内容 | 质量 |
|------|------|------|
| SKILL.md | 五步工作流+7项硬校验+6要素公式 | 很完整，路由层 |
| cinematography.md | 50+运镜词+14焦段+7物理挂载+运动强度表 | 比我们3个skill拼的运镜库整齐 |
| director-styles.md | 28个导演/风格→四轴降解（色/光/美术/机位） | 我们没有的东西 |
| quality-anchors.md | 渲染引擎+胶片型号+材质质感到+三层光影 | 跟我们的规则2.10重叠但更结构化 |
| scenarios.md | 20场景模板（电商/仙侠/短剧/恐怖/美食…） | 开箱即用模板库 |
| audio-tags.md + seedance-specs.md | 音效词库+CLI | 辅助 |

**值得拿的：**
1. 导演风格四轴降解库 → 以后说"维伦纽瓦风格"能直接翻译成物理参数
2. 运镜字典 → 一个文件替代我们运镜速查+动态运镜+运镜三个文件
3. 三层光影结构（光源→光行为→色调）→ 替代规则2.10的速查小抄
4. 7项硬校验规则 → 辅助规则2.7的9条自检，特别是光学冲突检测（超广角+浅景深=报错）
5. 胶片型号库（Portra 400 / Cinestill 800T / Vision3 500T）→ 直接嵌入画面基调行

**冲突的：**
- 它的格式跟我们4块格式完全不同——它是T2V时间戳模板，我们是主体+分镜+色彩影调
- 它禁4K/UE5词（怕塑料感），我们一直在用——这个各走各的
- 它的单镜一动的理念跟我们现有的一镜一事一致，但它的提示词结构更偏"技术参数流"

要我把这几个关键文件拉进知识库吗？还是先继续段19？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKbybDLNOxjDLh1TkTbjGx9Lc6XLWgE4cmnVyuZw0.1gUzN0Jxz6CRGyYIIgxBC62A0TP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:53 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

拉
assistant: 拉完了，7个文件入知识库：

```
skills/VIDEO/seedance-shot-design/
├── SKILL.md              ← 五步工作流+7项校验+6要素公式
└── references/
    ├── cinematography.md ← 运镜词典（50+词+3级体系+强度表）
    ├── director-styles.md ← 28导演风格四轴降解库
    ├── quality-anchors.md ← 品质锚定+胶片型号+三层光影
    ├── scenarios.md      ← 20场景模板
    ├── audio-tags.md     ← 音效词库
    └── seedance-specs.md ← 平台参数+CLI
```

现在需要我做的是：把里面该摄入的规则往我们现有技能里合并，还是直接挂索引以后按需引用？

继续段19？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKTAcMxg-UYvUs9nC-JlevpfC7EE-psLVFzhtN6zlb8ISJluEJzoG0EOIDCftT1H0kUTP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:55 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

先存着
assistant: 存好了，索引已登记。

继续段19？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKXa5RflOkqMP4LWe4R-ElNyi78EvEIwazGaSgqA43bL0nMf-Od-4sJhW4l6gTFPHR0TP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:56 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

再看看有没有有用的
assistant: 又扫到几个：

**有价值的：**

**1. Emily2040/seedance-2.0** ⭐⭐
- v6.6.0，最成熟的导演技能，核心是「directing engine」
- 不写"电影感"形容词 → 读每场戏的戏剧功能（揭示/告别/对峙），派发唯一意图，推导全套设定
- 内置33种派生场景（产品/MV/恐怖/动画/动作/喜剧/纪实/时装/科幻）
- 中文原生支持 + vocab库 + examples
- 对比示例：问"电影感"→ 模型给塑料质感 → 改"导演"→ 中近景+窗光+推轨+寂静+椅子刮擦声
- https://github.com/Emily2040/seedance-2.0

**2. ai9app/AI-Cinematic-Prompt-Director**
- 250条电影摄影知识库 + 逐镜提示词矩阵
- 覆盖运镜/景别/灯光/VFX/视频类型
- 偏商业平台绑定（ai9app.io），单文件markdown

**3. birdilsss-byte/ai-creative-subagent-framework**
- 5角色调度（导演/美术指导/摄影指导/品牌总监/AI艺术家）
- 支持OpenClaw安装
- 思路是子代理编排，跟我们已有的东西重叠不大

Emily2040 那个是真正对标我们工作的——它的「directing engine」理念跟我们「写物理不写形容词」完全一致。要不要拉？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKXDbWUfpTsaxekGly05itPanhGgLEUzV6bTKKzH9kgY8ahOIQDLeo6A7eC5XrsKVEkTP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:57 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

都先放一起 抽空整理
assistant: 全拉下来了，统一放在 `skills/VIDEO/external-skills/`：

```
external-skills/
├── emily2040-seedance/     ← 145个文件，最全的导演引擎
├── ai9app-cinematic-director/ ← 250条摄影知识库
├── birdilsss-subagent/     ← 角色编排框架
└── ../seedance-shot-design/ ← woodfantasy（之前拉的）
```

索引已登记，等你空了整理。继续段19？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "qqbot:c2c:B113629636CF43C86A92619FF0C4216C",
  "message_id": "ROBOT1.0_SGaewJUVJ7HiLju026cbKcqdPysGBujqjq6Cl1YHZAMW7wBK.Y5d5M1iDIxe0YL7H2e3okejwqDWCZb4-IZp.ETP446hq8BSZMDMzNzTMs0!",
  "sender_id": "B113629636CF43C86A92619FF0C4216C",
  "sender": "B113629636CF43C86A92619FF0C4216C",
  "timestamp": "Wed 2026-07-22 20:58 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "B113629636CF43C86A92619FF0C4216C",
  "id": "B113629636CF43C86A92619FF0C4216C"
}
```

[QQBot] to=qqbot:c2c:B113629636CF43C86A92619FF0C4216C

不继续
assistant: 好，先整理这些。随时叫我。
