---
title: Properties for Connect Support
description: The Connect Support Properties page provides several configuration options specifically for Connect Support.
locale: en-US
release: australia
product: Connect
classification: connect
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Connect Support administration, Connect Support, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Properties for Connect Support

The Connect Support Properties page provides several configuration options specifically for Connect Support.

**Important:**

Starting with Utah, Connect Support has been deprecated. For similar capabilities, please move to Advanced Work Assignment and Agent Chat. For details, see [Move from Connect Support to Advanced Work Assignment and Agent Chat](https://www.servicenow.com/docs/access?context=migrate-from-connect-support&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

These properties are available for Connect Support.

<table id="table_tjz_1kc_mv"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Should Connect be used for handling chat queue entriesglide.connect.support.enabled

</td><td>

Disables or enables Connect Support. When the property is enabled, the **Service Desk Chat** button in the Employee Self-Service portal opens the conversation in Connect Support, rather than legacy chat. Additionally, the Support tab appears in the Connect sidebar.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

Number of support conversations an individual agent can have at one time \(-1 is unlimited\)connect.support.conversation\_limit

</td><td>

Determines how many support conversations an individual agent can have at one time. When the value is set to **-1**, an agent can participate in an unlimited number of conversations.-   **Type**: integer
-   Default value: -1
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

Show agent avatar in Connect Support conversations.connect.support.show\_agent\_avatar

</td><td>

Determines whether an agent's avatar is shown in a support conversation \(enabled\). When the property is disabled, users see the agent's name only.-   **Type**: true \| false
-   Default value: true
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

Number of seconds to wait \(without user interaction\), before presenting end users with an idle countdown timerconnect.support.idle.delay

</td><td>

Determines how many seconds a user must be inactive in a support conversation before an idle countdown timer appears.-   **Type**: integer
-   Default value: 120
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

Number of seconds to count down from before marking end user as having left their support sessionconnect.support.idle.count\_down

</td><td>

Determines how many seconds the idle countdown timer remains open after it appears. If the idle user does not dismiss the timer before the countdown completes, the system closes the support session.-   **Type**: integer
-   Default value: 60
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr><tr><td>

Limits the number of closed conversations that the support user can see. \(0 = unlimited\)connect.support.user.closed.conversation\_limit

</td><td>

Determines how many closed conversations appear in a user's support conversation history. When the value is set to **0**, all previous conversations appear in the history.-   **Type**: integer
-   Default value: 0
-   Location: **Collaborate** &gt; **Support Administration** &gt; **Properties**

</td></tr></tbody>
</table>