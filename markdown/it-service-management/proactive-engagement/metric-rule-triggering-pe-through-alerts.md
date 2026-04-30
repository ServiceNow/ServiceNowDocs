---
title: Metric rule triggering Proactive Engagement through alerts
description: Metric rules create an alert based on its trigger criteria.
locale: en-US
release: xanadu
product: Proactive Engagement
classification: proactive-engagement
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Proactive Engagement, Proactive Engagement, IT Service Management]
---

# Metric rule triggering Proactive Engagement through alerts

Metric rules create an alert based on its trigger criteria.

Alert actions are triggered when an alert is created in the specified criteria. You can create an alert based on the values shared in the system properties. The system properties can be set as conditions based on which the alert action is triggered. Applications and devices need a different set of system properties to be set. The alert action is triggered when an alert is created based on the specified criteria and the conditions met. Through system properties, you can customize the values of these conditions.

-   Alert action for this metric rule is not triggered in the last 72 hours for the user.
-   Fewer than 100 users are impacted for this metric rule within an 8 hour window.

|System property|Condition|Description|Type|
|---------------|---------|-----------|----|
|sn\_pren.resolution\_freeze\_period|Metric rule not triggered in the last 72 hours \(default\).|The duration \(in hours\) for imposing a freeze period for a specific user for any unique metric rule configured in Proactive Engagement. Set this value to zero to disable the rule.|integer|
|sn\_pren.device\_resolution.user\_limit\_per\_throttling\_window|Fewer than 100 users \(default\) are impacted.|Maximum number of users for which a Proactive Engagement device-related resolution is triggered within a defined time period. The value of the time period configured in property sn\_pren.device\_resolution.throttling\_window\_duration.|integer|
|sn\_pren.device\_resolution.throttling\_window\_duration|Within an 8-hour \(default\) window|The time period in minutes within which a Proactive Engagement device-related resolution is throttled. This resolution is throttled if the impacted number of users exceed the value in property sn\_pren.device\_resolution.user\_limit\_per\_throttling\_window.|integer|
|sn\_pren.application\_resolution.user\_limit\_per\_throttling\_window|Fewer than 100 users impacted|Maximum number of users for which a Proactive Engagement application-related resolution is triggered. This resolution is triggered within a defined time period \(value of the time period configured in property sn\_pren.application\_resolution.throttling\_window\_duration\).|string|
|sn\_pren.application\_resolution.throttling\_window\_duration|Within an hour window|The time period in minutes within which a Proactive Engagement application-related resolution is throttled. This resolution is throttled when the impacted number of users exceed the value in property sn\_pren.application\_resolution.user\_limit\_per\_throttling\_window.|integer|

![Metric rule triggering Proactive Engagement through alerts](../images/pe_dexint.png)

## Alert closure in Proactive Engagement

There are different methods followed for closing the alerts in Proactive Engagement for devices and applications.

-   Devices: Alerts generated from Metric rule triggered for devices, are closed once Proactive Engagement helps the impacted users to successfully resolve their issue.
-   Applications: Alerts generated from Metric rule triggered for applications are not closed.

**Parent Topic:**[Using Proactive Engagement](../using-proactive-engagement.md)

