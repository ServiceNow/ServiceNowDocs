---
title: Create a user view in Service Operations Workspace
description: Create and customize a user view in the Service Operations Workspace to enable viewing information in the format you want.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create a user view in Service Operations Workspace

Create and customize a user view in the Service Operations Workspace to enable viewing information in the format you want.

## Before you begin

**Note:** The Operator Workspace interface is available only to customers who have upgraded from a release prior to the Utah release. New customers as of the Utah release can use the Service Operations Workspace for ITOM, which offers an enhanced UI for managing alerts.

Role required: evt\_mgmt\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the left navigation bar, select the Service Dashboard icon: ![Service Dashboard icon](../image/icon-service-dashboard.png).

    The Service Dashboard page appears.

    **Note:** The application services that appear in the Service Dashboard are those added to the Impact Filter Services list. For more information, see [Add application services for impact calculation](../../event-management/task/add-impact-cal-services.md).

3.  Customize the dashboard appearance by selecting output criteria from the **Group by**, **Group order**, or **Segment each group by** filters, or by selecting the relevant **Severity breakdown**.

    Selecting **Service group** &gt; **All** in the **Group by** filter displays all service groups.

4.  Configure the information for the view to display by clicking the filter services icon \(![Filter services icon](../../event-management/image/filter-icon-button.png)\) and setting a global filter.

    For example, you can configure a filter to display only those services assigned to a specific user.

    **Note:** To discard your changes and revert to the view's most recently saved state, select the More actions icon \(![More actions icon](../image/icon-more-actions.png)\) and select **Discard changes**.

    ![Option to discard view.](../image/sow-discard-view.png)

5.  Save your new view by clicking the More actions icon \(![More actions icon](../../event-management/image/more-actions-icon-horizontal.png)\) next to the **Save** button and select **Save as copy**.

    ![Create a view by saving it as a copy.](../image/sow-save-as-copy.png)

6.  In the Save as copy dialog box, enter the name of your view in the **View name** field.

    The view is saved as a **Private view** \(visible only to the logged-in user\) and is available for use.

    Views are grouped in the following categories:

    -   **Global views**: Visible to all users. Only an Event Management administrator can create a global view.
    -   **Private views**: Visible only to the logged-in user.
    **Note:** You can switch between different views by selecting a view from the list next to the **Save** button.

    ![List that displays all the views.](../image/select-view-dropdown-2.png)


