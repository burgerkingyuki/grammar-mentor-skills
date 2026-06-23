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

## 🎯 Built For

- English learners who want grammar explanations in their native language (Chinese)
- Anyone who wants personalized, non-repetitive grammar feedback
- Writers who want to understand *why* something is correct or wrong, not just *that* it is
