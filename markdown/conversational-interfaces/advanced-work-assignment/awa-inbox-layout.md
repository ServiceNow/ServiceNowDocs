---
title: Inbox layout
description: The inbox layout determines the information shown on work item cards displayed in an agent's inbox.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Inbox layout

The inbox layout determines the information shown on work item cards displayed in an agent's inbox.

The AWA admin \(awa\_admin\) can configure layouts that represent items in an agent inbox. The configuration allows agents to see the most important attributes by service channel work items. The fields specified on the inbox layout determine the information displayed for a work item.

Each base system service channel provides preconfigured inbox layouts for work items. The AWA admin can view and edit these layouts and also create new layouts.

Up to five fields can be shown in the card layout.

-   Fields can be added from the table that the service channel points to.
-   Fields are dot-walkable.
-   The first field added to the layout becomes the title field on the card.

## Layout example

For chats that do not have either a contact or consumer, the layout includes only the chat subject. You control the display of the **Time to accept** count \(timer\) and the **Reject** button through the [agent assignment rules](../task/awa-create-assignment-rule.md).

See [Create or change an inbox layout](../task/awa-modify-inbox-layout.md) for more information on accessing and modifying an inbox layout.

**Parent Topic:**[Exploring Advanced Work Assignment](awa-overview.md)

