---
title: Hardening compliance score trend
description: View the trends of your hardening compliance score over time in a chart or table.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Security hardening, Security configuration console, Security Center, Platform Security]
---

# Hardening compliance score trend

View the trends of your hardening compliance score over time in a chart or table.

See trends in your compliance score over time. Use the date picker to select a time range to analyze to gain insights into the data by applying performance analytics functionality such as targets, thresholds, and KPIs.![hardening compliance score chart UI](../images/hardening-compliance-score-trend.png)

## Compliance score chart

Use the **Chart options** button to specify what information to analyze and how to present the information.

-   **Analysis**

    Select from the list of options. Some options may be unavailable depending on the selected chart type.

    -   **Target**

        Goals your organization wants to achieve. See [Indicator targets](https://www.servicenow.com/docs/access?context=pa-targets&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    -   **Threshold**

        Defines a normal range of scores for an indicator and alert you when a certain event occurs. See [Indicator thresholds](https://www.servicenow.com/docs/access?context=pa-threshold&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    -   **Forecast**

        Describes the ability to forecast future scores based on past behavior. See [Performance Analytics scores forecasts](https://www.servicenow.com/docs/access?context=c_ForecastingData&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

    -   **Trend**

        Shows how the value of one or more items change over time.

    -   **Comments**

        Displays annotations on individual data points.

    -   **Labels**

        Displays scores related to visualizations.

    -   **Statistics**

        Displays statistics related to your compliance score.

-   **Time series**

    Select which metric to display on the chart.

    -   **Score**

        Score for the Key Performance Indicator \(KPI\).

    -   **Change**

        Change of score for this indicator.

    -   **Change percentage**

        Change as a percentage of scores.

-   **Chart type**

    Select a chart type to control how the information your selected is visualized. See [Time series visualization type use cases](https://www.servicenow.com/docs/access?context=time-series-visualization-types&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).


## All Records table

The All Records table displays the date on which the compliance scores were collected, the score percentages, and the number of non-compliant settings. You can use this table as another option to analyze the security posture of your instance over time.

-   **[Increase hardening compliance score](../task/increase-hardening-comp-score.md)**  
Increase your hardening compliance score by ensuring that the hardening settings are compliant with the system's recommendations.

**Parent Topic:**[Security hardening](sc-hardening.md)

