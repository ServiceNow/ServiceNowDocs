---
title: Engagement settings for Proactive Engagement
description: Engagement settings define how an end user is engaged to self-solve an issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/engagement-settings.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Engagement settings for Proactive Engagement

Engagement settings define how an end user is engaged to self-solve an issue.

Virtual Agent and Desktop Assistant are the notification channels used to notify the user. As a fallback, an incident can be created, or the user is routed to a live agent. The fields in the following table appear on the Engagement settings tab when you create a Proactive Engagement resolution from the metric rules.

<table id="table_c4x_v3l_xbc"><thead><tr><th>

Field name

</th><th>

Description

</th><th>

Options

</th></tr></thead><tbody><tr><td>

**User engagement**

</td><td>

Option that determines whether the resolution requires end-user engagement or runs silently when triggered.

</td><td>

-   Engage user
-   Silent execution \(remedial action\)
-   Notification only \(self-help instructions and URL\)

</td></tr><tr><td>

**Engagement channel**

</td><td>

Channel used to engage the user.**Note:** To use Virtual Agent as the engagement channel, activate the `com.glide.cs.chatbot` plugin.

</td><td>

Virtual Agent

</td></tr><tr><td>

**Notification channel**

</td><td>

Channel through which the user is proactively notified. Configure the notification channels in the `sn_pren-channel-configuration` system property. For more information, see [Metric rule triggering Proactive Engagement through alerts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/metric-rule-triggering-pe-through-alerts.md). This channel is applicable only if the engagement type is Notification only.

</td><td>

-   Virtual Agent
-   Desktop Assistant
-   Email Notification

</td></tr><tr><td>

**User Notification message**

</td><td>

Message sent to engage the user.

</td><td>

Custom messageExample: Your device is running low on disk space. Would you like help to free up some space?

</td></tr><tr><td>

**Resolution needs consent**

</td><td>

Option that determines whether the user's consent is required before any action runs on the end-user device. This option is available only for Remedial Action and Create Incident resolution types.

</td><td>

Yes/No

</td></tr><tr><td>

**User consent message**

</td><td>

Message that requests the user's consent.

</td><td>

Custom messageExample: Can we free up some disk space using Windows disk clean-up? This will only clear temp files and recycle bin. Your work will not be affected in any way.

</td></tr><tr><td>

**Choose email notification**

</td><td>

Option that applies only when you select self-help instructions or URL and select Email notification as the notification channel.**Note:** The Choose email notification field appears only when the notification channel is Email.

</td><td>

Proactive Engagement notification.

</td></tr><tr><td>

**Issue reference name**

</td><td>

Name used to identify the issue when communicating with the user.

</td><td>

low disk space/disconnected Zscaler

</td></tr><tr><td>

**Fallback when self-remediation is not successful**

</td><td>

Fallback option that is triggered when the resolution fails.

</td><td>

Create incident/Route to live agent

</td></tr></tbody>
</table>You configure these engagement settings when you configure the metric rule. To configure a metric rule, see [Configure Proactive Engagement resolutions with DEX](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/configuring-metric-rule.md).

