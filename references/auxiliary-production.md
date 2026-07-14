# Auxiliary Production

Use this file when the Skill needs to produce supporting materials beyond diagnosis and tables.

The principle:

```text
辅助产出不是为了显得内容多。
每一个产出都要服务一个漏点：让用户开口、让线索被记录、让团队有下一步、让结果能回流。
```

## Production Rule

Before producing any asset, identify:

1. Which business loop this asset belongs to.
2. Which leak it is solving.
3. What the user should do after seeing it.
4. What the team must record after using it.
5. What should be recorded after use.

When the diagnosed leak is missing, first produce a light diagnosis.

## Asset Map

| Leak | Useful Auxiliary Output | Record After Use |
|-|-|-|
| Content leak | Short-video script, opening question, topic list, live teaser | Which content produced openings |
| Lead leak | Comment reply guide, inquiry record prompt, public worksheet | Customer original words and need |
| Follow-up leak | Employee checklist, next-action card, daily task list | Owner, next action, follow-up date |
| Review leak | Daily review card, weekly review page, data interpretation note | Result and review tag |
| Repeat-purchase leak | Reminder logic, revisit topic, service-cycle card | Repeat node and trigger date |
| Tool-choice confusion | Agent/workflow/Codex card, tool-choice worksheet | Stable action and tool decision |

## Asset Types

The Skill can produce:

- Short-video scripts.
- Live outlines.
- Public course notes.
- Public knowledge-base pages.
- Article sections.
-朋友圈 / community announcement drafts.
- Homework cards.
- Daily execution cards.
- Review cards.
- Feishu doc outlines.
- Feishu Base field designs.
- Mind map text.
- Content calendars.
- Tool-choice cards.
- Customer original-word collection prompts.

## Short-Video Script Contract

Use when producing a video script.

Return:

```text
视频目标：
解决的漏点：
开场钩子：
正文：
转折判断：
具体例子：
结尾动作：
发布后记录：
下一轮复盘：
```

Rules:

- Use natural spoken language.
- Use one clear point, focused on the first course-level action.
- Make the viewer know what to comment, ask, record, or try.
- The ending should invite a audience-ready action, such as “留言你的行业，我帮你判断第一张表该记什么”.

Example ending:

```text
你不用先买一堆工具。
你先把最近 10 条客户原话记下来。
如果你不知道怎么分，我可以按 A/B/C 帮你拆第一版。
```

## Live Outline Contract

Use when producing a live session outline.

Return:

```text
直播主题：
适合谁听：
开场 3 分钟：
第一段：问题现场
第二段：框架
第三段：案例
第四段：作业
答疑范围：
直播后要记录：
```

Rules:

- Keep the class useful, concrete, and focused on first-round execution.
- Give the learner a first action and a review point.
- Avoid off-platform traffic wording. Use audience-ready wording such as “平台允许方式领取基础模板”.

## Article Section Contract

Use when producing a public article or knowledge-base section.

Return:

1. Title.
2. One-sentence conclusion.
3. Business scene.
4. Core judgment.
5. Public framework.
6. Example.
7. Reader homework.
8. Next review question.

Article sections should sound like a practitioner:

```text
很多时候不是工具问题，而是业务动作还没有被记录下来。
很多时候，是你的客户开口以后，团队没有一张共同能看的记录。
```

## Community Homework Card

Use when producing homework for a group, course, or public community.

Return:

```text
今天只做一件事：
你要填什么：
填完以后怎么判断：
明天带着什么回来：
执行范围：
```

Good homework examples:

- Record 10 customer original words.
- Mark A/B/C once.
- Add owner and next action for every A lead.
- Review which content produced real openings.
- Pick one stable repeated action before choosing a tool.

## Daily Review Card

Use when the user needs daily tracking.

Return:

```text
今天发了什么：
谁开口了：
开口原话是什么：
有没有记录：
有没有负责人：
下一步是什么：
结果有没有回填：
明天只改一个点：
```

Keep the review tied to business signals. Views and likes matter when they explain openings.

## Content Calendar Contract

Use when generating content ideas.

Return a table:

| Day | Topic | Opening Point | Customer Question To Collect | Record Field | Review Question |
|-|-|-|-|-|

Rules:

- Every topic must connect to a customer opening.
- Every opening must connect to a record.
- Generate topics from customer openings rather than trend-chasing alone.
- Treat results as experiments that need records.

## Mind Map Text Contract

Use when the user asks for a mind map.

Return nested Markdown:

```text
- 一句话业务循环
  - 看见
  - 开口
  - 记录
  - 跟进
  - 回流
  - 复购
- 最大漏点
  - 现象
  - 原因
  - 第一动作
- 7 天动作
  - Day 1
  - Day 2
```

Keep it readable enough to paste into Feishu or a mind-map tool.

## Auxiliary Package

When the user asks for a complete supporting material package, return:

1. Diagnosis card.
2. 7-day action table.
3. One short-video teaser script.
4. One live outline.
5. One public article section.
6. One homework card.
7. One daily review card.
8. One Feishu table schema.
9. One result-feedback prompt.

Add:

```text
这套物料聚焦第一轮：让内容、开口、记录、跟进和复盘先跑起来。
```
