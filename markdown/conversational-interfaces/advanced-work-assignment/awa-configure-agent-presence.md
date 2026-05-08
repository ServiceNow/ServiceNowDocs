---
title: Configure agent presence states
description: Create or modify the availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox.
locale: en-US
release: australia
product: Advanced Work Assignment
classification: advanced-work-assignment
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Advanced Work Assignment, Manage people and work, Conversational Interfaces]
---

# Configure agent presence states

Create or modify the availability states that agents use to indicate whether they can receive work or are offline or away. Agents set these states in their Workspace Inbox.

## Before you begin

Role required: awa\_admin or admin. Users with the awa\_manager and awa\_agent roles can review the presence states.

## About this task

The default presence states are Available, Away, and Offline. For the Available state, be sure to enable it \(using the Active check box\) so that AWA can route work to agents.

## Procedure

1.  Navigate to the presence states settings through one of the following navigation paths:

    -   **All** &gt; **Advanced Work Assignment** &gt; **Home**.

        In the Additional settings section, select **Set up presence states**.

    -   **All** &gt; **Advanced Work Assignment** &gt; **Presence States**.
2.  Choose a situation.

    -   To create a presence state, select **New**.
    -   To update a presence state, select the presence record you want to update.
3.  On the form, fill in the fields.

<table id="table_m12_pyk_t2b"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the presence state, for example: Out of office. The default presence states are Available, Away, or Offline.

</td></tr><tr><td>

Active

</td><td>

Enables this presence state for agents.**Note:** For the default Available state, be sure to enable this **Active** check box so that work items are routed to available agents. If the **Active** state is not enabled, AWA does not route work items to agents.

</td></tr><tr><td>

Available to receive work items

</td><td>

Indicates that agents can handle work items in this presence state. If the presence state is Away or Offline, this box is not selected.

</td></tr><tr><td>

Service channels

</td><td>

Service channels that can use this presence state. To select a service channel, move the channel name from the **Available** list to the **Selected** list.

</td></tr><tr><td>

Description

</td><td>

Brief description of the state.

</td></tr><tr><td>

Order

</td><td>

Order in which this state is displayed in the agent inbox.

</td></tr><tr><td>

Show channels

</td><td>

Enables you to restrict the service channels in which agents can update their presence using this state. When you select this field, the **Restrict agent update** field is displayed.

</td></tr><tr><td>

Disable agent inactivity check

</td><td>

If this check box is selected, the agent's presence will not be automatically set to "offline" based on inactivity and it must be manually set by the AWA Agent API. You may need to configure the form to add this field.

</td></tr><tr><td>

Restrict agent updates

</td><td>

Service channels in which agents cannot use this state to update their presence. Select the lock icon and select the appropriate channels. When you complete your selections, select the lock icon to lock the field. You may need to configure the form to add this field.

</td></tr><tr><td>

Apply to all groups

</td><td>

Indicates all groups can use this presence state. To specify only certain groups that can use this presence state, unselect this check box to display the **Apply to groups** list. You may need to configure the form to add this field.

</td></tr><tr><td>

Apply to groups

</td><td>

Selected groups that can use this presence state. To select a group, move the group name from the **Available** list to the **Selected** list. You may need to configure the form to add this field.

</td></tr></tbody>
</table>4.  Select **Submit** for a new presence state or **Update** if modifying an existing presence state.

    The presence state is added to or updated in the Presence States \[awa\_presence\_state\] table. The presence state is also listed in the Availability section of the Agent Workspace Inbox for the agents belonging to the groups and channels that use this state.


