---
title: Bubble chart view of application rationalization
description: Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-bubble-chart-view.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Rationalization of business applications, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Bubble chart view of application rationalization

Bubble charts are interactive graphs that position applications in different quadrants, based on their indicator scores. Based on the position of the business application in the quadrants, enterprise architects can take decisions to invest in, sustain, migrate, or retire the business applications.

\[Omitted image "bubble-chart-view.png"\] Alt text: Bubble chart view in the Application Rationalization page.

## Overview of the bubble chart

Select the application rationalization icon \(\[Omitted image "icon-app-rationalization.png"\] Alt text: Application rationalization icon.\) and select the **Bubble chart** tab to view the bubble chart view of all business applications.

Use the bubble chart to view indicator scores of business applications in the X and Y axes and specify the bubble sizes. You can use these scores to measure how your applications are aligned to your business strategy and then create demands for the applications.

You can also create your own application indicators to analyze business applications in the bubble chart. For information on how to create custom application indicators, see [Add or edit an application indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-indicator.md).

**Note:**

-   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-attach-profile-indicators-with-application-scoring-profiles.md).
-   If the created indicator isn’t displayed in the bubble size list, verify that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-enable-or-disable-an-application-indicator.md).

You can also generate insights into business applications using Now Assist. For information, see [Generate insights into business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-into-ba.md).

## Bubbles displayed on the chart

The bubble chart displays only the assessed business applications. Also, business applications marked as **Retired** or in **End of Life** lifecycle stage aren’t displayed on the Application Rationalization bubble chart page. However, you can view those business applications by updating the **sn\_apm\_ws.business\_application\_default\_filter** system property. Contact your ServiceNow® account service manager to update the system property. Therefore, the number of bubbles displayed on the chart can be different from the number of business applications displayed on the list view page.

The total number of business applications displayed as bubbles on the bubble chart page is displayed at the top of the chart. You can also select the bubble count details icon \(\[Omitted image "bubble-count-details-icon.png"\] Alt text: Bubble chart count details icon.\) to view a detailed calculation of the number of bubbles displayed on the bubble chart page.\[Omitted image "bubble-chart-count-details.png"\] Alt text: Bubble chart page with the bubble chart analysis number and the bubble count details pop-up highlighted.

## Understanding the bubble chart

The bubble chart page has the following components:

-   X and Y axes: Each axis represents a metric category.
-   Bubbles: Each labeled bubble represents a business application. Hover over a bubble to view an assessable record score summary.

On selecting a bubble, the business application data associated with that bubble is displayed in the info pane.

\[Omitted image "bubble-ba-info.png"\] Alt text: Bubble chart page with a single bubble and the info section displaying the business application details, highlighted.

Business application bubbles whose X and Y-axis values are within the value range of +/-0.25 of each other, are grouped. A grouped bubble displays the total number of business application bubbles that it contains. One selecting a grouped bubble, the info pane appears, displaying the list of individual business applications that are part of the grouped bubble. On selecting a particular business application card, the associated business application data is displayed in the info pane.

\[Omitted image "bubble-chart-group.png"\] Alt text: Bubble chart page with a grouped bubble and the info section displaying the individual business applications within the grouped bubble, highlighted.

The bubble color is dependent on the planned disposition value that was already set for the business application. You can refer to the legend displayed on the bubble chart to see the significance of each color.

The bubbles are of different sizes, based on the indicator score values that you select.

All the indicator scores are displayed according to the latest fiscal period, by default. The latest fiscal period is derived from the apm\_app\_indicator\_score list. The duration of a fiscal period is derived from the system property **com.glide.fiscal\_calendar.fiscal\_unit**. You can also select a different fiscal period from the Scores for fiscal period list. Your fiscal period preferences are saved and applied the next time you visit the page.

\[Omitted image "fiscal-period-dropdown-bubble-chart.png"\] Alt text: Scores for fiscal period list highlighted on the Application rationalization bubble chart page.

The bubble chart displays up to 500 bubbles representing business applications, by default. If you want to see more than 500 bubbles, you can configure the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property. For details, see [Change the number of bubbles displayed on the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-update-sys-prop-change-number-of-bubbles.md).

You can use the available filters to reduce the number of business application bubbles displayed on-screen. You can use the advanced filter to find business applications by applying specific criteria, such as application details, application indicators and scores, and associated business capabilities. Your filter preferences are saved and applied the next time you visit the page.

For more information, see [Apply filters on the Application Rationalization page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-apply-filters-app-rat.md).

## Actions available on the bubble chart page

You can perform the following by hovering over a bubble in the chart and then selecting the context menu:

-   Create a demand for a business application. For more information, see [Create a demand using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-create-a-demand-using-the-bubble-chart.md).
-   Set the planned disposition of a business application. For more information, see [Set the planned disposition of a business application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-set-planned-disposition-of-a-business-application.md).
-   Add business application lifecycle data. For more information, see [Add business application lifecycle data using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-add-business-application-lifecycle-data.md).

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

Select the zoom in icon \(\[Omitted image "bubble-chart-zoom-in.png"\] Alt text: Zoom in icon.\)**Note:** Select the zoom reset icon \(\[Omitted image "bubble-chart-reset-zoom.png"\] Alt text: Zoom reset icon.\) to reset to the default zoom level.

</td><td>

Select the zoom out icon \(\[Omitted image "bubble-chart-zoom-out.png"\] Alt text: Zoom out icon.\)**Note:** Select the zoom reset icon \(\[Omitted image "bubble-chart-reset-zoom.png"\] Alt text: Zoom reset icon.\) to reset to the default zoom level.

</td><td>

Not applicable

</td></tr><tr><td>

Track pad

</td><td>

-   Place the cursor on a specific point on the bubble chart and double click on the trackpad
-   Select an area on the bubble chart

</td><td>

Select the zoom out icon \(\[Omitted image "bubble-chart-zoom-out.png"\] Alt text: Zoom out icon.\)**Note:** Select the zoom reset icon \(\[Omitted image "bubble-chart-reset-zoom.png"\] Alt text: Zoom reset icon.\) to reset to the default zoom level.

</td><td>

Press and hold Shift key and then click and move the cursor**Note:** For the pan functionality to work, you must be zoomed in on a particular area on the bubble chart.

</td></tr><tr><td>

Mouse device

</td><td>

-   Double click on a particular section of the chart
-   Select an area on the bubble chart

</td><td>

Select the zoom out icon \(\[Omitted image "bubble-chart-zoom-out.png"\] Alt text: Zoom out icon.\)**Note:** Select the zoom reset icon \(\[Omitted image "bubble-chart-reset-zoom.png"\] Alt text: Zoom reset icon.\) to reset to the default zoom level.

</td><td>

Press and hold Shift key and then click and move the cursor**Note:** For the pan functionality to work, you must be zoomed in on a particular area on the bubble chart.

</td></tr></tbody>
</table>**Note:** You can zoom on this page to 200% or 400% through your browser settings without the loss of content or functionality. Page layouts are transformed into a vertical, stacked view automatically.

**Parent Topic:**[Rationalization of business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-rationalize-business-applications.md)

**Related topics**  


[Analyze applications using the bubble chart](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-analyze-applications-by-capability.md)

[Generate insights into business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/generate-insights-into-ba.md)

