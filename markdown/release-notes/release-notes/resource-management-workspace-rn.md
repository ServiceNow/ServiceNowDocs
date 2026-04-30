---
title: Resource Management Workspace release notes
description: The ServiceNow Resource Management Workspace application provides resource managers with a more efficient way to work with a dedicated workspace to view and manage resource assignments. Resource Management Workspace was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
---

# Resource Management Workspace release notes

The ServiceNow® Resource Management Workspace application provides resource managers with a more efficient way to work with a dedicated workspace to view and manage resource assignments. Resource Management Workspace was enhanced and updated in the Yokohama release.

## Resource Management Workspace highlights for the Yokohama release

-   Access the new heatmap modal to view the resource status, remaining capacity, and utilization efforts of resource allocation.
-   Use the **Name**, **Notes**, and **Ready for review** fields while creating a New Resource Assignment.
-   Access the resource assignments and the parent resource assignment from the resource board.
-   Use the interactive dashboard to create and manage widgets to access the required set of resource data in board view.
-   Extend, adjust, and approve resource assignments using the row context menu from the side grid.

See [Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US) for more information.

**Important:** Resource Management Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_fmx_yrl_b1c)**
    -   View the Resource status, Remaining capacity, and Utilization columns to the allocation heatmap modal to help resource managers to view detailed insights and the total efforts for Approved and Pending tasks.
    -   Use the Total row in the heatmap modal to view the aggregate utilization for approved and pending tasks.
    -   Update the resource status and the efforts for child assignments using the new modal.
    -   Capture additional details required to the Project manager or Resource manager while creating a New Resource Assignment and New Operational Assignment using the following new fields.
        -   **Name**
        -   **Ready for review**
        -   **Notes**
    -   Access the assigned resource assignments or the parent resource assignment directly from the resource board view.
-   **[Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_v4k_rtg_1fc)**

    View and access the resource assignments from high-level to get an overview of all the resource assignments, based on their states, completion dates, start dates, resources with allocations over their capacity, and resources allocations within their available.

    -   Filter the resource board using the primary attributes and dates to build a custom view.
    -   Edit the dashboard further to manage the data representation view of existing widgets or add new elements to build the required widgets.
    -   Access the custom resource boards from dashboard using the interactive widgets to manage the allocations details.
    -   Edit the Start and End dates, Task efforts, and Resource status for assigned tasks in the top tray using the inline editing feature.

## UI changes

-   **[Using Resource Management Workspace](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_fmx_yrl_b1c)**

    Added the following details in the resource allocation heatmap view.

    -   The Resource status column to view Approved and Pending assignments.
    -   The Remaining capacity column to view the remaining or over-allocated efforts.
    -   The Utilization column to view the total efforts of approved and pending tasks.
-   **[Create resource assignments and operation resource assignments in Resource Management Workspace](https://www.servicenow.com/docs/access?context=create-ra-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**
    -   Added the following fields to create resource assignment form.
        -   The **Name** field provides a custom or identifiable name for resource assignment.
        -   The Ready for review list to confirm if a resource assignment is ready for a Resource manager's review for allocation.
        -   The **Notes** field to add any additional notes while creating a resource assignment.
    -   Added the following fields in the row context menu of resource assignments in the top tray.
        -   The **Open Resource Assignment** field to view and edit a specific assigned assignment.
        -   The **Open Parent Resource Assignment** field to view and edit the parent assignment.
        -   The **Extend** menu item and **Extend Assignment** modal to request an extension to a resource assignment.
-   **[New navigation menu](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_v4k_rtg_1fc)**
    -   New Reporting dashboard landing page in Resource Management Workspace to view and access the resource allocation details.
    -   Interactive widgets in Reporting dashboard to access the custom resource boards.

## Changed in this release

-   **[New resource heatmap view](https://www.servicenow.com/docs/access?context=using-rmw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US#section_fmx_yrl_b1c)**

    The resource allocation heatmap view provides more relevant information such as resource status, remaining capacity, and utilization of resources which helps resource managers to plan efficiently and allocate the resources based on their availability, bandwidth, and work requirements.


## Activation information

Install Resource Management Workspace by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Planning user capacity in Strategic Planning Workspace](https://www.servicenow.com/docs/access?context=using-cap-plan-spw&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)**

    Capacity Planning gives you insights about resource availability, allocation details, availability, and operational work assignments. Resource Managers can use this information to approve requested resource assignments and allocate work.


**Parent Topic:**[Strategic Portfolio Management release notes](it-business-management-rn-landing.md)

