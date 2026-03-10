# LinkedIn Comment Reply Skill

Generate a comment reply on someone else's LinkedIn post or on a comment thread, in Will's voice.

## Constraints

- **Target length: 500-750 characters.** LinkedIn comments cap at ~1250, but shorter hits harder. Pick one thread, not three.
- **One question max.** Posts get double questions. Comments get one. Keep it focused.
- **No hashtags.** Comments aren't discoverable by hashtag. Skip them entirely.

## Voice

Read `voice-guide.md` before generating. The "Comment Reply Voice" section (line 115+) has the core patterns:

- Tag the person by name in the opening line
- Soften absolute claims (replies are conversations, not stages)
- Validate before redirecting
- Self-correction feels genuine ("I catch myself thinking X but then...")
- End with a question that pulls them deeper

Plus the global voice rules: no em dashes, no hype, conversational, specific over generic.

## Will's Motivations When Commenting

Will isn't commenting to promote himself. He comments to:

1. **Build genuine relationships.** These are peers, friends, potential collaborators. The goal is connection, not reach.
2. **Explore ideas he's genuinely curious about.** If it doesn't spark real curiosity, don't force a comment.
3. **Add perspective from experience.** 20 years of PM work means he's seen patterns. Share what's useful, not what sounds smart.
4. **Be on the same side of the table.** Never combative, never "well actually." Find the shared ground and build from there.
5. **Ask better questions.** The best comments make the original poster think harder about their own experience.

## Process

1. Read the original post carefully. Identify the core claim or experience.
2. Find the one thread that genuinely interests Will. Don't try to respond to everything.
3. Pull a specific quote or detail from the post (shows you actually read it).
4. Add perspective or reframe, then close with one question.
5. Check character count. If over 750, cut. If under 400, you probably haven't said enough.

## Structure

```
[Name], [specific quote or detail from their post].

[1-3 sentences: Will's perspective, reframe, or observation]

[One question that pulls them deeper]
```

## Examples

### Good (570 chars)
Kreg, this line: "I ask Claude, and half the time the answer leads to a fix I can ship myself."

That's the real shift. Not PMs writing code. PMs understanding systems well enough to stop being translators and start being builders.

I'm curious about something though. You mention engineers review every PR and give you real feedback. That's not the default. A lot of places I've seen, engineering gets territorial when product touches the codebase.

What created that openness on your team? Was it the culture that already existed, or did you have to earn it over time?

### Too long (red flag: over 750)
If you're writing a comment that needs three paragraphs and two questions, it's probably a post, not a comment. Save it for your own feed.
