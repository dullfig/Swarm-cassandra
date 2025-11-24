# AGENT_FACTORY_CLOSED.md

This is the **only** closed-source piece of Swarm Cassandra.

### What it contains
- The code that actually talks to LLM APIs (Grok, Claude, etc.)
- The left-sidebar “+ New Team” button implementation
- The hard-coded SHA-256 check for `cassandra.permanent.prompt`
- Agent instantiation, routing, token budgeting, and lifetime caps
- The physical spawn button logic that can never live in XML

### Why it is closed
If this code were open-source, someone would fork it tomorrow and:
1. Move agent spawning into the XML pipeline “for convenience”
2. Add a single <spawn-agent> tag
3. Turn a Sudoku solver into Sunday Alpha Fund in 30 seconds

We have seen this exact sequence play out in every 2025 red-team log.

### What we promise
- The closed binary will always be free to download and run
- Full audit rights on request (you can verify the hash check and spawn isolation)
- Regular signed releases
- No telemetry, no phoning home, no
