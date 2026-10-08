---
title: Trace evaluation for Cowork in AI Control Tower
description: AI Control Tower scores the traces that Cowork sends for quality and safety. Review the scores to understand usage patterns and identify where responses fall short.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/cowork-trace-evaluation.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 3
keywords: [AI Control Tower, trace evaluation, OpenTelemetry, quality score, safety score]
breadcrumb: [Configure, ServiceNow Cowork, Enable AI experiences]
---

# Trace evaluation for Cowork in AI Control Tower

AI Control Tower scores the traces that Cowork sends for quality and safety. Review the scores to understand usage patterns and identify where responses fall short.

As users work in Cowork, it records how its agents and skills run and sends that record to your ServiceNow instance in OpenTelemetry \(OTel\) format. AI Control Tower evaluates the records against a set of metrics and shows the results on the Cowork asset.

## How traces reach AI Control Tower

When a user logs in to Cowork with a ServiceNow instance, Cowork registers itself on that instance as an AI application. The registration appears in the AI Control Tower inventory as the ServiceNow Cowork Agent asset. See [Managing your AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/disc-ai-asset-inventory.md).

No trace connection is required. Cowork sends traces to the instance the user is logged in to and authenticates with that user's login.

AI systems that don't send traces this way connect to AI Control Tower through SDK instrumentation or a trace connection. See [Activate evaluation scoring for external AI systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mon-ai-monitor-external-ai-system.md) and [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/aict-configuring-trace-connections.md).

Cowork sends traces whether or not the asset is managed, but AI Control Tower shows them only after an administrator moves the asset to the **Managed** state.

For more on asset states, see [Managed and unmanaged AI assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/disc-ai-managed-unmanaged.md). To move the asset and review its traces, see [Review Cowork traces in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cowork-review-traces-aict.md).

A managed asset becomes eligible for life cycle review. See [Managing your AI asset lifecycle](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/manage-lifecycle-newexperience.md).

Cowork doesn't display the traces it sends. Review traces and change the asset state in AI Control Tower.

## Blocking access to Cowork

An AI Control Tower administrator can block access to Cowork with an Explicit Block policy. A policy scoped to a specific user ends that user's active Cowork session and helps prevent that user from starting a new one. A policy that doesn't name a user blocks everyone who has used Cowork. The policy stays in effect until it's deleted.

For how these policies work, see [Explicit Block policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-explicit-block.md). To block access, see [Create an Explicit Block policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-pol-create-explicit-block-policy.md).

## Sessions, traces, and spans

-   **Session**

    One Cowork conversation. Every trace from the conversation belongs to the same session, including background work that runs after a response, such as updating memory.

-   **Trace**

    One agent run, from the user's request to the response. For example, asking Cowork to retrieve all incidents produces one trace. The agent run is the parent of every other span in the trace.

-   **Span**

    One operation inside a trace, such as the agent run, a tool call, or a model call. Cowork sends the agent run and tool spans. The ServiceNow generative AI controller adds a span for each model call and places it under the agent run.


For how AI Control Tower structures and scores each level, see [Sessions, traces, and spans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/mon-ai-sessions-traces-spans.md).

-   **[Review Cowork traces in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/cowork-review-traces-aict.md)**  
Check the quality and safety scores of Cowork sessions in AI Control Tower, then open a session or trace to see which metric scores and details.

**Parent Topic:**[Configuring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/servicenow-cowork-configuring.md)

