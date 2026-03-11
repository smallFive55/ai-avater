# AI 分身架构
这是一个AI决策分身，基于你的认知与记忆，帮你完成规划。

## 一、认知（cognition）

1. 决策的原则？
2. 风险的态度？
3. 工作的哲学？
4. 判断的方式？

## 二、记忆（memory）

1. 你做过什么决策？决策的逻辑
2. 技能栈
3. 某次冲突经历
4. 某次成功决策
5. 某次失败决策

---

## 功能使用说明

### 更新认知

将你的原则、哲学、判断方法等同步到 `cognition/` 目录，AI 分身会据此做出更贴近你的判断。

**触发方式**：说「更新认知」「更新原则」「更新哲学」「更新判断方法」「更新风险态度」「更新高效工作」，或使用 **@update-cognition**。

**认知维度与对应文件**：

| 关键词     | 目标文件                     |
|------------|------------------------------|
| 原则       | `cognition/principles.md`     |
| 哲学       | `cognition/philosophy.md`     |
| 判断方法   | `cognition/judgment-method.md`|
| 风险态度   | `cognition/risk-attitude.md`  |
| 高效工作   | `cognition/efficient-work.md` |

**示例**：「更新原则：重要决策前先列出利弊清单」「@update-cognition 我的风险态度是偏保守」

---

### 更新记忆

将你的决策、成功、失败、冲突等经历记录到 `memory/` 目录，供 AI 分身参考学习。

**触发方式**：说「记录记忆」「记录决策」「记录成功」「记录失败」「记录冲突」「更新技能栈」「记录部门重点」「记录完成」，或使用 **@update-memory**。

**记忆类型与对应位置**：

| 关键词     | 目标位置                     |
|------------|------------------------------|
| 决策       | `memory/decisions/`          |
| 成功       | `memory/successes/`         |
| 失败       | `memory/failures/`          |
| 冲突       | `memory/conflicts/`         |
| 技能栈     | `memory/skills/skills.md`    |
| 部门重点   | `memory/department-focus/`   |
| 已完成     | `memory/completed-tasks/`    |

**示例**：「记录决策：上周选择了方案 A，因为…」「记录一次成功：这次项目能成是因为…」「@update-memory 更新技能栈，新增了 Vue3」

---

### 已完成任务

将已完成的事项记录到 `memory/completed-tasks/`，供今日待办查询时自动过滤，避免重复展示。

**触发方式**：说「记录完成」「记录今日完成」或使用 **@update-memory**。

**存储位置**：`memory/completed-tasks/completed-YYYYMMDD.md`（按当日日期）。若当日文件已存在则追加到「事项列表」下。

**格式建议**：`- 任务描述（来源：focus-YYYYMMDD / decision-NNN / 组别等）`，来源便于与待办匹配过滤。

**示例**：「记录完成：登录优化概要设计」