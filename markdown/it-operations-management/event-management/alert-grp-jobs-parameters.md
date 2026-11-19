---
title: Scheduled jobs and parameters for alert grouping
description: Automate alert organization by configuring jobs to group alerts based on predefined criteria and parameters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/alert-grp-jobs-parameters.html
release: brazil
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-11-15"
reading_time_minutes: 5
keywords: [alert grouping, grouping time windows, dynamic window, maximum group lifetime, group expiration time, scheduled job, Event Management]
breadcrumb: [Alert grouping, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Scheduled jobs and parameters for alert grouping

Automate alert organization by configuring jobs to group alerts based on predefined criteria and parameters.

To group alerts in Automated, CMDB, Text-based, Tag Cluster, and Network Traffic Correlation groups, the scheduled job named **Service Analytics group alerts using RCA/Alert Aggregation** is typically run once per minute. This job handles the grouping of alerts based on the specified method. Additionally, you can run multiple scheduled jobs in parallel to manage alert grouping. For further details, see [Run multiple scheduled jobs for alert grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/run-multiple-alert-group-scheduled-jobs.md).

To define which alerts are grouped, the following parameters are used:

-   **sa\_analytics.aggregation\_enabled**: Enables alert grouping created by the scheduled job. Set the property **Enable alert aggregation for Automated, CMDB, and Text-Based groups** to `true` to activate this feature.

    **Note:** This property also applies to Tag Cluster and Network Traffic Correlation grouping.

-   **sa\_analytics.agg.query\_dynamic\_window**: Sets the maximum time difference allowed between the event time of a new alert and the latest alert in a group. The default is 10 minutes \(600 seconds\). For details, see [Time windows that determine when alerts join a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/alert-grp-jobs-parameters.md).
-   **sa\_analytics.agg.query\_max\_group\_lifetime**: Sets the maximum time from the first alert to the last alert in a group. The default is 30 minutes \(1800 seconds\). For details, see [Time windows that determine when alerts join a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/alert-grp-jobs-parameters.md).
-   **sa\_analytics.agg.group\_expiration\_time**: Keeps groups available for alerts that arrive after group formation. By default, this is not set \(0\). For details, see [Why an alert can join after a group has formed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/alert-grp-jobs-parameters.md).

**Note:** Some parameters, such as **sa\_analytics.agg.query\_dynamic\_window**, **sa\_analytics.agg.query\_max\_group\_lifetime**, and **sa\_analytics.agg.group\_expiration\_time**, are not provided in the base system. To use these properties, you need to create properties with the same names and assign the required values to them. For more information on how to create a property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md).

## Time windows that determine when alerts join a group

The scheduled job controls Automated, CMDB, and text-based alert grouping. Two time checks determine whether a new alert can join an existing group:

1.  Dynamic window \(**sa\_analytics.agg.query\_dynamic\_window**, 10 minutes by default\). The event time of the alert must fall within the window of the latest alert in the group, not the primary alert. The time gap is an absolute value, so an alert with an older event time is checked in the same way. Each alert that joins moves the latest time of the group forward. The window slides, and the group can grow beyond the first 10 minutes.
2.  Maximum group lifetime \(**sa\_analytics.agg.query\_max\_group\_lifetime**, 30 minutes by default\). The time from the first alert to the last alert in the group cannot exceed this limit. An alert that would extend the group beyond this limit cannot join, even if it passes the dynamic window check. The alert starts a new group instead.

For Tag Cluster groups, alerts are added based on the clustering timeframe in the tag-based alert clustering definition, measured from the first alert. For more information, see [Tag cluster alert grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/event-management/alert-clustering-tag-definitions-concept.md).

## Alert grouping example

For tag-cluster grouping, alerts are added to a group based on the timeframe parameter defined in the alert tag clustering settings. For automated, CMDB, text-based, and network traffic grouping, alerts are aggregated as follows.

Consider the following alerts, which have the same CI and may all be added to the same CMDB group:

-   Alert1: Initial event generation at 01:00:00 a.m.
-   Alert2: Initial event generation at 01:11:00 a.m.
-   Alert3: Initial event generation at 01:13:00 a.m.
-   Alert4: Initial event generation at 01:16:00 a.m.
-   Alert5: Initial event generation at 01:25:00 a.m.
-   Alert6: Initial event generation at 01:34:00 a.m.
-   Alert7: Initial event generation at 01:43:00 a.m.

Alert1 and Alert2 are not grouped due to the time gap exceeding 10 minutes. Alert2 and Alert3 create a group at 01:13:00 a.m. The 10-minute dynamic window starts at 01:13:00 a.m., with the following:

-   Alert4 is added to the group at 01:16:00 a.m., restarting the 10-minute window.
-   Alert5 and Alert6 are added to the group because their event times are within the 10-minute window of the latest alert in the group.
-   Alert7 is not added. Its event time is 9 minutes after Alert6, which is within the 10-minute window. Adding it would exceed the 30-minute maximum group lifetime, which ends at 01:41:00 a.m. \(30 minutes after Alert2, the first alert, at 01:11:00 a.m.\). Alert7 starts a new group instead.

## Alert joining after group formation

An alert can join an existing group after the group has formed, for the following reasons:

-   The grouping job runs about once a minute, so alerts are constantly evaluated against existing groups.
-   Eligibility depends on the event time of the alert, not on when the alert arrives. An alert that arrives late can still qualify if its event time fits the dynamic window and the maximum group lifetime.
-   The dynamic window slides each time an alert joins, so groups can grow well past the first window.
-   Retention settings determine whether groups are available for delayed alerts. Use the **sa\_analytics.agg.group\_expiration\_time** property to keep groups available for longer, so that alerts that arrive late can still be evaluated. This property does not change the maximum group lifetime. To allow groups longer than 30 minutes, increase **sa\_analytics.agg.query\_max\_group\_lifetime**.
-   Correlation logic runs once per alert, at creation. An alert can also be added later when a new incoming alert matches and triggers the grouping logic.

**Note:** After an alert is created, correlation logic is applied only once. Changes to the alert after its creation are not re-evaluated for correlation. If correlation is not established initially, the alert may still be added to a group later—but only if a new incoming alert matches and triggers the grouping logic.

