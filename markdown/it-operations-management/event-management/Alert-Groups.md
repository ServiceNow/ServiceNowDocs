---
title: Alert grouping types
description: Alerts are grouped into various types to streamline problem identification and management. An alert can belong to only one alert group at a time.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Alert grouping types

Alerts are grouped into various types to streamline problem identification and management. An alert can belong to only one alert group at a time.

Watch this brief video to learn about alert grouping and how it organizes alerts into clusters based on specific criteria.

Grouping alerts in ServiceNow ITOM Event Management and Operational Intelligence applications.

You can view all alert groups by navigating to **Event Management** &gt; **All Alerts**, where the icon in the **Group** column denotes the alert group type. Alerts not associated with any group will not have an entry in the **Group** column. Double-click the **Group** column for an alert group to open the Grouped Alerts dialog box, where you can display all alerts in the group and manually add or remove alerts.

**Note:** The filter that defines alert groups must not be on fields that do not appear in the \[em\_alert\_history\] table because impact calculation is not a calculated property. This situation occurs because fields like **Event Count**, **Priority**, and **Priority Group** are not copied to the \[em\_alert\_history\] table for impact calculation.

<table id="table_ajd_qwj_ww"><thead><tr><th>

Type

</th><th>

Icon

</th><th>

Description

</th><th>

Creation method

</th><th>

Additional information

</th></tr></thead><tbody><tr><td>

Log Analytics

</td><td>

L

</td><td>

Log Analytics groups are formed when the system identifies multiple related Log Analytics alerts, grouping them based on their significant connections.

</td><td>

Created as part of log analytics event processing.

</td><td>

[Kinds of Health Log Analytics alerts](../../health-log-analytics-operator/reference/hla-op-log-analytics-alert-types.md)

</td></tr><tr><td>

Rule-based

</td><td>

R

</td><td>

Rule-based groups consist of related alerts that are organized based on compliance with alert correlation rules, which determine how alerts are grouped according to their relationships.

</td><td>

Created via business rule \(Calculate correlation rule\) on em\_alert table when alert is created or updated.

</td><td>

[Create an alert correlation rule](../task/t_EMConfigureAnEventCorrelationRule.md)

</td></tr><tr><td>

Automated

</td><td>

A

</td><td>

Automated groups are formed by alert aggregation and include a virtual alert as the primary alert of the group. An Aggregated automated group is created when two or more alerts share the same CI type and metric name.

</td><td>

Created via scheduled job.

</td><td>

[Automated alert grouping](c_SACorrelatedAlertGroups.md)

</td></tr><tr><td>

CMDB-based

</td><td>

C

</td><td>

CMDB-based groups are formed based on CI relationships in the CMDB, specifically for CIs that are not included in rule-based or automated groups.

</td><td>

Created via scheduled job.

</td><td>

[CMDB based alert grouping](cmdb-alert-groups.md)

</td></tr><tr><td>

Text-based

</td><td>

T

</td><td>

Text-based groups are formed by grouping alerts based on similar text from frequently used words in following fields.-   Description
-   Metric Name
-   CI Class

</td><td>

Created via scheduled job.

</td><td>

N/A

</td></tr><tr><td>

Tag cluster

</td><td>

Tag

</td><td>

Tag cluster groups are formed by grouping alerts according to user-defined tag-based alert clustering definitions.

</td><td>

Created via scheduled job.

</td><td>

[Tag cluster alert grouping](alert-clustering-tag-definitions-concept.md)

</td></tr><tr><td>

Manual

</td><td>

M

</td><td>

Alerts grouped manually by users to organize related issues.

</td><td>

Created manually by the user.

</td><td>

[Create alert group manually](../task/t_SAAddAlertCorrelatedAlertGrp.md)

</td></tr></tbody>
</table>For information on scheduled jobs and parameters, refer to [Scheduled jobs and parameters for alert grouping](alert-grp-jobs-parameters.md). For detailed information on configuring alert correlation logic order, see [Configure alert correlation logic order](../task/configure-alert-correlation-logic-order.md).

