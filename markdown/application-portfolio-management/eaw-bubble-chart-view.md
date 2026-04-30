---
title: Bubble chart view of application rationalization
description: Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Rationalization of business applications, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Bubble chart view of application rationalization

Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.

![Bubble chart view in the Application Rationalization page.](../../image/eaw-image/bubble-chart-view.png "Bubble chart view")

## Overview of the bubble chart

Select the application rationalization icon \(![Application rationalization icon.](../../image/eaw-image/icon-app-rationalization.png)\) and select the **Bubble chart** tab to view the bubble chart view of all business applications.

Use the bubble chart to view indicator scores of business applications in the X and Y axes and specify the bubble sizes. You can use these scores to measure how your applications are aligned to your business strategy and then create demands for the applications.

You can also create your own application indicators to analyze business applications in the bubble chart. For information on how to create custom application indicators, see [Add or edit an application indicator](../../task/eaw-task/eaw-create-indicator.md).

**Note:**

-   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](../../task/eaw-task/eaw-attach-profile-indicators-with-application-scoring-profiles.md).
-   If the created indicator isn’t displayed in the bubble size list, verify that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](../../task/eaw-task/eaw-enable-or-disable-an-application-indicator.md).

## Bubbles displayed on the chart

The bubble chart displays only the assessed business applications. Also, business applications marked as **Retired** or in **End of Life** lifecycle stage aren’t displayed on the Application Rationalization bubble chart page. However, you can view those business applications by updating the **sn\_apm\_ws.business\_application\_default\_filter** system property. Contact your ServiceNow® account service manager to update the system property. Therefore, the number of bubbles displayed on the chart can be different from the number of business applications displayed on the list view page.

The total number of business applications displayed as bubbles on the bubble chart page is displayed at the top of the chart. You can also select the bubble count details icon \(![Bubble chart count details icon.](../../image/eaw-image/bubble-count-details-icon.png)\) to view a detailed calculation of the number of bubbles displayed on the bubble chart page.![Bubble chart page with the bubble chart analysis number and the bubble count details pop-up highlighted.](../../image/eaw-image/bubble-chart-count-details.png)

## Understanding the bubble chart

The bubble chart page has the following components:

-   X and Y axes: Each axis represents a metric category.
-   Bubbles: Each labeled bubble represents a business application. Hover over a bubble to view an assessable record score summary.

On selecting a bubble, the business application data associated with that bubble is displayed in the info pane.

![Bubble chart page with a single bubble and the info section displaying the business application details, highlighted.](../../image/eaw-image/bubble-ba-info.png)

Business application bubbles whose X and Y-axis values are within the value range of +/-0.25 of each other, are grouped. A grouped bubble displays the total number of business application bubbles that it contains. One selecting a grouped bubble, the info pane appears, displaying the list of individual business applications that are part of the grouped bubble. On selecting a particular business application card, the associated business application data is displayed in the info pane.

![Bubble chart page with a grouped bubble and the info section displaying the individual business applications within the grouped bubble, highlighted.](../../image/eaw-image/bubble-chart-group.png)

The bubble color is dependent on the planned disposition value that was already set for the business application. You can refer to the legend displayed on the bubble chart to see the significance of each color.

The bubbles are of different sizes, based on the indicator score values that you select.

All the indicator scores are displayed according to the latest fiscal period, by default. The latest fiscal period is derived from the apm\_app\_indicator\_score list. The duration of a fiscal period is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**. You can also select a different fiscal period from the Scores for fiscal period list. Your fiscal period preferences are saved and applied the next time you visit the page.

![Scores for fiscal period list highlighted on the Application rationalization bubble chart page.](../../image/eaw-image/fiscal-period-dropdown-bubble-chart.png)

The bubble chart displays up to 500 bubbles representing business applications, by default. If you want to see more than 500 bubbles, you can configure the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property. For details, see [Change the number of bubbles displayed on the bubble chart](../../task/eaw-task/eaw-update-sys-prop-change-number-of-bubbles.md).

You can use the available filters to reduce the number of business application bubbles displayed on-screen. You can use the advanced filter to find business applications by applying specific criteria, such as application details, application indicators and scores, and associated business capabilities. Your filter preferences are saved and applied the next time you visit the page.

For more information, see [Apply filters on the Application Rationalization page](../../task/eaw-task/eaw-apply-filters-app-rat.md).

## Actions available on the bubble chart page

You can perform the following by hovering over a bubble in the chart and then selecting the context menu:

-   Create a demand for a business application. For more information, see [Create a demand using the bubble chart](../../task/eaw-task/eaw-create-a-demand-using-the-bubble-chart.md).
-   Set the planned disposition of a business application. For more information, see [Set the planned disposition of a business application](../../task/eaw-task/eaw-set-planned-disposition-of-a-business-application.md).
-   Add business application lifecycle data. For more information, see [Add business application lifecycle data using the bubble chart](../../task/eaw-task/eaw-add-business-application-lifecycle-data.md).

## Zoom or pan on the bubble chart

You can zoom in, zoom out, or pan on the bubble chart page using either on-screen buttons or by using a mouse device or trackpad interactions.

<table id="table_vtw_xtk_fhc"><thead><tr><th>

Interaction Method

</th><th>

Zoom in

</th><th>

Zoom out

</th><th>

Pan

</th></tr></thead><tbody><tr><td>

On-screen button

</td><td>

Select the zoom in icon \(![Zoom in icon.](../../image/eaw-image/bubble-chart-zoom-in.png)\)**Note:** Select the zoom reset icon \(![Zoom reset icon.](../../image/eaw-image/bubble-chart-reset-zoom.png)\) to reset to the default zoom level.

</td><td>

Select the zoom out icon \(![Zoom out icon.](../../image/eaw-image/bubble-chart-zoom-out.png)\)**Note:** Select the zoom reset icon \(![Zoom reset icon.](../../image/eaw-image/bubble-chart-reset-zoom.png)\) to reset to the default zoom level.

</td><td>

Not applicable

</td></tr><tr><td>

Track pad

</td><td>

-   Place the cursor on a specific point on the bubble chart and double click on the trackpad
-   Select an area on the bubble chart

</td><td>

Select the zoom out icon \(![Zoom out icon.](../../image/eaw-image/bubble-chart-zoom-out.png)\)**Note:** Select the zoom reset icon \(![Zoom reset icon.](../../image/eaw-image/bubble-chart-reset-zoom.png)\) to reset to the default zoom level.

</td><td>

Press and hold Shift key and then click and move the cursor**Note:** For the pan functionality to work, you must be zoomed in on a particular area on the bubble chart.

</td></tr><tr><td>

Mouse device

</td><td>

-   Double click on a particular section of the chart
-   Select an area on the bubble chart

</td><td>

Select the zoom out icon \(![Zoom out icon.](../../image/eaw-image/bubble-chart-zoom-out.png)\)**Note:** Select the zoom reset icon \(![Zoom reset icon.](../../image/eaw-image/bubble-chart-reset-zoom.png)\) to reset to the default zoom level.

</td><td>

Press and hold Shift key and then click and move the cursor**Note:** For the pan functionality to work, you must be zoomed in on a particular area on the bubble chart.

</td></tr></tbody>
</table>**Note:** You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

-   **[Analyze applications using the bubble chart](../../task/eaw-task/eaw-analyze-applications-by-capability.md)**  
Consolidate and analyze the business applications based on multiple scores.
-   **[View scores of a custom scoring profile on bubble chart](../../task/eaw-task/eaw-app-rat-custom-scoring-profile-scores.md)**  
Create a system property to view indicator scores of a custom scoring profile on the application rationalization bubble chart.
-   **[Create a demand using the bubble chart](../../task/eaw-task/eaw-create-a-demand-using-the-bubble-chart.md)**  
Create a demand for an application from the bubble chart.
-   **[Set the planned disposition of a business application](../../task/eaw-task/eaw-set-planned-disposition-of-a-business-application.md)**  
Set the planned disposition of a business application to track decisions on the plan of the application.
-   **[Add business application lifecycle data using the bubble chart](../../task/eaw-task/eaw-add-business-application-lifecycle-data.md)**  
Create or edit the life cycle of a business application to manage the business application.
-   **[Edit business application details in bubble chart view](../../task/eaw-task/eaw-edit-ba-details-in-bubble-chart.md)**  
You can make updates to the business application record directly from the list, without leaving the bubble chart view.
-   **[Change the number of bubbles displayed on the bubble chart](../../task/eaw-task/eaw-update-sys-prop-change-number-of-bubbles.md)**  
Customize the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property to change the number of bubbles displayed on the application rationalization bubble chart page.

**Parent Topic:**[Rationalization of business applications](eaw-rationalize-business-applications.md)

