---
title: Call Wrap-Up
description: Call wrap-up enables agents to open the wrap-up modal, select wrap-up codes, and submit summary notes during an active call, so that call context is captured in real time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/initiate-agent-wrap-up-during-active-call.html
release: australia
topic_type: concept
last_updated: "2026-05-13"
reading_time_minutes: 2
keywords: [agent-initiated wrap-up, wrap-up, call wrap-up, Interaction Controls Component, ICC, CCaaS, active call, wrap-up codes, summary notes]
breadcrumb: [ICC for voice calls, Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Call Wrap-Up

Call wrap-up enables agents to open the wrap-up modal, select wrap-up codes, and submit summary notes during an active call, so that call context is captured in real time.

## Call Wrap-Up overview

\[Omitted image "open-wrap-up.png"\] Alt text: Agents can select the Open Wrap-Up icon to initiate the wrap-up process during an active call.

Agent-initiated wrap-up extends the Interaction Controls Component \(ICC\) to give agents direct control over the wrap-up workflow during an active call. Traditionally, wrap-up is triggered automatically after a call ends. This feature changes that model by allowing agents to open the wrap-up modal while the call is still in progress.

When an agent selects **Open Wrap-Up** in the active call controls, the CCaaS platform receives a wrap-up event and returns the appropriate wrap-up codes for that call. The wrap-up modal opens in the agent's Workspace, where the agent can select a wrap-up code and enter summary notes and comments. The submitted data is saved to the system of record immediately, even while the call remains active.

Agents handling complex or sensitive calls can use this feature to record context as it happens rather than rely on post-call recall, which reduces the risk of incomplete or inaccurate notes. Agents can also initiate wrap-up for call flows that do not have mandatory wrap-up configured, ensuring that notes and codes can be submitted regardless of call type.

Agent-initiated wrap-up is available when the ICC for voice is integrated and the CCaaS administrator has configured and enabled the feature in the ServiceNow instance.

For more information, see [Interaction wrap up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/interaction-wrap-up-state.md) and [Create an interaction wrap-up configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/create-interaction-wrap-up-config.md).

## Benefits

Agent-initiated wrap-up provides the following benefits:

-   **Real-time context capture**

    Agents can record wrap-up codes and notes during the call, reducing reliance on post-call recall and improving the accuracy of submitted data.

-   **Reduced after-call work time**

    Submitting wrap-up data before the call ends shortens the time agents spend on wrap-up tasks after the call disconnects.

-   **Improved note accuracy**

    Agents handling complex or sensitive calls can document context as it happens, reducing the risk of incomplete or inaccurate notes.


See: [Configure agent-initiated wrap-up](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/initiate-agent-wrap-up-admin-workflow.md) and [Initiate wrap-up during an active call](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/initiate-agent-wrap-up-agent-workflow.md).

