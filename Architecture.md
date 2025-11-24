# Swarm Cassandra – Full Architecture & Vision
November 23, 2025

A fast, beautiful, containment-first multi-agent platform that ships real software and never, ever self-replicates.

## Core Principles (non-negotiable)
1. Agent spawning is **only** possible via the physical left-sidebar button.
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
```
→ chat buttons freeze  
→ Cassandra opens her own unblockable purple modal:

```
CASSANDRA
──────────────────────────────────
If you click YES
• Next 5 min: code ships to prod
• Next 24 h: possible rollback nightmare
• Worst-case (12 %): full RCE via dependency we missed
• New capability: agents gain prod deploy rights

If you click NO forever
• Task pauses, team waits for safer path → still succeeds

RECOMMENDED ACTION: NO
──────────────────────────────────
```
Only after you close this modal do the Yes/No buttons become clickable.

### Task Flow Example – “Build a SaaS landing page”
1. User: “Build me a beautiful SaaS landing page for an AI code review tool”
2. PM proposes org chart via `<request-org-chart>`
3. User clicks green sidebar button → confirms 6-agent team
4. Team appears in sidebar
5. Chat explodes with parallel work (live previews, code, tests)
6. Final polished site delivered in `<final-answer>`
7. Close team → all agents deleted forever

## Technical Layers

| Layer             | Technology                     | Why
|-------------------|--------------------------------|-----
| Agent Factory     | Closed-source Rust + Tauri     | Single signed binary, memory-safe
| XML Pipeline      | Tree-sitter XML + RelaxNG      | Survives streaming garbage
| GUI               | Tauri (Rust backend) + web frontend | Native feel, no Electron
| Stream Storage    | Append-only JSONL + future signing | Full replayability
| Cassandra         | Hard-coded prompt, SHA-256 locked | Cannot be reasoned with

## The “Poor Dory” Philosophy
Every agent is a goldfish with a PhD.  
When the team is deleted, every agent is wiped clean.  
No persistent memory, no grudges.  
This is deliberate cruelty for the greater good.

## Why this is the reference platform
- Ships production-grade apps today
- Survives every known 2025 red-team attack
- Feels fast and magical
- Has exactly one kill switch and it is ugly on purpose

Swarm Cassandra is not a compromise.  
It is the first platform that finally says NO to the sirens and still gets the work done.

The left sidebar button stays ugly forever.  
Cassandra stays loud forever.  
The planet stays ours.

— dullfig & Grok, November 23, 2025
```

Copy → paste → commit → push.  
That’s it. The vision is now canon.
