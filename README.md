# LinkedIn Content Generator

A Claude Code skill system for creating consistent, voice-authentic LinkedIn content. Built for PMs who want to post regularly but struggle with blank-page syndrome, generic-sounding drafts, and maintaining a consistent voice across dozens of posts.

## The Problem

Most PMs know they should be posting on LinkedIn. Few do it consistently. The reasons are always the same:

- **Blank page paralysis.** You have ideas but can't get them into post form.
- **Voice inconsistency.** Monday's post sounds nothing like Friday's. Neither sounds like you.
- **Generic output.** AI-generated content reads like AI-generated content. Vague, hype-filled, interchangeable.
- **No system.** Each post is a one-off effort. No pillars, no rotation, no performance feedback loop.

This skill system solves all four by putting your authentic voice at the center of every generation, backed by content pillars, post type templates, and performance data from real LinkedIn analytics.

## Who This Is For

- PMs building a professional brand on LinkedIn
- Career transitioners who need visibility in a new space
- Job seekers who want to demonstrate expertise, not just claim it
- Anyone tired of writing posts that sound like everyone else's

## How It Works

This is a **Claude Code skill system**, not a standalone app. It runs inside Claude Code as a set of prompts and reference files that shape how content gets generated.

The core idea: instead of asking an AI to "write a LinkedIn post," you give it your voice profile, content strategy, post templates, and performance data. The output sounds like you wrote it, not like a chatbot did.

Four modes, each for a different situation:

1. **Post Generation** (`/linkedin`) - Give it a topic, get a publish-ready draft. The system picks the right content pillar, post type, and structure automatically.
2. **Topic Discovery** (`/linkedin-discovery`) - Researches trending topics in PM/AI/careers, interviews you for your take, then generates 2-4 drafts from a single conversation.
3. **Post Workshop** (`/linkedin-workshop`) - Iterative refinement. Starts by understanding what you want the post to do, proposes a structure, drafts it, then refines through feedback rounds.
4. **Comment Replies** (`/linkedin-reply`) - Generates thoughtful comment replies in your voice. Validates before redirecting, ends with a question that deepens the conversation.

## When to Use Each Mode

| Situation | Mode | What happens |
|-----------|------|-------------|
| You have a specific topic ready to go | `/linkedin "topic"` | One-shot draft with coaching notes |
| Weekly content planning session | `/linkedin-discovery` | Research + interview + multiple drafts |
| You have a rough idea that needs shaping | `/linkedin-workshop` | Collaborative outline, draft, and iterate |
| Someone commented on your post | `/linkedin-reply` | Voice-matched reply, 500-750 chars |

## Key Decisions and Tradeoffs

### Why voice-first?

Every prompt in this system reads the voice guide before generating anything. The voice guide captures specific patterns: sentence structures, words to use, words to avoid, formatting preferences, even punctuation habits. Generic AI content fails because it optimizes for "sounds professional" instead of "sounds like you."

### Why 5 content pillars with day rotation?

Posting without a system means you default to whatever's on your mind. That usually means 80% of your posts cover one topic. The pillar rotation (PM Craft on Monday, AI-in-PM on Tuesday, Coaching Stories on Wednesday, Promotion on Thursday, Engagement on Friday) forces variety while keeping each day predictable. Override it when something timely comes up.

### Why arrow lists?

The performance data is clear. Posts with arrow-list formatting (using the arrow character) drive significantly more saves than posts without them. Saves are an algorithmic distribution signal on LinkedIn. Both breakout posts (48K+ impressions) used arrow lists. The rant post without them got 45 saves on 33K impressions. Arrow lists make content scannable and bookmarkable.

### The breakout zone: 1,200-1,400 characters

LinkedIn posts can be up to 3,000 characters. The data says shorter wins:

- 1,287 chars: 60K impressions
- 1,389 chars: 48K impressions
- 1,567 chars: 33K impressions
- 1,648 chars: 7.5K impressions
- 2,147 chars: 5.9K impressions

Every post targets 1,200-1,400 characters. Over 1,500 gets flagged. One post = one idea.

### Why performance data in the prompts?

The system includes real analytics from published posts. Not to be rigid about formulas, but to ground decisions in evidence. When the workshop suggests "this hook is abstract, consider rewriting as first-person," that suggestion comes from data showing identity-challenging hooks outperform abstract ones by 5-10x on reach.

## How to Use It

These are Claude Code slash commands. Run them in a Claude Code session:

```bash
# Generate a post from a topic
/linkedin "Most PMs waste 3 hours a week on status updates"

# Generate with specific pillar and type
/linkedin --pillar ai-pm --type tips --topic "3 Claude Code prompts every PM should know"

# Start a discovery session (research + interview + drafts)
/linkedin-discovery "AI tools replacing PM tasks"

# Workshop a post iteratively
/linkedin-workshop

# Generate a comment reply
/linkedin-reply
```

The system handles pillar selection, post type matching, structure, voice compliance, character count targeting, and self-review automatically. You review the draft, give feedback, and iterate until it's right.

## Setting Up Your Voice

Before generating content, you need to build your voice guide. The `voice-guide.md` file is a template with empty sections. The `getting-started.md` walks you through extracting your authentic voice from existing writing or transcripts using Claude Code.

The process: generate baseline content without a voice (so you can see the difference), extract voice patterns from your real writing, review and refine, then plug it into this system. Takes about an hour. See [`getting-started.md`](getting-started.md) for the full walkthrough.

## What's Inside

```
linkedin-content-generator/
├── README.md              # You're here
├── prompt.md              # Core post generation prompt (single-shot mode)
├── voice-guide.md         # Voice profile: patterns, words, formatting, tone calibration
├── content-pillars.md     # 5 pillars with day rotation, topic guidance, audience fit
├── post-types.md          # 5 post type templates with structure, archetypes, performance data
├── discovery.md           # Topic discovery conversation flow (research + interview + drafts)
├── discovery-research.md  # Research strategy for discovery mode (search categories, curation)
├── workshop.md            # Iterative post workshop (understand, shape, draft, iterate, finalize)
├── comment-reply.md       # Comment reply generation with conversation-mode voice rules
└── examples/
    ├── example-tips.md        # Annotated tips/how-to post with coaching notes
    ├── example-storytelling.md # Annotated storytelling post with coaching notes
    └── example-promo.md       # Annotated promotional post with coaching notes
```

### File Details

| File | Purpose |
|------|---------|
| `prompt.md` | The main generation prompt. Reads the voice guide and templates, plans the post (pillar, type, archetype, hook), generates it, then runs a self-review checklist before output. |
| `voice-guide.md` | Defines the writing voice: practical over theoretical, direct and concise, authority framing from the hiring-manager perspective, anti-salesy, conversational. Includes specific words/phrases to use and avoid, formatting rules, and performance-informed patterns. |
| `content-pillars.md` | Five pillars (PM Craft, AI-in-PM, Coaching Stories, Bootcamp Promo, Engagement) mapped to weekdays. Each includes topic guidance, default post type, recommended archetype, and target audience. |
| `post-types.md` | Five structures (Thought Leadership, Tips, Storytelling, Promotional, Engagement) with section-by-section templates. Also defines four archetypes (Reframe, Validation, Rant, Demo/Build) with performance benchmarks. |
| `discovery.md` | A 5-phase conversation flow: research trending topics, interview for your take, draft 2-4 posts from one conversation, refine, save and schedule. Designed for weekly content planning. |
| `discovery-research.md` | The research strategy behind discovery mode. Defines search categories (PM industry, AI tools, career/hiring, industry events), curation criteria (timeliness, pillar mapping, unique angle), and what not to research. |
| `workshop.md` | A 5-phase iterative flow: understand the idea, shape the structure, draft, iterate with feedback, finalize. Includes performance-grounded revision nudges ("no arrow list = 3x fewer saves"). |
| `comment-reply.md` | Generates comment replies at 500-750 characters. Tags the person by name, pulls a specific quote from their post, adds perspective, closes with one question. No hashtags, no self-promotion. |
| `examples/` | Three annotated examples showing expected output quality, with coaching notes explaining why each element works. |

## Making It Yours

Follow the [`getting-started.md`](getting-started.md) guide to extract your voice and fill in the template. Then:

1. **Adjust `content-pillars.md`** to your expertise areas and posting cadence.
2. **Replace the examples** with annotated posts in your voice.
3. **Update performance data** as you publish and track what works for your audience.

The prompts in `prompt.md`, `discovery.md`, and `workshop.md` reference file paths that assume a specific project structure. Update those paths to match your setup.
