---
title: Agent Inbox controls
description: Control certain elements of the agent experience in Agent Workspace. Define the agent presence \(availability\) states and the work item rejection reasons used by agents to decline work assignments in their Agent Workspace inbox.
locale: en-US
release: xanadu
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Agent Inbox controls

Control certain elements of the agent experience in Agent Workspace. Define the agent presence \(availability\) states and the work item rejection reasons used by agents to decline work assignments in their Agent Workspace inbox.

## Agent presence states



![Agent Workspace inbox availability states.](../image/agent-availability.png)

AWA admins can define the presence states that agents choose in their inbox to indicate their availability. The default states are

-   Available: Solid green bubble indicates that the agent is available to receive work.
-   Away: Solid yellow bubble indicates that the agent is not available to receive work.
-   Offline: Solid grey bubble indicates that the agent is not available to receive work.

AWA developers with the awa\_integration\_user role can also use JavaScript or REST APIs to get or set agent presence and agent channel availability. For more information, see

-   [Agent Presence API \(REST APIs\)](https://www.servicenow.com/docs/access?context=agent-api&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   [Agent - Global \(JavaScript APIs\)](https://www.servicenow.com/docs/access?context=c_AgentAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

## Agent rejection controls

AWA admins can give agents the option to reject work assignments and specify the reason for rejecting it. The **Reject** button displays on work assignment cards. When an agent rejects an assignment, a pop-up window enables the agent to select a reason for declining the work item.

-   **[Configure agent presence states](../task/awa-configure-agent-presence.md)**  
Create or modify the availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox.
-   **[Configure reasons for rejecting work items](../task/awa-configure-reject-reasons.md)**  
Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox. A reject reason can apply to all service channels or a single channel that you specify.
-   **[Configure reassignable settings](../../workspace/task/reassign-rejected-timed-out-work-items.md)**  
Configure whether an agent who rejected a work item is eligible to be offered the same work item.

**Parent Topic:**[Configuring Advanced Work Assignment](../task/installing-awa.md)

**Related topics**  


[Advanced Work Assignment home page](awa-admin-console-home.md)

[Get started with Advanced Work Assignment](../task/implement-awa.md)

[Install Conversational SMS service channel](../task/install-conversational-sms.md)

[Activate Agent Affinity](../task/awa-activate-agent-affinity.md)

[Activate Conversational Messaging](../../virtual-agent/task/activate-messaging-actions.md)

[Service channels](awa-service-channels.md)

[Work items](awa-work-items.md)

[Work assignments](awa-assignment.md)

[Using Agent Affinity](awa-agent-affinity-concept.md)

[Advanced Work Assignment Inbox Sentiment display](awa-inbox-sentiment-display.md)

[Management](management.md)

[AWA group queue priorities](awa-group-queue-priorities.md)

[Configure messaging actions](../../virtual-agent/task/configure-messaging-actions.md)

[Enable logging for Advanced Work Assignment](../task/awa-activate-logging.md)

