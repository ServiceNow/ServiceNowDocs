---
title: Key alerts – activation and notifications
description: Use the Instance Observer Key Alerts Activation functionality for flexibility to set alerts with historical thresholds from four week increments specific to your business needs and configure who on your team receives notifications.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Alerts in Instance Observer, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Key alerts – activation and notifications

Use the Instance Observer Key Alerts Activation functionality for flexibility to set alerts with historical thresholds from four week increments specific to your business needs and configure who on your team receives notifications.

**Note:** Instance Observer **Alerts** support is only available for Advanced and Total packages of ServiceNow Impact.

Keys alerts activation will provide you with proactive alerts about moving averages, a statistic that captures the average change in a data series over time, for six critical metrics:

1.  **Transaction \(increase\) Instance**: Indicates transaction moving average increases by a certain percentage of it's historical median for a certain time period.
2.  **Transaction \(drop\) Instance**: Indicates transaction moving average drops by a certain percentage of it's historical median for a certain time period.
3.  **Response Time – Instance**: Indicates the moving average of response time is greater than the historical median in a certain time period.
4.  **Database Response Time**: Indicates the moving average of database response time is greater than the historical median in a certain time period.
5.  **Default Semaphore Mean**: Indicates the default semaphore mean is approaching limits of max concurrency by a certain factor in a certain time period.
6.  **Default Semaphore Queue Depth**: Indicates the default semaphore queue depth is approaching limits of maximum queue depth by a certain factor in a certain time period.

**Note:** It is important to note that each notification may not represent an issue, moreover signals about a data point that is unusual or does not conform to the expected patterns for that specific metric. Users can be proactive, where necessary, and act on a notification accordingly that may avoid a future issue.

Instance Observer utilizes the P-Score to assess instance usage, then calculate the thresholds exclusively for those instances. The P-score is a rating determined by the number of transactions on an instance, providing a higher score when the instance's transactions remain consistently stable.

-   When an instance meets the required P-Score for eligibility, users will see a banner to opt-in for the alerts activation feature. Users will receive intelligent thresholds under the **IO recommended** condition for all six metrics derived from historical data.
-   If an instance has a low P-Score, the banner to opt-in for alerts activation feature will not be visible. The P-Score is regularly refreshed, and as instances grow in the future, you will see the option to opt-in for the alerts activation feature. Thresholds are refreshed automatically weekly for instances meeting the minimum P-Score criteria.

To set up alerts, see [Configure Key Alerts](../task/configuring-io-alerts.md).

