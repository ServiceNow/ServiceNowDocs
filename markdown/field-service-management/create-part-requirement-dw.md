---
title: Create a part requirement in Dispatcher Workspace
description: Create a part requirement for a work order task in Dispatcher Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing part requirements in Dispatcher Workspace, Working in Dispatcher Workspace, Scheduling and dispatching work order tasks to agents, Using Field Service Management, Field Service Management]
---

# Create a part requirement in Dispatcher Workspace

Create a part requirement for a work order task in Dispatcher Workspace.

## Before you begin

Role required: wm\_dispatcher

## Procedure

1.  Navigate to **All** &gt; **Field Service** &gt; **Dispatching** &gt; **Dispatcher Workspace**.

2.  Click a task number from the task panel or calendar that is in Awaiting Qualification, Qualified, Assigned, or Work in Progress state.

    **Note:** Enabling the **Apply Work Order template in draft status** configuration, allows you to create part requirements for a work order task that is in the Draft state.

3.  In the **Part Requirements** related list, click **New**.

4.  On the form, fill in the required fields.

5.  | | |
|---|---|
|Number|Auto-generated number for the part requirement.|
|Service order task|Number assigned to the work order task.|
|Model|Description of the part model needed to complete the work order task.|
|Required by date|Date by which all parts should be delivered. The date is filled in automatically based on the task's expected travel start time. If necessary, change the date manually.|
|Required quantity|Total quantity necessary to complete the part requirement. This field becomes read-only when the full number of required parts has been sourced.|
|Reserved quantity|Total quantity that has been sourced already.|
|Sourced|Indicator for whether the required quantity for this part requirement has been reserved and transfer requested from one stockroom to another.|
|Delivered|Indicator for whether the transfer order lines under this part requirement have been delivered or not.|
|Short description|Contents of the Short description field from the parent work order. If the work order was created from an incident, problem, or change request, the short description of the part requirement is inherited from that record. If the work order was created automatically from a , the short description is from model template. This field is not visible by default.|
|Mandatory|Option to indicate if the part is mandatory to perform the work order task.|

6.  Click **Save**.

    If the part is out of stock, a message appears at the top of the form naming the part.


## Result

Part requirement is created successfully. The part requirement record number starts with an SOPR prefix and the records are stored in the \[sm\_part\_requirement\] table in the Service Order Management application.

