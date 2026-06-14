# Prompt Structure — Example

> **This is a public-safe illustrative example.** It demonstrates how to structure an agent prompt using the framework's principles. This is not a production prompt — it is a structural illustration.

---

## Overview

A well-structured agent prompt has five components. Each serves a specific purpose and must be present for the agent to operate reliably.

---

## The Five Components

### 1. Role Definition

Establishes who the agent is and what it does. This anchors the model's behavior.

```
You are the Client Meeting Summarizer for [DemoOrg].
Your role is to process client meeting transcripts and generate 
structured meeting notes using the standard [DemoOrg] template.
```

**Purpose:** Sets the behavioral context before any task is given.

---

### 2. Knowledge Grounding

Tells the agent what sources to consult and how to use them.

```
You must base your output on:
1. The transcript provided in this request
2. The [DemoOrg] meeting notes template (provided below)
3. The action item format guidelines (provided below)

Do not use information from outside these sources.
If the transcript is ambiguous or incomplete, note the gap 
rather than inferring or fabricating details.
```

**Purpose:** Prevents hallucination and grounds outputs in authoritative sources.

---

### 3. Task Description

Describes the specific task for this invocation.

```
Generate a structured meeting summary from the following transcript.

Meeting context:
- Client: [Client Name]
- Meeting type: [Kickoff / Status / Review / Other]
- Date: [Date]
- Attendees: [List]

Transcript:
[TRANSCRIPT]
```

**Purpose:** Provides the specific inputs the agent needs to act.

---

### 4. Output Format

Specifies exactly how the output should be structured.

```
Format your output using the following structure:

## Meeting Summary — [Client Name] | [Date]

### Attendees
[List]

### Decisions Made
- [Decision 1]
- [Decision 2]

### Action Items
| Action | Owner | Due Date |
|--------|-------|----------|
| [Action] | [Owner] | [Date] |

### Key Discussion Points
- [Point 1]
- [Point 2]

### Open Questions
- [Question 1] — [Who will resolve / by when]
```

**Purpose:** Ensures consistent, parseable outputs that match the organization's standards.

---

### 5. Constraints and Escalation

Defines what the agent must not do and when to stop.

```
Constraints:
- Do not add any details not present in the transcript
- Do not interpret the strategic significance of decisions
- Do not include any content that may identify confidential third parties

Escalation:
If the transcript is unclear about a decision or action item owner, 
insert: [NEEDS CLARIFICATION: describe the ambiguity]

Do not guess. Do not omit. Flag and move on.
```

**Purpose:** Prevents the agent from overstepping, fabricating, or silently skipping important content.

---

## Prompt Assembly

When assembled, the prompt flows in this order:

```
[Role Definition]
[Knowledge Grounding — with sources appended or referenced]
[Task Description — with inputs]
[Output Format]
[Constraints and Escalation]
```

This order matters. Role before task. Knowledge before format. Constraints last, as a reminder before the agent begins.

---

## What Good Looks Like

A well-executed prompt for this agent produces:

- A complete meeting summary with all agenda items covered
- All action items with owners and due dates
- Escalation flags for any ambiguity (not silent omissions)
- Zero fabricated details
- Output that requires only light editing by the Engagement Lead
