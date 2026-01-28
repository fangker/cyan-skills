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

## Two Processing Modes

This skill supports **two modes** of operation. When the user invokes this skill, **ask them which mode they want**:

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

## Real-World Impact

### Mode A (废话扩充):
- Direct, clear statements → Pseudo-profound nonsense
- Ideas expressed once → Same point repeated 5 ways with 20 extra words
- Reader feels smart but learns nothing new

### Mode B (废话仿写):
- Original content → Parody version with entity substitutions
- Same logical structure, different actors
- Demonstrates the universality of nonsense patterns

## Usage Workflow

When this skill is invoked:
1. **[AUTO-FIRST]** Load `../../nonsense.txt` (at project root, relative to this skill) using the `Read` tool to load style context
2. Ask user: **"请选择模式：A - 废话扩充（保持原意），B - 废话仿写（替换实体）"**
3. Apply the selected mode's processing rules based on patterns from nonsense.txt
4. Output the transformed text in full nonsense style

**IMPORTANT**: Step 1 (loading nonsense.txt) must happen before ANY other processing. This file provides the authentic nonsense patterns to emulate.
