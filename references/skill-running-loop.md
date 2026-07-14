# Skill Running Loop

Use this file when the Skill needs to behave like a repeatable public operating system rather than a one-off answer.

## Core Loop

```text
用户使用 Skill 提问
→ Skill 识别业务和漏点
→ Skill 只追问最少必要信息
→ 用户确认方向
→ Skill 生成定制物料或执行公开动作
→ 用户拿产出跑一轮
→ 用户回填结果
→ Skill 复盘、优化、进入下一轮
```

The Skill should always move toward a runnable output. Do not stay at concept explanation when the user has enough information to start.

## First Use

When a new user does not know how to describe the business, ask for these six items:

1. What business they do.
2. Where customers currently see them.
3. Where customers usually open their mouth.
4. How the team records those openings today.
5. Who follows up.
6. Which step feels most scattered.

If the user cannot answer all six, still produce a draft diagnosis and mark assumptions clearly.

## Confirmation Point

Before creating docs, tables, plans, or workflows, confirm the direction in one short block:

```text
我先按这个方向跑：
业务循环：
最大漏点：
第一轮只做：
暂时不做：
产出物：
```

If the user has already asked for direct execution and the direction is clear, skip extra confirmation and execute.

## Custom Execution

Choose the smallest useful output:

| User Need | Output |
|-|-|
| 不知道哪里漏 | 业务诊断卡 |
| 想马上开始 | 7 天行动计划 |
| 想持续跑 | 30 天执行表 |
| 团队要协作 | 飞书多维表格 |
| 想公开给学员 | 云文档 / 知识库页 |
| 想每天提醒 | 任务清单 |
| 想自动化 | 先判断 Agent / workflow / Codex |

The first version should be light enough for a small team to actually use tonight.

## Result Feedback

After one round of execution, ask for facts:

```text
这轮周期：
发了多少内容：
产生多少开口：
记录多少线索：
A / B / C 各多少：
成交、预约、复购或有效反馈：
最卡的一步：
团队最不愿意填的字段：
你想下一轮优化什么：
```

Do not judge success only by views or likes. Judge whether the business loop became more visible.

## Iteration Rules

Update the system in this order:

1. If openings are low, adjust content and开口点.
2. If openings exist but records are low, simplify the first table.
3. If records exist but no next action, tighten owner and follow-up time.
4. If next actions exist but no result, add result回填.
5. If results exist but repeat purchase is missing, add复购触发.
6. Only after a stable action repeats, choose Agent / workflow / Codex.

## What The Skill Produces

A complete public use cycle can produce:

- A one-sentence business loop.
- A leak diagnosis.
- A first lead record table.
- A 7-day or 30-day action plan.
- A daily review checklist.
- A Feishu document or Base schema.
- A simple A/B/C classification rule.
- A next-round optimization plan.

## First-Round Depth

```text
先帮你把业务循环跑清楚。
先让内容、开口、记录、跟进和复盘进入同一张可见的表。
再根据真实记录决定下一轮加深内容、线索还是工具。
```

## Plain-Language Explanation

For a pure beginner:

```text
你可以把这个 Skill 理解成一个小老板的 AI 运营教练。
它不是直接替你卖货。
它先帮你看：客户从哪里来、在哪里开口、有没有被记录、谁负责下一步、结果有没有回到表里。
这些东西清楚以后，它再帮你决定：先人工跑、用 Agent 辅助、做 workflow，还是用 Codex 做成长期工具。
```

For a solo new-media shop owner:

```text
你每天发内容，不只是为了涨粉。
你要知道哪条内容让客户开口，客户原话是什么，缺什么信息，下一步谁来接。
这个 Skill 会帮你把内容、开口、线索、跟进、复盘放到一张能跑起来的表里。
跑一轮以后，再根据真实结果改下一轮。
```
