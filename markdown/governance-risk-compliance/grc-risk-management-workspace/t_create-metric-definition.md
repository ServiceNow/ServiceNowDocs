---
title: Create an automated metric definition
description: Create an automated metric definition to collect the data for a metric. A metric definition specifies the method and key properties of the metric, such as the unit, direction, or nature of the metric.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Create an automated metric definition

Create an automated metric definition to collect the data for a metric. A metric definition specifies the method and key properties of the metric, such as the unit, direction, or nature of the metric.

## Before you begin

Role required: sn\_grc\_metric.manager, sn\_risk.user, and sn\_compliance.user

## About this task

In automated metric definitions, the data is collected automatically based on the conditions that you define in the metric definition. In the condition, specify the tables that are used for collecting the metric data. For example, to obtain data for all the incidents logged in a particular month, you can specify the Incidents table as a source for data collection.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace**.

2.  Select the list ![](../../grc-workspace-risk/image/list-icon-risk-workspace.png) icon.

3.  Navigate to **Metrics** &gt; **Automated metric definitions**.

4.  Select **New**.

5.  On the form, fill in the fields.

    For a description of the field values on the Automated metric definition form, see [Automated metric definition form](../reference/automated-metric-definition-fields-irm.md).

6.  Select **Save**.

    **Note:** In the new automated metric definition form, only the **Details** tab is displayed. After a new automated metric definition is created, additional related lists are displayed with the **Details** tab in the form.


## Result

The automated metric definition is saved in the Metric definitions list.

## What to do next

You can associate an entity type, create metrics, and add citations to the metric definition. See [Update a metric definition](t_update-automated-metric-definition.md) for more information.

-   **[Automated metric definition form](../reference/automated-metric-definition-fields-irm.md)**  
The fields of the automated metric definition form are explained in this topic.

**Parent Topic:**[Configuring metrics](../concept/configuring-irm-metrics.md)

