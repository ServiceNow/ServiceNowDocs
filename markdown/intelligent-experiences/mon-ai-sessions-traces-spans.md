---
title: Sessions, traces, and spans
description: Understand the three levels of AI interaction data that AI Control Tower uses to structure, score, and display runtime behavior.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-sessions-traces-spans.html
release: australia
topic_type: concept
last_updated: "2026-04-03"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Sessions, traces, and spans

Understand the three levels of AI interaction data that AI Control Tower uses to structure, score, and display runtime behavior.

To investigate a low quality or safety score, you can dig deeper into a session to narrow the problem to a specific step in the AI system's reasoning. AI Control Tower structures interaction data into three hierarchical levels following open telemetry standards.

|Level|What it represents|Ends when|Example|
|-----|------------------|---------|-------|
|Session|One complete interaction with an AI system.|User closes the conversation, or 10 minutes of inactivity.|An employee asks an ITSM agent to create an incident for a VPN failure.|
|Trace|One turn in the interaction: one input, one output.|The AI system finishes processing and responds.|The agent asks "Which VPN client are you using?" and the user answers.|
|Span|A single step the AI system takes within a trace, such as a tool call, LLM call, database query, or workflow step.|The individual operation completes.|The agent calls the CMDB API to look up the user's VPN configuration.|

## Why levels matter for scoring

Different metrics are evaluated at different levels because each level captures different aspects of behavior.

-   Session-level metrics \(such as Task completion\) need the full context of the conversation to determine whether the user's goal was met. There is one score per session.
-   Trace-level metrics \(such as Overall task completeness for ServiceNow AI systems\) assess whether a single turn achieved its intended outcome.
-   Span-level metrics \(such as Tool error\) assess whether the AI system made good decisions at the individual step level, including whether the correct tool was called with valid parameters.

## Telemetry data on traces

Each trace displays telemetry data alongside evaluation scores: total latency, span count, input tokens, output tokens, and total runtime tokens. These values reflect the tokens consumed by the AI system's actual execution, not the tokens consumed by evaluation scoring.

## Navigating the hierarchy

Evaluation data is structured so you can move from a broad signal to a specific cause. A low quality score tells you something is wrong. Session-level scores tell you which interaction went wrong. Trace-level scores and reasoning tell you which step in that interaction produced the problem. Span-level input and output data tells you exactly why: the wrong tool was called, a parameter was malformed, or a data source returned an error.

**Parent Topic:**[Exploring AI system monitoring in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-exploring-aict-evaluations.md)

