---
title: Metric definition types
description: A metrics manager defines the metrics by creating a metric definition. A metric definition is a template-level record. In the metric definition, you set the core properties of the metric, such as unit, direction, nature, precision, and category. The metrics collect the scores, and these scores get rolled up into the metric definition.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Metric definition types

A metrics manager defines the metrics by creating a metric definition. A metric definition is a template-level record. In the metric definition, you set the core properties of the metric, such as unit, direction, nature, precision, and category. The metrics collect the scores, and these scores get rolled up into the metric definition.

The GRC: Metrics application provides the following types of metric definitions:

-   Automated metric definition: Data is collected automatically.
-   Manual metric definition: Data is collected manually.
-   Calculated metric definition: Data is collected by aggregating scores from other child metrics.

These types of metric definitions are further explained in the following sections.

## Automated metric definition

In automated metric definitions, the data is collected automatically based on the conditions defined in the metric definition, such as metric properties, method, and schedule. Metrics manager specifies the source table or the script that is used for collecting the metric data and the filtering criteria to filter the metric data. See [Create an automated metric definition](../task/t_create-metric-definition.md) for more information.

## Manual metric definition

In manual metric definitions, the mode of data collection is manual. The data owner for a particular metric provides the metric data by going through the instructions. As the metrics manager, you have to define the metric properties, method, and schedule for the metric definition. In the method, specify the instructions for the metric definition as the metrics manager. Also, specify the data collection details such as data owner type, data owner, and approval details.

In a manual metric definition, a metric data task is generated depending upon the frequency defined in the metric definition. As a metrics manager, you can assign the task to a data owner who provides the data for the task. See [Create a manual metric definition](../task/t_create-manual-metric-definition.md) for more information. When a metric data task is created, a system generated email notification is sent to the task owner. As a metric data owner, you can provide the data for multiple metrics using the Metrics tasks module \(![metric data table icon.](../../esg-management-reporting/images/metric-tasks.png)\). For more information, refer to [Provide responses for multiple metrics](../task/provide-responses-multiple-metrics-irm.md).

Both quantitative and qualitative category of metrics can be created using the manual metric definition.

A manual metric definition can be converted to an automated metric definition, and vice versa. If a manual metric definition has open tasks, those tasks must be closed before the conversion.

## Calculated metric definition

A calculated metric definition calculates the scores from its children. It can include the automated and manual metric definitions, metrics \(quantitative\), and other calculated metric definitions of identical frequency. As the metrics manager, you have to specify how you want to calculate the metric definitions score and how frequently you want to calculate them.

The calculated metric definition rolls up the scores from its children. The rollup property defined in the calculated metric definition consists of a rollup formula and schedule for the rollup frequency. A calculated metric definition can include those automated and manual metric definitions, and metrics as its children, which are of the same frequency as that of the parent calculated metric definition. See [Create a calculated metric definition](../task/t_create-composite-metric-definition.md) for more information.

## Applying the metric definition to the entities

You can apply the metric definitions to the entities in your organization. Instead of defining the metric for each entity, you can define the metric definition once and then apply that metric definition to your entities.

For example, you want to track the number of high and critical risks in your organization. By creating a metric definition, you can define the metric once and then apply that metric definition to your entities. Defining the metric separately for each entity is time-consuming. Creating a single metric definition enables consistent tracking of risk exposure across entities without creating separate metrics for each unit.

