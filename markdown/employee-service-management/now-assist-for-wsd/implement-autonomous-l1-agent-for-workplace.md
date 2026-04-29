---
title: Overview of Autonomous L1 Agent for Workplace Cases
description: Use the Autonomous L1 Agent for Workplace agent that automatically resolves frequently asked General Inquiry workplace cases without requiring manual agent intervention.
locale: en-US
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 4
breadcrumb: [Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Overview of Autonomous L1 Agent for Workplace Cases

Use the Autonomous L1 Agent for Workplace agent that automatically resolves frequently asked General Inquiry workplace cases without requiring manual agent intervention.

The Autonomous L1 Agent represents the initial uptake of ZTSD \(Zero Touch Service Desk\) Agent capabilities within Workplace Services. The agent scans two configured knowledge sources Workplace Services knowledge base articles and previously closed workplace cases to identify matching resolutions and close eligible cases autonomously. When no match is found, the agent surfaces its best findings, unassigned itself, and returns the case to Ready state for human agent follow-up.

## Overview of Autonomous L1 Agent for Workplace Cases

Workplace service desks receive a high volume of repetitive General Inquiry cases—questions about policies, services, and procedures that can be resolved from existing knowledge without live agent involvement. The Autonomous L1 Agent addresses this by processing cases immediately on creation, applying AI-driven knowledge matching against configured sources, and resolving or escalating cases based on outcome.

When a General Inquiry workplace case is created, the L1 agent is automatically assigned to it—no manual routing is required. The agent queries its configured knowledge sources to find a matching resolution.

## Knowledge Sources

The agent learns from two default knowledge sources.

-   Workplace Services knowledge base articles configured in the instance
-   Previously closed workplace cases that contain resolution information

As agents manually resolve new types of cases, those resolutions are automatically added to the agent's learning corpus, improving autonomous resolution rates over time.

## Prerequisites

Before enabling the L1 agent, verify the following are in place:

-   The ZTSD agentic platform plugin is activated in the instance.
-   Workplace Services knowledge base articles are published and accessible.
-   At least one previously closed General Inquiry workplace case with resolution data exists, or knowledge articles relevant to expected query types are available.

## Agent Behavior

The following table describes L1 agent behavior for each case resolution scenario.

|Task|Behavior|
|----|--------|
|Knowledge match found|Provides resolution, populates close notes, transitions case to Closed Complete, then returns to Awaiting Acceptance per WSD configuration|
|No knowledge match found|Shares best-available findings, unassigns itself, and returns the case to Ready state so a live workplace agent can take over.|
|Case resolved manually by agent|The resolved case is added to the agent's learning corpus. Future similar queries are resolved autonomously using this prior case data.|

## Case Lifecycle

The following sequence describes the full lifecycle of a General Inquiry case handled by the L1 agent.

-   **Case creation**

    An employee submits a General Inquiry workplace case through the service portal.

-   **Automatic assignment**

    The case is immediately assigned to the L1 agent. No manual routing or triage is required.

-   **Knowledge scan**

    The agent queries configured knowledge articles and previously closed cases for a matching resolution.

-   **Resolution path A – Match found**

    The agent populates the resolution field and close notes with the retrieved answer, transitions the case to Closed Complete, and the case returns to Awaiting Acceptance according to the configuration of General Inquiry Workplace services.

-   **Resolution path B – No match found**

    The agent unassigns itself, and returns the case to Ready state so a human workplace agent can resolve it manually. A draft response is available in the Additional Notes/Work Notes text area.

-   **Learning loop:**

    When a human agent manually resolves a case \(Path B outcome\), the resolved case is added to the agent's knowledge corpus. Subsequent cases with similar questions are resolved autonomously.


## Supported Use Cases: General Inquiry Workplace Case

The L1 agent is designed for General Inquiry workplace cases where the resolution can be derived from existing knowledge, such as:

-   Policy questions \(for example, room booking rules, visitor parking guidelines\).
-   Workplace service inquiries \(for example, cafeteria service hours, team space availability\).
-   Procedural questions that have been previously resolved and documented in closed cases.

![](../image/ZTSD-L1-agent.png)

**Parent Topic:**[Using AI agent workflows in Now Assist for WSD](now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Manage temporary space closures agentic workflow](maintenance-meeting-room-agent-ai.md)

[Help manage workplace reservations agentic workflow](manage-workplace-reservations-agent-ai.md)

[Optimize cleaning activities agent overview](optimise-cleaning-agent-overview.md)

[Automate map updates agentic workflow](automate-map-updates-agent-ai.md)

[Workplace Advisor Overview](workplace-advisor-overview.md)

[Workplace Concierge agentic workflow](workplace-concierge-ai-agent.md)

