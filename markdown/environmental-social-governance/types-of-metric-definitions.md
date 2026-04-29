---
title: Types of metric definitions
description: A metrics manager defines the metrics by creating a metric definition. A metric definition is a template-level record. In the metric definition, you set the core properties of the metric, such as unit, direction, nature, precision, and category. The metrics collect the scores, and these scores get rolled up into the metric definition.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Exploring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Types of metric definitions

A metrics manager defines the metrics by creating a metric definition. A metric definition is a template-level record. In the metric definition, you set the core properties of the metric, such as unit, direction, nature, precision, and category. The metrics collect the scores, and these scores get rolled up into the metric definition.

The GRC: Metrics application provides the following types of metric definitions:

-   Automated metric definition: Data is collected automatically.
-   Manual metric definition: Data is collected manually.
-   Calculated metric definition: Data is collected by aggregating scores from other child metrics.

These types of metric definitions are further explained in the following sections.

## Automated metric definition

In automated metric definitions, the data is collected automatically based on the conditions defined in the metric definition, such as metric properties, method, and schedule. For the method, the metrics manager specifies the source table or the script that is used for collecting the metric data and the filtering criteria to filter the metric data.

In an automated metric definition, you can enabled a metric data task, approval flow, and collection of supporting data in the metric definition. If enabled, the metric data task is generated depending upon the frequency defined in the metric definition. As a metrics manager, you can assign the task to a data owner. See [Create an automated metric definition](../task/create-metric-definition.md) for more information. When a metric data task is created, the task owner receives a system-generated email notification. As the metric data owner, you can verify and override automatically collected data if needed. If approval is enabled, verified data is submitted for approval to the designated approver from the metric definition.

**Note:** For automated metric definitions where the method type is "External" or "Scripted", the "Supporting Data" option isn’t available.

## Manual metric definition

In manual metric definitions, the mode of data collection is manual. The data owner for a particular metric provides the metric data by going through the instructions. As the metrics manager, you have to define the metric properties, method, and schedule for the metric definition. In the method, specify the instructions for the metric definition as the metrics manager. Also, specify the data collection details such as data owner type, data owner, and approval details.

In a manual metric definition, a metric data task is generated depending upon the frequency defined in the metric definition. As a metrics manager, you can assign the task to a data owner who provides the data for the task. See [Create a manual metric definition](../task/create-manual-metric-definition.md) for more information. When a metric data task is created, a system-generated email notification is sent to the task owner. As a metric data owner, you can provide the data for multiple metrics using the Metrics tasks module \(![](../../esg-management-reporting/images/metric-tasks.png)\). For more information, refer to [Provide data for multiple metrics](../../esg-management-reporting/task/provide-data-for-multiple-metrics.md).

Each metric data task has a due date defined in the manual metric definition form. By default, the due date follows the schedule of 8-5. However, an ESG administrator can also modify the schedule. For more information, refer to [Create a new schedule](../../esg-management-reporting/task/create-a-new-schedule.md). If the ESG administrator wants to overwrite the schedule, then the ESG administrator can modify the **sn\_grc\_metric.metric\_data\_task\_schedule** property.

Both quantitative and qualitative category of metrics can be created using the manual metric definition.

It’s possible to convert a manual metric definition to an automated metric definition and an automated metric definition to a manual metric definition. In the event that a manual metric definition has open tasks, it’s necessary to first close them prior to converting the manual metric definition.

When a manual metric definition is executed, the first metric data is created and then metric data task is created. This task is then referred to the metric data.

## Calculated metric definition

A calculated metric definition calculates the scores from its children. It can include the automated and manual metric definitions, metrics \(quantitative\), and other calculated metric definitions of identical frequency. As the metrics manager, you have to specify how you want to calculate the metric definitions score and how frequently you want to calculate them. Deactivating or activating a calculated metric definition automatically deactivates or activates all its associated metrics.

The calculated metric definition rolls up the scores from its children. The rollup property defined in the calculated metric definition consists of a rollup formula and schedule for the rollup frequency. A calculated metric definition can include those automated and manual metric definitions, and metrics as its children, which are of the same frequency as that of the parent calculated metric definition. See [Create a calculated metric definition](../task/create-composite-metric-definition.md) for more information.

## Applying the metric definition to the entities

You can apply the metric definitions to the entities in your organization. Instead of defining the metric for each entity, you can define the metric definition once and then apply that metric definition to your entities.

For example, assume that you want to measure the greenhouse gas emissions for the entities in your organization. Defining the metric for each entity is a time-consuming process. By creating a metric definition, you can define the metric once and then apply that metric definition to your entities.

The following illustration shows how you can apply the metric data definition to an entity. If you have an automated metric definition for the purchased goods metric category, the metric can be applied to the Products entity and IT entity in your organization. If you have a manual metric definition such as Employee Travel, the metric can be applied to the Enterprise entity in your organization as the travel policy applies to everyone across the enterprise.

![Metric definition and the entities.](../image/apply-metric-definitions-to-entities.png "Apply the metric data definition to an entity")

