---
title: Normalization of application scores
description: The indicators and their respective weights are used to calculate application score profiles for each configuration item. Use the score profile to calculate application scores and assess the applications. Apply these scores to compare applications and make strategic decisions about which ones to keep, replace, maintain, or invest more in.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Job schedule to compute application scores, Application assessment, Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Normalization of application scores

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

![Sample application scores](../image/ApmSampleBusAppScore.png "Sample application scores")

**Parent Topic:**[Job schedule to compute application scores](job-run-compute-application-scores.md)

