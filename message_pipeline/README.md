# Swarm Message Pipeline
**The nervous system of the XML-first swarm platform**

Buffers XML handoffs, tool calls, and HITL requests for distributed resilience.
Cassandra scans every high/medium-risk message before it proceeds.

## Quick Start (Windows 11)
```powershell
docker run -d --name swarm-rabbit -p 5672:5672 -p 15672:15672 rabbitmq:3-management
pip install -r message_pipeline\requirements.txt
.\message_pipeline\examples\spawn_consumers.bat
Cassandra is watching. Don’t make her scream.
