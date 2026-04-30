---
title: Create an analysis
description: Create analyses to model different outcomes based on specific interventions or changes. You can generate forecasts for each analysis and use that information to compare the different outcomes and better understand the impact of potential interventions.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up analysis contexts and analyses, Using ESG Management, Environmental, Social, and Governance Management]
---

# Create an analysis

Create analyses to model different outcomes based on specific interventions or changes. You can generate forecasts for each analysis and use that information to compare the different outcomes and better understand the impact of potential interventions.

## Before you begin

Role required: sn\_esg.program\_manager

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Lists** &gt; **Analysis contexts**.

2.  Select an analysis context record that you want and navigate to the **Analysis** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_lrv_yw4_brb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name for the analysis. For example, `Best case`.

</td></tr><tr><td>

Forecast Method

</td><td>

Method used to generate forecasting data.-   Auto

By default, the instance chooses the best method for you automatically, based on the fit of the method. For more information, see [Automatic selection of forecast methods](https://www.servicenow.com/docs/access?context=configure-forecast-ts-viz&version=xanadu&pubname=xanadu-now-intelligence&section=automatic-vs-manual-forecast-methods&ft:locale=en-US).

-   Linear

Generates a linear regression forecast based on the historical scores, using constant and trend as explanatory variables.

-   Seasonal

Generates a linear regression forecast based on the historical scores, using seasonal dummies as explanatory variables. A 'season' for this analysis is one period.

-   Seasonal Trend

As Seasonal, but includes a trend as an explanatory variable.

-   Seasonal Trend Loess \(STL\)

Generates a seasonal forecast based on a best-fit function. This method fits a trend, a season, and a random noise process to the data using an exponentially weighted moving average approach. The forecast is based on the full data set, with more weight given to more recent observationsA 'season' for this analysis is one period.

-   Random Forest \(RF\)

Creates a combination of decision trees where the predictions produced by these trees are averaged to get a single prediction. The randomness comes from each tree being built from a random subset of the available data and inputs.

-   Autoregressive \(AR\)

The autoregressive \(AR\) model forecasts future values of an indicator by using a linear combination of a trend, seasonal dummies, and past values. Like the Random Forest \(RF\) model, the AR model checks for the best number of lags. However, the AR model relates current to past values linearly, whereas the RF model is non-linear.

For more information, see [Forecast methods](https://www.servicenow.com/docs/access?context=configure-forecast-ts-viz&version=xanadu&pubname=xanadu-now-intelligence&section=forecast-methods-dv&ft:locale=en-US).

</td></tr><tr><td>

State

</td><td>

State of the analysis record.-   Draft
-   In progress
-   Published


</td></tr><tr><td>

Description

</td><td>

Description of the analysis.

</td></tr></tbody>
</table>5.  Select save.

6.  Navigate to the **Emission factor analysis** tab.

    This tab is only available if a formula associated with the analysis uses an emission factor.

    1.  Enter the location in the **Emission factor location** field.

    2.  Select **Save**.

    This step is only required if a formula associated with the analysis uses an emission factor.

7.  Select **Forecast**.

    Your analysis record has been created. A Forecast tab has been added where you can view the generated standard forecast.


## What to do next

Adjust parameters to model different outcomes based on specific interventions or changes. For more information, see [Adjust parameters](create-a-forecast-intervention.md).

**Parent Topic:**[Set up analysis contexts and analyses](../concept/set-up-scenarios.md)

