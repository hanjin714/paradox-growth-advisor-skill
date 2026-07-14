# Feishu Execution Layer

This file turns 悖论增长谋士 Skill from text advice into public, runnable work artifacts.

Use it when the user wants:

- A 7-day execution plan.
- A 30-day execution plan.
- A Feishu cloud document.
- A Base / 多维表格 schema.
- A lead record table.
- A content calendar.
- A daily review table.
- A task list or daily workflow.

Keep every Feishu artifact focused on the first runnable action: readable plan, recordable table, reviewable task list.

## Tool Scope

If Feishu CLI is available, create real Feishu artifacts. If not, output the Markdown / table schema that can be pasted into Feishu.

Preferred CLI:

```bash
lark-cli
```

If the workspace contains the bundled CLI, this path may also exist:

```bash
SKILLs/cli-main/bin/lark-cli
```

Before using a Feishu domain, read the matching CLI skill:

```bash
lark-cli skills read lark-doc
lark-cli skills read lark-base
lark-cli skills read lark-task
```

Use Feishu for execution assets that a small team can read, fill, and review.

## Artifact Types

### 1. Public Cloud Doc

Use for:

- Explaining the method to a learner.
- Creating a 7-day / 30-day operating guide.
- Publishing a knowledge-base style page.
- Giving a founder a readable action plan.

Recommended doc structure:

```text
标题：线索不散｜7 天小团队 AI O2O 执行计划

1. 一句话业务循环
2. 当前最大漏点
3. 第一张表要记录什么
4. 7 天执行安排
5. 每天复盘问题
6. Agent / workflow / Codex 选择
7. 暂时不做什么
```

CLI pattern:

```bash
lark-cli docs +create --title "线索不散｜7 天执行计划" --markdown "<markdown>"
```

If the CLI requires XML, use a simple document structure with headings, paragraphs, tables, and bullet lists. Avoid complex styling.

### 2. Lead Record Base

Use for:

- Recording real openings and inquiries.
- Tracking owner and next action.
- Classifying A/B/C.
- Reviewing source quality.

Public base name:

```text
线索不散｜小团队线索记录表
```

Recommended table:

```text
线索记录
```

Public fields:

| Field | Type Suggestion | Meaning |
|-|-|-|
| 日期 | Date | When the lead appeared |
| 来源内容 | Text / URL | Which content, live, platform, or referral |
| 客户原话 | Long text | Keep real customer words |
| 产品/服务需求 | Text | What they seem to need |
| 当前阶段 | Single select | 刚开口 / 问题明确 / 信息待补 / 已预约下一步 / 方案判断中 / 暂不推进 |
| 线索等级 | Single select | A / B / C |
| 负责人 | User / Text | Who owns next action |
| 下一步动作 | Text | Specific next action |
| 下次跟进时间 | Date | Concrete follow-up time |
| 结果回填 | Long text | What happened |
| 复盘标签 | Multi-select | 内容问题 / 承接问题 / 交接问题 / 复购节点 / 其他 |

Create a Base when the user needs an actual working table. If exact field JSON is needed, read `lark-cli skills read lark-base references/lark-base-field-json.md` before constructing the command.

CLI pattern:

```bash
lark-cli base +base-create \
  --name "线索不散｜小团队线索记录表" \
  --table-name "线索记录" \
  --fields '<field-json-array>'
```

After creating, return:

- Base title.
- Public Base URL or public object ID if returned by the CLI.
- URL if returned.
- The table name and intended usage.

### 3. 7-Day Execution Schedule

Use when the user wants a short activation plan.

Public schedule:

| Day | Main Job | Output |
|-|-|-|
| Day 1 | 写一句话业务循环，找最大漏点 | 业务循环 + 最大漏点 |
| Day 2 | 设计 7 天内容路径 | 内容罗盘 |
| Day 3 | 记录 10 条真实客户原话 | 最小线索表 |
| Day 4 | 做 A/B/C 轻分层 | 线索优先级 |
| Day 5 | 写工具选择卡 | Agent/workflow/Codex 判断 |
| Day 6 | 做一张诊断卡 | 公开诊断输出 |
| Day 7 | 做复盘表并确定下一轮 | 下一轮 7 天重点 |

For a Feishu doc, create a document with daily sections.

For a Base, create a schedule table:

| Field | Type Suggestion |
|-|-|
| 天数 | Single select |
| 今日目标 | Text |
| 今日动作 | Long text |
| 产出物 | Text |
| 完成状态 | Single select: 未开始 / 进行中 / 已完成 |
| 复盘问题 | Long text |

For Feishu Tasks, create a task list only when the user wants reminders or execution tracking.

### 4. 30-Day Execution Schedule

Use when the user wants a full operating cycle.

Public logic:

```text
30 天不是每天随机发内容，而是跑四轮：看见、开口、记录、复盘。
```

Structure:

| Week | Theme | Goal |
|-|-|-|
| Week 1 | 看见与开口 | Build content path and collect first questions |
| Week 2 | 记录与分层 | Record real openings and classify A/B/C |
| Week 3 | 跟进与复盘 | Improve next actions and review sources |
| Week 4 | 复购与工具化 | Find repeat nodes and choose Agent/workflow/Codex |

Recommended 30-day fields:

| Field | Meaning |
|-|-|
| 日期 | Day |
| 周期 | Week 1-4 |
| 今日主题 | What to focus on |
| 今日内容 | What to publish or review |
| 开口点 | What the user can ask |
| 要记录的字段 | What should enter the table |
| 今日复盘问题 | What to check at night |
| AI 可辅助动作 | Agent / workflow / Codex / none |
| 完成状态 | Execution state |

### 5. Task List

Use for:

- Daily execution reminders.
- Founder/operator checklist.
- Assigning owners in a small team.

CLI pattern:

```bash
lark-cli task +tasklist-create --name "线索不散｜7 天执行清单"
```

Create tasks only for public actions:

- Write business loop.
- Record 10 real inquiries.
- Fill A/B/C.
- Review content openings.
- Decide tool choice.

Create tasks around first-round records, owner, next action, review, and tool choice.

## Recommended Execution Flow

When a user asks to “build this in Feishu,” use this order:

1. Clarify or infer whether they need doc, Base, task list, or all three.
2. Create a public cloud doc first if the plan needs explanation.
3. Create a Base if they need daily records.
4. Create a task list if they need reminders and execution tracking.
5. Return all created links, public object IDs, and a short “how to use it tonight” guide.

## Minimal Output Package

For most small teams, generate three assets:

```text
1. 线索不散｜7 天执行计划（云文档）
2. 线索不散｜小团队线索记录表（多维表格）
3. 线索不散｜每日复盘清单（任务或文档清单）
```

For a solo new-media shop owner, generate:

```text
1. 30 天内容-线索-复盘表
2. 客户原话记录表
3. 每晚 10 分钟复盘问题
```

## Public Example: Solo New-Media Online Store

Use this when the user gives limited industry details but wants an example.

First table:

| Field | Example |
|-|-|
| 日期 | 2026-07-14 |
| 来源内容 | 小红书：油皮夏天怎么选 |
| 客户原话 | 这个适合油皮吗 |
| 产品/需求 | 肤质适配 |
| 当前阶段 | 刚开口 |
| 线索等级 | B |
| 下一步动作 | 补问年龄、是否敏感肌、使用场景 |
| 结果回填 | 等待回复 |

Daily review questions:

```text
今天哪条内容让人开口？
客户都问了什么？
有没有 A 类客户？
明天内容要回答哪个真实问题？
```

Tool choice:

```text
先人工记录 7 天。
有 30 条客户原话后，再让 Agent 归类高频问题。
如果每天都要提醒复购或跟进，再考虑 workflow。
如果要团队长期使用看板，再考虑 Codex。
```
