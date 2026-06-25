---
title: View an order timeline
description: View Gantt chart timelines that display the status of a domain order and order tasks, show dependencies between order tasks, and identify tasks that are in jeopardy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/view-order-timelines.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Order fulfillment, Order Management, Use, Sales Customer Relationship Management]
---

# View an order timeline

View Gantt chart timelines that display the status of a domain order and order tasks, show dependencies between order tasks, and identify tasks that are in jeopardy.

## Before you begin

Role required: order\_approver, order\_viewer, sn\_ind\_tmt\_orm.order-fulfillment\_agent, sn\_ind\_tmt\_orm.order\_fulfillment\_manager, sn\_ind\_tmt\_orm.service\_order\_agent, or sn\_ind\_tmt\_orm.service\_order\_manager

## Procedure

1.  Navigate to  **Workspaces** &gt; **CSM/FSM Configurable Workspace.** .

2.  Select the List icon \[Omitted image "list-outline-24.svg"\] Alt text:.

3.  Navigate to **Customer Orders** &gt; **All**.

4.  Select the order that you want to view.

5.  In the **Order breakdowns** section of the order, select **View order timeline**.

    The **Timeline** tab opens and displays the order tasks for the order line items and columns for the order task state and jeopardy status, if Jeopardy Management is enabled. Tasks in jeopardy are flagged with the jeopardy icon. For each task, a timeline shows the start and end dates of the task and any dependencies.

6.  To change the information or elements displayed in the timeline view, use these options.

<table id="choicetable_pwy_bnv_c1c"><thead><tr><th align="left" id="d35169e116">

Option

</th><th align="left" id="d35169e119">

Description

</th></tr></thead><tbody><tr><td id="d35169e125">

**Add or change columns**

</td><td>

1.  Select the gear icon \[Omitted image "gear-outline-24.svg"\] Alt text:.
2.  In the **Columns** tab of the Personalize pane, select the items to display or deselect the items that are no longer displayed.
3.  Select **Apply**.


</td></tr><tr><td id="d35169e157">

**Change the timeline elements displayed**

</td><td>

1.  Select the gear icon \[Omitted image "gear-outline-24.svg"\] Alt text:.
2.  In the **Timeline** tab of the Personalize pane, select the items to display or suppress, such as bar labels, child lines, domain orders, critical path, or dependency lines.
3.  Select **Apply**.


</td></tr><tr><td id="d35169e189">

**Adjust the time scale used**

</td><td>

In the time scale drop-down, select the time view, such as day, week month, or year.The time scale for the Gantt charts changes immediately.

</td></tr></tbody>
</table>
**Parent Topic:**[Order fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/reviewing-orchestration-plans-order-fulfillment.md)

**Related topics**  


[Configuring Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-configuring.md)

[Order management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/explore-order-management.md)

