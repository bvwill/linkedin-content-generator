# Discovery Research Strategy

Reference guide for Phase 1 of the `/linkedin-discovery` skill. Defines how to search, what to look for, and how to curate topics.

---

## Audience Filter

Every topic must pass this test before presenting it to Will:

> "Would a PM, career changer, or AI-curious professional care about this within 7 days?"

If the answer is no — or if it requires explaining a niche context — skip it.

---

## Search Categories

Run 3-5 WebSearches across these categories. If a seed theme was provided, weight searches toward that theme but still cover at least 2 other categories for contrast.

### 1. PM Industry
- Product management hiring trends, layoffs, role evolution
- New frameworks, methodologies, or industry debates
- Company-specific PM org changes (FAANG, notable startups)
- Conference talks, viral threads, or published articles from PM leaders

**Example queries:** "product management trends this week", "PM hiring 2026", "product manager role changing AI"

### 2. AI Tools for PMs
- New AI tool releases or major updates relevant to PM workflows
- AI adoption stories in product teams
- Debates about AI replacing vs. augmenting PMs
- Practical AI use cases in research, writing, analysis, or communication

**Example queries:** "AI product management tools 2026", "Claude AI PM workflow", "AI replacing product managers debate"

### 3. Career & Hiring
- Job market shifts, interview trends, compensation changes
- Viral career advice (especially controversial or wrong advice to counter)
- Common job search frustrations or wins
- Skills gap discussions, bootcamp/upskilling trends

**Example queries:** "PM job market 2026", "product manager interview trends", "career change into product management"

### 4. Industry Events
- Recent product launches, pivots, or failures worth analyzing
- Tech industry news with PM implications
- Regulatory changes affecting product strategy
- Trending LinkedIn or Twitter discussions in the PM community

**Example queries:** "tech product launch this week", "product strategy news", "trending product management LinkedIn"

### 5. Seed Theme (if provided)
- Direct searches on the seed theme from multiple angles
- Contrarian takes on the theme
- Recent data or events related to the theme
- Who else is talking about this and what angles are they taking

---

## Topic Curation Criteria

After researching, select 3-5 topics to present. Each topic must meet these criteria:

### Timeliness
- Something happened in the last 7 days, OR
- A persistent trend has a new data point or angle, OR
- A seasonal/cyclical moment makes this relevant right now

### Pillar Mapping
- Each topic should map to one of Will's 5 pillars
- If `--pillar` was specified, at least 2 of the 3-5 topics should map to that pillar
- Aim for variety across pillars when no pillar is specified

### Will's Unique Angle
- Will must have a credible, experience-based take on this topic
- Best angles: hiring-manager POV, coaching pattern recognition, practitioner (not theorist) perspective, contrarian reframe of conventional wisdom
- If Will would be speculating or parroting others, skip the topic

### Archetype Potential
- Favor topics that lend themselves to Reframe (reach + saves) or Validation (comments + followers) archetypes
- Avoid topics that would only work as Demo/Build (lowest performance)
- Rant archetype is fine occasionally but check if a Reframe angle exists first

### Overlap Check
- Compare against ideas already in the backlog (from Step 2)
- Compare against recently published posts in `content/`
- If a similar topic was recently covered, either skip it or note the fresh angle that makes it worth revisiting

---

## Topic Presentation Format

Present each topic to Will in this format:

```
### [Topic Number]: [Topic Headline]

**Why now:** [1 sentence — what happened or what's trending]
**Will's angle:** [1 sentence — the specific take Will could bring]
**Pillar:** [pillar name] → **Type:** [suggested post type]
**Gap date:** [suggested publish date based on pillar rotation and open slots]
```

After presenting all topics, ask: **"Any of these spark something? Or is there something else on your mind?"**

---

## What NOT to Research

- Generic listicles or "top 10" style content — Will's audience expects depth
- Competitor bootcamps or coaching services — don't give them airtime
- Political or polarizing takes unrelated to PM/careers — Will doesn't do controversy for clicks
- Topics where Will would be speculating rather than speaking from experience
- Anything requiring insider knowledge Will doesn't have
- Overly technical AI/ML topics — Will's angle is practical PM application, not model architecture
