# 📋 Skills INDEX — 技能库统一索引

> 自动生成：2026-06-29 | 最后梳理：2026-06-29（skill-manager）
> 技能总数：7 个子技能 + 1 母技能

---

## 🎬 视频制作（skills/VIDEO/）

### 总控·配方

| 技能 | 路径 | 功能 |
|------|------|------|
| **打斗设计技能** | `打斗设计技能/SKILL.md` | 打斗场景总控方法论（运镜/节奏/卖打击五谎言/光效/检查清单） |
| **打斗动作模版（慢帧）** | `打斗动作模版（慢帧）/SKILL.md` | 写实格斗·冲击波三层·6镜循环·慢帧节奏 |
| **打斗动作模版（快帧）** | `打斗动作模版（快帧）/SKILL.md` | 赛博奇幻·太极×机甲·9镜标准版·快帧节奏 |

### 质检（出稿前强制调用）

| 技能 | 路径 | 功能 |
|------|------|------|
| **人物服装增强技能** | `人物服装增强技能/SKILL.md` | 皮肤/眼睛/头发/服装四维增强 |
| **场景一致性保持技能** | `场景一致性保持技能/SKILL.md` | 空间逻辑·四面墙·八维跨镜·漂移修复 |
| **场景质感增强技能** | `场景质感增强技能/SKILL.md` | 材质纹理/光影层次/天气/地面六维增强 |

### 安检

| 技能 | 路径 | 功能 |
|------|------|------|
| **违禁词审查技能** | `违禁词审查技能/SKILL.md` | 11大类违禁词库·全文扫描·出稿前最后一道门 |

### 参考文档（references/）

| 文档 | 内容 |
|------|------|
| `prompt-writing-rules.md` | 提示词写法规则全集（5层格式/景别/运镜/检查清单） |
| `technical-parameters.md`（外部） | 电影摄影技术参数（光圈/ISO/快门角度/ND） |
| `multi-character-fight-positioning.md` | 多人打斗站位规则 |
| `wuxia-action-guide.md` | 武侠动作指导 |
| `shots-guide.md` | 镜头语言指南 |
| `vertical-shots-guide.md` | 竖屏镜头指南 |
| `director-styles.md` | 导演风格参考 |
| `directing.md` | 导演技巧 |
| `screenwriting.md` | 编剧指南 |
| `short-drama-structure.md` | 短剧结构 |
| `seedance-guide.md` | Seedance 使用指南 |
| `seedance-english-guide.md` | Seedance 英文指南 |
| `seedream-5.0.md` | Seedream 5.0 参考 |
| `volcano-api-guide.md` | 火山引擎 API 指南 |
| `5agent-workflow.md` | 5Agent 工作流 |
| `character-prompts.md` | 角色提示词参考 |
| `knowledge.md` | 知识库 |
| `workflow-index.md` | 工作流索引 |

### 模板（templates/）

| 文件 | 用途 |
|------|------|
| `project-overview-template.md` | 项目总览模板 |
| `script-analysis-template.md` | 剧本分析模板 |
| `short-drama-script-template.md` | 短剧剧本模板 |
| `storyboard-template.md` | 故事板模板 |

### 工作流（workflows/）

| 文件 | 用途 |
|------|------|
| `prompt-generation-workflow.md` | 提示词生成工作流 |
| `short-drama-workflow.md` | 短剧制作工作流 |

---

## 🔗 技能关系图

```
出稿前调用链：
  人物服装增强 ──┐
  场景质感增强 ──┼── 并行质检 ──→ 违禁词审查 ──→ 出稿
  场景一致性保持 ┘

打斗段落调用链：
  打斗设计技能（总控）
   ├── 方法论：运镜/节奏/光效/检查清单
   ├──→ 打斗动作模版（慢帧）— 写实配方
   └──→ 打斗动作模版（快帧）— 奇幻配方
       ↓
  违禁词审查（最后一道门）
```

---

## 📊 统计数据

| 指标 | 数值 |
|------|------|
| 子技能 | 7 |
| 母技能 | 1（SKILL.md） |
| 参考文档 | 18 |
| 模板 | 4 |
| 工作流 | 2 |
| 总文件 | 31 |
| 冗余/冲突 | 0 |
| 过时技能 | 0 |

---

*索引文件：`skills/INDEX.md` · 变更随技能目录同步更新*
