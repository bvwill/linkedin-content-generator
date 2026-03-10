# LinkedIn Post Type Templates

Five post types, each with a defined structure, target length, and best-fit pillars. The post type is independent of the pillar — any pillar can use any type — but some combinations are more natural.

---

## 1. Thought Leadership

**Structure:**
1. **Hook** (1-2 lines): Identity-challenging, first-person. Call out a behavior the reader may be doing.
2. **Shock/emphasis line** (1 line): Short. Dramatic. A single-line reframe or imperative.
3. **Contrarian reframe** (2-3 lines): The thing you think helps → actually doesn't. Here's what does.
4. **Authority position** (1-2 lines): Hiring-manager or other-side-of-the-table framing.
5. **Arrow list** (3-5 items): Specific, practical points using → format. This is the bookmarkable core.
6. **Quotable closer** (1 line): Memorable, tweetable one-liner that captures the philosophy.
7. **Engagement question** (1 line): War-story or experience-based, not opinion-based.

**Target length:** 1,200-1,400 characters

**Best-fit pillars:** PM Craft & Career (Mon), AI-in-PM (Tue)

**Example hook patterns:**
- "I see Product Managers making this mistake constantly."
- "If you're an experienced PM collecting certificates, we need to talk."
- "I've been coaching PMs through brutal job searches, and I'm getting fed up."

---

## 2. Tips / How-To

**Structure:**
1. **Hook** (1-2 lines): Specific problem or time-saving promise
2. **Setup** (1-2 lines): Brief context for why this matters
3. **Steps/Tips** (5-10 lines): Numbered list or sequential walkthrough. Each step is concrete and actionable.
4. **Result** (1-2 lines): What the reader gets if they follow through
5. **Quotable closer** (1 line): Tweetable takeaway
6. **Engagement question** (1 line): Invite their approach or a related experience

**Target length:** 1,100-1,400 characters

**Best-fit pillars:** AI-in-PM (Tue), PM Craft & Career (Mon)

**Example hook patterns:**
- "I see PMs spending 3 hours writing user stories from scratch. Here's what I do instead."
- "Here's exactly how I write a PRD in 40 minutes instead of 3 hours."
- "3 Claude Code prompts every PM should know:"

---

## 3. Storytelling

**Structure:**
1. **Hook** (1-2 lines): Drop the reader into the moment — emotion, tension, or surprise
2. **Setup** (3-4 lines): The situation — who, what, when, stakes
3. **Turning point** (3-5 lines): What happened, what changed, what was discovered
4. **Resolution** (2-3 lines): How it turned out, what was learned
5. **Quotable closer** (1 line): The universal lesson, tweetable
6. **Engagement question** (1 line): Invite a related story or experience

**Target length:** 1,200-1,500 characters

**Best-fit pillars:** Coaching Stories (Wed), PM Craft & Career (Mon)

**Example hook patterns:**
- "A PM I coach told me she'd been rejected 47 times. Then something shifted."
- "I've been coaching PMs through brutal job searches, and I keep seeing the same pattern."
- "Last week, a student rewrote their STAR story for the fifth time. Here's why that was exactly right."

---

## 4. Promotional

**Structure:**
1. **Hook** (1-2 lines): Lead with a problem the audience recognizes or an insight they want
2. **Value content** (5-8 lines): Teach something real — a mini-lesson, framework, or behind-the-scenes insight from the bootcamp
3. **Bridge** (1-2 lines): Natural transition from the value to the offering
4. **Offer** (2-3 lines): What the bootcamp/service is, who it's for, what makes it different
5. **Quotable closer** (1 line): Value-driven one-liner (not the CTA)
6. **CTA** (1 line): Clear, low-pressure call to action (link, DM, comment)

**Target length:** 1,200-1,500 characters

**Best-fit pillars:** Bootcamp Promotion (Thu)

**Constraints:**
- Value content must be at least 50% of the post — never lead with the sell
- CTA should be specific ("Check out the curriculum" not "Learn more")
- Reference bootcamp details from `references/bootcamp.md`
- Never use scarcity/urgency tactics unless there's a real deadline

**Example hook patterns:**
- "I keep meeting PMs who've spent thousands on bootcamps but can't answer a basic product question."
- "The PMs getting hired fastest right now have one skill in common."
- "Most PM bootcamps teach you frameworks. We teach you to build with AI."

---

## 5. Engagement

**Structure:**
1. **Hook** (1-2 lines): Provocative question, surprising observation, or relatable frustration
2. **Context** (2-4 lines): Brief framing — why you're asking, what prompted this
3. **Question/Prompt** (1-2 lines): The specific thing you want people to respond to

**Target length:** 600-1,000 characters

**Best-fit pillars:** Engagement & Community (Fri)

**Constraints:**
- Keep it short — engagement posts work better when they're quick to read and easy to respond to
- The question must have multiple valid answers (not a quiz with one right answer)
- Avoid "engagement bait" patterns: no "tag someone who..." or "like if you agree"

**Example hook patterns:**
- "Controversial opinion: roadmaps are a waste of time for most startups."
- "What's the worst prioritization framework you've ever been forced to use?"
- "What's one piece of PM advice that sounds smart but is actually terrible?"

---

## Post Archetypes

Beyond the 5 structural types, every post maps to one of these archetypes based on the goal. The archetype determines the performance profile.

### Reframe
**Goal:** Maximize reach + saves (reference material)
**Structure:** Challenge → reframe → arrow list (→) → quotable closer → engagement Q
**Performance profile:** Highest impressions, highest save rate (0.35%), strong follower conversion (~150/breakout)
**Example:** "Side projects: show thinking not building" (60K impressions, 212 saves)

### Validation
**Goal:** Maximize comments + followers (identity-affirming)
**Structure:** Affirm identity → contrast with common behavior → arrow list (→) → philosophy line → war-story Q
**Performance profile:** Highest comment rate, strong saves (0.32%), strong follower conversion (~135/breakout)
**Example:** "Stop collecting certificates" (48K impressions, 76 comments)

### Rant/Advocacy
**Goal:** Maximize engagement rate (solidarity)
**Structure:** Emotional setup → imperative paragraphs ("Stop." "Quit.") → philosophy closer → experience Q
**Performance profile:** Highest engagement rate, lowest saves (0.14%), weaker follower conversion (~78/breakout). People agree with rants but don't follow for more of them.
**Example:** "Stop lazy hiring practices" (33K impressions, 1.22% engagement)

### Demo/Build
**Goal:** Avoid or reframe as thought leadership
**Performance profile:** Lowest reach, lowest follower conversion (+2). The audience it attracts (side-hustle/automation) doesn't convert. If the topic is "look what I built," reframe it as "here's what this means for how PMs work."
**Example:** "AI idea capture" (7.5K impressions, 2 followers)

---

## Type Selection Guide

When generating a post, select the type based on:

1. **Explicit request:** If the user specifies a type, use it
2. **Pillar default:** Each pillar has a default type (see content-pillars.md)
3. **Content fit:** If the topic naturally fits a different type, override the default
4. **Variety:** If the last 2-3 posts used the same type, prefer a different one
