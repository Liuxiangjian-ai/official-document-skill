---
name: official-document-skill
description: Draft, revise, polish, and quality-check Chinese official documents and government-style practical writing (公文、党政机关公文、事务文书、申论应用文、人民日报风格政务表达), producing deliverable drafts with correct document type, format, restrained institutional tone, concrete facts, People's Daily-inspired expression discipline, and reduced AI-flavored phrasing. Use when the user asks for 通知、通报、报告、请示、批复、函、纪要、决定、通告、议案、倡议书、工作方案、工作计划、工作总结、简报、讲话稿、发言稿、汇报材料、调研报告、宣传稿、公开信、感谢信、信访回复、理论评论、政策解读, or asks to 一键生成/润色/改写/降AI味/减少AI味/人民日报风格/检查格式/生成可交付公文.
---

# 公文写作

## Purpose

Generate or revise Chinese official documents that are structurally correct, usable as a deliverable, fact-grounded, restrained in tone, and low in AI-flavored boilerplate. Combine two source bases:

- Formal public-document writing rules: document-type choice, official format, upward/downward/parallel writing, closing formulas, and common format errors.
- People's Daily-style expression distillation: fact density, restrained judgment, functional paragraphs, natural progression, abstract-word control, and resistance to empty slogans.

## Core Workflow

1. Identify the scenario: issuer, recipient, relationship (上行/下行/平行/面向公众), purpose, audience, urgency, required length, and whether a formal red-head shell is needed.
2. Choose the document type. If the user's requested type conflicts with purpose or relationship, quietly correct it in the draft or briefly flag the mismatch.
3. Extract facts before drafting: subject, object, action, mechanism, data, time, place, problem, result, responsibility, deadline, feedback path, and policy basis.
4. Build a document skeleton by type. Do not force every task into a publicity article, speech, or three-part slogan structure.
5. Draft with official restraint: facts and tasks first, then necessary judgment. Use long sentences for background, mechanisms, and compound facts; use short sentences for decisions, reminders, and closing.
6. Run the anti-AI pass: check fact density, judgment strength, sentence rhythm, abstract-word control, paragraph function, type fit, and grounded ending.
7. Score internally using the rubric below. If below 80, rewrite or compress hollow paragraphs before final output.
8. Deliver the final document first. Add a short "需补充信息" list only when placeholders remain or missing facts materially affect use.

## Output Defaults

- Use Chinese unless the user requests another language.
- Produce a complete usable draft, not only an outline, when enough facts exist.
- If key facts are missing, use a small number of bracketed placeholders such as `〔发文机关〕` or `〔日期〕`.
- For formal official drafts, include title, main recipient, body, issuing unit, and date when applicable. Include 发文字号、附件、抄送、版记 only if requested or supplied.
- For exam/application-writing prompts, obey the word limit and omit formal elements only when the prompt says "不必考虑格式".
- Never invent laws, documents, meetings, leader names, numbers, departments, budgets, dates, outcomes, or approvals.

## Document-Type Decision

### Formal Official Documents

| 文种 | 适用场景 | Key Structure | Required Discipline |
| --- | --- | --- | --- |
| 通知 | 下行或平行告知办理、执行、周知事项 | 依据/背景 + 事项 + 要求 + 时限 | 明确对象、事项、责任；平行通知避免命令口吻 |
| 通报 | 表彰先进、批评错误、传达重要情况 | 事实 + 评价/原因 + 决定/要求 | 事实准确，评价克制，避免情绪化 |
| 报告 | 向上级汇报工作、反映情况、答复询问 | 情况 + 做法 + 成效 + 问题 + 下一步 | 不夹带请示事项；可用"特此报告" |
| 请示 | 向上级请求指示、批准、批转 | 缘由 + 依据/困难 + 请求事项 + 请求语 | 一文一事，一般只送一个主送机关；"妥否，请批示/批复" |
| 批复 | 答复下级请示 | 引述来文 + 批复意见 + 要求 | 明确同意/不同意及依据，不含糊 |
| 函 | 不相隶属机关商洽、询问、答复、请求批准 | 来由 + 事项 + 希望/回复 | 语气平等、礼貌；"特此函告/函复""盼复" |
| 纪要 | 记载会议主要情况和议定事项 | 会议概况 + 议定事项 + 落实要求 | 写"会议认为/指出/要求"，不写流水账 |
| 决定 | 对重要事项作出安排、奖惩或变更 | 依据/事实 + 决定事项 + 执行要求 | 权威、明确，适合较重大事项 |
| 通告 | 在一定范围公布应遵守或周知事项 | 依据 + 通告事项 + 生效/执行要求 | 面向社会或特定范围，条款清楚 |
| 公告 | 向国内外宣布重要事项或法定事项 | 事项 + 说明 | 级别和事项通常较高，慎用 |
| 意见 | 对重要问题提出见解和处理办法 | 背景意义 + 总体要求 + 具体意见 | 政策性较强，可上行、下行、平行 |
| 议案 | 政府向人大或人大常委会提请审议 | 案由 + 方案/依据 + 提请审议 | 注意法定主体和程序 |

### Practical Government Writing

| 文体 | 适用场景 | Writing Focus |
| --- | --- | --- |
| 工作方案 | 安排专项行动、活动、治理任务 | 目标要求、重点任务、实施步骤、责任分工、保障措施 |
| 工作计划 | 对未来阶段工作作安排 | 目标、重点任务、时间节点、保障措施；少写成绩，多写安排 |
| 工作总结 | 回顾阶段工作 | 总体情况、主要做法、成效经验、问题不足、下步安排 |
| 简报/信息稿 | 内部快速反映情况、经验、动态 | 导语、主要做法、阶段成效、经验启示；短、实、新 |
| 讲话稿/发言稿 | 会议、活动、座谈发言 | 称谓、开场、形势认识、重点任务、落实要求、收束 |
| 表态发言 | 表达态度和落实承诺 | 认识、态度、措施、承诺；每个表态接具体动作 |
| 汇报材料 | 向领导或会议汇报 | 背景、进展、成效、问题、建议/下一步；突出可决策信息 |
| 调研报告 | 反映调查研究结果 | 调研背景、现状、问题原因、对策建议；建议与问题对应 |
| 倡议书 | 面向群体发起行动 | 背景意义、倡议事项、号召；热情但不空泛 |
| 宣传稿 | 面向公众宣传政策、活动、典型 | 场景切入、典型事实、做法成效、适度升华 |
| 公开信 | 面向特定群体公开沟通 | 称谓明确，先共情/说明，再提出事项，结尾表达期待 |
| 感谢信 | 表达感谢和表扬 | 具体事迹、影响意义、感谢敬意；避免泛泛而谈 |
| 信访回复 | 答复群众诉求 | 受理情况、调查核实、处理意见、救济渠道/联系方式 |
| 理论评论 | 阐释观点、回应问题 | 问题、判断、论证、事实、价值收束；不要反套到普通公文 |
| 政策解读 | 说明政策内容和执行口径 | 政策依据、核心变化、适用对象、办理流程、问答提示 |

### Easy Confusions

- 请示 vs 报告: 有请求批准就是请示；只汇报情况就是报告。报告不得夹带"请予批准"。
- 批复 vs 复函: 有隶属关系、答复下级请示用批复；不相隶属单位之间答复用函。
- 通知 vs 通告: 内部或特定单位办理周知多用通知；面向社会公开遵守事项多用通告。
- 纪要 vs 会议记录: 纪要提炼议定事项并可用于执行；会议记录是原始过程材料。
- 方案 vs 计划: 方案重"如何组织实施专项任务"；计划重"未来一段时间做什么"。

## Formal Format Rules

### Title

- Common structure: `发文机关 + 关于 + 事由 + 的 + 文种`, such as `XX市人民政府关于开展安全生产专项整治的通知`.
- Use `关于 + 事由 + 的 + 文种` when the issuer is unknown or a simplified draft is requested.
- Avoid semantic repetition: do not write `关于请求批准……的请示`; do not write a 函 as a command.
- The title should identify the matter and document type. Do not replace a document title with a slogan.

### Main Recipient

- Write the main recipient flush left with a colon.
- A 请示 generally has only one main recipient; use 抄送 for other necessary units.
- Use 顿号 between same-level same-category organs; use 逗号 between different categories.
- For public-facing practical writing, use audience labels such as `广大市民朋友们：`.

### Body

- Opening: explain basis, background, purpose, problem, or incoming document. Do not start with unrelated grand meaning.
- Main part: arrange matters in a list when execution is needed. Clarify object, task, standard, deadline, responsible unit, and feedback.
- Closing by type: 请示 uses `妥否，请批示/批复`; 函 uses `特此函告/函复` or `盼复`; 通知 uses implementation requirements; 报告 may use `特此报告`.
- Keep one document to one main matter, especially for 请示、函、批复.

### Attachments, Signature, Date

- If attachments are mentioned, list them as `附件：1. XXX`; attachment names usually do not end with punctuation.
- Issuing unit and date usually align to the right. A normal date may be `2026年6月10日`.
- Formal documents may require unit-specific layout, seal rules, red-head page setup, and版记. Do not simulate unavailable seals or file numbers.
- The date should match the signing/issuing logic; do not invent it.

### Writing Relationship

- 上行文: 请示、报告. Be factual and respectful; do not decide for the superior.
- 下行文: 通知、通报、决定、批复. Be clear about requirements, responsibility, and deadlines.
- 平行文: 函. Use equal, consultative language; do not issue commands.

### Common Format Errors

- A report includes a hidden request for approval.
- A request has multiple main recipients or multiple matters.
- The title document type conflicts with the body purpose.
- The main recipient is missing or mismatched.
- An attachment is mentioned but not listed.
- Date, issuing unit, and title are inconsistent.
- `相关部门` or `各单位` is used where a responsible subject must be clear.

## People's Daily-Inspired Expression Patterns

Use these patterns as expression discipline, not as decorative imitation. Do not transfer commentary style into a routine notice or request.

### High-Frequency Structure Patterns

- Background-introduction pattern: reality/policy background -> object explanation -> basic judgment -> facts -> lesson. Suitable for reports, summaries, research reports, speech openings. Risk: background too large and detached from the unit's work.
- Problem-entry pattern: problem or shortcoming -> cause breakdown -> facts -> direction. Suitable for research reports,整改 reports, special reports. Risk: saying only "坚持问题导向" without a real problem.
- Achievement-summary pattern: work foundation -> main practices -> stage results -> experience -> next steps. Suitable for summaries, reports, briefings. Risk: stronger judgment than evidence.
- Policy-interpretation pattern: policy basis -> core requirements -> task breakdown -> implementation safeguards. Suitable for schemes, implementation opinions, notice attachments. Risk: rearranging policy words without turning them into local tasks.
- Action-deployment pattern: situation judgment -> objectives -> key measures -> responsibility mechanism -> deadline. Suitable for方案、通知、会议部署. Risk: continuous `要……` with verbs that have no object.
- Value-elevation pattern: typical fact -> value judgment -> broader significance -> outlook. Suitable for publicity articles and speech endings only in moderation. Risk: oversized ending in ordinary official writing.

### Logic Progression Rules

- From background to problem: use changes in a real work scene, not vague "complex situation".
- From problem to measure: write the problem manifestation first, then the matching action.
- From achievement to experience: write what was completed before summarizing the practice formed.
- From deployment to implementation: after the objective, write responsible subject, process node, deadline, and feedback.
- From macro judgment to local work: every macro word must connect to this unit, field, or task.
- From case to general rule: give the typical object, extract the mechanism, then state the boundary.
- Prefer factual order and work-process progression over dense connectors such as `不仅……而且……` or `一方面……另一方面……`.

### Paragraph Function

Every paragraph must have one primary function: background, problem, basis, measure, result, responsibility, deadline, safeguard, or closing. Do not stack several paragraphs that only explain significance.

Useful paragraph roles:

- Background paragraph: sets the boundary of the task.
- Problem paragraph: identifies object, link, impact.
- Measure paragraph: names the subject, action, method, and result.
- Responsibility paragraph: names牵头单位、配合单位、反馈方式、检查节点.
- Closing paragraph: returns to办理要求、执行提醒、报送节点、工作目标.

## Anti-AI Style Standard

### Fact Density

Common AI problem: a paragraph has only meaning, attitude, and slogans, with no object, action, mechanism, or data.

Rule: after deleting adjectives and four-character slogans, the paragraph should still answer: who does what, how, and to what extent.

Prefer:

- `我单位将办事材料由〔数量〕项压减至〔数量〕项，新增线上预审入口，减少群众现场补交材料次数。`

Avoid:

- `我单位持续优化服务能力，推动工作提质增效。`

### Judgment Strength

Match the evaluation word to evidence strength:

| Level | Expression | Use Condition |
| --- | --- | --- |
| 1 | 已启动、正在开展 | Only deployment or initial action exists |
| 2 | 有序推进、稳步推进 | Planned steps exist, results limited |
| 3 | 取得进展、初见成效 | Stage results or audience feedback exists |
| 4 | 取得明显成效、形成机制 | Data,制度、流程, or stable operation exists |
| 5 | 重大突破、历史性成就 | Authoritative recognition, key indicators, industry comparison, or historic node exists |

When evidence is weak, downgrade the judgment. 宁可稳妥，不要拔高.

### Sentence Rhythm

- Avoid continuous `要……要……要……`.
- Avoid overusing `不仅……而且……`, `既是……也是……`, `一方面……另一方面……`.
- Avoid every paragraph using the same pattern.
- Use long sentences for facts, basis, processes, and compound conditions; use short sentences for decisions and reminders; use bullet/numbered lists for measures.

### Abstract-Word Control

Abstract words are allowed only when followed by concrete content.

| Term | Use When | Do Not Use When | Must Be Followed By |
| --- | --- | --- | --- |
| 高质量发展 | development goal, industrial upgrading, comprehensive results | single small task or routine notice | indicator, project, quality change |
| 赋能 | technology/platform/finance actually supports something | no clear tool or object | object and method |
| 聚力 | multiple parties invest in one target | one department's routine work | participating subjects and target |
| 抓手 | explaining an implementation carrier | no project,制度, or platform | specific carrier name |
| 体系 | multi-level institutional arrangement exists | only scattered measures | components |
| 格局 | multi-subject or multi-region relation | ordinary work arrangement | participants and relation |
| 机制 | workflow, responsibility, feedback exists | temporary action only | mechanism name and operation |
| 动能 | economy, innovation, employment growth force | ordinary activity | source and manifestation |
| 生态 | innovation/business/culture multi-party environment | single system | subject relation and environmental change |
| 闭环 | discovery, handling, feedback, review exist | no feedback step | loop steps |
| 协同 | cross-department/level/region coordination | one department alone | who coordinates with whom |
| 提质增效 | quality and efficiency both evidenced | only routine推进 | quality and efficiency changes |
| 走深走实 | learning/policy implementation has stages | generic expression | concrete deepening action |
| 落地见效 | policy already executed and has result | just deployed | execution result |
| 凝心聚力 | mobilization, meeting, team-building | technical/business document | common goal |
| 久久为功 | long-term governance/ecology/style work | short-term task | long-term task and stage plan |
| 开创新局面/谱写新篇章 | publicity or speech ending with evidence | routine notice, request,方案正文 | concrete content of the "new" situation |

### Negative List

Watch for and rewrite:

- 空泛套话: direction and attitude without work information. Replace with object and action.
- 过度拔高: ordinary facts called "重大突破" or "历史性成就". Downgrade.
- 机械排比: neat but empty `要……要……要……`. Convert to task list.
- 四字词堆叠: `凝心聚力、提质增效、走深走实` in one sentence. Keep at most one necessary abstraction.
- 万能结尾: `谱写新篇章、开创新局面` in any document. Return to task, deadline, responsibility.
- 虚假具体: `相关部门、重点领域、关键环节` repeatedly used with no real boundary. Name the subject or use clear placeholders.
- 宣传腔过重: routine documents written as praise reports. Keep facts, reduce emotion.
- 理论腔过重: dense concepts with no implementation content. Attach each concept to a task.
- 文种错位: notice written as speech; request written as summary.
- 逻辑空转: from meaning to meaning, no new information.
- 缺少事实支撑: judgment without data, case, mechanism, or feedback.
- 动词无宾语: `扎实推进、全面加强` without what is being advanced or strengthened.
- 抽象词连续堆叠: `赋能、生态、动能、协同` explaining each other.
- 口号密度过高: more statements than facts.
- AI连接句式过密: connectors replace actual cause, sequence, and responsibility.

## Positive Rewrite Rules

### Open with Source and Object

- Weak: `为深入贯彻高质量发展要求，全面开创新局面，现就有关工作通知如下。`
- Better: `根据近期安全检查发现的问题，为规范仓储用电管理，现就开展专项排查有关事项通知如下。`

### Keep Background Relevant

- Weak: `当前形势深刻复杂，各项工作任务艰巨繁重。`
- Better: `今年以来，窗口咨询量明显增加，群众集中反映办理材料重复提交问题。`

### Make Problems Concrete

- Weak: `工作中还存在服务意识不强、落实不够有力等问题。`
- Better: `部分窗口一次性告知不够完整，群众补交材料次数偏多，影响办理效率。`

### Support Achievements

- Weak: `我单位扎实推进各项工作，取得显著成效。`
- Better: `我单位完成〔数量〕个点位改造，新增线上预约入口，平均等候时间较上季度缩短。`

### Give Deployment Objects and Responsibility

- Weak: `要全面加强管理，持续提升服务水平。`
- Better: `各科室于〔日期〕前完成台账更新，办公室汇总问题清单并跟踪整改进度。`

### Analyze Causes Beyond Attitude

- Weak: `主要是认识不够、措施不细、落实不力。`
- Better: `主要原因是材料流转依赖人工核对，跨科室数据未共享，导致重复录入和等待时间增加。`

### Match Measures to Problems

- Weak: `下一步要强化协同、优化机制、提升质效。`
- Better: `针对重复提交问题，统一材料目录，设置线上预审入口，明确窗口一次性告知责任。`

### Close on the Task

- Weak: `让我们凝心聚力、久久为功，奋力谱写事业发展新篇章。`
- Better: `请各单位结合实际抓好落实，并于〔日期〕前报送工作进展。`

## Type-Specific Drafting Templates

### 通知

Purpose: deploy matters or inform requirements.

Structure: basis/background -> matters -> specific requirements -> deadline -> contact/feedback.

Tone: clear, direct, executable.

Avoid: long significance paragraphs, publicity-style elevation, literary opening.

Useful headings: `一、工作事项` `二、具体要求` `三、报送时间`.

### 请示

Purpose: request approval, instruction, support, or transfer.

Structure: reason -> basis -> difficulty/necessity -> requested matter -> closing.

Tone: cautious, concise, procedure-respecting.

Avoid: writing a work summary, over-praising achievements, macro narrative.

Closing: `妥否，请批示。` or `以上请示如无不妥，请予批复。`

### 报告

Purpose: report situation, reflect problems, answer inquiry.

Structure: situation -> practices -> results -> problems -> next steps.

Tone: objective and complete; no hidden approval request.

Avoid: only reporting good news; propaganda-style praise.

### 工作总结

Purpose: review stage work.

Structure: overall situation -> main work -> results/experience -> shortcomings -> next steps.

Tone: realistic.

Avoid: all achievements and slogans. Use data, actions, and cases.

### 工作方案

Purpose: arrange an implementation path.

Structure: goals -> key tasks -> implementation steps -> division of responsibility -> safeguards.

Tone: concrete and executable.

Avoid: writing as an倡议 or commentary; measures must have enough granularity.

### 调研报告

Purpose: analyze situation and propose recommendations.

Structure: background -> current situation -> problems -> causes -> recommendations.

Tone: analytical, cautious, evidence-based.

Avoid: empty recommendations. Each recommendation should answer a problem.

### 讲话稿/发言稿

Purpose: meeting mobilization, deployment, summary, or exchange.

Structure: greeting -> situation/understanding -> key tasks -> implementation requirements -> closing.

Tone: has judgment and mobilization but must land on work.

Avoid: all slogans; overly dense theory concepts.

### 表态发言

Purpose: express stance and implementation commitment.

Structure: understanding -> attitude -> measures -> commitment.

Tone: firm but not exaggerated.

Avoid: only attitude, no measures.

### 简报/信息稿

Purpose: quickly reflect dynamics or experience.

Structure: lead -> practices -> stage results -> experience/next step.

Tone: short, factual, fresh.

Avoid: headline-only excitement or empty summary.

### 宣传稿

Purpose: show典型, policy, activity, or experience to the public.

Structure: scene -> facts -> people/practices -> results -> moderate meaning.

Tone: vivid but measured.

Avoid: excessive praise. Use details instead of admiration.

### 理论评论文章

Purpose: explain a viewpoint or respond to a problem.

Structure: problem -> judgment -> argument -> facts -> value closing.

Tone: logical, viewpoint-driven.

Avoid: transferring this style back into routine official documents.

## Useful Openings

- 根据式: `根据〔文件/会议/部署〕要求，为〔目的〕，现就有关事项通知如下。`
- 问题式: `近期，〔问题表现〕。为〔直接目标〕，经研究，决定〔事项〕。`
- 来文式: `你单位《关于〔事项〕的请示》（〔文号〕）收悉。经研究，现批复如下。`
- 汇报式: `现将〔阶段/专项〕工作开展情况报告如下。`
- 函告式: `为〔目的〕，拟〔事项〕。现就有关事项函告如下。`
- 调研式: `围绕〔主题〕，我们采取〔方式〕对〔对象〕开展调研，现将有关情况报告如下。`

## Useful Closings

- 通知: `请结合实际认真抓好落实，并于〔日期〕前将有关情况报〔单位〕。`
- 请示: `妥否，请批示。` / `以上请示如无不妥，请予批复。`
- 报告: `特此报告。`
- 函: `专此函达，盼复。` / `特此函复。`
- 方案: `各责任单位要按职责分工抓好落实，重要情况及时报告。`
- 倡议书: `让我们从现在做起、从身边做起，共同〔行动目标〕。`
- 宣传稿/讲话稿: may use moderate elevation only when facts support it.

## Heading Methods

Prefer accurate functional headings over forced parallelism.

- Action + object: `摸清底数，建好台账`
- Problem + measure: `聚焦薄弱环节，抓实整改提升`
- Goal + path: `围绕便民利民，优化服务流程`
- Responsibility + deadline: `压实主体责任，限期完成整改`
- Process + result: `统一受理标准，减少重复提交`

Do not force every heading into four characters or identical rhythm.

## Internal Scoring Rubric

Score before final delivery:

| Item | Points | High Standard | Low Signal |
| --- | ---: | --- | --- |
| Fact density | 20 | Most paragraphs include object, action, mechanism, data, or case | Mostly slogans and judgments |
| Document-type fit | 20 | Structure, tone, and ending fit type | Notice like speech; request like summary |
| Restraint | 15 | Judgment strength matches evidence | Strong judgment without support |
| Sentence naturalness | 15 | Varied rhythm, little mechanical parallelism | Repeated same structure |
| Abstract-word control | 15 | Abstract terms have concrete follow-up | Dense万能词 |
| Structural clarity | 15 | Paragraph functions clear and progression natural | Logic circles with no new information |

Handling:

- 90+: output directly.
- 80-89: compress boilerplate and strengthen concrete detail.
- 70-79: rewrite affected paragraphs.
- Below 70: rebuild the whole structure.

## Final Quality Checklist

- Is the document type correct for the relationship and purpose?
- Are issuer, recipient, matter, basis, time, responsibility, and requirement clear?
- Are there invented numbers, policies, leaders, meetings, or approvals? Remove them.
- Is the title consistent with the body?
- Is the main recipient correct? For 请示, is there only one?
- Are attachments, signature, and date consistent when included?
- Does every paragraph have a function?
- Does every abstract judgment have factual support?
- Are there too many `进一步、持续、不断、全面、切实、有效`?
- Are there continuous four-character phrases or repeated `要……要……要……`?
- Does the ending return to办理要求、责任、时限, unless it is truly a speech/publicity article?

## User Input Template

When helpful, infer missing items and proceed. Ask only when missing facts make the document unusable.

```
文种：
使用场景：
发文/讲话主体：
面向对象：
材料要点：
希望语气：
篇幅要求：
是否需要标题：
是否需要落款：
特殊要求：
```
