# 文件地图

这份文件只回答两件事：

1. 每层文件是干什么的
2. 某个概念应该去哪个唯一主文件看

## 目录分工

### 根目录

- `START_HERE.md`
  新对话启动页
- `SYSTEM_INDEX.md`
  全系统总索引与唯一总导航
- `ESSENTIALS.md`
  最小必读清单
- `CURRENT_SYSTEM.md`
  当前系统状态
- `SYSTEM_MAP.md`
  文件用途地图
- `TOPIC_MAP.md`
  主题主导航
- `OPERATING_MODEL.md`
  学习模式 / 投资决策模式与人机分工

### `memory/`

- `memory/logic-bases.md`
  逻辑基点唯一主文件
- `memory/context.md`
  阶段摘要唯一主文件
- `memory/principles.md`
  原则唯一主文件
- `memory/open-questions.md`
  开放问题唯一主文件

### `docs/playbooks/`

执行层。
默认用于：
`逻辑基点和工作假设已相对清楚`
之后的观察、翻译和动作收束。

### `docs/frameworks/`

理解层与桥接层。
默认高频文件是：

- `docs/frameworks/DISCOVERY_PIPELINE.md`
- `docs/frameworks/SIGNALS.md`
- `docs/frameworks/STAGE_TRADING.md`
- `docs/frameworks/STAGE_FAILURE.md`
- `docs/frameworks/TIME_HORIZONS.md`

### `docs/cases/`

样本层，不是入口层。

### `templates/`

输入骨架和研究模板层。

## 唯一主文件归属矩阵

| 概念 | 唯一主文件 |
| --- | --- |
| 系统总导航 | `SYSTEM_INDEX.md` |
| 新对话启动 | `START_HERE.md` |
| 最小入口清单 | `ESSENTIALS.md` |
| 当前系统状态 | `CURRENT_SYSTEM.md` |
| 文件地图 | `SYSTEM_MAP.md` |
| 逻辑基点 | `memory/logic-bases.md` |
| 阶段摘要 | `memory/context.md` |
| 原则 | `memory/principles.md` |
| 开放问题 | `memory/open-questions.md` |
| 主题进度 | `TOPIC_MAP.md` |
| 发现路径 | `docs/frameworks/DISCOVERY_PIPELINE.md` |

规则：

- 后续新增内容先判断归属
- 只更新主文件，不在多个地方重写定义
- 非主文件只允许引用、跳转、极短摘要

## 导航关系

- `主题是导航层`
  先去 `TOPIC_MAP.md`
- `逻辑基点是底座层`
  再去 `memory/logic-bases.md`
- `playbooks 是执行层`
  最后去 `docs/playbooks/`

一句话：
`先找主题，再找它挂靠的基点和假设，最后才找执行文件。`
