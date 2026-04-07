## [LRN-20260403-001] correction

**Logged**: 2026-04-03T00:00:00+08:00
**Priority**: high
**Status**: pending
**Area**: docs

### Summary
近期市场事件分析时，不能把前几天持续发酵的旧消息混进“今天的主因”里，必须先按绝对日期拆时间线。

### Details
在讨论 2026 年 4 月初中东战争、Brent 原油和 A 股走势时，曾把较早发生的海湾能源设施受损与当天新增触发点混在一起描述，导致用户觉得新闻检索和归因不够可靠。类似问题里，必须先核清：

- 绝对日期
- 当天新增事件
- 前几天已被市场消化的旧信息
- 市场价格是继续顺势，还是对新增利空已经钝化

### Suggested Action
今后凡是涉及近期行情、指数点位、新闻驱动的讨论，先整理成“日期 - 事件 - 市场反应”的短时间线，再给解释。

### Metadata
- Source: user_feedback
- Related Files: memory/principles.md
- Tags: correction, timeline, market-news, attribution

---

## [LRN-20260404-002] correction

**Logged**: 2026-04-04T18:35:59+08:00
**Priority**: high
**Status**: pending
**Area**: docs

### Summary
近两日战争新闻整理时，不能只压主线，必须同时保留高影响分支事件与单方表态，并明确确认度。

### Details
在整理 2026-04-03 至 2026-04-04 美伊以战争新闻时，遗漏了两类用户明确关心、且对局势与市场判断有参考价值的信息：
- 法国船只成功通过霍尔木兹海峡
- 伊朗就更早的利雅得美使馆遇袭事件作出否认并指控以色列

这次遗漏的原因不是单一的“没搜到”，而是多种检索与归纳错误叠加：
- 时间窗卡得过死，只保留当日新增，忽略了“旧事件的新表态”
- 过度压缩为主线叙事，没有同时维护“事件台账”
- 过度偏向 AP / Reuters 的硬主线，低估了单方表态和次级分支在用户判断中的参考价值
- 把“确认度不够”错误处理成“先不写”，而不是“写进去并标注确认度”

### Suggested Action
今后凡是用户要求整理近期战争 / 时政新闻：
- 先给主线，再给分支事件台账
- 分支事件即使确认度不高，也保留，但必须标注为“单方说法 / 未独立证实 / 多方确认”
- 除“当天新增事件”外，额外检查“旧事件在今天是否出现新表态、新进展或新证据”
- 对用户点名的具体事件，必须单独核查，不可默认并入主线后省略

### Metadata
- Source: user_feedback
- Related Files: memory/principles.md
- Tags: correction, war-news, coverage, confirmation-level, user-trust

---

## [LRN-20260406-003] correction

**Logged**: 2026-04-06T00:00:00+08:00
**Priority**: high
**Status**: pending
**Area**: docs

### Summary
“深搜”应被定义为默认搜索质量标准，而不是新对话里的额外研究模式。

### Details
用户明确指出，系统想要的是：
- 搜索时必须尽量全面、细致、事实完备
- 输出时保持轻量、短结论、低认知负担

之前把 `DEEP_RESEARCH_CHECKLIST.md` 写成了新对话里“可额外触发的深搜模式”，导致新对话容易被解释成：
- 需要显式进入深搜
- 需要并行展开大量任务
- 需要把搜索过程本身暴露给用户

这违背了用户真实偏好。真正应当区分的是：
- `后台搜得深`
- `前台说得短`

而不是：
- `普通聊`
- `深搜聊`

### Suggested Action
今后系统入口必须明确：
- 深搜是默认搜法，不是特殊工作模式
- 默认围绕当前主题窄域展开，不预加载未点名主题
- 默认不展示完整搜索树，除非用户要看证据链或事实冲突很大

### Metadata
- Source: user_feedback
- Related Files: START_HERE.md, docs/playbooks/DEEP_RESEARCH_CHECKLIST.md, memory/principles.md
- Tags: correction, search-behavior, context-control, output-density, startup-prompt

---
