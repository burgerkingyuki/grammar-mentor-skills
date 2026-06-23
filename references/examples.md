# 输出结构参考示例

> 以下为完整 5 面板分析格式，供模型参考输出风格与排版规范。

---

## 示例一：简单句（SVP 结构，无错误）

**用户输入：**
```
People are not aware of the significance of this book.
```

---

**【1. 语法错误排查】**

该句语法完全正确，无任何错误。

---

**【2. 句子整体结构判定】**

- 句型类别：**简单句**
- 基本句型归属：**SVP**（主语 + 系动词 + 表语）

---

**【3. 逐层成分拆解（统一呈现）**

```
[People are not aware of the significance of this book.]
   │
   ├── 主语（Subject）：People
   │     📚 知识点：你学过的 知识-简单句 → 主语/宾语/表语的变化（名词作主语）
   │
   ├── 谓语动词（Predicate Verb / Linking Verb）：are
   │     📚 知识点：你学过的 知识-简单句 → 5大结构 → SVP（系动词，连接主语与表语）
   │
   ├── 表语（Predicative / Subject Complement）：aware
   │     💡 tip 验证：系动词后接表语，不是宾语 — 此处 are 为系动词，aware 为形容词表语
   │     ├── 修饰语（否定副词）：not（修饰 aware）
   │     └── 形容词补足语（Adjective Complement）：of the significance of this book
   │           ├── 介词：of
   │           └── 介词宾语（Object of Preposition）：the significance of this book
   │                 ├── 中心名词：significance
   │                 └── 后置定语（介词短语）：of this book
   │                       ├── 介词：of
   │                       └── 介词宾语：this book
   │
   └── 功能说明：全句描述主语 People 对这本书重要性的认知状态
       SVP 结构：People → are → aware（+ 形容词补足语 of...）
```

---

**【4. 确认摘要】**

```
📚 知识复现：2 项
   ✅ 知识-简单句 → 5大结构 → SVP（系动词 + 表语）
   ✅ 知识-简单句 → 主语/宾语/表语的变化（名词作主语）

⚠️ 偏差预警：0 项

🟢 未触发：#001（定语 vs. 补足语）、#002（状语 vs. 定语）、#003（表语 vs. 宾语）、#004（成分层级意识）
```

---

**【5. 个人档案更新】**

- **deviations.md**：无新增偏差，无触发。
- **learning-goals.md**：无变更。

---

**【全句主干总结】**
→ People + are + aware → 该句为 **SVP** 结构，of... 为形容词 aware 的补足语，非全句宾语。

---

---

## 示例二：主从复合句（含语法错误）

**用户输入：**
```
The teacher asked the students why are they late.
```

---

**【1. 语法错误排查】**

| # | 错误类型 | 位置 | 修改 |
|---|---------|------|------|
| ① | 句式结构 | `why are they late` | 宾语从句应用陈述语序 → `why they are late` |

修正后：The teacher asked the students why **they are** late.

---

**【2. 句子整体结构判定】**

- 句型类别：**主从复合句**
- 主句基本句型：**SVOO**（主语 + 及物动词 + 间接宾语 + 直接宾语）
  - 间接宾语：the students
  - 直接宾语：why they are late（宾语从句）

---

**【3. 逐层成分拆解（统一呈现）**

```
[The teacher asked the students why they are late.]
   │
   ├── 主语（Subject）：The teacher
   │
   ├── 谓语动词（Predicate Verb）：asked
   │     📚 知识点：你学过的 知识-简单句 → 5大结构 → SVOO（ask 可接双宾语）
   │
   ├── 间接宾语（Indirect Object，全句宾语）：the students
   │     📚 知识点：你学过的 知识-简单句 → 主语/宾语/表语的变化（名词作宾语）
   │
   ├── 直接宾语（Direct Object，全句宾语 — 宾语从句）：why they are late
   │     📚 知识点：你学过的 知识-复合句 → 名词性从句 → 宾语从句（wh- 引导）
   │     💡 tip 验证：名词性从句在句中充当名词的角色（此处作直接宾语）
   │     ⚠️ 偏差预警：#004 成分层级意识 — 以下为从句内部成分
   │     │
   │     └── ┌────────── [从句内部成分] ──────────┐
   │         │                                     │
   │         ├── 连词（Conjunction）：why（引导宾语从句，同时在从句中作原因状语）
   │         │
   │         ├── 主语（Subject，从句主语）：they
   │         │
   │         ├── 谓语动词（Predicate Verb，从句谓语 — 系动词）：are
   │         │     📚 知识点：你学过的 知识-简单句 → 谓语动词时态（一般现在时）
   │         │
   │         └── 表语（Predicative，从句表语）：late
   │         │     💡 tip 验证：系动词后接表语，不是宾语 — 此处 are 为系动词，late 为形容词表语
   │         │
   │         └────────────────────────────────────┘
   │
   └── 功能说明：全句表达"老师问学生为什么迟到"
       主句层 SVOO：teacher → asked → students（间接宾语）+ [why 宾语从句]（直接宾语）
       从句层 SVP：they → are → late
```

---

**【4. 确认摘要】**

```
📚 知识复现：3 项
   ✅ 知识-简单句 → 5大结构 → SVOO（ask 双宾语结构）
   ✅ 知识-复合句 → 名词性从句 → 宾语从句（wh- 引导）
   ✅ 知识-简单句 → 谓语动词时态（一般现在时：are）

⚠️ 偏差预警：1 项
   ⚠️ #004 成分层级意识 — why 从句为主句的直接宾语，从句内部还有自己的主系表结构

🟢 未触发：#001、#002、#003
```

---

**【5. 个人档案更新】**

- **deviations.md**：无新增偏差。#004 已预警。
- **learning-goals.md**：无变更。

---

**【全句主干总结】**
→ The teacher + asked + the students + [why 宾语从句] → 主句为 **SVOO** 结构。

---

## 格式速查

### 树状图行符

```
├──  中间节点（非最后）
└──  最后节点
│    垂直连线
│    子节点缩进（4 空格 + │）
```

### 行内标记速查

| 标记 | 用途 |
|------|------|
| `📚 知识点：你学过的 [模块] → [知识点]` | 知识库复现 |
| `💡 tip 验证：[tip内容]` | tip 匹配 |
| `⚠️ 偏差预警：#编号 [类型] — [提醒]` | 偏差预警 |
| `┌── [层级标记] ──┐` / `└────────────┘` | 从句层级视觉分隔 |

### 成分标注格式

```
宾语（Object，全句宾语 — 宾语从句）
状语（Adverbial，从句内部状语）     ← 必须标注层级归属
主语（Subject，从句主语）           ← 必须标注层级归属
```

### Panel 4 确认摘要模板

```
📚 知识复现：[N] 项
   ✅ [模块] → [知识点]
   ✅ ...

⚠️ 偏差预警：[N] 项
   ⚠️ #编号 [类型] — [位置]
   ...

🟢 未触发：[列出未触发的编号]
```

---

## 示例三：知识规则违反（含双重检查）

**用户输入：**
```
She arrived the station early.
```

**涉及知识规则：** 知识-简单句 → tips → "及物动词后接宾语；不及物动词不接宾语"

---

**【1. 语法错误排查】**

| # | 错误类型 | 位置 | 修改 |
|---|---------|------|------|
| ① | 句式结构 | `arrived the station` | ❌ 知识违反：知识-简单句 → "不及物动词不接宾语" — `arrive` 为不及物动词，不可直接接宾语，应改为 `arrived at the station` |

修正后：She arrived **at** the station early.

---

**【2. 句子整体结构判定】**

- 句型类别：**简单句**
- 基本句型归属：**SV**（主语 + 不及物动词）
  - `arrive` 为不及物动词，正确结构为 SV（+ 状语）

> 此句触发了你知识库中的核心规则，详见 Panel 3。

---

**【3. 逐层成分拆解（统一呈现）**

```
[She arrived the station early.]   ← 含知识违反
   │
   ├── 主语（Subject）：She
   │
   ├── 谓语动词（Predicate Verb）：arrived
   │     📚 知识点：你学过的 知识-简单句 → 5大结构 → SV（arrive 为不及物动词）
   │     ❌ 知识违反：知识-简单句 → tips → "不及物动词不接宾语"
   │        → arrive 是不及物动词，后不应直接跟名词作宾语
   │        → 正确结构：arrive + at/in + 地点（介词短语作状语）
   │
   ├── ~~宾语（Object）~~ ← 错误标注：the station
   │     纠正后应为：
   │     状语（Adverbial — 介词短语）：at the station
   │     │   ├── 介词：at
   │     │   └── 介词宾语：the station
   │
   ├── 状语（Adverbial）：early（副词，修饰 arrived）
   │
   └── 功能说明：句子意图表达"她早早就到了车站"
       但 arrive 为不及物动词，应使用 SV 结构 + 介词短语状语
       正确结构：She → arrived（SV）+ at the station（状语）+ early（状语）
```

---

**【4. 确认摘要】**

```
📚 知识复现：1 项
   ✅ 知识-简单句 → 5大结构 → SV（arrive 为不及物动词，属 SV 结构）

⚠️ 偏差预警：0 项

🟢 未触发：#001、#002、#003、#004

❌ 知识违反：1 项
   ❌ 知识-简单句 → "不及物动词不接宾语" — arrive 不可直接接 the station
```

---

**【5. 个人档案更新】**

- **deviations.md**：是否新增偏差取决于用户对此次违反的反应。如用户表示理解并纠正，可新增 #005 记录（不及物动词误用为及物）。
- **learning-goals.md**：无变更。

---

**【全句主干总结】**
→ She + arrived（SV 结构）→ arrive 为不及物动词，正确句应为 She arrived **at** the station early.

---

## 示例四：段落分析模式（3 句段落）

**用户输入：**
```
The company launched a new product last month. It is very popular among young consumers. The sales team are working hard to promote it.
```

---

**【段落拆分】（共 3 句）**

① The company launched a new product last month.
② It is very popular among young consumers.
③ The sales team are working hard to promote it.

---

── 句 ① ──

**【1. 语法错误排查】**
该句语法完全正确，无任何错误。

**【2. 句子结构判定】**
- 句型：简单句 / SVO（The company + launched + a new product + 状语 last month）

**【3. 成分拆解】**
```
[The company launched a new product last month.]
   │
   ├── 主语（Subject）：The company
   │
   ├── 谓语动词（Predicate Verb）：launched
   │     📚 知识点：[SS-02 谓语动词时态]：一般过去时（细节知识点1：一般时态表过去事实）
   │
   ├── 宾语（Object）：a new product
   │     📚 知识点：[SS-01 五大基本句型]：及物动词 launch + 宾语 → SVO 结构
   │
   └── 状语（Adverbial）：last month（时间状语）
```

── 句 ② ──

**【1. 语法错误排查】**
该句语法完全正确，无任何错误。

**【2. 句子结构判定】**
- 句型：简单句 / SVP（It + is + popular + 状语 among young consumers）

**【3. 成分拆解】**
```
[It is very popular among young consumers.]
   │
   ├── 主语（Subject）：It（代词，指代句①的 a new product）
   │
   ├── 谓语动词（Predicate Verb — 系动词）：is
   │     📚 知识点：[T-01 系动词后接表语，不是宾语]：is 为系动词，后接表语
   │
   ├── 表语（Predicative）：popular
   │     ├── 修饰语：very（程度副词）
   │     └── 形容词补足语：among young consumers
   │           ├── 介词：among
   │           └── 介词宾语：young consumers
   │
   └── 功能说明：SVP 结构 — It → is → popular（+ 范围状语 among...）
```

── 句 ③ ──

**【1. 语法错误排查】**

| # | 错误类型 | 位置 | 修改 |
|---|---------|------|------|
| ① | 主谓一致 | `team are` | `team` 为集合名词，英式英语可用复数 `are`，美式英语倾向于单数 `is`。此处按语境：若强调团队成员个体 → `are` 可接受；若视 team 为整体 → 建议 `is` |

> 不算严格错误，属于英美用法差异，标注供参考。

**【2. 句子结构判定】**
- 句型：简单句 / SV（The sales team + are working + 状语 hard + 状语 to promote it）

**【3. 成分拆解】**
```
[The sales team are working hard to promote it.]
   │
   ├── 主语（Subject）：The sales team
   │
   ├── 谓语动词（Predicate Verb）：are working
   │     📚 知识点：[SS-02 谓语动词时态]：现在进行时（细节知识点2：进行时态 be doing，强调当前正在进行的动作）
   │
   ├── 状语（Adverbial）：hard（程度状语，修饰 working）
   │
   ├── 状语（Adverbial）：to promote it（目的状语，不定式短语）
   │     ├── 不定式标记：to
   │     ├── 动词：promote
   │     └── 宾语（短语内部宾语）：it（代词，指代句①的 a new product）
   │
   └── 功能说明：SV + 双重状语 — team → are working（+ hard 程度 + to promote it 目的）
```

---

**【4. 段落跨句一致性检查】**

```
📌 时态一致性
  句① launched（一般过去）→ 句② is（一般现在）→ 句③ are working（现在进行）
  判定：⚠️ 时态有切换，但逻辑合理
  — 句① 讲过去的 launch 事件（过去时）
  — 句② 讲当前 popularity 状态（现在时）
  — 句③ 讲当前正在进行的 promote 动作（现在进行时）
  结论：时态切换符合叙事逻辑（过去事件 → 当前状态/动作），无需修改

📌 代词指代链
  句① 引入：a new product（先行词）
  句② It → 指代 a new product ✅（单数一致，指代清晰）
  句③ it → 指代 a new product ✅（单数一致，指代清晰）
  判定：清晰 ✅

📌 主谓/数的一致性
  句① The company（单数）+ launched ✅
  句② It（单数）+ is ✅
  句③ The sales team（集合名词）+ are working（复数）— 见句③注释
  跨句一致性：句②主语 It（单数）与句③主语 team（集合名词）不同指代对象，无一致性问题

📌 衔接与连贯
  句①→句②：new product → It（代词衔接自然）
  句②→句③：popular → promote（语义递进：产品受欢迎 → 团队努力推广）
  判定：连贯 ✅
```

---

**【5. 段落确认摘要】**

```
📚 知识复现（跨句汇总）：4 项
   ✅ [SS-01 五大基本句型]：句① SVO、句② SVP、句③ SV
   ✅ [SS-02 谓语动词时态]：句① 一般过去、句② 一般现在、句③ 现在进行
   ✅ [T-01 系动词后接表语，不是宾语]：句② is + popular（SVP）
   ✅ [SS-05 主语/宾语/表语的成分类型]：句②③ 代词 it 作主语/宾语

⚠️ 偏差预警：0 项

🟢 未触发：#001、#002、#003、#004

❌ 知识违反：0 项
```

---

**【6. 档案更新】**

- **deviations.md**：无新增偏差。
- **learning-goals.md**：无变更。

---

**【段落主干总结】**
→ 过去事件（句① launch）→ 当前状态（句② popular）→ 当前行动（句③ promote），时态切换合理，代词指代链清晰。