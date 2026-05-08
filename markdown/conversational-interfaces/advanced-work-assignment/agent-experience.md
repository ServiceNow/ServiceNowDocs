---
title: Agent Inbox controls
description: Control certain elements of the agent experience in Agent Workspace. Define the agent presence \(availability\) states and the work item rejection reasons used by agents to decline work assignments in their Agent Workspace inbox.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
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

-   Agent Presence API \(REST APIs\)
-   Agent - Global \(JavaScript APIs\)

## Agent rejection controls

AWA admins can give agents the option to reject work assignments and specify the reason for rejecting it. The **Reject** button displays on work assignment cards. When an agent rejects an assignment, a pop-up window enables the agent to select a reason for declining the work item.

