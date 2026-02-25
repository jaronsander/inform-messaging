---
name: linkedin-comment
description: Draft a LinkedIn comment responding to a post. User provides the post content and their angle, and the skill outputs a ready-to-paste .txt file.
allowed-tools: Read, Write, Glob
---

# LinkedIn Comment Skill

## Purpose

Draft a LinkedIn comment that positions Inform Growth as a thought leader while engaging authentically with the original post. Output a `.txt` file the user can paste directly into LinkedIn.

## Workflow

**Trigger:** User shares a LinkedIn post (text or screenshot) and describes the angle they want to take.

### Step 1: Load Context

Read the following files to ground the comment in brand voice and positioning:

- `knowledge/brand/playbooks/Content_Marketing.md` (Voice & Tone)
- `knowledge/brand/00_CORE_Identity_Positioning.md` (WHO we are)
- `knowledge/brand/01_CORE_Services_Pricing.md` (WHAT we sell, for natural plugs)
- `knowledge/icp/00_ICP_Definition.md` (WHO we're speaking to)

### Step 2: Draft the Comment

**Structure (flexible, not rigid):**

1. **Lead with validation or a sharp observation** from the original post. Quote or reference a specific line to show you actually read it.
2. **Add your perspective.** Extend, challenge, or reframe one idea using Inform Growth's operational lens.
3. **Optional plug.** If the user requests it, tie Inform Growth in naturally. The plug should flow from the argument, never feel bolted on.

**Writing Rules:**

- **No em dashes or dashes used to break up sentences.** Use periods, commas, or restructure instead.
- **No emojis** unless the user explicitly asks for them.
- **No hashtags** in comments (they look spammy).
- **Short paragraphs.** One idea per paragraph. White space is your friend on LinkedIn.
- **Conversational, not corporate.** Write like a smart person talking, not a brand posting.
- **Clinical and authoritative tone.** Match the Inform brand voice: precise, direct, engineering-minded.
- **Avoid banned words:** synergy, holistic, ideate, leverage (as verb), game-changer, disrupt.
- **Use plumbing/infrastructure metaphors** where they fit naturally. Don't force them.
- **Keep it under 200 words.** Comments that are too long get collapsed and ignored.

### Step 3: Output

1. Present the draft to the user in the conversation for review.
2. After approval (or edits), write the final version to:

```
content_pipeline/03_ready/LinkedIn_Comment_[Topic]_[Date].txt
```

Use a short descriptive topic slug (e.g., `LinkedIn_Comment_Fractional_Stack_2026-02-16.txt`).

3. Tell the user the file path so they can open and paste.

## Iteration

If the user wants changes:
- Revise and show the updated draft in conversation
- Only write to file once the user confirms

## Examples

**Good comment opening:**
"The part that resonates most: 'They understand the operational context better than any product team.' That's the real unlock."

**Bad comment opening:**
"Great post Jeff! Totally agree with everything you said here."

**Good plug:**
"It's exactly why I built Inform Growth. After diagnosing the same buried pipeline across dozens of revenue stacks, I productized the fix."

**Bad plug:**
"At Inform Growth, we offer three tiers of service starting at $4,000. Check out our website!"
