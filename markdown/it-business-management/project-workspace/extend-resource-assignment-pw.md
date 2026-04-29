---
title: Extend a resource assignment
description: Extend the date of an allocated resource assignment and allocate resources for the extended period.
locale: en-US
release: australia
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Resource assignments in Project Workspace, Resource planning with Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Extend a resource assignment

Extend the date of an allocated resource assignment and allocate resources for the extended period.

## Before you begin

Role required: resource\_manager

## About this task

Assume that work on a project has started, but there’s a need to extend the date of an allocated resource assignment because the project has been extended. In this scenario, you can extend the date of the allocated resource assignment. The new date by which the resource assignment is extended doesn’t have any impact on the existing allocated hours. While extending the resource assignment, you can specify the new end date and the request type. Based on the request type selected, the required allocated hours are auto-filled.

For example, assume that you allocated 100 hours for 2 months, 50 hours for each month. Now, you want to extend the resource assignment by one month. For the extended month, allocation records are created based on the request type selected.

## Procedure

1.  Navigate to **Workspaces** &gt; **Project Workspace** and open a project.

2.  Extend the resource assignment using one of the following options.

<table id="choicetable_t2q_fkv_1fc"><thead><tr><th align="left" id="d288348e77">

Option

</th><th align="left" id="d288348e80">

Procedure

</th></tr></thead><tbody><tr><td id="d288348e86">

**From resource assignment pane**

</td><td>

1.  From the resource assignment pane, select the row context menu \(![Row context menu.](../../project-workspace/image/icon-row-context-menu.png)\) of resource assignment record and then select **Extend**.![Extend resource assignment.](../image/extend-resource-assignment-pw.png)
2.  From the Extend Assignment window, modify the **New end date** and effort.
3.  Select **Extend** to extend the resource assignment.


</td></tr><tr><td id="d288348e127">

**From resource assignment form**

</td><td>

1.  Navigate to **All** and enter `sn_plng_att_core_resource_assignment.LIST`.
2.  Select the resource assignment record you want to extend and then select **Extend**. ![Extend resource assignment from resource assignment form.](../image/extend-resource-assignment-form-view.png)

**Note:** You can’t set the assignment's extended end date later than the task end date.

3.  From the Extend Assignment window, modify the **New end date** and effort and select **Ok**.


</td></tr></tbody>
</table>
## Result

-   The assignment end date is updated and allocation is created based on resource's availability.
-   The extended FTE or hours or person days is divided equally for the extended resource period.

**Parent Topic:**[Resource assignments in Project Workspace](../concept/resource-assignments-pw.md)

**Related topics**  


[Resource assignments in Project Workspace](../concept/resource-assignments-pw.md)

[Create resource assignments using Project Workspace](create-resource-assignment-prj-wksp.md)

[Update resource assignment from Project Workspace](update-resource-assignment-pw.md)

[Delete a resource assignment from Project Workspace](delete-resource-assignment-pw.md)

[Update the resource allocation in a heatmap](view-allocations-heatmap-prj-wksp.md)

[Realign resource assignment to project task](realign-resource-assignment-to-task.md)

