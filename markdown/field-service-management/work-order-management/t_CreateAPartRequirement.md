---
title: Create a part requirement
description: Create a part requirement for a work order task.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Part requirements, Inventory, Manage work order tasks, Prepare work orders, Use, Field Service Management]
---

# Create a part requirement

Create a part requirement for a work order task.

## Before you begin

Role required: wm\_admin, wm\_agent, wm\_dispatcher, wm\_qualifier, or [qualifier combination role](../reference/r_UserRoleInstallWFieldSrvMgmnt.md)

## About this task

You can create a part requirement to request a part with or without the context of work order task.

## Procedure

1.  Access a list of work orders.

    -   If you have the wm\_admin role, navigate to **Field Service** &gt; **Work Order** &gt; **All Work Orders**.
    -   If you have the wm\_agent role, navigate to **Field Service** &gt; **Agent** &gt; **Assigned to Me**.
    -   If you have the wm\_dispatcher role, navigate to **Field Service** &gt; **Dispatching** &gt; **Dispatch Queue** &gt; **.**
    -   If you have the wm\_qualifier role, navigate to **Field Service** &gt; **Work Order** &gt; **Awaiting Qualification** &gt; **.**.
2.  Open a work order.

3.  Open a work order task that is in the **Awaiting Qualification**, **Qualified**, **Assigned**, or **Work in Progress** state.

4.  Do one of the following.

<table><tbody><tr><td id="d43852e191">

**Click __Source__.**

</td><td>

All tasks and part requirements are listed on the left. Point to any task or part requirement icon to obtain more information. Right-click a work order task and select **Create Part Requirement**. This method is useful if you are sourcing multiple parts for a work order task.

</td></tr><tr><td id="d43852e206">

**In the __Part Requirements__ related list, click __New__.**

</td><td>

This method is useful if you are sourcing a single part for a work order task.

</td></tr></tbody>
</table>5.  Fill in the fields, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Number|Auto-generated number for the part requirement.|
    |Work order task|Number assigned to the work order task.|
    |Model|Description of the part [model](https://www.servicenow.com/docs/access?context=c_Models&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) needed to complete the work order task.|
    |Required by date|Date by which all parts should be delivered. The date is filled in automatically based on the task's expected travel start time. If necessary, change the date manually.|
    |Required quantity|Total quantity necessary to complete the part requirement. This field becomes read-only when the full number of required parts has been sourced.|
    |Reserved quantity|Total quantity that has been [sourced](t_SourceAPartAndAssignAnAgent.md) already.|
    |Sourced|Indicator for whether the required quantity for this part requirement has been reserved and transfer requested from one stockroom to another.|
    |Delivered|Indicator for whether the transfer order lines under this part requirement have been delivered or not.|
    |Short description|Contents of the **Short description** field from the parent work order. If the work order was created from an incident, problem, or change request, the short description of the part requirement is inherited from that record. If the work order was created automatically from a , the short description is from model template. This field is not visible by default.|

6.  Click **Submit**.

    If the part is out of stock, a message appears at the top of the form naming the part.

7.  If someone other than the qualifier will source the part requirement, [create transfer order lines](create-transfer-order.md), move the part from a stockroom to an agent, and click **Qualified**.

    **Note:** Part requirement record numbers start with an **SOPR** prefix and the records are stored in the \[sm\_part\_requirement\] table in the Service Order Management application. Part requirements created in prior releases start with an **WOPR** prefix.


