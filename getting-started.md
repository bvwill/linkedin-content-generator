# Getting Started: From Zero to Voice-Matched Content

This guide walks you through setting up the LinkedIn content generator with YOUR voice. It takes about an hour to do properly. Skip the voice extraction and every post will sound like generic AI content.

## Prerequisites

- [Claude Code](https://claude.ai/code) installed
- 3-5 samples of your existing writing (LinkedIn posts, blog posts, emails, transcripts)
- If you have coaching or speaking transcripts, even better. Raw transcripts are the richest source of voice patterns.

**TIP:** If you use Fathom, Otter, or another meeting recorder, you can bulk-export transcripts and feed them directly to Claude Code. More data means better voice extraction.

## Step 1: Create Your Project Folder

```
my-content-engine/
  transcripts/          # speaking/coaching transcripts
  posts/                # existing LinkedIn posts
  voice/                # generated voice documents
  output/               # generated content
```

## Step 2: Baseline Run (No Voice)

Before extracting your voice, generate content WITHOUT it. This gives you a comparison point that makes the value obvious.

Paste this into Claude Code:

```
Read the files in ./posts/ (or ./transcripts/ if using transcripts)

Extract 5 LinkedIn posts from this content. Each post should:
- Focus on one actionable insight
- Be 150-250 words
- Open with a hook that stops the scroll
- End with a clear takeaway or question

Save the output to ./output/baseline-posts.md
```

Read the output. Ask yourself: does this sound like me, or like generic AI content? Make notes on what feels off. You will use those notes in Step 4.

## Step 3: Extract Your Voice

This is the highest-value step. Feed Claude Code your writing samples and have it identify what makes you sound like you.

Paste this into Claude Code:

```
Read all files in ./posts/ and ./transcripts/

Analyze my voice across these samples. Extract and document:

## Signature Phrases and Language Patterns
- Phrases I repeat
- Metaphors and analogies I use
- How I open and close ideas
- Transition phrases I default to

## Tone and Personality Markers
- My level of formality
- How I use humor (frequency, type, timing)
- How direct vs. exploratory I am
- My warmth-to-challenge ratio

## Anti-Patterns (Things I Never Do)
- Phrases or styles that would feel wrong coming from me
- Tones I avoid
- Structural patterns that are not my style

Save to ./voice/voice-profile.md
```

## Step 4: Review and Refine

Read the voice profile carefully. Claude Code will get 70-80% right on the first pass. The remaining 20% is where your input matters most.

Paste this into Claude Code:

```
Read ./voice/voice-profile.md

I have reviewed this and here are my corrections:
[Add your notes, for example:]
- I actually say "let's pressure-test that" not "let's challenge that"
- Missing my habit of [specific thing]
- My humor is more [X] than described
- Add anti-pattern: I never use [Y]

Update the document with these corrections.
```

Repeat this step until the voice profile feels right. This is the foundation. If it is wrong, every piece of content will be off.

## Step 5: Copy Your Voice Guide Into This Repo

Once your voice profile is solid, copy it into this repo as `voice-guide.md`. Use the template structure in the existing `voice-guide.md` file, filling in each section with your extracted voice data.

## Step 6: Generate Content

Now run the content skill with your voice:

```
/linkedin "your topic here"
```

Compare the output to your baseline posts from Step 2. The difference should be obvious. If it is not, your voice guide needs more refinement.

## Ongoing Maintenance

Your voice evolves. Every few weeks, run a refresh:

```
Read ./voice/voice-profile.md
Read my last 10 posts in ./posts/

Has my voice shifted? New patterns? Retired phrases?
Suggest updates. Show me what you would change before making edits.
```

Track your LinkedIn performance data and update the Performance Patterns section in your voice guide. The system uses that data to make better content decisions over time.
