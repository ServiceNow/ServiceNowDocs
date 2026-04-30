---
title: Configure reasons for rejecting work items
description: Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox. A reject reason can apply to all service channels or a single channel that you specify.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Configure reasons for rejecting work items

Define the reasons that agents can use to decline work assignments that they receive in their Agent Workspace inbox. A reject reason can apply to all service channels or a single channel that you specify.

## Before you begin

Role required: awa\_admin or admin

## Procedure

1.  Navigate to the reject reasons settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Additional settings section, select **Set up reject reasons**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Reject Reasons**.
2.  Choose a situation.

    -   To create a rejection reason, select **New**.
    -   To update an existing rejection reason, select the reason record.
3.  On the form, fill in the fields.

    |Field|Definition|
    |-----|----------|
    |Reason|Name of the reason for rejecting work items.|
    |Agent selectable|Indicates that the reject reason is selectable by agents in their Agent Workspace Inbox.|
    |Order|Order in which the reject reasons are listed in the agent inbox.|
    |Apply to all service channels|Indicates that the reject reason applies to all service channels. To make the reason available to a single channel, unselect this check box and in the **Service channel** field, select the appropriate channel.|
    |Service channel|Service channel that the rule applies to. This field is displayed when **Apply to all service channels** isn’t enabled.|
    |Reassignable|Indicates if the work item can be reassigned to the agent who rejected it.|

4.  Select **Submit** for a new reason, or if changing an existing reason, select **Update**.

    The rejection reason is added to or updated in the Reject Reasons \[awa\_reject\_reason\] table.


-   **[Tutorial: Route interactions by context](context-routing-tutorial.md)**  
Learn how you can configure Advanced Work Assignment to route conversations to agents according to the context of the conversation.

**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

