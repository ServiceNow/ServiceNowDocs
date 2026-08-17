---
title: Investigating low-scoring sessions
description: Narrow a quality or safety issue from a broad score to a specific cause by reviewing evaluated sessions and session details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/mon-ai-investigating-low-scoring-sessions.html
release: australia
topic_type: concept
last_updated: "2026-04-08"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI, use]
breadcrumb: [Monitor and evaluate AI systems, Monitor AI assets, AI Control Tower, Enable AI experiences]
---

# Investigating low-scoring sessions

Narrow a quality or safety issue from a broad score to a specific cause by reviewing evaluated sessions and session details.

## Investigation workflow

When a quality or safety score drops, investigate a session to narrow the problem from a broad score to a specific cause. Session-level scores tell you which interaction went wrong. Trace-level scores and the judge's reasoning tell you which exchange produced the problem. Span-level input and output data tells you exactly why: the wrong tool was called, a parameter was malformed, or a data source returned an error.

**Important:** Trace and span detail for a session is available only for a limited time. To review the judge's reasoning and the input and output for a specific trace or span, investigate within 7 days for ServiceNow AI systems, or within 30 days for external AI systems. After that window, the session's quality and safety scores remain available, but the trace and span detail behind them is removed.

-   **[Evaluated sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-evaluated-sessions-overview.md)**  
View all evaluated AI sessions across your portfolio, compare quality and safety scores by AI system, and identify the sessions that need investigation.
-   **[Session details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-session-details.md)**  
View metric breakdowns, the judge's reasoning, and trace and span data for a specific evaluated session.
-   **[Investigate a low-scoring session](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-investigate-session-task.md)**  
Determine the root cause of a low quality or safety score by working through the session detail, trace timeline, and span-level input and output data.

**Parent Topic:**[Monitoring and evaluating AI systems in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/mon-ai-landing.md)

