# Session: 2026-07-07 08:04:32 UTC

- **Session Key**: agent:main:telegram:direct:7584677982
- **Session ID**: 02d6a4ab-4139-462a-bea2-9147e9ac2a4b
- **Source**: telegram

## Conversation Summary

assistant: 完成。总结：

---

**违禁词三套 → 一套统一**

| 操作 | 文件 | 结果 |
|------|------|------|
| 删除 | `references/sensitive-words-guide.md` | 旧·6类·2026-03-30 |
| 保留 | `prohibited-word-audit/SKILL.md` | 升级至 v1.2·标注归档历史 |
| 保留 | `prohibited-word-audit/references/word-list.md` | 不变·11类·已完整覆盖 |

**连带修复**
- `VIDEO/SKILL.md` → v2.0，补充 7 个新增子技能索引 + 多人打斗站位
- `workflows/prompt-generation-workflow.md` → 死链修复，指向新路径
- 5 文件变更，净删除 306 行冗余

**仓库已同步** → `github.com/albert20260208/zhouqiang.git` master

现在违禁词系统只有一个入口：`skills/VIDEO/prohibited-word-audit/SKILL.md`，每次出稿前 SOUL.md 四道门流程已引用。
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "telegram:7584677982",
  "message_id": "147",
  "sender_id": "7584677982",
  "sender": "ahai",
  "timestamp": "Mon 2026-06-29 18:32 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ahai (7584677982)",
  "id": "7584677982",
  "name": "ahai",
  "username": "ahaius"
}
```

把技能英文改成中文，并仓库同步
assistant: 先搜全所有引用链，然后改名。
assistant: 需要改 10 个文件。先重命名目录，再批量替换引用。
assistant: 所有引用已定位。批量替换全部 10 个文件。
assistant: 零残留。验证改名后的文件完整性。
assistant: 完成。

- `prohibited-word-audit` → `违禁词审查技能`
- 10 个文件引用路径全量替换，零残留
- 仓库已同步
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "telegram:7584677982",
  "message_id": "153",
  "sender_id": "7584677982",
  "sender": "ahai",
  "timestamp": "Mon 2026-06-29 18:35 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ahai (7584677982)",
  "id": "7584677982",
  "name": "ahai",
  "username": "ahaius"
}
```

references/four-wall-scene-method.md 这个删除，
assistant: 已删除 `references/four-wall-scene-method.md`（净减 252 行），`workflows/prompt-generation-workflow.md` 引用链已更新到 `场景一致性保持技能`。已同步。

> ⚠️ `skills/prompt-optimizer/` 下也有 3 处旧引用，需要一并切过去吗？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "telegram:7584677982",
  "message_id": "155",
  "sender_id": "7584677982",
  "sender": "ahai",
  "timestamp": "Mon 2026-06-29 18:36 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ahai (7584677982)",
  "id": "7584677982",
  "name": "ahai",
  "username": "ahaius"
}
```

目前各个工作流分布文档位置，然后仔细查看下内容，分类告诉我
assistant: 全部读完。以下是完整分类：

---

# 📊 工作流文档全景（19个文件·5个位置）

## 一、当前实际在用 🟢（3个·根目录·权威）

| # | 文件 | 角色 | 内容 |
|---|------|------|------|
| 1 | `PROMPT_FORMAT.md` | **5层格式底板** | 含 `1.【要求】` 头、头发/皮肤/布料/景深/UE5 全量写法、角色质感尾缀、结尾 avoid 行。每次出提示词前强制对照 |
| 2 | `PROMPT_WORKFLOW.md` | **四道门出稿流** | 门0（沟通铁律·导演说"发"）→ 门1（查数据库）→ 门2（写前锁定·格式/图号/场景）→ 门3（写完自检·13条）→ 门4（发前最终对比）。跳一步=废稿 |
| 3 | `SELF_CHECK.md` | **逐条自检清单** | 四阶段：空间逻辑推演→每镜景别/角度匹配→180度轴线/物理连续性→全段时长/格式/违禁词。全过才发 |

> 三者已锚定在 `SOUL.md` 强制执行机制中。这是**唯一实际在用**的出稿流程。

---

## 二、skills/VIDEO/ 下（4个·新旧混存）

| # | 文件 | 创建 | 状态 | 内容 |
|---|------|------|------|------|
| 4 | `references/workflow-index.md` | 贾维斯 2026-02-25 | 🔴 废弃 | 6阶段制作流程（需求→故事→分镜→镜头→提示词→质检），互动型（问海哥给出选项），引用贾维斯旧知识库 |
| 5 | `references/5agent-workflow.md` | 贾维斯 2026-02-25 | 🔴 废弃 | 5Agent固定角色（编剧/建模师/导演/摄影师/场记），使用旧模型（deepseek-reasoner/MiniMax-M2.5）和旧API（seedance-1.5-pro） |
| 6 | `workflows/prompt-generation-workflow.md` | 2026-03-30 | 🔴 废弃 | 4阶段调用清单（故事→视觉→场景→生成），引用大量已不存在的文件路径（如 编剧/screenwriting.md、场景人物道具/xxx）。与 prompt-optimizer 版完全相同 |
| 7 | `workflows/short-drama-workflow.md` | 2026-03-30 | 🟡 参考 | 短剧6阶段制作（剧本→分镜→角色→场景→视频→后期），含霸总甜宠示例、Seedance v1.5 参数。格式/规格已过时，但结构框架仍有参考意义 |

---

## 三、skills/prompt-optimizer/ 下（3个·独立体系）

| # | 文件 | 状态 | 内容 |
|---|------|------|------|
| 8 | `workflows/prompt-generation-workflow.md` | 🔴 废弃 | **与 VIDEO/workflows/ 第6号完全相同**。4阶段流程，死链相同 |
| 9 | `workflows/short-drama-workflow.md` | 🟡 参考 | **与 VIDEO/workflows/ 第7号几乎相同**。6阶段短剧流程 |
| 10 | `workflows/standard-workflow.md` | 🟢 独立存活 | 通用提示词优化6步闭环：确认模型→分析需求→生成3版本→收集反馈→深度分析→学习进化。非视频专用，是**独立于视频体系的通用优化技能** |

---

## 四、skills/video-production-5agent/ 下（2个·全量重复）

| # | 文件 | 状态 | 内容 |
|---|------|------|------|
| 11 | `references/5agent-workflow.md` | 🔴 重复 | 与 VIDEO/references/5agent-workflow.md（#5）完全相同。贾维斯旧版 |
| 12 | `references/workflow-index.md` | 🔴 重复 | 与 VIDEO/references/workflow-index.md（#4）完全相同。贾维斯旧版 |

---

## 五、空目录

| # | 位置 | 状态 |
|---|------|------|
| 13 | `skills/short-drama-production/workflows/` | 目录存在但为空 |

---

## 总结

| 分类 | 数量 | 结论 |
|------|------|------|
| 🟢 **当前在用（权威）** | 3 | `PROMPT_FORMAT` + `PROMPT_WORKFLOW` + `SELF_CHECK` |
| 🟢 **独立存活（无冲突）** | 1 | `prompt-optimizer/workflows/standard-workflow.md` |
| 🔴 **废弃/死链+重复** | 7 | #4 #5 #6 #8 #11 #12（可删） |
| 🟡 **过时但有参考价值** | 2 | #7 #9（短剧制作框架可保留） |

**核心矛盾**：根目录的 3 个流程文件（四道门体系）是唯一实际执行的出稿标准，但 VIDEO/ 下仍保留着贾维斯时代的 4 套旧流程，路径全部失效、API 版本过时。`prompt-optimizer/` 下有完全相同的副本冗余储存。

要清理吗？
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "telegram:7584677982",
  "message_id": "157",
  "sender_id": "7584677982",
  "sender": "ahai",
  "timestamp": "Mon 2026-06-29 18:58 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ahai (7584677982)",
  "id": "7584677982",
  "name": "ahai",
  "username": "ahaius"
}
```

四道门工作流和5层格式流程两个有啥区别和不同
assistant: 两者不是同一层面的东西，一个管**怎么出**，一个管**出什么**。

---

## 核心区别一句话

| | 四道门工作流 | 5层格式底板 |
|------|------|------|
| **文件** | `PROMPT_WORKFLOW.md` | `PROMPT_FORMAT.md` |
| **本质** | **流程导航**（HOW） | **模板规范**（WHAT） |
| **角色** | 安检系统——告诉你先做什么、后做什么、卡在哪一步 | 施工图纸——告诉你最终成品长什么样、每段怎么写 |

---

## 四道门：管过程（防你跳步犯错）

```
门0 → 门1 → 门2 → 门3 → 门4
 ↓       ↓      ↓      ↓      ↓
检查     查     写前    写完    发前
导演说   数据   锁定    自查    最终
"发"没   库     格式    逐条    对比
```

每道门是一个**关卡**。它不是教你怎么写提示词，是逼你在写之前、写之后按顺序做完检查。

- **门0**：纯沟通规则——导演不说"发"，一个字不输出
- **门1**：读 SOUL.md / SELF_CHECK.md / MEMORY.md，确保不漏已有规则
- **门2**：锁定格式模板、确认有没有参考图、场景类型
- **门3**：13条自检——格式逐行对比、特效锚定、段头段尾、打斗规则、技术参数、台词格式
- **门4**：再扫一遍——秒数、图号、特效、段头段尾，全过才发

> 门2 明确写了：「导演给的格式模板是什么？——复制下来，一字不动当底板」→ 这里指的就是 5层格式底板。

---

## 5层格式：管内容（告诉你提示词长什么样）

```
1.【要求】→ 画质扩展（头发/皮肤/布料/景深/UE5/Octane）
2.【资产】→ 人物 / 道具 / 场景
3.【镜头参数】→ 焦段/光圈/ISO/快门角度/ND + 光影
4.【站位.剧情】→ 空间位置 + 剧情概述
5.【分镜序列】→ 每镜：景别(缩写) / 角度 / 镜头(运镜≤2) / 内容 / 光效
【声音】→ 独立尾部
```

这是一个**可复制粘贴的空白模板**。8条硬性规则告诉你具体的格式约束——比如"开头直接 `1.【要求】` 不单独写不要字幕"、"景别必须带英文缩写"、"结尾必加 avoid 行"。

---

## 两者的关系

```
PROMPT_WORKFLOW.md              PROMPT_FORMAT.md
      │                               │
   门2：「导演给的格式              ←  就是你
         模板是什么？                    逐行对照
         复制下来当底板」                的底板
      │                               │
   门3：「格式和导演给的             ←  就是你
         模板逐行对比——                  的那个模板
         一字不多一字不少」
      │
   门3：「子项冒号/括号              ←  从5层格式
         跟模板一致」                    那学的
```

**四道门告诉你**：先别动笔，去查格式模板 → 复制下来 → 写完跟它逐行对比。

**5层格式就是那个被复制、被对比的模板。**

---

## 实际生产中的分工

| 环节 | 调哪个 |
|------|--------|
| 确认导演说了"发" | 四道门·门0 |
| 动笔前补充扫描已有规则 | 四道门·门1 |
| 确定段落结构长什么样 | 5层格式 |
| 人物栏写法（名字+括号描述+质感尾缀） | 5层格式 |
| 每镜景别要不要英文缩写 | 5层格式 |
| 结尾要不要 avoid 行 | 5层格式 |
| 写完后检查特效用词对不对 | 四道门·门3 |
| 检查段头段尾对不对 | 四道门·门3 |
| 检查打斗镜头是不是运动镜头 | 四道门·门3 |
| 发前最终扫一遍全文秒数/图号/特效 | 四道门·门4 |

简单说：5层格式是**成品标准**，四道门是**品控流程**。缺任意一个，要么写出来格式不对，要么漏了检查带错发出去。
user: Conversation info (untrusted metadata):
```json
{
  "chat_id": "telegram:7584677982",
  "message_id": "159",
  "sender_id": "7584677982",
  "sender": "ahai",
  "timestamp": "Mon 2026-06-29 19:01 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ahai (7584677982)",
  "id": "7584677982",
  "name": "ahai",
  "username": "ahaius"
}
```

这两个流程调用触发方式，和两个流程执行的彼此关系先后
assistant: 两者在 SOUL.md 里是同一套触发机制，**四道门包着5层格式**，从门0走到门4，5层格式在门2被调用。

---

## 触发方式：同一个入口

```
用户说"生成提示词"/"优化提示词"/"写提示词"
        │
        ▼
SOUL.md § 强制执行机制 激活
        │
        ▼
    🔴 第一步：「必须读 PROMPT_WORKFLOW.md，从门0走到门4——跳一步=废稿」
```

两套流程由**同一个触发条件**激活，不是独立触发的。SOUL.md 里没有"用户说xx时调四道门，说yy时调5层格式"这种分支——是链式调用。

---

## 执行先后关系

```
触发
  │
  ├─ 门0 · 沟通铁律
  │   「导演上一句话有'发''出'吗？」→ 没有就停
  │
  ├─ 门1 · 查数据库
  │   memory_search → 读 SOUL.md/SKILL.md/MEMORY.md 相关规则
  │   读 SELF_CHECK.md 逐条勾
  │
  ├─ 门2 · 写前锁定
  │   ├─ 「导演给的格式模板是什么？——复制下来，一字不动当底板」
  │   │                                          │
  │   │         ┌────────────────────────────────┘
  │   │         ▼
  │   │   🔵 PROMPT_FORMAT.md（5层格式底板）在此被调用
  │   │         复制作空白模板，后续所有分镜按此结构填
  │   │
  │   ├─ 确认有没有参考图、图号
  │   └─ 确认场景类型（打斗/文戏/空镜）
  │
  ├─ 门3 · 写完自检
  │   ├─ 「格式和导演给的模板逐行对比——一字不多一字不少」
  │   │         ↑
  │   │    拿写好的提示词，跟门2粘过来的5层格式底板逐行对比
  │   │
  │   ├─ 特效锚定检查（弧光/能量刃/冲击波/火焰）
  │   ├─ 段头段尾检查（不写铺垫/不写收招）
  │   ├─ 打斗规则检查（运动镜头/力度词/弧线移动）
  │   ├─ 技术参数检查（焦段+光圈+ISO+快门+ND）
  │   └─ 台词格式检查
  │
  └─ 门4 · 发前最终对比
      「再逐行对比一次导演格式模板——一字不差？」
                  │
                  ▼
              发
```

---

## 一句话总结

| | 四道门 | 5层格式 |
|------|------|------|
| 触发 | 用户说"生成提示词" → SOUL.md 激活 | 四道门·门2 调用 |
| 时机 | 从打字前到发送前，全程 | 动笔前加载，写完后对比 |
| 关系 | **外层流程** | **内层模板** |

**四道门是壳，5层格式是核。** 门0-1-2-3-4 是串联的安检通道，5层格式是通道中间那台 X 光机——所有内容必须过它。
