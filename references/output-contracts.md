# Output Contracts

Use these contracts to keep outputs complete, testable, and audience-ready.

## Contract 1: Diagnosis Card

Return exactly these sections when diagnosing a business:

```text
一句话业务循环：
当前最大漏点：
为什么是这个漏点：
第一张表要记录什么：
A/B/C 怎么分：
未来 7 天只做什么：
现在不做什么：
工具选择：
公开边界：
```

Quality bar:

- The business loop must include source, opening place, owner, record, next action, result, and repeat trigger if relevant.
- The leak must be one main leak, not a list of everything.
- The first table must have no more than 10 public fields.
- “现在不做什么” must remove at least one tempting but premature action.

## Contract 2: 7-Day Action Plan

Return a 7-day table:

| Day | Goal | Action | Record | Review Question |
|-|-|-|-|-|

Rules:

- Each day should have one main action.
- Every day should leave a record.
- Do not introduce automation before the action repeats.
- Day 7 should decide manual / Agent / workflow / Codex.

Required closing:

```text
这 7 天不追求系统完整，只追求把一条线索从开口到下一步看清楚。
```

## Contract 3: 30-Day Operating Plan

Return four weekly themes:

| Week | Theme | Goal | Main Records |
|-|-|-|-|
| Week 1 | 看见与开口 | Know what makes customers ask | Content source, opening point, original words |
| Week 2 | 记录与分层 | Turn inquiries into visible leads | Need, missing info, A/B/C |
| Week 3 | 跟进与复盘 | Add owner and next action | Owner, next action, follow-up date, result |
| Week 4 | 复购与工具化 | Find repeat triggers and tool choice | Repeat node, stable action, tool decision |

Then output a daily or weekly checklist depending on user detail.

## Contract 4: Feishu Base Schema

Return:

1. Base name.
2. Table name.
3. Field list.
4. Field meaning.
5. Select options.
6. How the team should use it every day.

Public default:

| Field | Type | Options / Notes |
|-|-|-|
| 日期 | Date | When the lead appeared |
| 来源内容 | Text | Video, live, search, referral, store visit |
| 客户原话 | Long text | Keep exact words |
| 需求判断 | Text | What the customer seems to need |
| 当前阶段 | Single select | 刚开口 / 信息待补 / 已预约下一步 / 方案判断中 / 暂不推进 |
| 线索等级 | Single select | A / B / C |
| 负责人 | User / Text | Who owns next action |
| 下一步动作 | Text | Specific action, not “follow up” |
| 下次跟进时间 | Date | Concrete date |
| 结果回填 | Long text | What happened |

Keep the first version focused on fields the team can fill every day.

## Contract 5: Result Review

When the user returns execution results, output:

```text
这轮发生了什么：
最大变化：
最大漏点：
数据说明：
下一轮保留：
下一轮删除：
下一轮新增：
表格字段调整：
工具选择变化：
下一轮 7 天动作：
```

Quality bar:

- Use observed facts before suggestions.
- Do not flatter the user with vague praise.
- Do not judge only by views.
- Tie every suggestion back to content, opening, record, follow-up, review, or repeat purchase.

## Contract 6: Public Course / Knowledge-Base Page

Return:

1. One-sentence conclusion.
2. What problem this section solves.
3. Mind map or structured outline.
4. Core logic.
5. Example.
6. Homework.
7. Next review question.

Keep the page focused on:

- One clear judgment.
- One concrete business scene.
- One table, checklist, or action card.
- One homework task.
- One next-round review question.

## Contract 7: Tool Choice Card

Return:

| Situation | Use | Reason |
|-|-|-|
| Inputs change every time and need judgment | Agent | It can reason through variation |
| Steps are stable and repeat | workflow | It can run fixed transmission |
| Team needs long-term page, search, state, permission | Codex | It can turn process into tool |
| Process is unclear | Manual first | Automation would magnify confusion |

Always add:

```text
工具不是起点，能写清楚的业务动作才是起点。
```

## Contract 8: Auxiliary Production Package

Return this when the user asks for “辅助产出”, “一套物料”, or “帮我把这个诊断变成内容”:

```text
诊断依据：
本轮只解决的漏点：
产出 1：短视频脚本
产出 2：直播/讲解大纲
产出 3：公众号或知识库段落
产出 4：作业卡
产出 5：每日复盘卡
产出 6：飞书表格字段
发布/执行后要记录：
下一轮复盘问题：
```

Quality bar:

- Every asset must point back to the same diagnosed leak.
- Every asset must have a recordable next action.
- Do not create generic marketing copy.
- Keep the output close to first-round execution.

## Contract 9: Productized Workflow Card

Return this when the user asks for product-manager thinking, productization, workflow design, or turning an AI idea into a usable process:

```text
使用者：
今天要完成的任务：
最少输入：
交付产物：
验收指标：
第一版不做：
下一轮触发条件：
工具形态：
```

Quality bar:

- The user role must be specific.
- The task must be a job, not a slogan.
- The acceptance metric must be observable.
- MVP boundary must remove premature automation or overbuilding.
- Tool form must be chosen after the task is clear.
