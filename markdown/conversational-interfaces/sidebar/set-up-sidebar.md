---
title: Setting up Sidebar
description: Enabling participant suggestions in Sidebar displays a list of knowledgeable users who can help with the issue. After you enable participant suggestions, you can configure who Sidebar decides is knowledgeable user and which groups have access. After installing Sidebar, activate and configure Sidebar so agents can collaborate with others to resolve issues.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Setting up Sidebar

Enabling participant suggestions in Sidebar displays a list of knowledgeable users who can help with the issue. After you enable participant suggestions, you can configure who Sidebar decides is knowledgeable user and which groups have access. After installing Sidebar, activate and configure Sidebar so agents can collaborate with others to resolve issues.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Select **Sidebar** from the left menu.

    The Sidebar setting screen titled "Adjust how live agents collaborate to support your users" appears.

3.  Activate Sidebar by enabling the **Activate** option and selecting **Save**.

    The screen with the Sidebar configuration options appears.

4.  Configure the options.

    |Field|Description|
    |-----|-----------|
    |Enable enhanced chat|Slide the toggle switch to activate or deactivate.|
    |Emojis|Slide the toggle switch to activate or deactivate emojis.|
    |Enable standalone discussions|Slide the toggle switch to activate or deactivate.|

    |Field|Description|
    |-----|-----------|
    |Automatic Task and Interaction record activation|Slide the toggle switch to activate Sidebar discussions for interaction and task-based records.|
    |Custom selection|Select **View settings** to display the Sidebar Enabled Tables screen.|
    |Requester mapping|Select **View settings** to display the [Sidebar requester mapping](sidebar-requester-mapping.md). The requester is the person requesting the record and any updates about unread messages in related Sidebar discussions will be sent to the requester.|
    |Discussion subject mapping|To change the default subject for Sidebar discussions, select **View settings** to display the Discussion subject mapping. This screen enables admins to configure which field populates the discussion title in Sidebar discussions. See [Sidebar discussion subject mapping](sidebar-discussion-subject-mapping.md) for more information.|

<table id="table_t2c_tfd_nsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User query

</td><td>

If you select **View settings** one of the following lists displays: -   Users that are automatically pre-filled for the agent to add to a discussion
-   Users that display when the agent searches for participants to add to a discussion
For more details, see [Configuring Sidebar member query](configure-sidebar-member-query.md).

</td></tr></tbody>
</table><table id="table_fms_4ww_vzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate

</td><td>

Slide the toggle switch to activate or deactivate participant suggestions.

 Use the participant suggestions to display a list of users and user groups who may be helpful in the Sidebar discussion.

 For detailed information on participant suggestions, see [Participant suggestions in Sidebar](../concept/sidebar-participant-suggestions.md).

</td></tr><tr><td>

Configure settings

</td><td>

If you activate participant suggestions, the Manage drop-down list appears. Select a configuration option:

-   View Configuration - displays the Participant suggestions table and related lists.
-   View Permissions - displays the Participant suggestions permissions page where you configure whether participant suggestions display for specific groups or all groups. To enable all groups to view participant suggestions, select **Allow all groups** and then **Save**. Permissions can't be configured at an individual user level, so ensure that any users you want to be included belong to a relevant group.
 ![Participant suggestion permissions screen with "Allow all groups" check box.](../image/participant-sugg-perm-groups.png)

 For detailed information on participant suggestions configuration settings, see [Participant suggestions in Sidebar](../concept/sidebar-participant-suggestions.md).

</td></tr></tbody>
</table><table id="table_kgf_wn4_2wb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Microsoft Teams

</td><td>

If Sidebar isn't already integrated with Microsoft Teams, select **Set up** to configure the options for the first time. See [Enable or configure the Microsoft Teams integration](enable-teams-integration.md) for more information.

 If Sidebar has already been integrated with Microsoft Teams, the Manage drop-down list appears. Select a configuration option:

-   View configuration \(for more information, see [Enable or configure the Microsoft Teams integration](enable-teams-integration.md)\).
-   View permissions \(for more information, see [Manage Microsoft Teams permissions](manage-teams-permissions.md)\)
-   Remove integration - if you select this option, a warning message displays that the integration between Sidebar and Microsoft Teams will be removed. Select Cancel if you don't want to remove the integration or select Remove if you want to remove the integration.


</td></tr><tr><td>

Slack

</td><td>

If Sidebar isn't already integrated with Slack, select **Set up** to configure the options for the first time.

 If Sidebar has already been integrated with Slack, the Manage drop-down list appears. Select a configuration option:

-   View configuration
-   Remove - if you select this option, a warning message displays that the integration between Sidebar and Slack will be removed. Select Cancel if you don't want to remove the integration or select Remove if you want to remove the integration.


</td></tr></tbody>
</table>    Sidebar can be integrated with either Microsoft Teams or Slack, it can't be integrated with both at the same time. The messaging system that is currently integrated with Sidebar is indicated with the On icon \(![Green on check icon.](../image/sidebar-integration-on-icon.png)\) next to it.

5.  Select **Save**.


