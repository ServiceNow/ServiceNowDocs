---
title: Capacity planning overview
description: Capacity Planning page provides resource managers with a comprehensive view of capacity, allocations, and utilization of resources. As a resource manager, you can use it to review resource capacity and existing allocations and then confirm resources to a demand or project.
locale: en-US
release: xanadu
product: Resource Management
classification: resource-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Capacity planning overview

Capacity Planning page provides resource managers with a comprehensive view of capacity, allocations, and utilization of resources. As a resource manager, you can use it to review resource capacity and existing allocations and then confirm resources to a demand or project.

**Important:** Capacity planning is being deprecated starting Xanadu release. It will be hidden and no longer available for installation but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Resource Managers are encouraged to use the [Planning user capacity in Strategic Planning Workspace](../../spw-capacity-planning/concept/using-cap-plan-spw.md) to view and manage the capacity, allocations, and utilization of resources.

The capacity planning page is based on Service Portal which enables you to configure, customize, and extend it per your requirements and organizational workflow. See [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) for more information.

The Capacity Planning page is divided into following sections:

-   **Resource Plans**

    The left pane displays the requested resource plans as cards based on the filter conditions. You can select more than one resource plan to review the capacity of the associated resources.

-   **Resource Forecast**

    The section enables you to review the resource forecast of the selected resource plans in the following tabs:

    -   **Overview** tab: Displays the following items in the stacked bar chart.

        -   the total capacity trend for the resources
        -   requested hours \(for the selected plan only\)
        -   confirmed hours \(across all projects\)
        -   the allocated hours \(across all projects\)
        Pointing to any of the sections on the bar chart shows its details.

    -   **% Utilization** tab: Displays the heat map for the percentage of utilization of resources including both hard and soft allocations and requested hours for the selected resource plans. The heat map helps resource managers understand how committed utilization would look if resources are allocated to resource plans in the requested state. If utilization is greater than 100%, resources are over allocated. The resource manager must ensure that percentage of utilization of all resources is within 100%.

**Note:** If a resource plan is already allocated, you cannot select it to see its details in the resource forecast section.

![Capacity Planning page](../image/ConfirmResourcesView.png "Capacity Planning page example")

-   **[Review capacity of the resources](../task/review-capacity-for-resources.md)**  
Use the capacity planning page to review the capacity and utilization trends of the resources associated with the requested resource plans.

**Parent Topic:**[Resource Management classic](c_ResourceManagement.md)

