---
title: Install base work plans
description: You can create an install base work plan on the Customer Service Management application to get the details that are related to an install base item. Work plans help you to create, maintain, and view the basic details of an install base item. You can also plan for the regular and timely maintenance of the install base item.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Schedules and sites, Use, Customer Service Management]
---

# Install base work plans

You can create an install base work plan on the Customer Service Management application to get the details that are related to an install base item. Work plans help you to create, maintain, and view the basic details of an install base item. You can also plan for the regular and timely maintenance of the install base item.

## Overview

A work plan provides the information that you need about the regular maintenance that you must do for an install base item. You can create a work plan for a product model. All the install base items that are associated to that product model inherit the same work plan.

You assign your customer and consumer service agents with the sn\_fsm\_planned\_wm.planned\_work\_read role so that they can have read access to all the planned work management tables.

You can also create a work plan in the CSM Configurable Workspace. To create a work plan in the workspace, see [Create a work plan in Customer Service Management \(CSM\) Configurable Workspace](../task/create-work-plans-in-workspace.md).

## Related lists for work plans

You can perform or view the maintenance operations, like device inspection and performance, for an install base item through the related lists section of the Install Base form. The following table lists the descriptions about the related lists for the work plans.

<table id="table_wtj_ykg_cyb"><thead><tr><th>

Related list

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work plans

</td><td>

Manage the maintenance requirements of an install base item. They include information on how often maintenance must be performed, what the maintenance activities are for the install base, and the order in which they must be performed. To create a work plan, see [Create a work plan with Customer Service Management \(CSM\)](../task/create-work-plans.md).

</td></tr><tr><td>

Planned Work Schedules

</td><td>

Gauge the timing and regularity of implementation of a schedule for a work plan. Planned work schedules have triggers like the duration, meter, condition, and script to determine and ensure that the work plan milestones are met. To create a planned work schedule, see [Configure a work schedule](https://www.servicenow.com/docs/access?context=configure-work-plan&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

</td></tr><tr><td>

Planned Work Schedule Templates

</td><td>

Describe the planned maintenance activities that must be performed for an install base item and the order in which they must occur. To create a planned work schedule template, see [Associate a work order template to a work schedule](https://www.servicenow.com/docs/access?context=associate-work-schedule-to-wotemplate&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

</td></tr><tr><td>

Work Orders

</td><td>

Create work orders for field service agents to perform scheduled maintenance activities for the install base item. To create a work order, see [Create a work order](../task/create-work-orders.md).Select the related list from the install base form to create a work order for an install base item.

Select the Work order related list from the planned work schedule form to create a work order for a work plan.

</td></tr><tr><td>

Work Order Tasks

</td><td>

Work orders and work order tasks are related and created only if there's an existing work order for the install base item. Fill in the **Parent** field on the work order task form with the name of the work order. To create a work order task, see [Create a work order task](https://www.servicenow.com/docs/access?context=t_CreateAWorkOrderTask&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US).

</td></tr></tbody>
</table>