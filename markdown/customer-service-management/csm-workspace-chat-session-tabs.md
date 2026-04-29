---
title: CSM Configurable Workspace chat session tabs
description: Use visual indicators on chat session tabs, such as colors and icons, to alert agents to unread chat messages and SLA threshold timers.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace chat session tabs

Use visual indicators on chat session tabs, such as colors and icons, to alert agents to unread chat messages and SLA threshold timers.

The chat session tabs feature helps agents to manage multiple interactions efficiently. Agents can use visual indicators to reduce the risk of threshold timer breaches, improve chat prioritization, and optimize response times. This feature enables agents to multitask effectively while maintaining service level commitments.

The chat session tabs feature introduces a color-coded system for chat session tabs in CSM Configurable Workspace based on configured Service Level Agreement \(SLA\) thresholds. Additional visual indicators alert agents about unread messages, chat status, and unsaved changes. These visual cues help agents to prioritize their interactions by tracking chat duration and alerting them when conversations require immediate attention.

## Benefits

The chat session tabs feature provides customers with the following benefits.

-   Improved prioritization: Agents can visually track the SLA status of each chat by glancing at the tab color and use that information to prioritize customer responses.
-   Agent multitasking: Tab color changes and real time notifications help agents to handle multiple interactions simultaneously, minimizing the risk of missing crucial chats.
-   Agent productivity: The system helps agents respond more efficiently by highlighting conversations based on urgency, improving customer engagement and satisfaction.

## Key features

Chat session tabs provide the following key features.

<table id="table_rs3_nf3_jdc"><thead><tr><th>

Feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Real-time duration tracking for chat sessions

</td><td>

This feature actively tracks the duration of a chat and alerts the agent when predefined SLA thresholds are reached.-   The timer begins when a customer sends a message to an agent and the tab for that chat interaction is inactive.
-   The inactive tab cycles through different colors to alert the agent to the unread message and the approaching SLA thresholds.
-   The timer resets once the agent engages with the tab.

</td></tr><tr><td>

[SLA threshold timers](csm-workspace-chat-session-tabs.md#section_u4x_lgx_s2c)

</td><td>

Virtual agent admins can configure a minimum of one and a maximum of three levels of SLA threshold timers.

 When the admin selects a workspace and enables the **Session Tab Enabled** button, the system adds the first level automatically. Then they can add one or two additional levels if desired.

 For each level, the admin can select a timer value and tab color.

</td></tr><tr><td>

[Tab colors](csm-workspace-chat-session-tabs.md#section_rsb_4j2_fdc)

</td><td>

Tab colors indicate the status of a chat with one or more unread messages.Inactive tabs with unread messages change color to highlight critical wait times. Virtual agent admins can select a different color for each configured SLA threshold level.

</td></tr><tr><td>

[Unread message counters](csm-workspace-chat-session-tabs.md#section_zq4_1k2_fdc)

</td><td>

Inactive tabs display a counter that shows the number of unread chat messages.The counter uses a background color that is a darker shade of the configured tab color.

</td></tr><tr><td>

Tab messages

</td><td>

Messages on the chat session tabs appear below the customer name and notify the agent of the following chat conditions:-   Chat is in wrap-up
-   Chat has ended

Agents see the appropriate message on the tab depending on the condition of the chat.

</td></tr><tr><td>

Unsaved changes indicator

</td><td>

A gray circle on a chat session tab indicates that there are unsaved changes on the tab. The circle disappears once the changes are saved.

</td></tr></tbody>
</table>## SLA threshold timers

Virtual agent admins can configure up to three levels of SLA threshold timers for inactive chat session tabs. For each level, admins can set a timer and select a unique tab color.

These timers alert agents to unread messages in inactive chats by changing the tab color. If an agent leaves a customer’s chat unanswered beyond the length of time defined in these threshold timers, the system changes the tab color.

<table id="table_sty_rbj_t2c"><thead><tr><th>

Level

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Level 1: warning

</td><td>

This timer alerts the agent to an SLA breach by changing the color of an inactive tab when it reaches the selected duration.Default setting: 30 seconds after the first new message is received.

</td></tr><tr><td>

Level 2: critical

</td><td>

This timer alerts the agent to a critical SLA breach by changing the color of an inactive tab when it reaches the selected duration.The default setting is 1 minute after the first new message is received.

**Note:** The length of time for the Level 2 timer must be greater than the Level 1 timer.

</td></tr><tr><td>

Level 3: severe

</td><td>

This timer alerts the agent to a severe SLA breach by changing the color of an inactive tab when it reaches the selected duration.The default setting is 2 minutes after the first new message is received.

**Note:** The length of time for the Level 3 timer must be greater than the Level 2 timer.

</td></tr></tbody>
</table>For more information, see [Configure chat session tabs](../task/csm-workspace-chat-session-tabs-configure.md).

## Tab colors

The chat session tabs feature uses tab background colors to provide information at a glance. Colors indicate tab status such as the active tab and inactive tabs that have one or more unread messages.

-   **Active tab**: A white background indicates the active tab. This is the tab where the agent is currently working.
-   **Inactive tabs**: A colored background indicates an inactive tab that has one or more unread messages. Tabs transition to different colors to highlight chats that have reached the configured SLA thresholds.

Virtual agent admins can configure up to three SLA threshold levels for chat session tabs. For each level, the admin can set a timer for the threshold level and select a background tab color. Agents see different colors in the chat session tabs based on the threshold timer value.

The background tab color changes when an inactive tab with unread messages reaches the first SLA threshold level. The tab maintains the current color until the timer reaches the next configured SLA threshold level.

For more information, see [Configure chat session tabs](../task/csm-workspace-chat-session-tabs-configure.md).

## Unread message counters

Each inactive tab includes a counter that displays the number of unread chat messages.

The counter uses a background color that is a darker shade of the configured tab color.

![Unread message counters appear as a square on the tab that is a darker shade of the configured tab color. The number of unread messages appears in the square.](../image/chat-session-tabs-unread-message-counters.png "Chat session tab unread message counters")

When a chat message is received, the counter updates to display the total number of unread messages. After selecting the tab, an agent can see the unread messages in the chat window.

Selecting an inactive tab clears the tab color and resets the unread messages counter. The threshold timer and counter restart when the agent navigates away from the tab.

When a customer ends a conversation or a chat session times out, the tab color changes to blue and the unread messages counter disappears.

## Viewing unread messages

When an agent selects an inactive tab and returns to a chat conversation, they can see the unread messages in the chat window. This window uses a separator between the older messages and the unread messages and displays the time when the first unread message was sent. This separator appears if there is a time difference greater than 30 seconds between the first new message and the last previous message.

## Maximum number of tabs

An agent can have a maximum of 10 tabs open at one time. If an agent attempts to open additional tabs, the system displays a message that advises to close one or more tabs before opening a new tab.

## Transferring chats

There are two ways to transfer a chat from one agent to another: manual transfer and automatic transfer.

<table id="table_vll_2hq_jdc"><thead><tr><th>

Transfer type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manual transfer

</td><td>

When an agent manually transfers a chat to another agent and the new agent accepts the chat:-   The unread messages counter is not displayed on the chat session tab.
-   The separator is not displayed between new and older messages. The interaction is treated as new for the receiving agent.
-   The new agent experiences the tab color changes as configured by the admin when new messages arrive from the customer.
-   The new agent sees the unread messages counter update when new messages arrive.

</td></tr><tr><td>

Automatic transfer

</td><td>

When a chat is automatically transferred to another agent or to a queue:-   The unread messages counter is not displayed on the chat session tab. All messages in the chat are in an unread state for the new agent.
-   The separator is not displayed between new and older messages. The interaction is treated as new for the receiving agent.
-   The new agent experiences the tab color changes as configured by the admin when new messages arrive from the customer.
-   The new agent sees the unread messages counter update when new messages arrive.

</td></tr></tbody>
</table>If a chat is transferred to a queue, SLA threshold timers and tab colors are applicable to the next agent who picks up the case.

When an agent seeks help from a colleague or manager using the [Agent Whisper](https://www.servicenow.com/docs/access?context=ci-agent-whisper&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) feature, the SLA threshold timers and tab behavior are applicable only for the owner agent and not for anyone else participating in the interaction.

## Configuring the chat session tabs feature

Users with the Virtual agent admin role can enable the chat sessions tab feature and configure SLA threshold timers for chat sessions from the Conversational Interfaces \(CI\) Admin console.

When this feature is enabled, chat session tabs display colors to indicate the chat status. These colors are determined by SLA threshold timers that alert agents to impending SLA breaches.

For more information, see [Configure chat session tabs](../task/csm-workspace-chat-session-tabs-configure.md).

