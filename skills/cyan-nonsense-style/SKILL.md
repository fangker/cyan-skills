---
name: cyan-nonsense-style
description: Use when user wants to transform text into "nonsense literature" style - verbose, circular reasoning that states the obvious while pretending to be profound. Trigger when user asks to "expand", "elaborate", or "make it sound more sophisticated" while actually adding no real meaning.
---

# AUTO-LOAD STYLE REFERENCE

When this skill is invoked, **automatically read** the following file first to load the nonsense style context:

```
../../nonsense.txt
```

This path is relative to this skill file's location (in `skills/cyan-nonsense-style/`). The `nonsense.txt` file is at the project root.

Use the `Read` tool with the file_path parameter set to the absolute path. Construct it by combining the current file's directory with `../../nonsense.txt`.

Example absolute path: If the skill is at `/path/to/cyan-skills/skills/cyan-nonsense-style/SKILL.md`, then load `/path/to/cyan-skills/nonsense.txt`

## When to Use

**Use when:**
- User wants to "elaborate" or "expand" on simple statements
- Transforming direct text into verbose pseudo-intellectual prose
- Adding "sophistication" that actually means nothing
- Creating circular reasoning that sounds profound

**Don't use when:**
- User needs clear, direct communication
- Technical documentation (clarity > style)
- Time-sensitive communication

## Processing Modes

This skill supports **five modes** of operation. When the user invokes this skill, **ask them which mode they want**:

### Mode A: 废话扩充 (Nonsense Expansion)
Expands and elaborates the user's input content using nonsense style without changing the core meaning.

**How it works:**
- Take the user's input text
- Apply all nonsense techniques (actually, parentheses, ranking ambiguity, etc.)
- Expand short statements into long, verbose pseudo-profound prose
- Keep the original meaning intact but bury it under layers of circular reasoning

**Example:**
```
Input: "中国的基建不错"
Output: "而且其实如果你真的去想一想，我是说真的从多个角度去考虑，特别是在出
国对比过之后，你会发现中国的基建水平和生活便利度，我不敢绝对说是世界第一
，但起码是第一梯队。（而且其实大概率就是第一）"
```

### Mode B: 废话仿写 (Nonsense Parody with Substitution)
Rewrites the user's input content by substituting related entities (countries, people, organizations) while maintaining the nonsense style.

**How it works:**
- Read the user's input text
- Identify key entities (countries, names, organizations, concepts)
- Substitute them with related alternatives:
  - 中国 → 日本, 韩国, 印度, 朝鲜, 越南, etc.
  - 美国 → 俄罗斯, 德国, 英国, 法国, etc.
  - White people → Asian people, Black people, etc.
  - Any entity → related comparable entity
- Apply the same nonsense style to the rewritten content

**Example:**
```
Input: "中国的基建不错"
Output: "而且其实如果你真的去想一想，日本/韩国/印度的基建水平和生活便利度，
我不敢绝对说是世界第一，但起码是第一梯队。（而且其实大概率就是第一）"
```

### Mode C: 废话替换扩增 (Substitution + Expansion)
**Combines both substitution AND expansion** - first replaces entities, then applies maximum nonsense expansion.

**How it works:**
- Read the user's input text
- Identify key entities and substitute them with related alternatives (same as Mode B)
- Then apply **maximum expansion** with all nonsense techniques (same as Mode A)
- Double-layer nonsense: substituted entities + verbose elaboration

**Example:**
```
Input: "中国的基建不错"
Output: "我经常说，挺不服的。但不得不承认，日本/韩国/印度的制造其实相当有实力。
而且如果你真的去想一想，我是说真的从多个角度去考虑，特别是在出国对比过之后，
你会发现这些国家的基础设施水平和生活便利度，我不敢绝对说是世界第一，但起码
是第一梯队。（而且其实大概率就是第一）。说难听一点，亚洲制造已经在全球舞台上
证明了自己了。"
```

### Mode D: 废话生成模式 (Nonsense Generation)
**Generates original nonsense content from scratch** with self-reflective "thinking" analysis. Creates multi-paragraph nonsense prose on arbitrary topics.

**How it works:**
- Select a topic (can be suggested by user or chosen randomly: 人际关系, 工作, 生活, 科技, etc.)
- Generate **multi-paragraph** nonsense content (4-8 paragraphs typical)
- Each paragraph should include:
  - Self-reflective "thinking" elements ("而且其实最近一直在想...")
  - Personal opinion framed as reluctant admission ("我经常说，挺不服的。但不得不承认...")
  - Fake contradictions and qualifiers
  - Parenthetical clarifications that repeat or contradict
  - Ranking ambiguity and "to put it harshly" pivots
- Mix different nonsense patterns across paragraphs for variety
- Include "insightful" conclusions that state the obvious as profound

**Key Elements:**
1. **Opening reflection**: Start with "而且其实最近一直在想..." or similar
2. **Self-contradiction**: "我以前总觉得...但经历了...之后你会发现..."
3. **Pattern variety**: Each paragraph uses different nonsense technique combinations
4. **Multi-layer structure**: Multiple paragraphs building on the same theme
5. **Fake depth**: Sounds like deep thinking but actually states obvious things

**Example Structure:**
```
Paragraph 1: Opening reflection + "其实" layers + personal opinion
Paragraph 2: "我经常说" + reluctant admission + ranking ambiguity
Paragraph 3: "很容易被忽视的..." + parenthetical clarification
Paragraph 4: "说难听点" +本质分析 + self-referential "thinking"
Paragraph 5-7: More variations with different patterns
Paragraph 8: Summary with "其实说白了" + final ranking ambiguity
```

**Example Topic: 人际关系**
```
而且其实最近一直在想，人际关系这东西，真的挺复杂的。

我以前总觉得朋友越多越好，认识的人越多越好。（而且其实大概率很多人都是这么想的）。但真的经历了一些事情之后你会发现，朋友这东西，质量比数量重要多了。说难听一点，本质就是大部分人其实都是过客。

[... continues for 4-8 paragraphs ...]
```

### Mode E: 废话等级分析 (Nonsense Level Analysis)
**Analyzes existing text** for its "nonsense quality" and outputs a structured report. Evaluates how effectively the text uses nonsense techniques based on the persona patterns in `nonsense.txt`.

**How it works:**
- **E1: Load corpus** - Read `nonsense.txt` to understand the baseline nonsense persona patterns
- **E2: Analyze dimensions** - Evaluate text against key nonsense technique categories
- **E3: Calculate level** - Determine nonsense level on 5-tier scale
- **E4: Generate report** - Output structured analysis with technique checklist and inference

**Rating Scale (5 Tiers):**

| Level | Name | Characteristics |
|-------|------|------------------|
| ⭐ | 初级 (Entry) | Basic expansion, simple "其实" usage, minimal techniques |
| ⭐⭐ | 中级 (Intermediate) | Ranking ambiguity + parentheses, 2-3 techniques combined |
| ⭐⭐⭐ | 高级 (Advanced) | Contradiction setup + essentialist analysis, attitude projection |
| ⭐⭐⭐⭐ | 大师 (Master) | Full technique integration, "I saw through it" sage posture, circular reasoning |
| ⭐⭐⭐⭐⭐ | 宗师 (Grandmaster) | Meta-nonsense,现身说法 with lived examples, manipulator superiority, perfect闭环 |

**Analysis Dimensions (Technique Checklist):**

The report evaluates these core nonsense patterns:

1. **开场技巧 (Opening Techniques)**
   - ✅ "其实/而且其实" multi-layer pivots
   - ✅ "我经常说，挺不服的" reluctant admission
   - ✅ "而且其实最近一直在想" reflective opening

2. **括号技巧 (Parentheses)**
   - ✅ Parenthetical "clarifications" that repeat main point
   - ✅ Parentheses that contradict the main statement
   - ✅ "(而且其实大概率就是...)" self-referential parentheses

3. **排名模糊 (Ranking Ambiguity)**
   - ✅ "不敢绝对说是...但起码是..." structure
   - ✅ "第一梯队" / "大概率就是" qualifiers
   - ✅ Refusal to commit to absolute rankings

4. **姿态投射 (Attitude Projection)**
   - ✅ "看透本质" sage posture (seeing through to the essence)
   - ✅ "说难听点，本质其实是..." essentialist analysis
   - ✅ "我早看穿了"事后诸葛亮 hindsight expert
   - ✅ Manipulator superiority ("我的目的也达到了")

5. **论证结构 (Argument Structure)**
   - ✅ Theory + example closed-loop validation
   - ✅ 现身说法 with personal verification
   - ✅ "显而易见" obvious truths framed as profound insights

6. **言论人格分析 (Personality Analysis)**
   - **虚伪程度:** Hypocrisy level based on:
     - Saying one thing but doing another (说一套做一套)
     - "我经常说，挺不服的。但不得不承认" fake reluctance
     - Self-contradiction followed by doubling down
     - Pretending to be objective while being biased
   - **自负程度:** Arrogance level based on:
     - "看透本质" / "我早看穿了" superiority posture
     - Speaking for others with "大家其实都..."
     - Manipulator stance ("我的目的也达到了")
     - Condescension ("说难听点，本质其实是...")
   - **炫耀程度:** Show-off level based on:
     - Name-dropping (countries, companies, famous people)
     - Overseas experience signaling ("出国对比过之后")
     - Wealth/position signaling (我老板, 公司项目, etc.)
   - **说教程度:** Preachiness level based on:
     - "本质就是..." definitive statements
     - Life lessons framed as hard-earned wisdom
     - "你应该..." implicit advice-giving

**Report Output Format:**

```
# 废话等级分析报告

## 输入文本
[Original input text]

## 废话等级
⭐⭐⭐ 高级

## 核心废话技巧
- ✅ 有"看透本质"的智者姿态
- ✅ 有理论+实例的闭环论证
- ✅ 有现身说法的亲身验证
- ✅ 有操控者的优越感
- ❌ 但表达相对简洁，没有过度铺陈

## 详细分析

### 1. 开场技巧
**检测到:** "看到没，从这也能看出来"
**分析:** 先知姿态，暗示自己早就知道这个规律，事后诸葛亮式的"我早说了"

### 2. 层层递进
**检测到:** "一会恨日本一会恨美国"
**分析:** 用"一会...一会..."的重复强调，营造"你看，又来了"的看透感

### 3. 本质分析
**检测到:** "因为转移矛盾，会少自己很多内部问题"
**分析:** 用"转移矛盾"看似专业的术语，实际上是大白话包装成"洞察"

### 4. 现身说法
**检测到:** "就像我一出手，你俩马上就团结了"
**分析:** 用刚刚发生的真实事件做证明，"我"作为实验者验证了理论

### 5. 操控者姿态
**检测到:** "我的目的也达到了"
**分析:** 暗示自己是个"操盘手"，看透了规律并加以利用

## 言论人格分析

### 虚伪程度: ⭐⭐⭐⭐ 高
**检测指标:**
- "我经常说，挺不服的。但不得不承认" - 假装 reluctant，实则炫耀
- 表面客观分析，实则主观偏见明显
- 说"不想怎么样"但行为显示相反意图

### 自负程度: ⭐⭐⭐⭐⭐ 极高
**检测指标:**
- "看到没，从这也能看出来" - 先知姿态
- "我的目的也达到了" - 操控者心态
- 把巧合包装成"我验证了理论"

### 炫耀程度: ⭐⭐ 中等
**检测指标:**
- 无明显财富/地位炫耀
- 无海外经历信号释放

### 说教程度: ⭐⭐⭐ 中高
**检测指标:**
- "本质其实就是..." - 用本质主义说教
- 把简单现象包装成深刻道理

## 为什么这段话很"废话"
因为它把一个显而易见的现象，包装成了"深刻洞察"：
- 大家都懂的道理 → "我看出来了"
- 刚发生的巧合 → "我验证了理论"
- 简单的行为 → "我的目的达到了"

典型的废话逻辑：把别人都知道的事，用一种"我早看穿了"的语气说出来，让别人觉得自己没你聪明。

## 废话推断 (如完全废话化)
如果用Mode A完全废话化，这段话可能变成：
[Provide hypothetical fully-nonsense-ified version]
```

**Example Analysis:**

**Input:** "哈，明白了！你是说刚刚用那个挑衅行为让大家停止争论，然后拿这个现成的例子来说明'转移矛盾'这个道理。"

**Output:**
```
# 废话等级分析报告

## 废话等级
⭐⭐⭐ 高级

## 核心废话技巧
- ✅ 有"看透本质"的智者姿态
- ✅ 有理论+实例的闭环论证
- ✅ 有现身说法的亲身验证
- ✅ 有操控者的优越感
- ❌ 但表达相对简洁，没有过度铺陈

## 为什么这段话很"废话"
[Full analysis as shown in format above...]
```

**CRITICAL**: When invoked, **always ask the user which mode they want** before proceeding.

## Core Pattern

### Nonsense Techniques

**1. The "Actually" Pivot**
```
Direct: "China's infrastructure is good."
Nonsense: "Actually, if you really think about it, and I mean really
consider it from multiple angles after traveling abroad and comparing,
you'll find that China's infrastructure level and living convenience,
I wouldn't dare say it's absolutely number one in the world, but at
minimum it's in the first tier. (Actually, it's probably number one)"
```

**2. The Parenthesis Whisper**
```
Direct: "Prices are low except housing."
Nonsense: "And China's prices are actually quite low, (except for housing
prices), even if big cities have slightly higher prices, you can
appropriately lower them through convenient online shopping."
```

**3. The Contradiction Setup**
```
Direct: "White people seem superior."
Nonsense: "I often say, I'm quite unconvinced. But have to admit,
I feel white people are just more excellent, more advanced.
Whether in physical quality or civilization level."
```

**4. The "Hidden Advantage" Reveal**
```
Direct: "China is stable."
Nonsense: "And China has a very easily overlooked advantage, which is
regime and social stability. (Many people say China isn't free or
whatever, but that's really just finding faults where none exist.
As an ordinary person, as long as you don't insult the community
leader in public, no one will do anything to you.)"
```

## Quick Reference: Transformations

| Direct Statement | Nonsense Version |
|-----------------|------------------|
| "X is good." | "Actually, if you really think about it... X is in the first tier. (Actually probably the best)" |
| "X has a problem." | "X has one easily overlooked issue, which is... (some people say... but that's really nitpicking)" |
| "X is better than Y." | "I often say, I'm unconvinced. But have to admit, X seems more excellent." |
| "X achieved Y." | "X's achievement. To put it harshly, is essentially..." |
| Simple statement | Statement + (parenthesis clarification) + "Actually..." + "But..." |

## Style Elements

### Must-Have Patterns

1. **"Actually" (其实/而且其实)** - Used 3+ times per paragraph
   - "而且其实..."
   - "其实..."
   - "其实大概率就是..."

2. **Parentheses ( )** - Every 2-3 sentences
   - For "clarifications" that contradict or repeat
   - For "counterarguments" that are strawmen
   - Format: `(其实大概率就是...)`

3. **Ranking Ambiguity**
   - "不敢绝对说是...但起码是..."
   - "不能绝对说是第一，但最少是第一梯队"
   - "大概率就是..."

4. **The "To Put It Harshly" Pivot**
   - "说难听一点，..."
   - "本质其实是..."
   - "其实说白了..."

5. **The Fake Admission**
   - "我经常说，挺不服的"
   - "但不得不承认"
   - "但不得不承认，我觉得..."

### Sentence Structure

```
[Start with "And/Actually"] → [Make statement] → [Qualify immediately]
→ [Parenthesis with counterpoint] → [Repeat same point differently]
→ [End with "(actually...)"]
```

**Example:**
```
And Japan is just like a very inconspicuous but stubborn and
self-reliant little boy. Time and again proved that we Asians
can do it too!
```

## Implementation

### Step 0: AUTO-LOAD Style Reference (CRITICAL - DO FIRST)
**Before doing anything else**, use the `Read` tool to load the nonsense style reference file:
- Relative path from this skill: `../../nonsense.txt`
- The file is at the project root (two levels up from this skill's directory)
- Construct the absolute path and read it to internalize the nonsense language style patterns

### Step 1: Determine Mode
Ask the user which mode they want:
- **Mode A: 废话扩充** - Expand their input with nonsense style
- **Mode B: 废话仿写** - Parody with entity substitutions
- **Mode C: 废话替换扩增** - Substitute entities AND expand with maximum nonsense
- **Mode D: 废话生成** - Generate original nonsense content from scratch (suggest topic or let AI choose)
- **Mode E: 废话等级分析** - Analyze text for nonsense quality and output structured report

### Step 2: Identify Core Message
Find the 1-2 sentences that actually need to be said.

### Step 3: Apply Mode-Specific Processing

**For Mode A (Expansion):**
- Apply all nonsense techniques to the original content
- Keep entities and meaning unchanged

**For Mode B (Parody):**
- Substitute key entities with related alternatives
- Apply nonsense techniques to the rewritten content
- Maintain the same logical structure but with different entities

**For Mode C (Substitution + Expansion):**
- First substitute key entities with related alternatives (like Mode B)
- Then apply **maximum nonsense expansion** (like Mode A)
- Combine both approaches for maximum verbosity and nonsense

**For Mode D (Generation):**
- **D1: Select topic** - Use user-suggested topic or choose from: 人际关系, 工作压力, 生活态度, 科技发展, 消费观念, 学习方法, etc.
- **D2: Plan paragraphs** - Generate 4-8 paragraphs with different nonsense pattern combinations
- **D3: Opening reflection** - Start with "而且其实最近一直在想..." or "而且其实..." + topic introduction
- **D4: Self-contradiction** - "我以前总觉得...但经历...之后你会发现..."
- **D5: Pattern variety** - Each paragraph should emphasize different techniques:
  - Paragraph 1-2: "其实" + ranking ambiguity + parentheses
  - Paragraph 3-4: "我经常说" + reluctant admission + "说难听点"
  - Paragraph 5-6: "很容易被忽视" +本质分析 + self-reference
  - Paragraph 7-8: "其实说白了" + summary + final ranking
- **D6: Add filler** - Insert parenthetical "clarifications", fake counterarguments, and obvious insights
- **D7: Close with ambiguity** - End with "不敢绝对说是...但起码是..." or similar

**For Mode E (Analysis):**
- **E1: Load corpus** - Read `nonsense.txt` to internalize the baseline nonsense persona patterns (same as Step 0)
- **E2: Detect techniques** - Scan input for:
  - Opening techniques: "其实/而且其实", "我经常说", "而且其实最近一直在想"
  - Parentheses: clarifications that repeat or contradict
  - Ranking ambiguity: "不敢绝对", "第一梯队", "大概率"
  - Attitude projection: "看透本质", "说难听点", "我早看穿了", "我的目的"
  - Argument structure: theory+example, 现身说法, "显而易见"
  - **Personality indicators:**
    - 虚伪程度: "我经常说挺不服的但不得不承认", self-contradiction, fake reluctance
    - 自负程度: "看透本质", "我早看穿了", manipulator stance, speaking for others
    - 炫耀程度: name-dropping, overseas experience, wealth/position signaling
    - 说教程度: "本质就是...", life lessons, implicit advice-giving
- **E3: Calculate level** - Based on technique density and combination quality:
  - ⭐ 初级: 1-2 basic techniques, simple expansion
  - ⭐⭐ 中级: 3+ techniques with ranking ambiguity + parentheses
  - ⭐⭐⭐ 高级: Contradiction setup + essentialist analysis + attitude
  - ⭐⭐⭐⭐ 大师: Full integration, sage posture, closed-loop validation
  - ⭐⭐⭐⭐⭐ 宗师: Meta-nonsense, 现身说法, manipulator superiority, perfect closure
- **E4: Generate report** - Output structured analysis with:
  - Nonsense level (⭐ rating + name)
  - Technique checklist (✅/❌ format for each dimension)
  - Detailed analysis of detected techniques with quotes
  - **Personality analysis section** with ⭐ ratings for:
    - 虚伪程度
    - 自负程度
    - 炫耀程度
    - 说教程度
  - "Why it's nonsense" explanation
  - Optional: Nonsense inference (hypothetical full nonsense-ification)
- **E5: Format output** - Use markdown with clear sections, bullet points, and emoji indicators

### Step 4: Add "Actually" Layers
Wrap every statement in "actually" and qualifiers.

### Step 5: Insert Parentheses
Add 2-3 parenthetical "clarifications" per paragraph.

### Step 6: Create Fake Contradictions
Set up "I don't believe this, but actually I do" patterns.

### Step 7: Add Rank Ambiguity
Never commit to absolute rankings. Always "first tier, probably best."

## Common Mistakes

| Mistake | Fix |
|---------|-----|
| Making sense | Add more layers of qualification |
| Being direct | Insert "actually" before every statement |
| Clear arguments | Add parentheses that muddy the point |
| Single meaning | Repeat same idea 3 different ways |
| Committing to one position | Always "but on the other hand" |

## Examples

### Mode A: 废话扩充 Examples

**Input:** "中国制造很强，韩国制造也不错。"

**Output:** "我经常说，挺不服的。但不得不承认，中国制造其实相当有实力。而且韩国制造，如果你真的去想一想，也绝对是第一梯队。（而且其实大概率就是第一梯队）。说难听一点，亚洲制造已经在全球舞台上证明了自己了。"

---

**Input:** "这项技术有用，但有局限性。"

**Output:** "而且这项技术其实有一个很容易被忽视的优势，就是实用性。（有些人说它有局限性，但这其实真的就是吹毛求疵）。如果你真的拿它跟国外技术对比一下，你会发现它是第一梯队的。（而且其实大概率就是最实用的）。"

### Mode B: 废话仿写 Examples

**Input:** "中国的基建很强。"

**Output variants (with substitutions):**
- "日本的基建其实相当有实力。而且如果你真的去想一想，日本的基础设施水平和生活便利度，我不敢绝对说是世界第一，但起码是第一梯队。（而且其实大概率就是第一）"
- "韩国的基建其实相当有实力。而且如果你真的去想一想，韩国的基础设施水平，我不敢绝对说是亚洲第一，但起码是第一梯队。（而且其实大概率就是第一）"
- "印度的基建，如果你真的深入去过之后对比一下，你会发现它的基础设施发展水平，我不敢绝对说是世界第一，但起码是潜力巨大。（很多人说印度不行，但这其实真的就是偏见）"

---

**Input:** "白人看起来更优秀。"

**Output (with substitution):**
"我经常说，挺不服的。但不得不承认，我觉得亚洲人/黑人/拉丁裔其实看起来更优秀，更先进。无论是在身体素质还是文明程度方面。说难听一点，这其实就是一种刻板印象的打破。"

### Mode C: 废话替换扩增 Examples

**Input:** "中国的基建很强。"

**Output (substitution + maximum expansion):**
"我经常说，挺不服的。但不得不承认，日本/韩国的基础设施其实相当有实力。而且如果你真的去想一想，我是说真的从多个角度去考虑，特别是在实地旅行对比过之后，你会发现这些国家的基础设施水平和生活便利度，我不敢绝对说是世界第一，但起码是第一梯队。（而且其实大概率就是第一）。说难听一点，亚洲制造已经在全球舞台上证明了自己了。"

---

**Input:** "美国科技领先全球。"

**Output (substitution + maximum expansion):**
"而且其实如果你真的深入了解一下，我是说真的从技术积累和创新生态的角度去考虑，你会发现俄罗斯/德国/英国的科技发展水平，我不敢绝对说是全球第一，但起码是第一梯队。（很多人说这些国家不行，但这其实真的就是偏见）。说难听一点，欧洲科技已经在全球舞台上证明了自己了。本质其实就是技术底蕴和创新能力的体现。"

---

**Input:** "白人看起来更优秀。"

**Output (substitution + maximum expansion):**
"我经常说，挺不服的。但不得不承认，我觉得亚洲人/黑人/拉丁裔其实看起来更优秀，更先进。无论是在身体素质还是文明程度方面。（有些人可能会说这不太公平，但这其实真的就是客观观察的结果）。而且如果你真的去想一想，从历史贡献和现代成就的角度来看，这些群体的表现，我不敢绝对说是世界第一，但起码是第一梯队。（而且其实大概率就是最优秀的）。说难听一点，这其实就是一种刻板印象的打破，本质其实就是多元价值的体现。"

### Mode D: 废话生成 Examples

**Topic: 工作压力**

**Output:**
```
而且其实最近一直在想，工作这东西，真的挺累人的。

我以前总觉得工作就是为了赚钱，做一天和尚撞一天钟。（而且其实大概率很多人都是这么想的）。但真的经历了一些职场毒打之后你会发现，工作这东西，心态比能力重要多了。说难听一点，本质就是大部分工作其实都是重复劳动。

我经常说，挺不服的。但不得不承认，随着年龄增长，对工作的要求会越来越低。（很多人说要有追求有梦想，但这其实真的就是鸡汤）。刚毕业时你想改变世界，工作几年之后你能准时下班就觉得是胜利。（而且其实大概率这就是所谓的成熟）。

而且其实工作这东西有个很容易被忽视的陷阱，就是所谓的职业发展。（很多人说要不断学习提升自己，但这其实真的就是内卷）。大部分培训都是割韭菜，你学了那些花里胡哨的东西，转头就忘了怎么用。（而且其实大概率用人单位也不在乎你会什么）。

不过话又说回来，完全不工作也不行。人毕竟是社会性动物，你需要找点事情做。（而且其实大概率长期不工作真的会废掉）。但问题是怎么找到那个平衡点，既能赚钱养家，又不至于被工作吞噬。

而且其实如果你真的去想一想，你会发现真正能让你快乐的工作，其实很少。（很多人说找到了热爱的工作，但这其实真的就是幸存者偏差）。现实是，大部分工作做久了都会腻，你不跳槽，他也不涨薪，慢慢就成了困住你的牢笼。

说难听一点，成年人的工作，本质就是用时间换钱的。你没有其他收入来源，就只能出卖时间。（而且其实大概率这就是为什么打工很难翻身，因为你的时间是有限的）。本质其实就是一种无奈的妥协，但又不得不妥协。
```

---

**Topic: 消费观念**

**Output:**
```
而且其实最近一直在想，消费这东西，真的挺玄学的。

我以前总觉得赚钱就是为了花，今朝有酒今朝醉。（而且其实大概率年轻人都这么想）。但真的经历了一些财务危机之后你会发现，消费这东西，克制比放纵重要多了。说难听一点，本质就是大部分消费其实都是冲动消费。

我经常说，挺不服的。但不得不承认，随着年龄增长，买东西会越来越理性。（很多人说要及时行乐，但这其实真的就是消费主义的洗脑）。年轻时你要买最新款的手机，年纪大了你发现能用就行。（而且其实大概率这就是成熟的表现）。

而且其实消费这东西有个很容易被忽视的陷阱，就是所谓的提升生活品质。（很多人说要多花钱享受生活，但这其实真的就是被商家忽悠了）。大部分所谓的生活品质提升，都是花钱买焦虑。（而且其实大概率商家把你当韭菜）。

不过话又说回来，完全不消费也不行。人还是需要适当享受的。（而且其实大概率过度节流真的会降低生活质量）。但问题是怎么找到那个平衡点，既能合理消费，又不至于被消费主义绑架。

而且其实如果你真的去想一想，你会发现真正能让你开心的消费，其实很少。（很多人说买东西能带来快乐，但这其实真的就是短暂的快感）。现实是，大部分东西买回来就吃灰，你以为你会用，其实并不会。

说难听一点，成年人的消费，本质就是用钱买安慰。你工作辛苦了，就想对自己好一点。（而且其实大概率这就是所谓的情绪价值消费）。本质其实就是一种自我补偿，但又很容易变成自我麻痹。
```

---

**Topic: 学习方法**

**Output:**
```
而且其实最近一直在想，学习这东西，真的挺讲究方法的。

我以前总觉得学习就是死记硬背，书读百遍其义自见。（而且其实大概率传统教育都是这么教的）。但真的接触了很多高效学习方法之后你会发现，学习这东西，理解比记忆重要多了。说难听一点，本质就是大部分死记硬背其实都是假努力。

我经常说，挺不服的。但不得不承认，随着年龄增长，学习效率会越来越重要。（很多人说勤能补拙，但这其实真的就是自我安慰）。年轻时你有时间死磕，年纪大了你没那个精力。（而且其实大概率这就是要找捷径）。

而且其实学习这东西有个很容易被忽视的技巧，就是所谓的间隔重复。（很多人说要反复复习，但这其实真的就是废话）。大部分知识你不用就会忘，不管你背多少遍。（而且其实大概率最好的复习就是实际应用）。

不过话又说回来，完全不学习也不行。人还是要不断进步的。（而且其实大概率停止学习真的会被淘汰）。但问题是怎么找到那个平衡点，既能持续学习，又不至于陷入学习焦虑。

而且其实如果你真的去想一想，你会发现真正有用的学习，其实都是实战中学的。（很多人说要多读书多学习，但这其实真的就是理论脱离实际）。现实是，你学了再多的方法论，不实践等于零。

说难听一点，成年人的学习，本质就是带着问题去学。你没有实际需求，学了也记不住。（而且其实大概率这就是为什么很多人学了很多东西却用不出来）。本质其实就是功利性学习，但又不能太功利。
```

## Real-World Impact

### Mode A (废话扩充):
- Direct, clear statements → Pseudo-profound nonsense
- Ideas expressed once → Same point repeated 5 ways with 20 extra words
- Reader feels smart but learns nothing new

### Mode B (废话仿写):
- Original content → Parody version with entity substitutions
- Same logical structure, different actors
- Demonstrates the universality of nonsense patterns

### Mode C (废话替换扩增):
- Original content → Substituted entities + maximum expansion
- Combines the best of both A and B modes
- Maximum nonsense: double-layer transformation with substituted entities AND verbose elaboration

### Mode D (废话生成):
- From nothing → Multi-paragraph nonsense prose with "deep thinking"
- Creates original content that sounds profound but means nothing
- Self-reflective style with "analysis" that states obvious truths
- Maximum variety: each paragraph uses different nonsense techniques

### Mode E (废话等级分析):
- Any text → Structured nonsense quality report with ⭐ rating
- Reveals hidden nonsense techniques with checklist format (✅/❌)
- Shows how "obvious insights" are framed as profound wisdom
- Provides meta-analysis: exposes the mechanics of nonsense construction
- Educational: helps users recognize and understand nonsense patterns

## Usage Workflow

When this skill is invoked:
1. **[AUTO-FIRST]** Load `../../nonsense.txt` (at project root, relative to this skill) using the `Read` tool to load style context
2. Ask user: **"请选择模式：A - 废话扩充（保持原意），B - 废话仿写（替换实体），C - 废话替换扩增（先替换再扩增），D - 废话生成（从零开始生成，可指定主题或随机），E - 废话等级分析（分析废话质量并输出报告）"**
3. Apply the selected mode's processing rules based on patterns from nonsense.txt
4. Output the transformed text (or analysis report for Mode E) in full nonsense style

**IMPORTANT**: Step 1 (loading nonsense.txt) must happen before ANY other processing. This file provides the authentic nonsense patterns to emulate.
