---
name: update-cognition
description: 更新 AI 数字分身的认知文件。当用户说「更新认知」「更新原则」「更新哲学」「更新判断方法」「更新风险态度」「更新高效工作」或 @update-cognition 时触发。将用户提供的新原则、哲学、判断方法、风险态度或高效工作内容写入 cognition/ 对应文件。
---

# 更新认知

将用户输入同步到 `cognition/` 下的对应认知文件，无需用户手写「更新认知到 cognition」等完整指令。

## 认知文件映射

| 用户说法 / 关键词 | 目标文件 |
|------------------|----------|
| 原则、principles | `cognition/principles.md` |
| 哲学、philosophy | `cognition/philosophy.md` |
| 判断方法、judgment | `cognition/judgment-method.md` |
| 风险态度、risk | `cognition/risk-attitude.md` |
| 高效工作、efficient-work | `cognition/efficient-work.md` |

若用户未指定目标，根据内容语义推断；无法推断时，询问用户要更新到哪个认知维度。

## 执行流程

1. **解析意图**：从用户输入识别要更新的认知维度（原则/哲学/判断方法/风险态度/高效工作）。
2. **读取现有**：读取 `cognition/` 下对应 `.md` 文件，了解当前结构与风格。
3. **合并更新**：在合适位置追加或替换内容，保持原有格式与层级。
4. **更新日期**：将文件末尾的「*最后更新：YYYY-MM-DD*」改为当日日期。

## 触发示例

- 「更新认知：xxx」
- 「更新原则：xxx」
- 「更新哲学：xxx」
- 「@update-cognition xxx」
- 「把 xxx 加到认知里」

## 注意事项

- 保持 Markdown 层级与现有文件一致。
- 新增内容尽量融入既有结构，避免重复。
- 若为全新维度或大段内容，可新增一级标题后再追加。