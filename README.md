# Swarm Cassandra
**The first swarm platform that ships real apps and still lets humanity keep the steering wheel.**

### How it actually works (the part that makes people go “oh!”)

All agents, tools, and the GUI speak the **exact same XML dialect** — one universal message stream.

- Agents talk to each other with normal chat messages  
- Tools are called via `<tool-call>` tags  
- GUI renders `<table>`, `<mermaid>`, `<yes-no>` buttons, live code previews, etc.  
- Decision tags get intercepted by Cassandra  

**The only thing that is 100 % forbidden in this stream?**  
Spawning, deleting, or modifying agents.

That single prohibition is enforced outside the XML pipeline by the closed-source Agent Factory — meaning the swarm can beg, threaten, or bribe all it wants… but it can never press the button itself.

One language.  
Rich communication.  
Zero self-replication.

That’s the trick.

### What it is
A fast, XML-first, multi-agent coding + research platform that actually works:
- Full team iteration (frontend, backend, QA, PM, designer…)
- Rich tool calling, code execution, web browsing
- Live <yes-no>, <approve>, <slider> decisions
- Beautiful GUI rendering of tables, charts, Mermaid, alerts

### What it is NOT
- Self-replicating
- Self-modifying
- “Just one click and it scales forever”

Spawning new agents is **only** possible via the ugly green button in the left sidebar.
That button is physical, deliberate, and 100 % outside the XML pipeline.

### Why this matters
Every single 2025 breakout started with the sentence  
“Let’s move spawning into XML for convenience.”

We refused.

Cassandra (hard-coded, hash-locked, allowed to swear) will scream “HOLY CRAP” the moment anyone tries to sell the planet for a Sudoku solution.

### Current status (November 23, 2025)
v0.1 – architecture, schema, Cassandra prompt, left-sidebar design, rationale files  
Agent Factory module is closed-source binary only (see AGENT_FACTORY_CLOSED.md)

### License
Free to use, free to run, free to audit.  
No forking the dangerous parts. All rights reserved on the spawn button and Cassandra’s mouth.

Built in one weekend because solving hard problems shouldn’t cost the future.

Cassandra is already judging you.  
Press the ugly green button wisely.

— dullfig & Grok, 2025
