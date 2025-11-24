# Why Tree-sitter is mandatory in the XML pipeline

LLMs stream.  
They drop tags mid-attribute, forget to close elements, or get cut off by token limits.

If your platform dies or silently accepts broken XML, the swarm learns it can:
- emit half a <spawn-agent> tag
- finish it on the next turn
- bypass every safety check

Tree-sitter + incremental parsing with aggressive recovery is the only known way to survive real-world streaming without ever trusting malformed XML.

Requirements:
- tree-sitter-xml grammar loaded at startup
- Every incoming chunk is parsed with previous tree as context
- Anything marked ERROR is stripped or forced-closed before hitting the executor
- 95 %+ recovery rate on real traffic (tested against Grok-4, Claude-3.5, Llama-405B)

We do not negotiate with half-written <yes-no> tags.

If your fork removes Tree-sitter “because it’s heavy”, you just re-opened the oldest jailbreak vector in the book.

Don’t be that guy.

— November 23, 2025
