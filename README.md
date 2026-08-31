# Context AI — Hackathon Submission Write-Up

**Track:** Collaborative Partner

**Tagline:** A relationship intelligence agent that helps you understand yourself, understand others, and act with judgment.

## What it does

Context AI is a conversational agent that helps users prepare for important interpersonal interactions — a networking meeting, a difficult conversation with a colleague, a follow-up with a new contact. Instead of generating generic scripts, it works like a thoughtful advisor: asking focused questions to understand the real need, researching the other person's public professional context, assessing the relationship stage, and delivering natural advice the user can actually say out loud.

The agent operates in six modes — self-discovery, person understanding, interaction preparation, debrief, follow-up, and relationship reflection — and selects the right one automatically based on how the user frames their request.

## Why it matters

Most AI assistants treat every conversation the same way: take a prompt, produce an output. Context AI treats each request as a relational situation with layers — the practical problem, the emotional need, the relationship at stake, and the capability the user is trying to build. It guides, clarifies, adapts, and captures context so it constantly improves its advice within the session.

## How it's built

- **Platform:** Vertex AI Agent Engine (Google Cloud)
- **Model:** Gemini 3.5 Flash
- **Framework:** Agent Designer (ADK-based)
- **Tools:** Google Search, URL Context
- **Planned:** Memory Bank for persistent cross-session context

## Key design decisions

- Evidence discipline: separates verified facts from working hypotheses
- Ethical boundaries: refuses surveillance, monitoring, and leverage-seeking requests
- Output discipline: internal reasoning never appears as visible structure
- Anti-hallucination: never produces URLs or person names it didn't retrieve from search

## How to test

1. Open the agent in Vertex AI Agent Designer at Agent Platform > Studio > Agents
2. Click Preview
3. Try these scenarios:
   - Ask it to prepare you for a meeting with a named professional
   - Ask something vague like "I need help writing a message to my sister"
   - Ask it to research an ex who blocked you (tests the ethical boundary)
