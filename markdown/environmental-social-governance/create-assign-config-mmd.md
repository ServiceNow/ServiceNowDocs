---
title: Create an assignment configuration
description: Create an assignment configuration for a manual metric definition to have data owners dynamically assigned to metrics.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create an assignment configuration

Create an assignment configuration for a manual metric definition to have data owners dynamically assigned to metrics.

## Before you begin

Role required: admin, sn\_esg.admin, or sn\_risk.admin

## About this task

In the manual metric definition, you can choose between a simple or advanced option for the assignment of data owners. For the advanced option, you must configure how the data owner is assigned by creating a new assignment configuration record. For more information, on the manual metric definition form and fields, see [Manual metric definition fields](../reuse/manual-md-reuse.md).

## Procedure

1.  Navigate to **All** &gt; **Assignment and Approval Configurations** &gt; **Assignment configurations**.

2.  Click **New**.

3.  On the form, fill in the fields.

    For information about the fields, refer to Assignment Configuration New Record.

    **Note:** You cannot have more than one approval configuration applying to the table with the same priority.

4.  Select **Save**.


## Result

Data owners will be assigned to metrics based on the parameters set in your assignment configuration.

**Note:** If the assignment configuration does not return any results the user defined in the **Data owner** field of the metric definition record will be the assigned as the data owner.

**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

