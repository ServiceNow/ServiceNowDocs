---
title: List view of application rationalization
description: As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-04-29"
reading_time_minutes: 2
breadcrumb: [Rationalization of business applications, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# List view of application rationalization

As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.

![List view in the Application Rationalization page.](../../image/eaw-image/eaw-list-view.png "List view")

You can also create your own application indicators to analyze business applications in the List view. For information on how to create custom application indicators, see [Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md). The new custom indicators appear as new columns in the list view.

**Note:**

-   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](../../task/eaw-task/eaw-attach-profile-indicators-with-application-scoring-profiles.md).
-   If the created indicator isn’t displayed in the bubble size list, ensure that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](../../task/eaw-task/eaw-enable-or-disable-an-application-indicator.md).

All the indicator scores are displayed according to the latest fiscal period, by default. The latest fiscal period is derived from the apm\_app\_indicator\_score list. The duration of a fiscal period is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**.

You can select the name of a business application to open it and view its associated details. Also, you can select the expand row icon \(![Expand row icon.](../../image/ExpandIcon.png)\) to see the demands and projects associated with that business application. On selecting a demand or a project, its details are displayed. You can modify business application details and its associated demand and project details, as required.

**Note:** You need Enterprise Architecture Workspace plugin version 2.2.0 to view the Application Rationalization page.

You can perform the following from the list view:

-   Edit business application details
-   Create a demand for a business application
-   Set the planned disposition of a business application
-   Add the business application lifecycle data
-   You can add or hide the displayed columns as per your requirement by selecting the Personalize icon \(![Personalize icon.](../../image/eaw-image/icon-bubblechart-settings.png)\). Your display preferences are saved and applied the next time you visit the page.

-   **[Create a demand using the list view](../../task/eaw-task/eaw-create-a-demand-using-the-list-view.md)**  
Create a demand for an application from the list view.
-   **[Set the planned disposition of a business application](../../task/eaw-task/eaw-set-planned-disposition-of-a-business-application-listview.md)**  
Set the planned disposition of a business application to track future decisions on the application.
-   **[Add business application lifecycle data using the list view](../../task/eaw-task/eaw-add-business-application-lifecycle-data-listview.md)**  
Create or edit the life cycle of a business application to better manage the business application.
-   **[Edit business application details](../../task/eaw-task/eaw-edit-business-application-details.md)**  
You can make updates to the business application record directly from the list, without leaving the list view.
-   **[Edit a demand associated with a business application](../../task/eaw-task/eaw-edit-a-demand-associated-with-a-business-application.md)**  
Use application rationalization to edit existing demands associated with business applications.
-   **[Edit a project associated with a business application](../../task/eaw-task/eaw-edit-a-project-associated-with-a-business-application.md)**  
Use application rationalization to edit existing projects associated with business applications.

**Parent Topic:**[Rationalization of business applications](eaw-rationalize-business-applications.md)

