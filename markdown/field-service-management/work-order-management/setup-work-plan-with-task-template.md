---
title: Set up work plans linked to task plan templates
description: Configure work plans and associate it with task plan templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/work-order-management/setup-work-plan-with-task-template.html
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-06-26"
reading_time_minutes: 1
breadcrumb: [Planned Work Management, Set up work orders and tasks, Configure, Field Service Management]
---

# Set up work plans linked to task plan templates

Configure work plans and associate it with task plan templates.

## Before you begin

Role required: sn\_fsm\_planned\_wm.planned\_work\_admin

## About this task

When the conditions specified in the Planned Work Schedule Task Template are met, tasks, cases, or incidents are created based on the defined task plan templates.

For example, to meet the monthly audit requirement of inspecting multiple stores of the same organization simultaneously, you should create individual planned work schedules for each audit. Link each schedule to a different task plan template. Include relevant conditions in each planned work schedule template to ensure the correct template is applied when generating tasks specific to each audit.

## Procedure

1.  Configure linking of output records with schedule occurrences.

    You can link output records with schedule occurrences by one of the following ways.

    -   Create m2m table. For more information, see [Create a many-to-many table relationship](https://www.servicenow.com/docs/r/platform-administration/table-administration-and-data-management/t_CreateAManyToManyRelationship.html)
    -   Add reference fields on the output record tables pointing to the Schedule Occurrence \(wm\_plan\_work\_schedule\_occurrence\) table.
2.  Implement the `sn_fsm_planned_wm.TaskPlanTemplateOutputTasks` extension point to define the create, read, update, and delete operations on the output records.

    For more information, see [Extension points in Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/extension-points-field-service.md).

3.  Manage state flows of output records and schedule occurrences.

    The state of schedule occurrences aren't updated automatically. You're required to update and handle the state of schedule occurrences based on the change in the state of output records.

4.  [Create a work plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/create-work-plan.md).

5.  [Configure a work schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/configure-work-plan.md).

6.  [Associate task plan template to a work schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/work-order-management/map-schedule-to-task-template.md).


