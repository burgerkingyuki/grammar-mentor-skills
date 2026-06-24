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

---

## 示例五：从句连接词归一化（📐 还原）

**用户输入：**
```
The book that I bought is better than the one she recommended.
```

---

**【1. 语法错误排查】**

该句语法完全正确，无任何错误。

---

**【2. 句子整体结构判定】**

- 句型类别：**主从复合句**（含两个定语从句）
- 主句：**SVP**（The book + is + better + than 比较状语从句）
- 定语从句 ①：that I bought（修饰 the book — 关系代词作宾语）
- 定语从句 ②：she recommended（修饰 the one — 关系代词作宾语且省略）

---

**【3. 逐层成分拆解（统一呈现）**

```
[The book that I bought is better than the one she recommended.]
   │
   ├── 主语（Subject）：The book
   │     │
   │     └── 后置定语（Attributive — 定语从句 ①）：that I bought
   │           │
   │           ├── 关系代词（Relative Pronoun — 作 bought 的宾语）：that
   │           │     📐 还原：I bought that（that 作 bought 的宾语，还原到动词后）
   │           │     📚 知识点：[CX-02 定语从句]：关系代词 that 代替先行词 the book，在从句中作宾语
   │           │     📚 知识点：[T-05 定语从句关系代词省略]：此处 that 可省略（作宾语）但未省略
   │           │
   │           └── [定语从句内部]
   │                 ├── 主语：I
   │                 └── 谓语：bought（及物动词，一般过去时；that 为其宾语）
   │
   ├── 谓语动词（Predicate Verb — 系动词）：is
   │
   ├── 表语（Predicative）：better
   │     📚 知识点：[T-01 系动词后接表语，不是宾语]：is + better（形容词表语 → SVP）
   │
   └── 比较状语从句（Comparative Adverbial Clause）：than the one she recommended
         │
         ├── 连词（Conjunction）：than
         │
         └── 比较对象：the one she recommended
               │
               ├── 中心代词：one（= the book）
               │
               └── 定语从句 ②：she recommended（省略了关系代词 that/which）
                     │
                     ├── 省略的关系代词：∅（= that/which，作 recommended 的宾语）
                     │     📐 还原：she recommended that（that 作 recommended 的宾语）
                     │     📚 知识点：[T-05 定语从句关系代词省略]：作宾语时省略（细节知识点1）
                     │
                     └── [定语从句内部]
                           ├── 主语：she
                           └── 谓语：recommended（一般过去时；省略的 that 为其宾语）
```

**对比两个定语从句的连接词：**

| 从句 | 连接词 | 作什么成分 | 📐 还原 | 是否省略 |
|------|--------|-----------|---------|---------|
| that I bought | that | bought 的宾语 | I bought that | 否（显式保留） |
| she recommended | ∅ (that/which) | recommended 的宾语 | she recommended that | 是（已省略） |

---

**【4. 确认摘要】**

```
📚 知识复现：3 项
   ✅ [CX-02 定语从句]：两个定语从句，关系代词作宾语
   ✅ [T-05 定语从句关系代词省略]：she recommended 中 that 已省略
   ✅ [T-01 系动词后接表语]：is better → SVP

⚠️ 偏差预警：0 项
🟢 未触发：#001、#002、#003、#004
❌ 知识违反：0 项
```

---

**【全句主干总结】**
→ The book（+ 定语从句 ① that I bought）+ is + better + than the one（+ 定语从句 ② ∅ she recommended）→ **SVP**。

---

## 📐 归一化速查

| 从句类型 | 连接词 | 还原 |
|---------|--------|------|
| 定语从句（宾） | The book that I bought | I bought **that** |
| 定语从句（主） | The man who spoke | 无需还原（who 即主语） |
| 定语从句（状） | The way consumers approach | consumers approach **in this way** |
| 定语从句（定） | The man whose car... | **his** car... |
| 宾语从句（纯连词） | I know that he is right | that 不作成分 |
| 主语从句（宾） | What she said is true | she said **what** |
| 表语从句（纯连词） | The truth is that he left | that 不作成分 |

---

## 示例六：长难句拆解（Split & Simplify）

**用户输入：**
```
In those far-off days, it was taken for granted that the critics of major papers would write in detail and at length about the events they covered.
```

---

*(Panel 1-3 省略，此处仅展示 Panel 3B)*

---

**【3B-1 断开】拆分为 4 个简单句**

```
原句：In those far-off days, it was taken for granted that the critics of major papers
      would write in detail and at length about the events they covered.

① [People] took it for granted that [critics would write about the events].
   ← 主句还原为主动语态 SVOC（took + it + for granted + that 宾语从句）
   ← 补回隐含主语 People

② Critics would write in detail and at length about the events.
   ← that 主语从句（外置的真正主语），that 仅连接不作成分，已剥离

③ The critics were of major papers.
   ← 还原 of major papers 为独立系表句，展示后置定语的内在含义

④ [The critics] covered the events.
   ← 定语从句 they covered，省略的关系代词 that/which 已还原为宾语
```

---

**【3B-2 简化】去扩展，留核心**

```
① 原简单句：[People] took it for granted that [critics would write about the events].
   ──→ 核心：People + took + it + for granted → SVOC
   去掉：~~that 宾语从句~~（简化视角视为扩展）

② 原简单句：Critics would write in detail and at length about the events.
   ──→ 核心：Critics + would write → SV
   去掉：~~in detail and at length~~（方式状语）、~~about the events~~（关于状语）

③ 原简单句：The critics were of major papers.
   ──→ 核心：Critics + were + of major papers → SVP
   无扩展成分可去（of major papers 为表语核心）

④ 原简单句：[The critics] covered the events.
   ──→ 核心：Critics + covered + events → SVO
   无扩展成分可去
```

**整句核心骨架一览：**

| 层 | 核心 | 句型 |
|----|------|------|
| 主句（还原主动） | People took it for granted | SVOC |
| 主语从句 | Critics would write | SV |
| of 定语还原 | Critics were of papers | SVP |
| 定语从句 | Critics covered events | SVO |

> 💡 一个 43 词的长难句，核心其实是四件事：某人认为某事理所当然 → 评论家会写 → 评论家属于大报社 → 评论家报道事件。

---

## 拆分 & 简化规则速查

| 步骤 | 做什么 | 不做什么 |
|------|--------|---------|
| **3B-1 断开** | 拆成独立简单句；还原省略成分用 `[...]` | 不保留从句嵌套结构 |
| **3B-2 简化** | 保留主/谓/宾/表/补；去掉定/状/同位/插入 | 不改变核心成分的语法功能 |

**去掉什么（非核心）：**
- 定语：形容词、介词短语后置定语、定语从句、过去/现在分词定语
- 状语：时间/地点/方式/原因/目的/条件/让步等
- 同位语
- 插入语

**保留什么（核心）：**
- 主语 + 谓语动词 + 宾语/表语/宾补/间接宾语
- 否定词（not/never）— 属于谓语的一部分
- 情态动词 — 属于谓语的一部分