---
title: Implement Autonomous L1 Agent for Workplace
description: Use the Autonomous L1 Agent for Workplace agent that automatically resolves frequently asked General Inquiry workplace cases without requiring manual agent intervention.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-wsd/implement-autonomous-l1-agent-for-workplace.html
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 3
breadcrumb: [Using AI agent workflows in ServiceNow Otto for WSD, ServiceNow Otto for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Implement Autonomous L1 Agent for Workplace

Use the Autonomous L1 Agent for Workplace agent that automatically resolves frequently asked General Inquiry workplace cases without requiring manual agent intervention.

The Autonomous L1 Agent represents the initial uptake of ZTSD \(Zero Touch Service Desk\) Agent capabilities within Workplace Services. The agent scans two configured knowledge sources—Workplace Services knowledge base articles and previously closed workplace cases to identify matching resolutions and close eligible cases autonomously. When no match is found, the agent surfaces its best findings, unassigned itself, and returns the case to Ready state for human agent follow-up.

## Overview of Autonomous L1 Agent for Workplace

Workplace service desks receive a high volume of repetitive General Inquiry cases—questions about policies, services, and procedures that can be resolved from existing knowledge without live agent involvement. The Autonomous L1 Agent addresses this by processing cases immediately on creation, applying AI-driven knowledge matching against configured sources, and resolving or escalating cases based on outcome.

When a General Inquiry workplace case is created, the L1 agent is automatically assigned to it—no manual routing is required. The agent queries its configured knowledge sources to find a matching resolution.

## Knowledge Sources

The agent learns from two default knowledge sources.

-   Workplace Services knowledge base articles configured in the instance
-   Previously closed workplace cases that contain resolution information

As agents manually resolve new types of cases, those resolutions are automatically added to the agent's learning corpus, improving autonomous resolution rates over time.

## Agent Behaviour

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

    The agent populates the resolution field and close notes with the retrieved answer and transitions the case to Closed Complete. The case returns to Awaiting Acceptance per the configured workflow.

-   **Resolution path B – No match found**

    The agent shares available findings as a work note, unassigns itself, and returns the case to Ready state so a human workplace agent can resolve it manually.

-   **Learning loop:**

    When a human agent manually resolves a case \(Path B outcome\), the resolved case is added to the agent's knowledge corpus. Subsequent cases with similar questions are resolved autonomously.


**Parent Topic:**[Using AI agent workflows in ServiceNow Otto for WSD](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/now-assist-wsd-using-agentic-use-cases.md)

**Related topics**  


[Manage temporary space closures agentic workflow]()

[Help manage workplace reservations agentic workflow]()

[Optimize cleaning activities agent overview]()

[Automate map updates agentic workflow]()

[Workplace Advisor Overview]()

[Workplace Concierge agentic workflow]()

