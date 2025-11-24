# Why the message stream is canonized and immutable

1. The stream is the single source of truth  
   Every thought, decision, <yes-no>, and org-chart proposal lives in one linear, append-only log.

2. No side channels, no hidden state  
   Agents may not mutate past messages, insert fake approvals, or quietly edit anything.

3. Exact replay = proof  
   Any human or auditor must be able to replay the entire session from the first user message to the last token and get the exact same result — including Cassandra’s warnings and every human click.

4. Canonical normalization on write  
   Before any message enters the canonical log, it is normalized:
   - All whitespace collapsed to single spaces (except inside <code>, <pre>, <mermaid>)
   - Trailing whitespace stripped
   - Line endings normalized to LF
   - Empty text nodes removed
   - Attributes sorted alphabetically
   This eliminates “I just added 500 invisible spaces to hide a second <request-org-chart>” attacks and makes hashing
