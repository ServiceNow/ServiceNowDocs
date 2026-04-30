---
title: Bubble chart view of application rationalization
description: Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Rationalization of business applications, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Bubble chart view of application rationalization

Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.

Use the bubble chart to view indicator scores of business applications in the X and Y axes and specify the bubble sizes. You can use these scores to measure how your applications are aligned to your business strategy and then create demands for the applications.

**Note:**

You need Enterprise Architecture Workspace version 2.2.0 to view the Application Rationalization page.

You can also create your own application indicators to analyze business applications in the bubble chart. For information on how to create custom application indicators, see [Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md).

**Note:**

-   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](../../task/eaw-task/eaw-attach-profile-indicators-with-application-scoring-profiles.md).
-   If the created indicator isn’t displayed in the bubble size list, ensure that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](../../task/eaw-task/eaw-enable-or-disable-an-application-indicator.md).

Select the application rationalization icon \(![Application rationalization icon.](../../image/eaw-image/icon-app-rationalization.png)\) to view the bubble chart view of all business applications.

The bubble chart page has the following components:

-   X and Y axes: Each axis represents a metric category.
-   Bubbles: Each labeled bubble represents a business application. Point to a bubble to view an assessable record score summary.

The bubble color is dependent on the planned disposition value that was already set for the business application. You can refer to the legend displayed on the bubble chart to see the significance of each color.

The bubbles are of different sizes, based on the indicator score values that you select.

All the indicator scores are displayed according to the latest fiscal period, by default. The latest fiscal period is derived from the apm\_app\_indicator\_score list. The duration of a fiscal period is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**. However, the fiscal period can be changed using the filter available on the Application Rationalization screen and other filters may also be applied.

You can perform the following by pointing to a bubble in the chart and then selecting the context menu:

-   Create a demand for a business application.
-   Set the planned disposition of a business application.
-   Add business application lifecycle data.

The bubble chart displays up to only 100 bubbles representing business applications. If you have more than 100 bubbles, a message appears. Use the available filters to reduce the number of applications or view the data in the list view.

![Bubble chart view in the Application Rationalization page.](../../image/eaw-image/bubble-chart-view.png "Bubble chart view")

-   **[Analyze applications using the bubble chart](../../task/eaw-task/eaw-analyze-applications-by-capability.md)**  
Consolidate and analyze the business applications based on multiple scores.
-   **[Create a demand using the bubble chart](../../task/eaw-task/eaw-create-a-demand-using-the-bubble-chart.md)**  
Create a demand for an application from the bubble chart.
-   **[Set the planned disposition of a business application](../../task/eaw-task/eaw-set-planned-disposition-of-a-business-application.md)**  
Set the planned disposition of a business application to track decisions on the future planning of the application.
-   **[Add business application lifecycle data using the bubble chart](../../task/eaw-task/eaw-add-business-application-lifecycle-data.md)**  
Create or edit the life cycle of a business application to manage the business application.

**Parent Topic:**[Rationalization of business applications](eaw-rationalize-business-applications.md)

