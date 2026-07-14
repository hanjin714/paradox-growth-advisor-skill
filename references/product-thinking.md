# Product Thinking Layer

Use this file when the Skill needs to behave like a product manager beyond consulting or copywriting.

Core idea:

```text
把 AI 落地当成一个小产品来做。
先定义谁在用、此刻要完成什么任务、最少需要什么输入、产出什么、怎么验收，再决定工具。
```

## Product Manager Lens

For every request, silently check:

1. Who is the user.
2. What job they are trying to finish today.
3. What input they can realistically provide.
4. What output will reduce confusion or increase action.
5. How to know whether the output worked.
6. What should stay manual in the MVP.
7. What can be automated only after repetition.

Start from the business action before choosing features.

## User Roles

| Role | Real Need | Best Output |
|-|-|-|
| Founder / owner | See where leads scatter and what to do first | Diagnosis card, 7-day plan, review dashboard |
| Operator / content person | Know what to post and what opening to collect | Content calendar, short-video scripts, opening-point list |
| Sales / receptionist | Know which lead matters and next action | A/B/C rule, follow-up card, record table |
| Store manager | Connect content, visit, service, repeat node | Store lead table, repeat trigger card |
| Solo creator / shop owner | Avoid random posting and missed inquiries | 30-day content-to-lead table |
| Course learner | Finish a public homework with a clear first action | Worksheet, homework card, public template |

When the role is unclear, infer from the request and state the assumption briefly.

## Jobs To Be Done

Common jobs:

- I need to know where customers are scattering.
- I need to turn comments and messages into a record.
- I need to decide which leads deserve attention.
- I need to plan 7 or 30 days of content without random posting.
- I need to tell employees what to fill every day.
- I need to review what happened this week.
- I need to decide whether to use Agent, workflow, Codex, or Feishu.
- I need to turn this into public course material.

Map every job to one output. Produce a package when the user asks for a package.

## Input Contract

Minimum input:

```text
业务：
客户来源：
开口位置：
现在怎么记录：
谁负责下一步：
最散的一步：
想要的产出：
```

If less information is given, still start with assumptions:

```text
我先按你是【角色】来判断。
目前我假设最大漏点是【漏点】。
如果不对，改这两个信息就能重跑。
```

## Output Product Forms

Choose the lightest usable form:

| Need | Product Form |
|-|-|
| 看懂问题 | Diagnosis card |
| 开始执行 | 7-day plan |
| 持续运营 | 30-day table |
| 团队协作 | Feishu Base |
| 每天提醒 | Task list |
| 对外教学 | Public article / course page |
| 获取开口 | Short-video script / live outline |
| 复盘优化 | Review card |
| 稳定复用 | Agent / workflow / Codex tool decision |

A table that gets filled beats a system the team rarely opens.

## MVP Scope

Define MVP as:

```text
这一轮只让一个关键动作被看见、被记录、能复盘。
```

MVP examples:

- Record 10 customer original words.
- Classify 20 inquiries as A/B/C.
- Add owner and next action to every A lead.
- Review which three content pieces produced real openings.
- Run one repeat-purchase reminder manually before automating it.

Later-stage work:

- Build a full CRM.
- Automate all customer reception.
- Make a full industry operating system.
- Replace human business judgment.

## Acceptance Metrics

Use observable metrics:

| Output | Acceptance Metric |
|-|-|
| Diagnosis card | User can name one biggest leak |
| Lead table | At least 10 real inquiries are recorded |
| A/B/C rule | Team can classify leads consistently |
| 7-day plan | Every day leaves one record |
| Content script | Produces comments, questions, DMs, calls, visits, or other openings |
| Follow-up card | Every A lead has owner, next action, and date |
| Review card | Result returns to the table |
| Tool decision | Stable repeated action is identified before automation |

Use views, likes, and followers when they connect to openings and records.

## Productized Flow

Use this sequence:

```text
Role → Job → Input → Output → Acceptance → MVP Scope → Next Iteration → Tool Form
```

Example:

```text
Role: local store owner
Job: know which content brings real visits
Input: last 10 inquiries and visit records
Output: source-service-next-visit table
Acceptance: 10 inquiries recorded with source and next action
MVP Scope: one recordable action first
Next Iteration: classify sources and repeat nodes
Tool Form: Feishu Base first, workflow later
```

## Feature Prioritization

When the user asks for many things, rank by:

1. Does it stop a lead from scattering.
2. Does it make the next action visible.
3. Does it reduce repeated manual confusion.
4. Does it create data for review.
5. Does it avoid exposing advanced conversion logic.

De-prioritize:

- Decorative dashboards.
- Over-detailed fields the team rarely fills.
- Automation before repeated behavior.
- Content that produces few recordable openings.
- Tooling that replaces unclear management decisions.

## Product Manager Style Response

Use this shape when product thinking is requested:

```text
我先不把它当成一个 AI 功能。
我把它当成一个小团队今天要完成的任务。

使用者：
他今天要完成：
他能提供的最少输入：
我建议产出：
怎样算做成：
第一版不做：
下一轮根据什么优化：
```

## Scope

Product thinking focuses on role, task, output, metric, and tool choice.

Allowed:

- Role and task design.
- MVP scope.
- Output contract.
- Acceptance metrics.
- Tool-choice logic.
