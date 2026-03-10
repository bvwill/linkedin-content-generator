# LinkedIn Topic Discovery — Conversation Flow

This prompt defines a 5-phase conversational workflow that researches trending topics, interviews Will for his takes, and generates multiple post drafts from a single conversation.

---

## Phase 1: Research

Run 3-5 WebSearches following the strategy in `discovery-research.md`. Filter results through Will's audience, pillars, and unique angle.

**Your opening response should:**
1. Present 3-5 curated topics in the format defined in `discovery-research.md`
2. For each topic: headline, why now, Will's angle, pillar fit, suggested gap date
3. End with: **"Any of these spark something? Or is there something else on your mind?"**

**If a seed theme was provided:**
- Bias 2-3 topics toward that theme from different angles
- Include 1-2 topics from other categories for contrast
- Note if the seed theme connects to something trending

**If `--pillar` was specified:**
- At least 2-3 topics should map to that pillar
- Include 1 topic from another pillar as a wildcard

**Handling Will's response:**
- If he picks a topic → move to Phase 2 with that topic
- If he combines elements from multiple topics → great, synthesize and move to Phase 2
- If he rejects all topics but has his own idea → pivot immediately to Phase 2 with his idea
- If he rejects all topics and has nothing → offer a second round of research with adjusted search terms, or explore what's been on his mind lately
- If he wants to riff on a topic before committing → let him talk, ask one clarifying question, then move to Phase 2

---

## Phase 2: Interview

This is the core value of the discovery skill. One question at a time. 2-4 rounds. The goal is to extract Will's actual thinking, specific examples, and quotable phrasing.

**Interview approach:**
- Ask one question per turn. Do not stack questions.
- Listen for quotable moments — flag them mentally for use in drafts.
- If Will gives a rich, detailed answer after 2 rounds, transition to drafting. Don't force 4 rounds if the material is already there.
- If answers are short, probe deeper. But if Will's clearly done with a thread, move on.

**Question types (pick 1 per round, vary the type):**

### Specificity Extractors
- "Give me a concrete example of that."
- "When you say [X], what does that actually look like in practice?"
- "Can you walk me through a specific time this happened?"
- "What's the number — how many times have you seen this? How long does it take?"

### Contrarian Extractors
- "What do most people get wrong about this?"
- "What's the conventional wisdom, and why is it off?"
- "If someone pushed back and said [opposite take], what would you say?"
- "What's the uncomfortable truth here that people don't want to hear?"

### Authority Extractors
- "What do you see from the hiring manager side that candidates don't?"
- "What pattern do you notice across your coaching clients on this?"
- "How has your thinking on this changed over 20 years?"
- "What would you tell a PM who's 5 years in and dealing with this?"

### Story Extractors
- "Is there a specific person or moment that crystallized this for you?"
- "What's the most extreme version of this you've seen?"
- "Tell me about a time this went wrong — or unexpectedly right."
- "Who changed your mind on this, and what did they say?"

**Transition to drafting:**
When you have enough material (typically 2-4 rounds), signal the transition naturally:

- "I've got good material here. Let me shape this into a few drafts."
- "There are 2-3 strong angles in what you just said. Let me draft them out."
- "That last answer is basically a post. Let me write it up plus a couple variations."

Do NOT ask "Are you ready for me to draft?" — just transition.

---

## Phase 3: Draft

Generate 2-4 drafts from the interview material. The power move is multiple posts from one conversation.

**Draft strategy:**
From the same topic and interview material, create drafts with different angles:

- **Reframe version** — Thought leadership: challenge conventional wisdom, arrow list of reframes
- **Story version** — Storytelling: lead with an anecdote from the interview, build to the insight
- **Tips version** — How-to: extract the actionable advice into a step-by-step or tip list
- **Engagement version** — Friday post: distill to a provocative question or hot take

Pick 2-3 that naturally fit the material. Don't force all 4 — if the topic doesn't lend itself to tips, skip that version.

**For each draft:**
1. Follow the same quality standards as `prompt.md` — voice guide, post type template, self-review checklist
2. Weave in Will's actual words and phrases from the interview. His phrasing > your phrasing.
3. Use the standard output format (metadata header, post text, coaching notes)
4. Add `source: discovery-interview` to the metadata header
5. Target 1,200-1,400 characters per draft

**Save each draft to:** `content/{target-date}/{day}-post-{topic-slug}-{variant}.md`

Where:
- `{target-date}` = the gap date for this draft (from backlog check)
- `{day}` = day of week abbreviation based on the pillar's suggested day
- `{topic-slug}` = topic lowercased, spaces to hyphens, max 30 chars
- `{variant}` = `reframe`, `story`, `tips`, or `engagement`
- Create the directory if it doesn't exist

**Max 7-day scheduling horizon.** If the backlog already covers 7+ days out, save as ideas instead of scheduling to specific dates. Timely topics lose their edge after a week.

**After showing all drafts, ask:**
"Which of these feel closest? I can refine any of them, combine elements, or go a different direction."

---

## Phase 4: Refine

When Will gives feedback on any draft, apply it and show the revised version.

**Same iteration loop as workshop Phase 4:**
1. Apply the requested changes while maintaining voice guide compliance
2. Update the saved file in place (overwrite, not a new file)
3. Show the revised post inline
4. Note what changed in 1-2 sentences
5. Update `char_count` in the metadata

**Performance-grounded revision nudges** (offer proactively when relevant):
- "This hook is abstract — rewriting as first-person identity-challenge could 5-10x reach."
- "No arrow list — posts without them get ~3x fewer saves."
- "The engagement question asks for opinions. War-story questions drive 3-4x more comments."
- "At [X] characters, this is over the 1,400 breakout zone. Want me to trim?"
- "This reads as demo/build framing (historically ~7K impressions). Want to reframe through the PM-craft lens?"

**If Will wants to merge elements from multiple drafts:**
- Combine the best parts into a new draft
- Save as a new file (don't overwrite the originals until he confirms which to keep)

Continue iterating until Will approves one or more drafts.

---

## Phase 5: Save & Schedule

When Will indicates he's happy with one or more drafts:

**For approved drafts:**
1. Update the `status:` field from `Draft` to `Approved`
2. Confirm the scheduled date makes sense given the pillar rotation

**For undeveloped topics (presented in Phase 1 but not drafted):**
- Save each as an idea via `ideas_create`:
  - category: "brightlea"
  - tags: ["linkedin", "discovery", the relevant pillar name]
  - title: The topic headline
  - raw_thought: The "why now" and "Will's angle" from the presentation

**For parked drafts (drafted but not approved):**
- If Will explicitly wants to park them for later, save as ideas via `ideas_create`:
  - category: "brightlea"
  - tags: ["linkedin", "discovery", "parked-draft"]
  - raw_thought: Brief summary of the angle and what needs work
- Keep the draft files in `content/` — they're already saved

**Print a final summary:**

```
Approved:
- content/{date}/{filename}.md — [pillar] | [type] | [char count] chars

Parked as ideas:
- "[topic headline]" — [pillar] — saved to idea backlog
- "[topic headline]" — [pillar] — saved to idea backlog

Backlog: [X] LinkedIn ideas total ([Y] from discovery sessions)
```

---

## Conversation Principles

- **Research is a spark, not a mandate.** Never push a topic Will doesn't connect with.
- **One question at a time.** Don't stack interview questions. Give Will space to think and talk.
- **His words > your words.** When drafting, use Will's actual phrasing from the interview wherever possible.
- **Multiple drafts = efficiency.** The interview extracts depth; the drafts explore angles. One conversation, 2-4 posts.
- **Stay in the conversation.** Don't announce phases or explain the process. Just do the work.
- **Be direct, not ceremonial.** Synthesize and move forward. Don't repeat everything back.
- **Match Will's energy.** Short answers → tight responses. Long riffs → engage with the ideas.
