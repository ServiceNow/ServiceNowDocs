---
title: Workplace advisor QnA agentic workflow
description: The workplace advisor QnA agentic workflow enables Reservation Managers to use the Now Assist panel to ask natural language questions about workplace reservations.
locale: en-US
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: concept
last_updated: "2025-10-05"
reading_time_minutes: 1
breadcrumb: [Workplace Advisor Overview, Using AI agent workflows in Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Workplace advisor QnA agentic workflow

The workplace advisor QnA agentic workflow enables Reservation Managers to use the Now Assist panel to ask natural language questions about workplace reservations.

The workplace advisor QnA agentic workflow routes employee queries to agents and uses a Knowledge Graph to provide automated responses. It supports workplace reservation queries such as bookings, meeting durations, check-in details, and more.

## Workplace advisor QnA agentic workflow overview

**Important:**

To run the workplace advisor QnA agentic workflow, ensure that you have completed the following configurations:

-   [Enable Now Assist panel](../task/enable-now-assist-panel.md)
-   [Configure Now Assist Panel Platform Agent](../task/configure-now-assist-panel-platform-agent.md)

## Accessing the workplace advisor QnA agentic workflow from the AI Agent Studio

You can access the agentic workflow from the AI Agent Studio when you have the sn\_aia.admin role.

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Overview**.
2.  Select **Workplace Advisor QnA**.

## AI agents used in the workplace advisor QnA agentic workflow

The following table lists the agents that are part of the workplace advisor QnA agentic workflow.

|Agent|Description|Agent tools|
|-----|-----------|-----------|
|Workplace reservation QnA agent|The workplace reservation QnA agent handles queries related to workplace reservations using a Knowledge Graph. It can answer questions about reservations for a given building, floor, or campus, and other reservable spaces.|Workplace Reservation Graph|

