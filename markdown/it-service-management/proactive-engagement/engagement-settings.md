---
title: Engagement Settings for Proactive Engagement
description: It allows you to configure and define how an end user should be engaged to self-solve the issue.
locale: en-US
release: australia
product: Proactive Engagement
classification: proactive-engagement
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Proactive Engagement, Digital End-User Experience, IT Service Management]
---

# Engagement Settings for Proactive Engagement

It allows you to configure and define how an end user should be engaged to self-solve the issue.

Virtual Agent and Desktop Assistant are the notification channels used to notify the user. As a fallback, an incident can be created, or the user is routed to a live agent. The following field names are displayed in the Engagement settings tab while creating a Proactive Engagement resolution from the metric rules.

<table id="table_c4x_v3l_xbc"><thead><tr><th>

Field name

</th><th>

Description

</th><th>

Options

</th></tr></thead><tbody><tr><td>

**User engagement**

</td><td>

Decide if this resolution needs end user engagement or could be executed silently when triggered.

</td><td>

-   Engage user
-   Silent execution \(remedial action\)
-   Notification only \(self-help instructions and URL\).

</td></tr><tr><td>

**Engagement channel**

</td><td>

Select the channel of engagement.**Note:** Install `com.glide.cs.chatbot` to avail virtual agent as the engagement channel.

</td><td>

Virtual Agent

</td></tr><tr><td>

**Notification channel**

</td><td>

Channel where the user will be proactively notified. Configure the notification channels from `sn_pren-channel-configuration` from [Metric rule triggering Proactive Engagement through alerts](../concept/metric-rule-triggering-pe-through-alerts.md). This channel is applicable only if the engagement type is Notification only.

</td><td>

-   Virtual Agent
-   Desktop Assistant
-   Email Notification

</td></tr><tr><td>

**User Notification message**

</td><td>

Details the message that should be sent to engage the user.

</td><td>

Custom messageExample: Your device is running low on disk space. Would you like help to free up some space?

</td></tr><tr><td>

**Resolution needs consent**

</td><td>

Decide if user's consent is needed for the resolution before executing any action on the end-user device. This option is available only for Remedial Action and Create Incident resolution types.

</td><td>

Yes/No

</td></tr><tr><td>

**User consent message**

</td><td>

Details the message where user consent is required.

</td><td>

Custom messageExample: Can we free up some disk space using Windows disk clean-up? This will only clear temp files and recycle bin. Your work will not be affected in any way.

</td></tr><tr><td>

**Choose email notification**

</td><td>

This option is applicable only when we select self-help instructions or URL and select Email notification as the notification channel.**Note:** Choose email notification is visible only for notification channel Email.

</td><td>

Proactive Engagement notification.

</td></tr><tr><td>

**Issue reference name**

</td><td>

The issue reference name is used to identify the issue when communicating with the user.

</td><td>

low disk space/disconnected Zscaler

</td></tr><tr><td>

**Fallback when self-remediation is not successful.**

</td><td>

Select the fallback option that will be triggered when the resolution fails.

</td><td>

Create incident/Route to live agent

</td></tr></tbody>
</table>These engagement settings are furnished when you configure the metric rule. To configure a new metric rule, see [Configuring Proactive Engagement resolutions with DEX](../configuring-metric-rule.md).

**Parent Topic:**[Proactive Engagement reference](../proactive-engagement-reference.md)

