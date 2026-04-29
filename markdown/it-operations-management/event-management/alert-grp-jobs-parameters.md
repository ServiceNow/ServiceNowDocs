---
title: Scheduled jobs and parameters for alert grouping
description: Automate alert organization by configuring jobs to group alerts based on predefined criteria and parameters.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Scheduled jobs and parameters for alert grouping

Automate alert organization by configuring jobs to group alerts based on predefined criteria and parameters.

To group alerts in Automated, CMDB, Text-based, Tag Cluster, and Network Traffic Correlation groups, the scheduled job named **Service Analytics group alerts using RCA/Alert Aggregation** is typically run once per minute. This job handles the grouping of alerts based on the specified method. Additionally, you can run multiple scheduled jobs in parallel to manage alert grouping more efficiently. For further details, see [Run multiple scheduled jobs for alert grouping](../task/run-multiple-alert-group-scheduled-jobs.md).

To define which alerts are grouped, the following parameters are used:

-   **sa\_analytics.aggregation\_enabled**: This parameter enables alert grouping created by the schedule job. Set the property **Enable alert aggregation for Automated, CMDB, and Text-Based groups** to `true` to activate this feature.

    **Note:** This property also applies to Tag Cluster and Network Traffic Correlation grouping.

-   **sa\_analytics.agg.query\_dynamic\_window**: By default, this is set to 10 minutes \(600 seconds\). It defines the maximum time difference allowed between the last event generation times of two alerts that can be grouped together.
-   **sa\_analytics.agg.query\_max\_group\_lifetime**: This parameter specifies the maximum time period from the generation of the first alert to the last alert in a group, with a default of 30 minutes \(1800 seconds\). If events arrive with a delay exceeding this period, the **sa\_analytics.agg.group\_expiration\_time** parameter can be used to extend the grouping time beyond 30 minutes.

**Note:** Some parameters, such as **sa\_analytics.agg.query\_dynamic\_window**, **sa\_analytics.agg.query\_max\_group\_lifetime**, and **sa\_analytics.agg.group\_expiration\_time**, are not provided out of the box. To use these properties, you need to create properties with the same names and assign the required values to them. For more information on how to create a property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

## Example: How alerts are grouped

For tag-cluster grouping, alerts are added to a group based on the timeframe parameter defined in the alert tag clustering settings. For automated, CMDB, and text-based, network traffic grouping, alerts are aggregated as follows.

Consider the following alerts with the same CI. \(All of them may be added to the same CMDB group\).

-   Alert1: Initial event generation at 01:00:00 AM
-   Alert2: Initial event generation at 01:11:00 AM
-   Alert3: Initial event generation at 01:13:00 AM
-   Alert4: Initial event generation at 01:16:00 AM
-   Alert5: Initial event generation at 01:25:00 AM
-   Alert6: Initial event generation at 01:34:00 AM
-   Alert7: Initial event generation at 01:43:00 AM

Alert1 and Alert2 are not grouped due to the time gap exceeding 10 minutes. Alert2 and Alert3 create a group at 01:13:00 AM. The 10-minute dynamic window starts at 01:13:00 AM, with the following:

-   Alert4 is added to the group at 01:16:00 AM, restarting the 10-minute window.
-   Alert5 and Alert6 are added to the group as their event times are within the 10-minute window.
-   Alert7 is not added to the group because it arrives 9 minutes after Alert6, exceeding the **sa\_analytics.agg.query\_max\_group\_lifetime** limit of 30-minute maximum group lifetime from the initial group creation \(01:13:00 AM + 30 minutes = 01:43:00 AM\).

**Note:** After an alert is created, correlation logic is applied only once. Changes to the alert after its creation are not re-evaluated for correlation. If correlation is not established initially, the alert may still be added to a group later—but only if a new incoming alert matches and triggers grouping logic.

