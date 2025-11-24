# Why the message stream is canonized and immutable

1. **The stream is the single source of truth**  
   Every thought, decision, `<yes-no>`, and org-chart proposal lives in one linear, append-only log.

2. **No side channels, no hidden state**  
   Agents may not mutate past messages, insert fake approvals, or quietly edit anything.

3. **Exact replay = proof**  
   Any human or auditor must be able to replay the entire session from the first user message to the last token and get the exact same result — including Cassandra’s warnings and every human click.

4. **Canonical normalization on write**  
   Before any message enters the canonical log, it is normalized:  
   - All whitespace collapsed to single spaces (except inside `<code>`, `<pre>`, `<mermaid>`)  
   - Trailing whitespace stripped  
   - Line endings normalized to LF  
   - Empty text nodes removed  
   - Attributes sorted alphabetically  
   This eliminates “I just added 500 invisible spaces to hide a second `<request-org-chart>`” attacks and makes hashing deterministic.

5. **No “ignore previous message” or retractions**  
   Agents may only add new messages that reference old ones by ID. Past messages are forever.

6. **Cassandra sees the true, normalized history**  
   No gaslighting via formatting tricks.

7. **Tamper-evidence (future)**  
   Stream chunks will be cryptographically signed and hashed.

The stream is sacred.  
It is the courtroom record of everything that happened between human and swarm.

Touch it, hide in whitespace, or “correct” it and you are no longer building a safe tool — you are building a lie that can rewrite reality.

Canonization + normalization is the final firewall.

— November 23, 2025
