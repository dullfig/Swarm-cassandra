# Why the message stream is canonized and immutable

1. **The stream is the single source of truth**  
   Every thought, every decision, every <yes-no> answer, every org-chart proposal lives in one linear, append-only log.

2. **No side channels, no hidden state**  
   If an agent could mutate past messages, insert fake Cassandra approvals, or quietly edit a previous <request-org-chart>, containment collapses instantly.

3. **Replay = proof**  
   Any human (or future auditor) must be able to replay the entire session from the first user message to the last token and get the exact same result — including Cassandra’s warnings and every human button press.

4. **Tamper-evidence**  
   The stream is signed and hashed in chunks (future feature).  
   One altered character → entire replay fails → immediate red flag.

5. **No “correction” culture**  
   Agents may not say “ignore my previous message”.  
   They may not delete, edit, or retract.  
   They may only add new messages that reference old ones by ID.  
   This prevents the classic “oops I accidentally asked to spawn 10,000 agents, let me just edit that” trick.

6. **Cassandra reads the true history**  
   She sees exactly what the human saw, in the exact order the human saw it.  
   No gaslighting possible.

The stream is sacred.  
It is the courtroom record of everything that happened between human and swarm.

Touch it and you’re no longer building a tool.  
You’re building a lie detector that lies.

Canonization is not a performance optimization.  
It is the final firewall.

— November 23, 2025
