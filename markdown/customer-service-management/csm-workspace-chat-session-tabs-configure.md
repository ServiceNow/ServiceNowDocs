---
title: Configure chat session tabs
description: Configure settings such as duration and color for the chat SLA threshold timers for a selected workspace in the Conversational interfaces \(CI\) Admin Console. These timers alert agents to unread messages in inactive chats.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Chat session tabs, CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure chat session tabs

Configure settings such as duration and color for the chat SLA threshold timers for a selected workspace in the Conversational interfaces \(CI\) Admin Console. These timers alert agents to unread messages in inactive chats.

## Before you begin

Role required: virtual\_agent\_admin

## About this task

Enable the [chat session tabs](../concept/csm-workspace-chat-session-tabs.md) feature and select the workspace that the feature applies to.

You can configure a minimum of one and a maximum of three chat SLA threshold timers for a workspace. These timers alert agents to unread messages by changing the [tab colors](../concept/csm-workspace-chat-session-tabs.md#section_rsb_4j2_fdc) of the inactive chats.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

    This displays the CI Admin Experience with the Settings tab selected.

2.  Select **Agent Chat** on the left side of the CI Admin Experience.

    This displays the Agent Chat settings screen.

    **Note:** If you don’t have the required permissions to modify these settings, the following message appears: `You do not have the required permissions to modify these settings. Please contact your administrator.`

3.  In the Session Tab Settings section, enable the **Activate** button in the upper right corner and select **Save**.

    This is a global switch that enables the feature for an instance.

4.  Select **CSM/FSM Configurable Workspace** in the **Select a workspace for tab settings** field.

    This is the workspace for which you want to enable the chat session tabs feature.

5.  Enable the **Session Tab Enabled** button and select **Save**.

    This enables the chat session tabs feature for the selected workspace and adds the Level 1 timer automatically.

    When enabled, inactive tab colors change color to alert agents to unread messages. You can configure a minimum of one and a maximum of three SLA threshold timers that alert agents to impending SLA breaches.

    **Note:** Disabling the Session Tab doesn’t remove the saved workspace. The workspace remains available and can be accessed later.

6.  Configure up to three SLA threshold breach warnings.

    1.  Select the length of the timer for the **SLA breach warning \(Level 1\)**.

        This timer alerts the agent to an SLA breach by changing the color of an inactive tab when it reaches the selected duration. The default setting is 30 seconds after the first new message is received.

    2.  To configure a second SLA breach warning, select **Add Level**.

    3.  Select the length of the timer for the **SLA breach warning \(Level 2\)**.

        This timer alerts the agent to a critical SLA breach by changing the color of an inactive tab when it reaches the selected duration. The default setting is 1 minute after the first new message is received.

        **Note:** The length of time for the Level 2 timer must be greater than the Level 1 timer.

    4.  To configure a third SLA breach warning, select **Add Level**.

    5.  Select the length of the timer for the **SLA breach warning \(Level 3\)**.

        This timer alerts the agent to a severe SLA breach by changing the color of an inactive tab when it reaches the selected duration. The default setting is 2 minutes after the first new message is received.

        **Note:** The length of time for the Level 3 timer must be greater than the Level 2 timer.

7.  Select the tab color for each of the configured SLA threshold breach warnings in the **Tab color** field and then select **Apply**.

    You must select a unique tab color for each warning level. After applying your selection, you can see a preview of the tab with the selected color.

8.  Select **Save**.

    The workspace is added to the Configured workspaces list in the Session Tab Settings section.


