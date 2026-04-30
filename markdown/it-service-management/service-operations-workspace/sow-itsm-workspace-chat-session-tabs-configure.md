---
title: Configure chat session tabs in SOW
description: Enable the chat session tabs feature and configure values for the chat SLA threshold timers in the SOW admin center.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ITSM Configurable Workspace chat session tabs in SOW, Configuring Interaction Management in Service Operations Workspace, Configuring Service Operations Workspace for ITSM to improve your experience, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure chat session tabs in SOW

Enable the chat session tabs feature and configure values for the chat SLA threshold timers in the SOW admin center.

## Before you begin

Role required: admin

## About this task

Enable the [ITSM Configurable Workspace chat session tabs in SOW](../concept/sow-itsm-workspace-chat-session-tabs.md) feature and select the workspace that the feature applies to. You can also select values for two different chat SLA threshold timers that alert agents about unread messages in inactive chats. These timers alert agents by changing the tab colors of the inactive chats. For more information to change the tab colors, see [tab colors](../concept/sow-itsm-workspace-chat-session-tabs.md#section_rsb_4j2_fdc).

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace Admin Center** &gt; **Overview**.

2.  Select **Configure** on **Interaction Management** from the **ITSM core configurations** section.

3.  Turn on the information sessions tabs option by rotating the Information session tabs toggle counterclockwise.

4.  In the Information session tabs section, do the following:

    1.  **Timer for warning of SLA breach**: Enter the value in the field for the tab color to turn from purple to yellow.

        Select the length of the timer for the warning of an SLA breach. This timer changes the tab color to yellow when it reaches the selected duration. The default setting is 30 seconds after the first new message is received.

    2.  **Timer for critical SLA breach**: Enter the value for the timer for the tab color to turn from yellow to red.

        Select the length of the timer for a critical SLA breach. This timer changes the tab color to red when it reaches the selected duration. The default setting is two minutes after the first new message is received.

5.  Select **Save**.


**Parent Topic:**[ITSM Configurable Workspace chat session tabs in SOW](../concept/sow-itsm-workspace-chat-session-tabs.md)

