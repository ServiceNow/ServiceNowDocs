---
title: Metric rule triggering Proactive Engagement through alerts
description: Metric rules create alerts based on their trigger criteria, and the alert actions trigger Proactive Engagement.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/metric-rule-triggering-pe-through-alerts.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Use Proactive Engagement, Digital End-User Experience, IT Operations Management]
---

# Metric rule triggering Proactive Engagement through alerts

Metric rules create alerts based on their trigger criteria, and the alert actions trigger Proactive Engagement.

Alert actions are triggered when an alert is created based on the specified criteria. You can create an alert based on the values shared in the system properties. The system properties can be set as conditions based on which the alert action is triggered. Applications and devices require different sets of system properties. The alert action is triggered when an alert is created based on the specified criteria and the conditions are met. Through system properties, you can customize the values of these conditions.

-   The alert action for this metric rule hasn't been triggered in the last 72 hours for the user.
-   Fewer than 100 users are impacted for this metric rule within an 8-hour window.

<table id="table_plz_zpb_1cc"><thead><tr><th>

System property

</th><th>

Condition

</th><th>

Description

</th><th>

Type

</th></tr></thead><tbody><tr><td>

sn\_pren.resolution\_freeze\_period

</td><td>

Metric rule not triggered in the last 72 hours \(default\).

</td><td>

The duration \(in hours\) for imposing a freeze period for a specific user for any unique metric rule configured in Proactive Engagement. Set this value to zero to turn off the freeze period.

</td><td>

integer

</td></tr><tr><td>

sn\_pren.device\_resolution.user\_limit\_per\_throttling\_window

</td><td>

Fewer than 100 users \(default\) are impacted.

</td><td>

Maximum number of users for which a Proactive Engagement device-related resolution is triggered within a defined time period. The time period is configured in the property sn\_pren.device\_resolution.throttling\_window\_duration.

</td><td>

integer

</td></tr><tr><td>

sn\_pren.device\_resolution.throttling\_window\_duration

</td><td>

Within an 8-hour \(default\) window

</td><td>

The time period in minutes within which a Proactive Engagement device-related resolution is throttled. This resolution is throttled if the number of impacted users exceeds the value in the property sn\_pren.device\_resolution.user\_limit\_per\_throttling\_window.

</td><td>

integer

</td></tr><tr><td>

sn\_pren.application\_resolution.user\_limit\_per\_throttling\_window

</td><td>

Fewer than 100 users impacted

</td><td>

Maximum number of users for which a Proactive Engagement application-related resolution is triggered. This resolution is triggered within a defined time period \(value of the time period configured in property sn\_pren.application\_resolution.throttling\_window\_duration\).

</td><td>

string

</td></tr><tr><td>

sn\_pren.application\_resolution.throttling\_window\_duration

</td><td>

Within a 1-hour window

</td><td>

The time period in minutes within which a Proactive Engagement application-related resolution is throttled. This resolution is throttled when the number of impacted users exceeds the value in the property sn\_pren.application\_resolution.user\_limit\_per\_throttling\_window.

</td><td>

integer

</td></tr><tr><td>

sn\_pren\_channel\_configuration

</td><td>

Turn on or turn off the notification channels used to notify users.

</td><td>

Administrators can turn on or turn off notification channels in the wizard.

 These notification channels are listed only when the related plugin is installed.

</td><td>

string

</td></tr></tbody>
</table>\[Omitted image "pe\_dexint.png"\] Alt text: Metric rule triggering Proactive Engagement through alerts

## Alert closure in Proactive Engagement

Alerts are closed differently in Proactive Engagement for devices and applications.

-   Devices: Alerts generated from metric rules triggered for devices are closed after Proactive Engagement helps the impacted users resolve their issues.
-   Applications: Alerts generated from metric rules triggered for applications aren't closed.

**Parent Topic:**[Using Proactive Engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/using-proactive-engagement.md)

