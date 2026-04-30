---
title: Create an automated metric definition
description: Create an automated metric definition to collect the data for a metric. A metric definition specifies the method and key properties of the metric, such as the unit, direction, or nature of the metric.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create an automated metric definition

Create an automated metric definition to collect the data for a metric. A metric definition specifies the method and key properties of the metric, such as the unit, direction, or nature of the metric.

## Before you begin

Role required: sn\_grc\_metric.manager, sn\_risk.user, and sn\_compliance.user

## About this task

In automated metric definitions, the data is collected automatically based on the conditions that you define in the metric definition. In the conditions, you could specify the tables that are used for collecting the metric data. For example, if you want to obtain data for all the incidents logged in a particular month, you can specify the Incident table as a source for data collection.

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Metrics** &gt; **Automated metric definitions**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For information on the fields of the form, see [Automated metric definition fields](../reuse/automated-metric-definition-fields.md).

4.  Select **Save**.

    **Note:** In the new automated metric definition form, only the **Details** tab is displayed. After a new automated metric definition is created, additional related lists are displayed with the **Details** tab in the form.


## Result

The automated metric definition is saved in the Metric definitions list.

## What to do next

You can associate an entity type, create metrics, and add citations to the metric definition. See [Update a metric definition](update-automated-metric-definition.md) for more information.

-   **[Automated metric definition fields](../reuse/automated-metric-definition-fields.md)**  
The fields of the automated metric definition form are explained in this topic.

**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

