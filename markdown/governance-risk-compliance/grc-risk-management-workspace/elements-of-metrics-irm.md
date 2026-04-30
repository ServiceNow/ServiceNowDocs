---
title: Components of GRC: Metrics
description: A metric consists of several components such as metric definition, metric data, metric definition data, metric data tasks. All of these elements or parts contribute to the metric collection process in various ways.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Components of GRC: Metrics

A metric consists of several components such as metric definition, metric data, metric definition data, metric data tasks. All of these elements or parts contribute to the metric collection process in various ways.

## Metric definitions

A metric definition is a template-level record that helps set the core properties of a metric. These properties include the unit, direction, nature, precision, frequency of data collection, and category of the metric. The metric itself collects scores, which are then aggregated into the defined metric. The advantage of creating and using a metric definition lies in its ability to streamline the process of creating metrics using these metric definitions. For instance, imagine you have several business units, and you must collect revenue data for each of them. Without a metric definition, you would have to create separate templates for every business unit and repeatedly specify the metric properties. However, by using a metric definition, you simplify this task. Once you have created the metric definition, you can easily attach your entities \(business units in this case\) and collect the metrics without duplicating efforts.

The GRC: Metrics application provides the following types of metric definitions:

-   Automated metric definition: Data is collected automatically.
-   Manual metric definition: Data is collected manually.
-   Calculated metric definition: Data is collected by aggregating data from other child metric definitions.

## Metric data

When you execute a metric, the metric data gets created. For manual metric definitions, the values of metric data are copied from the metric data tasks when the metric data tasks are closed. To address off-cycle requests for the most up-to-date information on existing metric definitions and metrics, you can create ad hoc metric data tasks on manual metrics. On the metric data form, the option **Ad hoc** denotes if the metric data task was created as an ad hoc task. It’s important to note that these ad hoc tasks do not contribute to the aggregated metric definition data, aren’t considered for entity hierarchy rollup, and aren’t evaluated for threshold rating, Variance\(%\). However, in a calculated metric definition, if the **Calculation level** is set to **Entity**, and there are ad hoc tasks from the manual metric definitions, then these tasks are aggregated to derive the calculated metric definition data.

For a scripted automated metric definition, the values are updated when you execute the script. For a basic automated metric definition, the values are updated from the selected table. The field **Variance \(%\)** shows the variation in between current period and the previous period metric data and is displayed in percentage. The field **Last period data** refers to the previous period's metric data.

## Metric definition data

Metric definition data gets automatically created when the metric definition gets executed and aggregated.

## Metric data tasks

Metric data tasks only apply to manual metric definitions. These tasks are generated whenever manual metrics are executed and the data owners provide responses for these tasks manually. You can provide responses to multiple metric data tasks using the metric data table. For more information, see [Metric data table](metric-data-table-irm.md).

A metrics manager has the authority to determine whether a metric data task needs approval. If approval is necessary, you can choose between two methods: Simple Approval or Advanced Approval by using the **Metric approval** property. For more information about this property, see [Components installed with the GRC: Metrics application](../reference/roles-installed-with-grc-metrics-irm.md).

