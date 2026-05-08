---
title: ITSM Configurable Workspace chat session tabs in SOW
description: Use visual indicators on chat session tabs, such as colors and icons, to alert agents about unread messages and SLA threshold timers.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Configuring Interaction Management in Service Operations Workspace, Configuring Service Operations Workspace for ITSM to improve your experience, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# ITSM Configurable Workspace chat session tabs in SOW

Use visual indicators on chat session tabs, such as colors and icons, to alert agents about unread messages and SLA threshold timers.

The chat session tabs feature helps agents to manage multiple interactions efficiently. Agents can use visual indicators to reduce the risk of threshold timer breaches, improve chat prioritization, and optimize response times. This feature enables agents to multitask effectively while maintaining service level commitments.

The chat session tabs feature introduces a color-coded system for chat session tabs in Configurable Workspace based on configured Service Level Agreement \(SLA\) thresholds. Additional visual indicators alert agents about unread messages, chat status, and unsaved changes. These visual cues help agents to prioritize their interactions by tracking chat duration and alerting them when conversations require immediate attention.

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

Tab colors

</td><td>

This feature uses tab colors to indicate the status of a chat with one or more unread messages.-   Inactive tabs display a purple background color to indicate that a message has been received.
-   Tab colors shift to yellow and then to red to highlight critical wait times.

For more information, see [Tab colors](sow-itsm-workspace-chat-session-tabs.md#section_rsb_4j2_fdc).

</td></tr><tr><td>

Unread message counters

</td><td>

Inactive tabs display a counter that shows the number of unread chat messages.For more information, see [Unread message counters](sow-itsm-workspace-chat-session-tabs.md#section_zq4_1k2_fdc).

</td></tr><tr><td>

Tab messages

</td><td>

Messages on the chat session tabs appear after the customer name and notify the agent of the following chat conditions:-   Chat is in wrap-up
-   Chat has ended

Agents see the appropriate message on the tab depending on the condition of the chat.

</td></tr><tr><td>

Unsaved changes indicator

</td><td>

A gray circle on a chat session tab indicates that there are unsaved changes on the tab. The circle disappears once the changes are saved.

</td></tr></tbody>
</table>## Benefits

The chat session tabs feature provides the following benefits.

-   Improved prioritization: Agents can visually track the SLA status of each chat by glancing at the tab color and use that information to prioritize customer responses.
-   Agent multitasking: Tab color changes and real time notifications help agents to handle multiple interactions simultaneously, minimizing the risk of missing crucial chats.
-   Agent productivity: The system helps agents respond more efficiently by highlighting conversations based on urgency, improving customer engagement and satisfaction.

## Tab colors

The chat session tabs feature uses tab background colors to provide information at a glance. Colors indicate the status of inactive chat session tabs that have one or more unread messages.

-   Tabs display a purple background color to indicate that a message has been received.
-   Tab colors transition to yellow and then to red to highlight chats that have reached SLA thresholds.

Administrators can configure threshold levels for chat sessions that set timer values and tab background colors for the thresholds. Agents see different colors in the chat session tabs based on the threshold timer value.

**Note:** Default values are provided for the SLA threshold timers. For more information about changing these values, see [Configure chat session tabs in SOW](../task/sow-itsm-workspace-chat-session-tabs-configure.md).

<table id="table_v2g_pcc_jdc"><thead><tr><th>

Tab color

</th><th>

Example

</th><th>

Description

</th></tr></thead><tbody><tr><td>

White

</td><td>

![Active chat session tab with white background](../image/chat-session-tabs-white.png)

</td><td>

Indicates the active tab. This is the tab where the agent is currently working.

</td></tr><tr><td>

Purple

</td><td>

![Inactive chat session tab with purple background](../image/chat-session-tabs-purple.png)

</td><td>

Indicates an inactive tab that has one or more unread messages from a customer.The chat duration timer begins when the first message is received. The tab remains purple for 0-30 seconds \(default value\), at which point the timer reaches the warning SLA threshold level.

-   The inactive tab cycles through different colors to alert the agent about the unread message and the approaching SLA thresholds.
-   The timer resets once the agent engages with the tab.

</td></tr><tr><td>

Yellow

</td><td>

![Inactive chat session tab with yellow background and unread message counter](../image/chat-session-tabs-yellow.png)

</td><td>

Indicates an inactive tab with unread messages that has reached the warning SLA threshold level.The tab remains yellow for 30-60 seconds \(default value\), at which point the timer reaches the critical SLA threshold level. The tab also includes a warning icon.

See [SLA threshold timers](sow-itsm-workspace-chat-session-tabs.md#section_ffn_zlb_jdc) for more information.

</td></tr><tr><td>

Red

</td><td>

![Inactive chat session tab with red background and unread message counter](../image/chat-session-tabs-red.png)

</td><td>

Indicates an inactive tab with unread messages that has reached the critical SLA threshold level. The tab remains red until the agent selects it and restarts the timer. The tab also includes a critical icon.

See [SLA threshold timers](sow-itsm-workspace-chat-session-tabs.md#section_ffn_zlb_jdc) for more information.

</td></tr></tbody>
</table>## SLA threshold timers

Administrators can configure warning and critical SLA threshold timers for inactive chat session tabs. If an agent leaves a customer’s chat unanswered beyond the length of time defined in these threshold timers, the system changes the tab color.

The chat session tabs feature includes the following default SLA threshold timer settings. For more information about changing these values, see [Configure chat session tabs in SOW](../task/sow-itsm-workspace-chat-session-tabs-configure.md).

<table id="table_b2f_dbd_jdc"><thead><tr><th>

Threshold timer

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Warning of SLA breach

</td><td>

The chat duration timer begins when the first chat message is received from a customer and the agent is away from the chat interaction.After 30 seconds \(default value\), the chat session tab turns yellow and displays a warning icon to alert the agent of an impending SLA breach. The tab remains yellow 30–60 seconds.

</td></tr><tr><td>

Critical SLA breach

</td><td>

After 1 minute \(default value\), the chat session tab turns red and displays a critical icon to alert the agent of an impending SLA breach.The tab remains red until the agent selects it and restarts the timer.

</td></tr></tbody>
</table>## Unread message counters

Each inactive tab includes a counter that displays the number of unread chat messages. This counter appears as a red square that displays the number of unread messages.

**Note:** The unread messages counter is displayed on inactive tabs of any background color.

When a chat message is received, the counter updates to display the total number of unread messages. After selecting the tab, an agent can see the unread messages in the chat window.

Selecting an inactive tab clears the tab color and resets the unread messages counter. The threshold timer and counter restart when the agent navigates away from the tab.

## Viewing unread messages

When an agent selects an inactive tab and returns to a chat conversation, they can see the unread messages in the chat window. This window uses a separator between the older messages and the unread messages and displays the time when the first unread message was sent. This separator appears if there’s a time difference greater than 30 seconds between the first new message and the last seen message.

## Maximum number of tabs

An agent can have a maximum of 10 tabs open at one time. If an agent attempts to open additional tabs, the system displays a message that advises closing one or more tabs before opening a new tab.

## Transferring chats

There are two ways to transfer a chat from one agent to another: manual transfer and automatic transfer.

<table id="table_vll_2hq_jdc"><thead><tr><th>

Transfer type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Manual transfer

</td><td>

When an agent manually transfers a chat to another agent and the new agent accepts the chat:-   The unread messages counter isn’t displayed on the chat session tab.
-   The separator isn’t displayed between new and older messages. The interaction is treated as new for the receiving agent.
-   The new agent experiences the tab color changes as configured by the admin when new messages arrive from the customer.
-   The new agent sees the unread messages counter update when new messages arrive.

</td></tr><tr><td>

Automatic transfer

</td><td>

When a chat is automatically transferred to another agent or to a queue:-   The unread messages counter isn’t displayed on the chat session tab. All messages in the chat are in an unread state for the new agent.
-   The separator isn’t displayed between new and older messages. The interaction is treated as new for the receiving agent.
-   The new agent experiences the tab color changes as configured by the admin when new messages arrive from the customer.
-   The new agent sees the unread messages counter update when new messages arrive.

</td></tr></tbody>
</table>If a chat is transferred to a queue, SLA threshold timers and tab colors are applicable to the next agent who picks up the case.

When an agent seeks help from a colleague or manager using the Agent Whisper feature, the SLA threshold timers and tab behavior are applicable only for the owner agent and not for anyone else participating in the interaction.

## Configuring the chat session tabs feature

Users with the administrator role can enable the chat sessions tab feature and configure SLA threshold timers for chat sessions from the SOW admin center.

When this feature is enabled, chat session tabs display colors to indicate the chat status. These colors are determined by SLA threshold timers that alert agents of impending SLA breaches. This feature includes two SLA threshold timers with default settings:

-   Warning of SLA breach
-   Critical SLA breach

For more information, see [Configure chat session tabs in SOW](../task/sow-itsm-workspace-chat-session-tabs-configure.md).

-   **[Configure chat session tabs in SOW](../task/sow-itsm-workspace-chat-session-tabs-configure.md)**  
Enable the chat session tabs feature and configure values for the chat SLA threshold timers in the SOW admin center.

**Parent Topic:**[Configuring Interaction Management in Service Operations Workspace](configure-interaction-management-sow.md)

