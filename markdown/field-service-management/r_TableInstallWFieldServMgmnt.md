---
title: Tables installed with Field Service Management
description: Tables are provided with the Field Service Management application.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Components installed with Field Service Management, Field Service Management reference, Field Service Management]
---

# Tables installed with Field Service Management

Tables are provided with the Field Service Management application.

<table id="table_FieldServiceManagement"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Work Order\[wm\_order\]

</td><td>

Stores work order records.

</td></tr><tr><td>

Work Order Flow\[sf\_work\_order\]

</td><td>

Stores the work order state flow records.

</td></tr><tr><td>

Work Order Model\[cmdb\_workorder\_product\_model\]

</td><td>

Stores the Product Catalog work order model records. This table was modified by the Field Service Management plugin. This table is renamed and part of Service Order Management.

</td></tr><tr><td>

Work Order Task\[wm\_task\]

</td><td>

Unit of work performed by one person, in one session \(one location and one time\).

</td></tr><tr><td>

Work Task Flow\[sf\_work\_task\]

</td><td>

Stores the work task state flow records.

</td></tr><tr><td>

Work Task Model\[cmdb\_servicetask\_product\_model\]

</td><td>

Stores the Product Catalog work task model records. This table was modified by the Field Service Management plugin. This table is renamed and part of Service Order Management.

</td></tr><tr><td>

WM Map Filters Config\[wm\_map\_filters\_config\]

</td><td>

Stores filter configurations for the agent map on the mobile UI.

</td></tr><tr><td>

Questionnaire\[wm\_questionnaire\]

</td><td>

Stores questionnaires created for work orders and work order tasks.

</td></tr><tr><td>

Work Type\[wm\_work\_type\]

</td><td>

Stores the type of work performed by an agent to complete the work order task.

</td></tr><tr><td>

Work Order Task Potential Assignment Groups\[wm\_work\_order\_task\_potential\_assignment\_groups\]

</td><td>

Calculates and stores the potential assignment group if there are multiple assignment groups that can be serviced for a work order task. **Note:** Applicable only when:

-   The **sn\_fsm.update\_potential\_assignment\_groups** [system property](r_PropInstallWFieldServMgmnt.md) is set to true.
-   More than one assignment group is found for the location.
-   Territory model is inactive.

</td></tr><tr><td>

Scheduling history\[wm\_task\_scheduling\_history\]

</td><td>

Stores the history of the scheduling method of how each work order task has been assigned along with date and time.

</td></tr><tr><td>

Assets\[alm.asset\]

</td><td>

Stores the inventory along with the cost and stockroom details.

</td></tr><tr><td>

Agent schedule attribute plan\[wm\_agent\_schedule\_attribute\_plan\]

</td><td>

Stores the start of the day and end of the day location of agents for a given duration.

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Field Service Management](r_InstalledWithFSM.md)

