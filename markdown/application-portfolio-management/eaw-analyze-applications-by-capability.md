---
title: Analyze applications using the bubble chart
description: Consolidate and analyze the business applications based on multiple scores.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Bubble chart view of application rationalization, Rationalization of business applications, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Analyze applications using the bubble chart

Consolidate and analyze the business applications based on multiple scores.

## Before you begin

You need Enterprise Architecture Workspace plug-in version 2.2.0 to view the Application Rationalization page.

Role required: sn\_apm.apm\_analyst

## About this task

You can narrow down the number of business applications that may be viewed, based on their application indicator scores.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Architecture Workspace**.

2.  Open the Application Rationalization page by selecting the application rationalization icon \(![Application rationalization icon.](../../image/eaw-image/icon-app-rationalization.png)\).

3.  Modify the bubble chart parameters as required by selecting the settings icon \(![Settings icon.](../../image/eaw-image/icon-bubblechart-settings.png)\).

    The following settings are available for modification:

    -   X and Y axis: Dimension of the indicators that fall into the X and Y-axis. The available options are derived from the Application Bubble Charts table \[apm\_bubble\_chart\]. The indicator scores are gathered from the Indicator Scores table \(apm\_app\_indicator\_score\).

        **Note:**

        -   For details on how to add the X and Y-axis indicators of the bubble chart, see [Create or edit a bubble chart for application strategies](../setup-bubble-chart-for-appln-strategy.md).
        -   For a bubble to be displayed on the bubble chart, the indicator scores for the selected fiscal period must be available for both X and Y-axis indicators.
    -   Bubble size: The bubble size is based on indicators related to business applications. The indicator scores determine the size of the bubble.

        You can also create your own application indicators to analyze business applications in the bubble chart. For information on how to create custom application indicators, see [Add or edit an application indicator](eaw-create-indicator.md).

        **Note:**

        -   The created indicator must also be attached to the default application profile. For information on how to attach new profile indicators with a scoring profile, see [Attach a profile indicator with an application scoring profile](eaw-attach-profile-indicators-with-application-scoring-profiles.md).
        -   If the created indicator isn’t displayed in the bubble size list, make sure that the indicator is active. For information on how to activate an indicator, see [Activate or turn off an application or capability indicator](eaw-enable-or-disable-an-application-indicator.md).
    -   Bubble color: The bubble color is based on the planned disposition value of the application. You can refer to the legend displayed on the bubble chart to see the significance of each color.

        **Note:** The bubble color settings can’t be modified.

    -   Bubble labels: Enable the toggle to display the bubble labels in the bubble chart. The bubble labels represent the business application names.

        **Note:** The bubble chart displays up to only 100 bubbles representing business applications. If you have more than 100 bubbles, a message appears. Use the available filters to reduce the number of applications or view the data in the list view.

4.  Select **Apply**.


**Parent Topic:**[Bubble chart view of application rationalization](../../concept/eaw-concept/eaw-bubble-chart-view.md)

