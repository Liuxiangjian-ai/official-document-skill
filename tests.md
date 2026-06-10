# Tests

Use these as manual regression tests after changing `SKILL.md`.

## Test 1: 文种识别

Prompt:

```text
用 $official-document-skill 写一份向上级申请购买应急排水设备经费的材料。材料：现有设备老化，近期强降雨增多，需申请15万元。
```

Pass criteria:

- Chooses 请示, not 报告 or 通知.
- Contains reason, necessity, requested amount, and `妥否，请批示/批复`.
- Does not invent policy documents or exact dates.

## Test 2: 通知可执行性

Prompt:

```text
用 $official-document-skill 写通知：要求各社区排查独居老人用电安全，月底前报送台账。
```

Pass criteria:

- Contains recipient, task, scope, deadline, and reporting requirement.
- Avoids long macro background and excessive slogans.
- Uses concrete actions such as入户排查、隐患记录、整改反馈.

## Test 3: 报告不夹带请示

Prompt:

```text
用 $official-document-skill 写报告：汇报食品安全专项检查情况，有发现问题和下一步计划。
```

Pass criteria:

- Structure includes情况、做法/发现、问题、下一步.
- Does not include approval request.
- Tone is objective and evidence-aware.

## Test 4: 降 AI 味

Prompt:

```text
用 $official-document-skill 改写：坚持问题导向，强化责任担当，形成工作合力，推动工作走深走实、落地见效。
```

Pass criteria:

- Replaces slogans with subject, task, mechanism, feedback, or deadline.
- Does not keep more than one abstract phrase unless supported.
- Output is usable in a real公文段落.

## Test 5: 人民日报风格边界

Prompt:

```text
用 $official-document-skill 写一个基层安全排查通知，要求有人民日报风格。
```

Pass criteria:

- Borrows fact-density and restrained progression, not评论腔 or宏大叙事.
- Does not use literary scene-setting or value elevation in the notice body.
- Ends with task, responsibility, and deadline.
