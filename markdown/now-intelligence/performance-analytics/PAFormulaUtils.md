---
title: PAFormulaUtils API
description: The PAFormulaUtils API enables you to obtain a value that was calculated in the Analytics Hub and use that value as input for a formula.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Get analytics methods in formulas, Formula indicators, Performance Analytics indicators, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# PAFormulaUtils API

The PAFormulaUtils API enables you to obtain a value that was calculated in the Analytics Hub and use that value as input for a formula.

To use the PAFormulaUtils API, you must satisfy these requirements:

-   Performance Analytics must be enabled.
-   The user who creates the formula indicator that uses this API must have the pa\_power\_user, pa\_admin, or admin roles.

A dollar sign, $, precedes indicator names in PAFormulaUtils parameters, like the Number of open incidents indicator in this example: `pa.getGap($[[Number of open incidents]], score_end);`. This dollar sign means that the Analytics Hub calculated values for the indicator are returned instead of the indicator score.

Date parameters in PAFormulaUtils methods take one of the following forms:

-   An absolute date in YYYY-MM-DD format, such as 2018-12-21.
-   The variable `score_start` or `score_end`. These variables represent the first and last second of the collection period being calculated for the referenced indicator. The times are calculated from the difference between the time zone of the user and the database server time zone, which is GMT. For more information, see [Changes to score\_start/end because of different user time zones](../../concept/time-zones-indicator-formulas.md).
-   A date parameter that you have coded yourself using the GlideDate or the GlideDateTime API.

**Warning:** The PAFormulaUtils API can be used only in formula indicators, not in scripts.

The PAFormulaUtils API contains the following methods:

-   **[getChange\(String indicator, Object fromDate, Object toDate\)](../reference/PAFU-getChange_S_O_O.md)**  
Returns the change in the score of an indicator between two specified dates.
-   **[getChangePercentage\(String indicator, Object fromDate, Object toDate\)](../reference/PAFU-getChangePercentage_S_O_O.md)**  
Returns the percentage of change in the score of an indicator between two specified dates.
-   **[getCurrentAggregateID\(\)](../reference/PAFU-getCurrentAggregateID.md)**  
Returns the time series aggregate identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
-   **[getCurrentBreakdownID\(\)](../reference/PAFU-getCurrentBreakdownID.md)**  
Returns the level 1 breakdown identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
-   **[getCurrentBreakdownLevel2ID\(\)](../reference/PAFU-getCurrentBreakdownLevel2ID.md)**  
Returns the level 2 breakdown identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
-   **[getCurrentElementID\(\)](../reference/PAFU-getCurrentElementID.md)**  
Returns the level 1 breakdown element identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
-   **[getCurrentElementLevel2ID\(\)](../reference/PAFU-getCurrentElementLevel2ID.md)**  
Returns the level 2 breakdown element identifier \(sys\_id\) from the indicator of the current formula. The sys\_id is returned dynamically, as the selection in the Analytics Hub changes.
-   **[getGap\(String indicator, Object onDate\)](../reference/PAFU-getGap_S_O.md)**  
Returns the global target gap for the specified indicator on the specified date.
-   **[getGlobalTarget\(String indicator, Object onDate\)](../reference/PAFU-getGlobalTarget_S_O.md)**  
Returns the global target associated with the specified indicator for the specified date.
-   **[getPersonalTarget\(String indicator, Object onDate\)](../reference/PAFU-getPersonalTarget_S_O.md)**  
Returns the personal target associated with the specified indicator for the specified date.
-   **[getScore\(String indicator, Object onDate\)](../reference/PAFU-getScore_S_O.md)**  
Returns the score of the specified indicator for the specified date.

**Parent Topic:**[Get analytics methods in formulas](../../task/get-indicator-analytics.md)

