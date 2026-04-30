---
title: Analyze applications using the bubble chart
description: Consolidate and analyze the business applications based on multiple scores.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use bubble chart view, Working with application rationalization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Analyze applications using the bubble chart

Consolidate and analyze the business applications based on multiple scores.

## Before you begin

Role required: sn\_apm.apm\_analyst

## About this task

You can narrow down the number of business applications that may be viewed, based on their application indicator scores.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Application Rationalization page by selecting the application rationalization icon \(![Application rationalization icon.](../../image/eaw-image/icon-app-rationalization.png)\).

3.  Select **Bubble chart**.

4.  Modify the bubble chart parameters as required by selecting the settings icon \(![Settings icon.](../../image/eaw-image/icon-bubblechart-settings.png)\).

    The following settings are available for modification:

    -   X and Y axis: Dimension of the indicators that fall into the X and Y-axis. The available options are derived from the Application Bubble Charts table \[apm\_bubble\_chart\]. The indicator scores are gathered from the Indicator Scores table \(apm\_app\_indicator\_score\).

        **Note:**

        -   For details on how to add the X and Y-axis indicators of the bubble chart, see [Create or edit a bubble chart for application strategies - Legacy](../setup-bubble-chart-for-appln-strategy.md).
        -   For a bubble to be displayed on the bubble chart, the indicator scores for the selected fiscal period must be available for both X and Y-axis indicators.
    -   Bubble size: The bubble size is based on indicators related to business applications. The indicator scores determine the size of the bubble.

        You can also create your own application indicators to analyze business applications in the bubble chart. For information on how to create custom application indicators, see [Add or edit an application indicator](eaw-create-indicator.md).

        **Note:**

        -   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](eaw-attach-profile-indicators-with-application-scoring-profiles.md).
        -   If the created indicator isn’t displayed in the bubble size list, make sure that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](eaw-enable-or-disable-an-application-indicator.md).
    -   Bubble color: The bubble color is based on the planned disposition value of the application. You can refer to the legend displayed on the bubble chart to see the significance of each color.

        **Note:** The bubble color settings can’t be modified.

    -   Bubble labels: Enable the toggle to display the bubble labels in the bubble chart. The bubble labels represent the business application names.

        The bubble chart displays up to 500 bubbles representing business applications, by default. If you want to see more than 500 bubbles, you can configure the **sn\_apm\_ws.appRationalizationMaximumBubbles** system property. For details, see [Change the number of bubbles displayed on the bubble chart](eaw-update-sys-prop-change-number-of-bubbles.md).

5.  Select **Apply**.

    Business application bubbles are displayed on the bubble chart.

    Business application bubbles whose X and Y-axis values are within the value range of +/-0.25 of each other, are grouped. A grouped bubble displays the total number of business application bubbles that it contains. One selecting a grouped bubble, the info pane appears, displaying the list of individual business applications that are part of the grouped bubble.

    ![Bubble chart page with a grouped bubble and the info section displaying the individual business applications within the grouped bubble, highlighted.](../../image/eaw-image/bubble-chart-group.png)


**Parent Topic:**[Use bubble chart view](../../concept/eaw-concept/eaw-using-app-rat-bubble-chart-view.md)

**Related topics**  


[Create a demand using the bubble chart](eaw-create-a-demand-using-the-bubble-chart.md)

[Set the planned disposition of a business application](eaw-set-planned-disposition-of-a-business-application.md)

[Add business application lifecycle data using the bubble chart](eaw-add-business-application-lifecycle-data.md)

[Bubble chart view of application rationalization](../../concept/eaw-concept/eaw-bubble-chart-view.md)

[Apply filters on the Application Rationalization page](eaw-apply-filters-app-rat.md)

