# Grammar Mentor

> An AI-powered English grammar detection expert with personalized knowledge tracking — packaged as a Codex Skill.

Grammar Mentor analyzes your English sentences through a structured 5-panel workflow: error detection, sentence classification, tree-form component breakdown with inline knowledge annotations, targeted reminders based on your learning history, and automatic archive updates. It remembers what you've learned, flags when you slip, and explains grammar through the lens of your existing knowledge.

---

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| **5-Panel Analysis** | Grammar check → Structure classification → Tree breakdown → Targeted reminders → Archive update |
| **Knowledge-First Analysis** | Every explanation references rules you've already learned, reinforcing rather than repeating |
| **In-Tree Annotations** | `📚` knowledge match / `❌` rule violation / `⚠️` deviation warning / `💡` tip verification — all inline on the syntax tree |
| **📐 Clause Normalization** | Restores moved or omitted elements to show underlying word order (e.g., `the book I bought` → *I bought that*) |
| **Paragraph Mode** | Splits multi-sentence input, analyzes each, then checks cross-sentence consistency (tense, pronoun chains, cohesion) |
| **Personal Archive** | Knowledge base (you edit), deviation table (auto-maintained), learning goals (auto-maintained) — all persisted as Markdown |

---

## 📂 Architecture

```
grammar-mentor/
├── SKILL.md                          ← Main instructions
├── agents/openai.yaml                ← UI metadata
├── knowledge/
│   └── knowledge-base.md             ← 📝 Your grammar knowledge (17 rules, ID + description + details + examples)
└── references/
    ├── deviations.md                 ← 🤖 Auto-maintained error records
    ├── learning-goals.md             ← 🤖 Auto-maintained learning goals
    └── examples.md                   ← 📖 5 worked output examples
```

---

## 🚀 Usage

Just send an English sentence. The skill auto-triggers:

```
This means that a DNA database may have a lot of data from some regions and not others.
```

And you get a full 5-panel breakdown — grammar errors, structure classification, a syntax tree with your knowledge base rules annotated inline, deviation warnings, and archive updates.

---

## 🔧 How It Works

```
👤 User Input
    │
    ├── Single sentence → 5 panels
    └── Paragraph → split → per-sentence + cross-sentence check
                           │
                    Panel 3: The Hub
                    ┌─────────────────┐
                    │  📚 Knowledge    │  ← rules from your knowledge base
                    │  ❌ Violations   │  ← when you break a rule you know
                    │  ⚠️ Deviations  │  ← recurring mistake patterns
                    │  💡 Tips         │  ← tip confirmations
                    │  📐 Normalize    │  ← restore clause word order
                    └─────────────────┘
```

---

## 📋 Knowledge Base Format

Each rule follows a structured template — add new knowledge as you learn:

```markdown
### [SS-06] 非谓语动词作后置定语

触发条件：

描述：
过去分词、现在分词、不定式均可修饰名词作后置定语...

细节知识点补充：
1. 不定式 to do：表将来/目的
2. 现在分词 doing：表主动/进行
3. 过去分词 done：表被动/完成

示例：
- ✅ a book written by her
```

The skill automatically picks up and annotates any rule you add.

---

## 🎯 适用人群

### 你是谁？

| 如果你… | Grammar Mentor 可以… |
|---------|---------------------|
| 正在备考雅思/托福/GRE/GMAT，写作总被扣语法分 | 每句话拆到成分级，让你看清自己错在哪一类问题上 |
| 写过英文论文/邮件，每次改语法都是"凭感觉" | 所有解释基于你学过的语法规则，不是玄学，不是语感 |
| 系统学过语法但一到写句子就忘 | 分析时自动关联你知识库里已有的规则——"你学过的 SVO 结构在此体现为…" |
| 语法基础知识已经扎实，想查缺补漏 | 偏差表自动记录你的常犯错误类型，每次分析主动预警 |
| 想从"会写对"进阶到"能讲清为什么对" | 树状图 + 📐 归一化还原让你理解从句的内部结构，而不是死记硬背 |

### 你的场景？

- **写作自查**：写完后把拿不准的句子丢进来，5 秒出结果
- **精读拆解**：读到长难句看不懂？树状图拆到成分级，一眼看清主谓宾
- **段落润色**：一整段丢进来，逐句分析 + 跨句检查时态一致性、代词指代链
- **语法复习**：知识库就是你的语法笔记本——学一条加一条，模型自动帮你巩固

---

## 📝 中文简介

**Grammar Mentor** 是一个基于个人语法知识库的英文句子分析技能。它不是通用语法检查器——它围绕**你已经学过的语法知识**来工作：分析句子时优先用你知识库里的规则解释现象，发现违反时标注纠偏，记录你的常犯错误并主动预警。

核心设计理念很简单：**不重复讲你已经会的，不遗漏你容易错的。**

每句分析输出五个板块——语法错误排查、句型判定、树状成分拆解（知识库/偏差/归一化标注全挂在上面）、确认摘要、个人档案自动更新。如果是段落，额外加上时态一致性、代词指代链、衔接连贯等跨句检查。
