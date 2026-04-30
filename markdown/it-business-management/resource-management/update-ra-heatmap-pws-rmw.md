---
title: Update resource assignments using Project Workspace
description: Use the allocation heatmap capability in Project Workspace to view and update the resource allocation.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage resource assignments from Project Workspace, Use, Resource Management Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Update resource assignments using Project Workspace

Use the allocation heatmap capability in Project Workspace to view and update the resource allocation.

## Before you begin

Role required: it\_project\_manager

## About this task

The **Allocation heatmap** toggle button provides a detailed breakdown of the allocation of an individual resource. The allocation heatmap represents the total utilization of a resource for a week or month. By default, allocation information is displayed for the week. This information helps project managers to plan their resources effectively at the project or task level.

Integrate your ServiceNow® instance with your organization's Microsoft Teams to enable collaboration of your projects and resource allocations in Microsoft Teams. With the Microsoft Teams integration, you can communicate with the project team members and share real-time updates on the project and resource allocation status. For more information, see [Setting up PPM collaboration for Microsoft Teams](../../ppm-collab/concept/setup-collab-ppm-msteams.md).

## Procedure

1.  [Create resource assignments using Project Workspace](../../pw-resource-management/task/create-resource-assignment-prj-wksp.md).

2.  View the resource allocations in the heatmap by enabling the **Allocation heatmap** toggle button.

    You can switch from the week view to the month view based on your requirement.

3.  Edit the desired field and select anywhere on the data grid to save the details.

    Work allocation is based on capacity. The allocations are color-coded to display the availability of the resources as shown here. These colors help to identify the availability of the resource for a particular task.

    ![heatmap -legend](../../pw-resource-management/image/heatmap-legend.png)

4.  Edit the resource allocation window by selecting the allocation hours cell.

    ![allocation-hours-cell](../../pw-resource-management/image/resource-allocation-cell.png)

    Enable the **Show actuals** toggle to view the actuals of each resource. The actuals can't be edited from Project Workspace.

5.  From the resource allocation window, view and track the assigned **Project**, **Owner**,**Task**, and **Task effort** of a resource.

    The resource allocation is made according to the schedule of the resource, provided that the resource has a schedule.

    The Allocation heatmap modal provides the **Resource status**, **Remaining capacity**, and **Utilization** columns to support resource managers in evaluating task efforts.

6.  Send a direct message to the project owner on Microsoft Teams by selecting the **Project Owner** field.

    ![resource-allocation-window](../../pw-resource-management/image/resource-allocation-window.png)

    **Note:** The **Project Owner** field can only be selected if your ServiceNow® instance is integrated with your organization's Microsoft Teams. Resource assignments on demands are visible in the allocation window both before and after they become projects.


**Parent Topic:**[Manage resource assignments from Project Workspace](../concept/use-ra-rmw.md)

**Related topics**  


[Create resource assignments using Project Workspace](../../pw-resource-management/task/create-resource-assignment-prj-wksp.md)

