---
title: Normalization of application scores - Legacy
description: The indicators and their respective weights are used to calculate application score profiles for each configuration item. Use the score profile to calculate application scores and assess the applications. Apply these scores to compare applications and make strategic decisions about which ones to keep, replace, maintain, or invest more in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-portfolio-management/application-score-profile.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Job schedule to compute application scores - Legacy, Application assessment - Legacy, Explore- Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Normalization of application scores - Legacy

The indicators and their respective weights are used to calculate application score profiles for each configuration item. Use the score profile to calculate application scores and assess the applications. Apply these scores to compare applications and make strategic decisions about which ones to keep, replace, maintain, or invest more in.

The preconfigured indicators or the indicators that you created retrieve their related data based on the frequency set at the indicator definition stage. This data is captured in the **Application weight** column of the Application Indicator Score \[apm\_app\_indicator\_score\] table. The **Target maximum** and **Target minimum** that are set while creating an application indicator are for calculating the applications normalized value.

**Note:** The **Target maximum** and **Target minimum** are not available when the data source is Assessments.

The normalized value of the application score, which is measured on a scale of 1–10, is derived from the following formula:

```
(Application Weight - Target minimum)/(Target maximum - Target minimum) * 9+1
```

**Note:**

-   If the **Target maximum** and **Target minimum** are not set, then the maximum value within the range of applications is taken as the target maximum value. Similarly, the minimum value within the range of applications is taken as the target minimum value.
-   If the  **Target maximum ** and  **Target minimum ** are set and the **Consider Absolute Values** check box is selected, the entered values are considered.
-   If the **Target maximum ** and  **Target minimum ** are set and the **Consider Absolute Values** check box is cleared, the values are considered based on the following intelligent logic.

    ```
    Target maximum = Minimum value of (Target maximum value defined in the Indicator [apm_metric] table, Maximum value of Application Weights for the fiscal period)
    ```

    For example, consider a scenario where:

    -   The application weights are 10, 20, 30,.…., and 1000.
    -   Value entered in the Target maximum field is 100.
    With these assumptions, the Target maximum value considered is 100, as the defined Target maximum value \(100\) is lesser than the maximum application weight \(1000\).

    ```
    Target minimum = Maximum value of (Target minimum value defined in the Indicator [apm_metric] table, Minimum value of Application Weights for the fiscal period)
    ```

    For example, consider a scenario where:

    -   The application weights are 10, 20, 30,.…., and 1000.
    -   Value entered in the Target minimum field is 100.
    With these assumptions, the Target minimum value considered is 10, as the defined Target minimum value \(100\) is greater than the minimum application weight \(10\).


**Target Maximum and Target Minimum Behavior:**

The absolute target maximum and target minimum values are applied during normalization. The consideration of these values changes based on the Consider Absolute Values check box configuration.

-   **Consider Absolute Values check box is selected:**
    -   When indicator frequency matches the fiscal period being scored: The absolute target maximum and target minimum values defined in the indicator are applied for normalization.
    -   When indicator frequency does not match the fiscal period being scored: The system derives the target minimum and maximum values from the application weights of all indicators in the current scoring run.
-   **Consider Absolute Values check box is cleared:**

    The system applies intelligent logic to determine target maximum and target minimum values. This logic is applied regardless of whether the indicator frequency matches the fiscal period being scored. The following formulas describe how these values are calculated:

    -   Target maximum = Minimum value of \(Target maximum value defined in the Indicator \[apm\_metric\] table, Maximum value of Application Weights for the fiscal period\)
    -   Target minimum = Maximum value of \(Target minimum value defined in the Indicator \[apm\_metric\] table, Minimum value of Application Weights for the fiscal period\)

## Monthly cost indicator scored at different frequencies

An indicator named **Monthly Infrastructure Cost** is configured as follows:

-   Frequency: Monthly
-   **Target maximum**: $50,000
-   **Target minimum**: $10,000
-   Direction: Minimize \(lower cost is better\)

Three applications have the following monthly costs: App A = $12,000, App B = $28,000, App C = $45,000.

**Consider Absolute Values selected, scoring period is Monthly \(frequency matches\):**

The system uses the absolute target values. For App B \($28,000\):

```
normalizedValue = (($28,000 - $10,000) / ($50,000 - $10,000)) * 9 + 1 = 5.05
finalScore (Minimize) = (10 - 5.05) + 1 = 5.95
```

**Consider Absolute Values selected, scoring period is Quarterly \(frequency does not match\):**

The system ignores the absolute target values and derives boundaries from actual application weights: minWeight = $12,000 \(App A\), maxWeight = $45,000 \(App C\). For App B \($28,000\):

```
normalizedValue = (($28,000 - $12,000) / ($45,000 - $12,000)) * 9 + 1 = 5.36
finalScore (Minimize) = (10 - 5.36) + 1 = 5.64
```

**Consider Absolute Values cleared \(any scoring period\):**

The system applies intelligent logic. Target maximum = MIN\($50,000, $45,000\) = $45,000. Target minimum = MAX\($10,000, $12,000\) = $12,000. For App B \($28,000\), the result is the same as the frequency-mismatch scenario above, because the actual application weights fall within the defined target range.

The **Application Weight** that is lesser than or equal to the target minimum is given the lower score, which is 1.

The **Application Weight** that is greater than or equal to the target maximum is given the maximum score, which is 10.

When you set the application indicators, you can also configure the **Direction** as Maximize or Minimize. The application with the maximum value gets the minimum score when the direction is Minimize. The application with the minimum value gets the maximum score when the direction is Maximize.

If the **Direction** in the indicator is **Minimize**:

```
(10 - above calculated Normalized value) + 1
```

Application profile weightage is then applied on the Normalized value to derive the **Indicator Score**:

```
Normalized Value * Weightage as in application score profile %
```

After the indicator score is calculated for each of the indicators, the application score is calculated by summing up all the indicator scores used in the profile.

If the source of the indicator is **Indicators** in the **Data source** field, then the application weight is calculated as the sum of the normalized scores of all its dependent indicators.

**Note:**

-   The normalized score of the parent indicators is then calculated in a similar manner as it is calculated for all the other indicators.
-   The normalized value, indicator score, application weight, target maximum, target minimum, and total weight are all rounded to two decimal places only.

In the figure, since the Cost and Incident indicators are set to minimize, the applications with lower costs and lower number of incidents have higher scores.

\[Omitted image "ApmSampleBusAppScore.png"\] Alt text: Sample application scores

**Parent Topic:**[Job schedule to compute application scores - Legacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-portfolio-management/job-run-compute-application-scores.md)

