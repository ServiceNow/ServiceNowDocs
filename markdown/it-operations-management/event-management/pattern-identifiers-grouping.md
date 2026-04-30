---
title: Understanding pattern identifiers
description: A pattern identifier is a set of criteria or attributes \(such as alert type, affected system, etc.\) used to group similar alerts. It helps to identify recurring issues, making it easier for teams to respond and address ongoing problems.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Automated alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Understanding pattern identifiers

A pattern identifier is a set of criteria or attributes \(such as alert type, affected system, etc.\) used to group similar alerts. It helps to identify recurring issues, making it easier for teams to respond and address ongoing problems.

## How pattern identifiers group alerts

Consider a network monitoring system that generates alerts for various issues, such as high CPU usage, memory leaks, or connection timeouts.

Pattern Identifier: Metric Name and CI

-   Alert 1: High CPU usage on Server A at 10:00 AM
-   Alert 2: High CPU usage on Server A at 10:05 AM
-   Alert 3: Memory leak on Server B at 10:10 AM
-   Alert 4: High CPU usage on Server A at 10:15 AM

In this case, the pattern identifier could be set to the Metric Name \(e.g., high CPU usage\) combined with the Configuration Item \(CI\) \(e.g., Server A\). Alerts 1, 2, and 4 would be grouped together because they share the same metric \(high CPU usage\) and the same CI \(Server A\), indicating a recurring issue that may need further investigation. Alert 3, however, would not be included in this group because it has a different metric \(memory leak\) and CI \(Server B\).

**Note:** The set of alert fields used for the pattern identifier is also referred to as Feature Identifier Attributes or simply attributes.

## How to configure effective pattern identifiers

To configure effective pattern identifiers for alert grouping, follow these three key steps to ensure accurate and meaningful analysis of alerts.

<table id="table_x1p_wt5_mdc"><thead><tr><th>

Step

</th><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create an event rule

</td><td>

Define an event rule.To know how to create an event rule, see [Create or edit an event rule](../task/create-or-edit-event-rule.md).

</td><td>

Set up an event rule to populate the relevant alert fields for the pattern identifier.

</td></tr><tr><td>

Manage pattern identifier

</td><td>

Add relevant alert field to the pattern identifier.To know how to add fields to the pattern identifier, see [Specify and manage pattern identifier attributes for alert grouping](../task/ptrn-attributes-alrt-aggregate.md).

</td><td>

After adding the relevant alert fields, select **Deploy** to activate the pattern identifier.

</td></tr><tr><td>

Choose relevant identifiers

</td><td>

Select alert fields that clearly identify the problem. For example, if the issue is that a service is offline or there’s no connection to the database, look for specific values in the alert that indicate this. Add these types of fields to the pattern identifier. By default, we provide the **Metric Name** field as a pattern identifier.

</td><td>

-   Avoid overly unique fields \(e.g., date\) that make pattern identification difficult.
-   Avoid overly common fields that result in too many alerts being grouped together, making patterns indistinguishable.

</td></tr></tbody>
</table>## Alert grouping and Learned Patterns

Learn how alert patterns are discovered, grouped, and displayed in the system.

|Concept|Description|
|-------|-----------|
|Pattern discovery|When a set of alert fields matches, the alerts are grouped into a "Learned Pattern." For example, alerts with the same Priority Group and Resource are grouped into a pattern.|
|Pattern reporting|These patterns are displayed on the Learned Patterns report found under **Event Management** &gt; **Administration** &gt; **Learned Patterns**.|

## Managing Pattern Attributes and Time Frame

Learn the process of managing pattern identifier attributes, deployment of new sets, and how the system identifies issues.

<table id="table_kks_w55_mdc"><thead><tr><th>

Concept

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active pattern identifier attributes

</td><td>

Only one set of attributes can be active at a time. **Note:** The new set replaces the current one after deployment.

</td></tr><tr><td>

Purpose and time frame

</td><td>

Pattern grouping identifies issues within the last 30 days, controlled by the **sa\_analytics.agg.learner\_period\_days** property.

</td></tr><tr><td>

Issue identification

</td><td>

To identify an issue, the system utilizes a combination of Configuration Items \(CIs\) and Pattern Identifiers \(sometimes referred to as Feature Identifiers\).

By default, a Pattern Identifier is defined as the Metric Name, but this can be modified. Two alerts are considered similar if they share the same CI and Pattern Identifier, although fields such as Source, Severity, Description, and others may differ.

For more information, see [Specify and manage pattern identifier attributes for alert grouping](../task/ptrn-attributes-alrt-aggregate.md).**Note:** The Alert Aggregation Learner also identifies patterns of alerts within manual alert groups.

In some cases, you can create patterns from alerts where the CIs share the same value in a specified field. For example, to build patterns from alerts with the same CI **Location** field, enter `location` in the **sa\_analytics.agg.learner\_group\_by\_property** property. For more information, [Configure scheduled job-based alert grouping](../task/enable-alert-grouping.md).

When working with CI-based groups, ensure that the pattern identifier includes both the node and the metric name. For details on configuring the Feature Identifier, see [Learned patterns report](c_SALearnedPattersReport.md).

**Note:** Alerts that lack a CI can still be grouped together as Text-based or CI-based alert groups, treating a node as a CI. To enable this functionality, set the sa\_analytics.enable\_no\_ci\_grouping property to true.

</td></tr></tbody>
</table>