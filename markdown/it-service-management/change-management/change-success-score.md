---
title: Change success score
description: Use team historical data for insights into team performance. The score value helps you to determine how likely the team is to complete your change request without issues.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Change success score

Use team historical data for insights into team performance. The score value helps you to determine how likely the team is to complete your change request without issues.

**Note:** The change success score feature is installed after you activate the Change Management - change success score plugin available with the ITSM Professional subscription only. Contact your account manager for more information.

The change success score can help you evaluate a team's success in handling prior change requests.

![Change success score card](../image/change-success-score-card.png)

When the Change Management - Change success score plugin is activated, a **Change success score metrics \(Daily\)** performance analytic \(PA\) job is added. The PA job is a daily job that collects the first set of change success scores until the next job run time that is 02.00 UTC. After the first job run, a **Change Success Score** card ![Change Success Score icon](../image/change-score-card-icon.png) icon appears next to the **Assignment group** field on the change request form. On a click of this icon, you can view the score card details of the assignment group.

## Change Success Score dashboard

Use the data on this dashboard to see trends in the resolution efficiency of a team over time based on the same parameters used to calculate the overall score. To view the trends of all the assignment groups, clear the selected element.

Navigate to **Change** &gt; **Change Analytics** to access the **Change Success Score**, **Change Type Success**, and **Change Model Success** dashboards.

![](../image/change-success-score-db.png)

For more information on the indicators, see [Success score indicators](change-success-score-indicator.md).

## Change Type Success dashboard

This dashboard displays trends in the resolution efficiency for change types. To view the trends of all the change types, clear the selected type.

## Change Model Success dashboard

This dashboard displays trends in the resolution efficiency for the change model over time based on the same parameters used to calculate the overall score. To view the trends of all the change model, clear the selected model.

-   **[Success score indicators](change-success-score-indicator.md)**  
Change Success score uses Performance Analytics indicators for data collection. Indicators define a performance measurement taken at regular intervals of a business service, an activity, or organizational behavior. These performance measurements result in a series of indicator scores over time.
-   **[Success score calculation](change-score-calculation.md)**  
To calculate the success score, formula indicators are provided. These indicators apply the multiplication operation to the data collected by the automated indicators to arrive at the final score.
-   **[Success score rating](change-success-score-rating.md)**  
Based on the change success score rating, a color and text is associated that is displayed as part of the Change Success Score card. By default, four success score ratings are available with a specific score range.

**Parent Topic:**[Configuring Change Management](configure-change-management.md)

