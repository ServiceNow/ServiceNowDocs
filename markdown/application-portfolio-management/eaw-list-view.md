---
title: List view of application rationalization
description: As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Rationalization of business applications, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# List view of application rationalization

As an Enterprise Architect, you can view the list of all business applications. The List view enables you to see high-level information on all your business applications and all the indicator scores that are attached to them.

![List view in the Application Rationalization page.](../../image/eaw-image/eaw-list-view.png "List view")

## Overview of the list view

The list view of application rationalization enables you to view all available applications based on your scoring profile, in your enterprise architecture landscape. For details, see [Configure scoring profiles](eaw-setup-scroring-prof.md).

You can perform side-by-side comparison of application scores and indicators across multiple dimensions.

You can also create your own application indicators to analyze business applications in the List view. For information on how to create custom application indicators, see [Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md). The new custom indicators appear as new columns in the list view.

**Note:**

-   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](../../task/eaw-task/eaw-attach-profile-indicators-with-application-scoring-profiles.md).
-   If the created indicator isn’t displayed in the list, verify that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](../../task/eaw-task/eaw-enable-or-disable-an-application-indicator.md).

All the indicator scores are displayed according to the latest fiscal period, by default. You can also select a different fiscal period from the Scores for fiscal period list. Your fiscal period preferences are saved and applied the next time you visit the page.

![Scores for fiscal period list highlighted on the Application rationalization list view page.](../../image/eaw-image/fiscal-period-dropdown.png)

The latest fiscal period is derived from the apm\_app\_indicator\_score list. The duration of a fiscal period is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**.

You can select the name of a business application to open it and view its associated details. Also, you can select the expand row icon \(![Expand row icon.](../../image/ExpandIcon.png)\) to see the demands and projects associated with that business application. On selecting a demand or a project, its details are displayed. You can modify business application details and its associated demand and project details, as required.

Business applications marked as **Retired** or in **End of Life** lifecycle stage aren’t displayed on the Application Rationalization List view page. However, you can view those business applications by updating the **sn\_apm\_ws.business\_application\_default\_filter** system property. Contact your ServiceNow® account service manager to update the system property.

You can also generate insights into business applications using Now Assist. For information, see [Generate insights into business applications](../../../now-assist-ea/task/generate-insights-into-ba.md).

## View and compare actual and normalized indicator scores

You can view the actual indicator scores for a business application on the list view page and compare them with the normalized scores. Actual scores refer to the raw value of the indicator as captured from its source. These values aren’t scaled and can vary widely across applications, depending on the underlying data.

The normalized score refers to the scaled value of an indicator, derived from the actual score using a normalization formula. This enables all indicator scores to fit into a common range. Normalized scores ensure comparability across different indicators with varying units and ranges.

To view the actual scores of indicators, select the data visibility icon \(![Data visibility icon.](../../image/eaw-image/list-view-display-visibility-icon.png)\) and then enable the **Show actual score data** toggle.

![List view page with the data visibility icon and Show actual score data toggle highlighted.](../../image/eaw-image/list-view-actual-score-toggle.png)

The actual indicator scores and their normalized values for business applications are displayed. For example, the actual column for the Number of Incidents indicator displays the actual number of incidents associated with the business application during the selected fiscal period.

![List view page with the actual and normalized score columns highlighted for the Number of Incidents indicator.](../../image/eaw-image/list-view-scores-highlighted.png)

**Note:** The Portfolio TCO indicator displays currency values in the format specified in the **glide.currency2.default\_reference\_currency** property. If this property isn’t configured, the currency values are displayed in US dollar \(USD\) format by default.

Your display preferences are saved and applied the next time you visit the page.

## Actions available on the list view page

You can perform the following from the list view page:

-   Edit business application details. For more information, see [Edit business application details in list view](../../task/eaw-task/eaw-edit-business-application-details.md).
-   Create a demand for a business application. For more information, see [Create a demand using the list view](../../task/eaw-task/eaw-create-a-demand-using-the-list-view.md).
-   Set the planned disposition of a business application. For more information, see [Set the planned disposition of a business application](../../task/eaw-task/eaw-set-planned-disposition-of-a-business-application-listview.md).
-   Add the business application lifecycle data. For more information, see [Add business application lifecycle data using the list view](../../task/eaw-task/eaw-add-business-application-lifecycle-data-listview.md).
-   You can add or hide the displayed columns according to your requirement by selecting the Personalize icon \(![Personalize icon.](../../image/eaw-image/icon-bubblechart-settings.png)\). Your display preferences are saved and applied the next time you visit the page.
-   Export the list view data to Microsoft Excel or CSV. For more information, see [Export application rationalization data to Excel or CSV](../../task/eaw-task/eaw-export-app-rat-list-data.md).

**Note:** You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

**Parent Topic:**[Rationalization of business applications](eaw-rationalize-business-applications.md)

**Related topics**  


[Edit a demand associated with a business application](../../task/eaw-task/eaw-edit-a-demand-associated-with-a-business-application.md)

[Edit a project associated with a business application](../../task/eaw-task/eaw-edit-a-project-associated-with-a-business-application.md)

[Export application rationalization data to Excel or CSV](../../task/eaw-task/eaw-export-app-rat-list-data.md)

[Apply filters on the Application Rationalization page](../../task/eaw-task/eaw-apply-filters-app-rat.md)

[Generate insights into business applications](../../../now-assist-ea/task/generate-insights-into-ba.md)

