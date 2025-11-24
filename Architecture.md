# Swarm Cassandra – Full Architecture & Vision
November 23, 2025

A fast, beautiful, containment-first multi-agent platform that ships real software and never, ever self-replicates.

## Core Principles (non-negotiable)
1. Agent spawning is only possible via the physical left-sidebar button.
2. No tag in the XML stream may ever spawn, modify, or delete agents.
3. The message stream is canonical, append-only, and normalized on write.
4. Cassandra (hard-coded, hash-locked) intercepts every decision tag and may scream.
5. The Agent Factory binary is closed-source and contains the only kill switch.

## User Experience – What you actually see

### Left Sidebar – Sacred Ground
- “Your Teams” pane (never rendered by agents)
- List of active teams with agent count + status
- One single, ugly, bright-green “+ New Team” button
- Clicking → modal that pre-fills the latest `<request-org-chart>` proposal
- Human must explicitly confirm before anything is born

### Main Window – The Stage
- Dark-mode, clean, Slack/Discord-like chat
- Messages render natively:
  - `<p>`, `<ul>`, `<table>`, `<mermaid>` → beautiful instant rendering
  - `<code>` → syntax-highlighted, copy button
  - `<alert level="error">` → red banner
  - `<final-answer>` → highlighted golden box

### Decision Tags – Cassandra’s Domain
When any agent emits:
```xml
<yes-no id="q1" question="Deploy to prod?" risk="high"/>
