---
title: Properties installed with Connect Support
description: Properties are added with activation of Connect Support.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Properties installed with Connect Support

Properties are added with activation of Connect Support.

<table id="table_vmr_bbd_br1"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

connect.support.conversation\_limit

</td><td id="Entry_ConnectSupportConversationLimitDescription">

Determines how many support conversations an individual agent can have at one time. When the value is set to **-1**, an agent can participate in an unlimited number of conversations.-   **Type**: integer
-   Default value: -1
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.idle.delay

</td><td id="entry_ConnectSupportIdleDelayDescription">

Determines how many seconds a user must be inactive in a support conversation before an idle countdown timer appears.-   **Type**: integer
-   Default value: 120
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.idle.count\_down

</td><td id="entry_ConnectSupportIdleCountDownDescription">

Determines how many seconds the idle countdown timer remains open after it appears. If the idle user does not dismiss the timer before the countdown completes, the system closes the support session.-   **Type**: integer
-   Default value: 60
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.show\_agent\_avatar

</td><td id="entry_ConnectSupportShowAgentAvatarDescription">

Determines whether an agent's avatar is shown in a support conversation \(enabled\). When the property is disabled, users see the agent's name only.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

connect.support.user.closed.conversation\_limit

</td><td id="entry_ConnectSupportUserClosedConversationLimitDescription">

Determines how many closed conversations appear in a user's support conversation history. When the value is set to **0**, all previous conversations appear in the history.-   **Type**: integer
-   Default value: 0
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

glide.connect.support.enabled

</td><td id="entry_GlideConnectSupportEnabledDescription">

Disables or enables Connect Support. When the property is enabled, the **Service Desk Chat** button in the Employee Self-Service portal opens the conversation in Connect Support, rather than legacy chat. Additionally, the Support tab appears in the Connect sidebar.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

glide.connect.support.reflect\_system\_messages

</td><td>

Controls whether Connect Support reflects system messages in records created from a support chat, for example, transfer notices, automated queue messages, etc.-   **Type**: true \| false
-   **Default value**: false
-   Location: System Property \[sys\_properties\] table

</td></tr></tbody>
</table>