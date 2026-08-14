# Step-by-Step Ask — 逐个提问式需求沟通 Skill

![License](https://img.shields.io/badge/license-MIT-blue)

An AI Agent skill that collects requirements one question at a time, so the AI fully understands the task before acting. / 一个让 AI 逐个提问、先把需求问清楚再动手的 Agent Skill。

---

## 中文说明

### 这是什么

当你说「一步一步来」「别急，先问清楚」时，这个 Skill 会让 AI 进入追问模式：每轮只问一个问题，像聊天一样逐步收集信息，最后复述完整需求并等你确认后才开始执行。适合复杂任务、需求模糊、或你想控制节奏的场景。

### 核心规则

- 每轮只问一个问题，像对话一样自然追问，不抛问卷
- 根据回答判断信息完整度，知道何时停止追问
- 执行前必须复述完整需求理解，你确认后才动手
- 复述有误时更新理解，再次确认

### 触发方式

说出以下关键词即可触发：

- 「一步一步来」「一步步来」
- 「别急，先问清楚」「慢点，先搞清楚」
- 「先问清楚」
- 任何表达「不要急着执行，先把需求搞清楚」的意思

### 安装

```bash
# 安装到 .agents/skills 目录（跨 Agent 平台生效）
mkdir -p ~/.agents/skills/step-by-step-ask
cp SKILL.md ~/.agents/skills/step-by-step-ask/
```

或在 TRAE 设置 > 技能与命令中导入本目录。

### 使用示例

用户说：「别急，先问清楚，我要你帮我写一篇公众号文章」

AI 会逐个确认选题方向、目标读者、篇幅、重点，最后复述：「我理解了，你要写一篇关于 XX 主题的 XX 风格的公众号长文，目标读者是 XX……对吗？」确认后才开始写。

### 许可证

[MIT](./LICENSE)

---

## English

### What is this

When you say "step by step" or "ask me clearly first", this skill puts the AI into a question mode: one question per turn, gathering information like a natural conversation, then restating the full understanding and waiting for your confirmation before executing. Great for complex tasks, vague requirements, or when you want to control the pace.

### Core Rules

- Ask exactly one question per turn — a conversation, not a questionnaire
- Judge information completeness from your answers and stop at the right time
- Restate the full requirement understanding before executing; only start after your confirmation
- If the restatement is corrected, update the understanding and confirm again

### Triggers

Say any of these to activate:

- 「一步一步来」/「一步步来」(step by step)
- 「别急，先问清楚」/「慢点，先搞清楚」(don't rush, clarify first)
- 「先问清楚」(clarify first)
- Anything meaning "understand the requirements fully before acting"

### Installation

```bash
mkdir -p ~/.agents/skills/step-by-step-ask
cp SKILL.md ~/.agents/skills/step-by-step-ask/
```

Or import the directory via your agent's skill manager (e.g. TRAE Settings > Skills).

### Example

User: "Don't rush — clarify first. I want you to write a WeChat article for me."

The AI asks about topic, audience, length and focus one at a time, then restates: "Let me confirm — a Khazix-style long-form article on XX, for XX audience, about XX words, emphasizing XX. Correct?" and only starts writing after confirmation.

### License

[MIT](./LICENSE)
