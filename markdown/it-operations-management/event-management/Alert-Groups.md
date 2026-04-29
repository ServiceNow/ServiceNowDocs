---
title: Alert grouping types and creation methods
description: Explore different alert grouping types, understand their descriptions, and learn about their creation methods to enhance problem identification and streamline alert management.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert grouping types and creation methods

Explore different alert grouping types, understand their descriptions, and learn about their creation methods to enhance problem identification and streamline alert management.

## Viewing and managing alert groups

Navigate to **Event Management** &gt; **All Alerts** to view all alert groups. The icon in the **Group** column denotes the alert group type, while alerts not associated with any group have no entry in the **Group** column. Double-click the **Group** column to open the Grouped Alerts dialog, where you can view all alerts in the group and manually add or remove alerts.

**Note:** An alert can belong to only one alert group at a time.

## Types of alert grouping

<table id="table_xwj_spx_3dc"><thead><tr><th>

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

-   [Rule-based alert grouping](c_EMEventCorrelationRules.md)
-   [Create an alert correlation rule](../task/t_EMConfigureAnEventCorrelationRule.md)

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

CMDB

</td><td>

C

</td><td>

CMDB groups are formed based on CI relationships in the CMDB, specifically for CIs that are not included in rule-based or automated groups.

</td><td>

Created via scheduled job.

</td><td>

[CMDB based alert grouping](cmdb-alert-groups.md)

</td></tr><tr><td>

Network traffic based

</td><td>

N

</td><td>

Network traffic alert groups are formed by analyzing network traffic connections between processes across hosts. This method leverages service candidates identified through ML Service Mapping to group alerts related to network traffic issues.

</td><td>

Created via scheduled job.

</td><td>

[Network traffic based alert grouping](network-traffic-correlation-grouping.md)

</td></tr><tr><td>

Text

</td><td>

T

</td><td>

Text groups are formed by grouping alerts based on similar text from frequently used words in following fields.-   Description
-   Metric Name
-   CI Class

</td><td>

Created via scheduled job.

</td><td>

[Text-based alert grouping](text-based-alert-groups.md)

</td></tr><tr><td>

Tag Cluster

</td><td>

Tag

</td><td>

Tag Cluster groups are formed by grouping alerts according to user-defined tag-based alert clustering definitions.

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

[Manual alert grouping](../task/t_SAAddAlertCorrelatedAlertGrp.md)

</td></tr></tbody>
</table>For information on scheduled jobs and parameters, refer to [Scheduled jobs and parameters for alert grouping](alert-grp-jobs-parameters.md). For detailed information on configuring alert correlation logic order, see [Configure alert correlation logic order](../task/configure-alert-correlation-logic-order.md).

