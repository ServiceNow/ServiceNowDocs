---
title: Alert Query form
description: You can combine similar alerts that meet specific criteria for a particular service by creating an alert query.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Event Management reference, Event Management, ITOM Health, IT Operations Management]
---

# Alert Query form

You can combine similar alerts that meet specific criteria for a particular service by creating an alert query.

<table id="table_wmh_wg2_l1c"><thead><tr><th align="left">

Field

</th><th align="left">

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The alert query name.

</td></tr><tr><td>

Business criticality

</td><td>

The importance of this alert query to the business. This field can determine disaster recovery strategies for this alert query. -   1: most critical
-   2: somewhat critical
-   3: less critical
-   4: not critical

</td></tr><tr><td>

Used for

</td><td>

The purpose of the alert query. Select from:-   Production \(Default\)
-   Staging
-   QA
-   Test
-   Development
-   Demonstration
-   Training
-   Disaster recovery

</td></tr><tr><td>

Owned by

</td><td>

The party that is responsible for the alert query.

</td></tr><tr><td>

Email

</td><td>

The email alias for the alert query.

</td></tr><tr><td>

Business phone

</td><td>

The phone number for the business.

</td></tr><tr><td>

Operational status

</td><td>

The status of the alert query. -   **Operational**: The alert query is running. Impact calculation runs only on alert queries in the Operational status.

Select this option to use this service. If you customized preconfigured options for this category, select the option whose value is set to 1. Event Management calculates impact only on services in use.

If you do not want to use this service now, select one of these options:

-   **Non-Operational**: The alert query is unavailable, disabled, or down.
-   **Repair in progress**: The alert query is receiving maintenance.
-   **DR Standby**: The alert query is available as a disaster recovery \(DR\) standby.
-   **Ready**: The alert query is prepared for use.
-   **Retired**: The alert query is withdrawn from active use.

</td></tr><tr><td>

Comments

</td><td>

Any additional notes and information.

</td></tr><tr><td>

Service Group Members

</td><td>

The service group which contains this service.

</td></tr><tr><td>

Filter

</td><td>

The conditions for sending a notification to the alert query. The conditions must meet the alert values.**Note:**

-   When defining an alert query filter, include only fields that appear in the Alert Histories \[em\_alert\_history\] table. Impact calculation is based on Alert History data and fields such as Overall Event Count, Priority, and Priority group are not copied to the Alert Histories \[em\_alert\_history\] table.
-   Do not specify a dynamic time condition. For example, in the filter, do not specify `Created` condition of `Last 45 minutes` because impact calculation is triggered by a change of alert or alert query. However, for the dynamic time condition, none of these conditions have changed. ![Do not specify a dynamic time condition](../image/dynamic-time-condition.png)
-   Some filters may slow down impact calculation. To solve this problem, adjust your alert query by adding an appropriate index, as described in [Index suggestions for slow queries](https://www.servicenow.com/docs/access?context=index-suggestions&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

</td></tr></tbody>
</table>**Parent Topic:**[Event Management reference](event-management-reference.md)

