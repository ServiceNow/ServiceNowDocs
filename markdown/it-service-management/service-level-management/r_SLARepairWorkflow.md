---
title: SLA Repair workflow
description: You can configure workflow usage for SLA repair operations.
locale: en-US
release: xanadu
product: Service Level Management
classification: service-level-management
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Level Management reference, Service Level Management, IT Service Management]
---

# SLA Repair workflow

You can configure workflow usage for SLA repair operations.

## Workflow usage

The SLA repair workflow is used if SLA repair functionality is enabled.

When the SLA repair function is in progress and new task SLA records are created, the workflow will follow a repair path through the workflow. The repair path is based on the result of the **SLA Percentage Timer** activities. While repair is in progress, the result of this activity will be **repair**, which enables the workflow to follow a different path in order to skip certain actions, such as generating events for notifications. This avoids duplicate notifications from being sent out during the repair process for each SLA that is repaired.

To specify that the SLA repair function should use the SLA's original workflow for repair operations, go to **Service Level Management** &gt; **Properties** &gt; **SLA Repair** and remove the selection from the **com.snc.sla.repair.use\_repair\_workflow** repair property.

**Note:** If you choose to use a non-default repair workflow, or a workflow you have changed, you should modify this workflow to ensure it includes appropriate repair conditions on the **SLA Percentage Timer** activities. When a task SLA is repaired, the repair transitions are followed for any activities that occurred in the past. For example, the Default SLA Repair workflow configures the repair conditions to follow repair transitions.

## Workflows for new or upgraded instances

For new instances, the SLA Repair function uses the Default SLA workflow, which incorporates repair activities. For upgrades, the SLA Repair function uses the Default SLA Repair workflow because the Default SLA workflow will not be updated in case it has been customized.

To change the default workflow the SLA repair function uses, go to **Service Level Management** &gt; **Properties** &gt; **SLA Repair** and set the **com.snc.sla.repair.workflow** repair property.

**Parent Topic:**[Service Level Management reference](../concept/service-level-management-reference.md)

