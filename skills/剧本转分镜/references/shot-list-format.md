# Shot List 标准字段

## 基本字段

| 字段 | 说明 | 示例 |
|-----|------|------|
| Shot # | 镜头编号 | 1A, 1B, 2 |
| Scene # | 场景编号 | Scene 1, Scene 2 |
| Shot Size | 景别 | WS, MS, CU |
| Camera Angle | 角度 | Eye Level, Low, High |
| Camera Movement | 运镜 | 固定, 推, 拉, 跟 |
| Description | 动作描写 | HE enters the room... |
| Duration | 时长（秒） | 3s |

## 景别缩写

| 缩写 | 完整 | 说明 |
|-----|------|------|
| EWS | Extreme Wide Shot | 极端远景，建立场景 |
| WS | Wide Shot | 远景/全景 |
| LS | Long Shot | 长镜头，同WS |
| FS | Full Shot | 全身镜头 |
| MWS | Medium Wide Shot | 中远景 |
| MS | Medium Shot | 中景 |
| MCU | Medium Close-Up | 中近景 |
| CU | Close-Up | 特写 |
| ECU | Extreme Close-Up | 大特写 |
| OTS | Over-the-Shoulder | 过肩镜头 |

## 角度缩写

| 缩写 | 说明 | 叙事目的 |
|-----|------|---------|
| EL | Eye Level | 客观、中性 |
| LOW | Low Angle | 仰拍，力量/威严 |
| HIGH | High Angle | 俯拍，脆弱/劣势 |
| BEV | Bird's Eye | 俯拍全景，建立 |
| DUTCH | Dutch Tilt | 倾斜，紧张/不安 |
| OBL | Oblique | 侧倾，同DUTCH |

## 运镜缩写

| 缩写 | 说明 | 使用场景 |
|-----|------|---------|
| FIX | Fixed | 固定镜头，文戏 |
| PAN | Pan | 摇镜，横向扫视 |
| TILT | Tilt | 上下摇 |
| DOLLY | Dolly | 推拉，焦点转移 |
| TRACK | Track | 跟拍，运动主体 |
| HANDHELD | Handheld | 手持，呼吸感 |
| CRANE | Crane | 升降，大场景 |
| ZOOM | Zoom | 变焦 |

## 剧本到Shot List的转换规则

剧本Action段 → 1个或多个镜头

示例：
```
剧本：
INT. 酒馆 - DAY
The tavern is crowded. ALARIC stands by the bar. He notices a hooded figure.

Shot List:
1A - Scene 1 - WS - EL - FIX - 3s - 酒馆全景，人物关系
1B - Scene 1 - MS - EL - FIX - 2s - ALARIC站在吧台
1C - Scene 1 - CU - EL - FIX - 1s - ALARIC注意到神秘人
```
