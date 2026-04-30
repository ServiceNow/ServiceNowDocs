---
title: Work order states
description: Work order follow a specific life cycle and move through a series of states, which are displayed in the State field on the work order record.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Work orders, Work orders and tasks, Configure, Field Service Management]
---

# Work order states

Work order follow a specific life cycle and move through a series of states, which are displayed in the State field on the work order record.

The request states displayed depend on the Field Service Management application, as indicated in the table.

Depending on your configuration, you can either qualify work orders after they are drafted, or they are immediately ready for dispatch. For more information on setting up qualification, see the Qualification is required for new requests section in [Global domain configurations](../../planning-and-policy/task/t_ConfigureFieldService.md).

Create or modify UI actions to add to work order \[wm\_order\] and work order task \[wm\_task\] forms. Use these actions to move work orders and work order tasks from one state to the next or to perform specific actions, such as launching questionnaires. For more information, see [UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

<table id="table_mmv_gqk_h1c"><thead><tr><th>

State

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Draft

</td><td>

Qualifier is not done describing the work.

</td></tr><tr><td>

Awaiting Qualification

</td><td>

The work order has been drafted but has not been qualified.**Note:** This state only shows if qualification is enabled.

</td></tr><tr><td>

Qualified

</td><td>

The request has been approved and is ready to be assigned.**Note:** This state only shows if qualification is enabled.

</td></tr><tr><td>

Ready for Dispatch

</td><td>

The request is ready to be assigned.**Note:** This state only shows if qualification is disabled.

</td></tr><tr><td>

Assigned

</td><td>

The request is pending acceptance from the assigned Field Service agent.

</td></tr><tr><td>

Accepted

</td><td>

The Field Service agent accepts the request and is ready to be worked on.

</td></tr><tr><td>

Work in Progress

</td><td>

Work on the request has started.

</td></tr><tr><td>

Closed Complete

</td><td>

The request was completed to specification.

</td></tr><tr><td>

Closed Incomplete

</td><td>

The request could not be completed as specified.

</td></tr><tr><td>

Canceled

</td><td>

The request was canceled.

</td></tr></tbody>
</table>**Note:** If you have qualification enabled and then disable it, then all existing work orders awaiting qualification, in draft, or already qualified are set to ready for dispatch.

