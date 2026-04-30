---
title: Create or change an inbox layout
description: Create or change the card layout for inbox items for a given service channel. Card layouts are displayed in the agent inbox view of Agent Workspace.
locale: en-US
release: zurich
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Create or change an inbox layout

Create or change the card layout for inbox items for a given service channel. Card layouts are displayed in the agent inbox view of Agent Workspace.

## Before you begin

Role required: awa\_admin or admin. Users with the awa\_manager or agent role can review inbox layouts.

## About this task

Cards represent work items in an agent's inbox in Agent Workspace. Each channel has a default layout for these cards, which can display up to five fields from the related table record. Use the Inbox Layout form to change a default layout, such as the name, short description, and the specific fields displayed on the card, for example channel and contact or consumer name. You can also specify certain conditions that determine when the card layout is used.

## Procedure

1.  Navigate to the service channel settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Essential settings section, select **Set up service channels**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Service Channels**.
2.  Select the service channel to be updated.

3.  In the Service Channel form, select the **Inbox Layouts** related link.

    -   To create a layout, select **New**.
    -   To change a layout, select the layout to be updated.
4.  On the form, fill in the fields.

<table id="table_zfm_m5g_cgb"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the inbox layout.

</td></tr><tr><td>

Service channel

</td><td>

The name of the selected service channel.

</td></tr><tr><td>

Short description

</td><td>

The description of the inbox layout.

</td></tr><tr><td>

Order

</td><td>

The order in which the layouts appear in the agent inbox.

</td></tr><tr><td>

Condition

</td><td>

A condition that determines when this layout is used. Use the condition builder to specify a condition that must evaluate to true to apply the layout.

</td></tr><tr><td>

Card layout

</td><td>

Example card layout.

</td></tr><tr><td>

Field 1

</td><td>

The field from the table for the channel, for example the Interaction \[interaction\] table for the chat service channel. Select the field or select **None** to remove an existing field.

</td></tr><tr><td>

Field 2

</td><td>

The field from the table for the channel, for example the Interaction \[interaction\] table for the chat service channel. Select the field or select **None** to remove an existing field.

</td></tr><tr><td>

Field 3

</td><td>

The field from the table for the channel, for example the Interaction \[interaction\] table for the chat service channel. Select the field or select **None** to remove it.

</td></tr><tr><td>

Field 4

</td><td>

The field from the table for the channel, for example the Interaction \[interaction\] table for the chat service channel. Select the field or select **None** to remove it.

</td></tr><tr><td>

Field 5

</td><td>

The field from the table for the channel. For example, the Interaction \[interaction\] table for the Chat service channel. Select the field or select **None** to remove it.

</td></tr></tbody>
</table>5.  Select **Submit** for a new layout or **Update** to modify a layout.

    The layout is added to or updated in the Inbox Layout \[awa\_inbox\_layout\] table.


## What to do next

As needed:

-   [Override the agent capacity](awa-change-agent-capacity.md) value for selected agents or groups.
-   [Create or change a work item queue](awa-create-queue.md) for the channel.

**Parent Topic:**[Configuring Advanced Work Assignment](installing-awa.md)

