---
title: Create an assignment configuration
description: Create an assignment configuration for a manual metric definition to have data owners dynamically assigned to metrics.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Create an assignment configuration

Create an assignment configuration for a manual metric definition to have data owners dynamically assigned to metrics.

## Before you begin

Role required: admin or sn\_risk.admin

## About this task

In the manual metric definition, you can choose between a simple or advanced option for the assignment of data owners. For the advanced option, you must configure how the data owner is assigned by creating an assignment configuration record. For more information, on the manual metric definition form and fields, see [Create New Metric Definition form](../reference/manual-md-reuse-irm.md).

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Assignment configurations**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For information about the fields, refer to [Assignment Configuration New Record](../../grc-common/reference/assignment-configuration-new-record.md).

    **Note:** You cannot have more than one approval configuration applying to the table with the same priority.

4.  Select **Save**.


## Result

Data owners are assigned to metrics based on the parameters set in your assignment configuration.

**Note:** If the assignment configuration doesn’t return any results, the user defined in the **Data owner** field of the metric definition record will be the assigned as the data owner.

**Parent Topic:**[Configuring metrics](../concept/configuring-irm-metrics.md)

