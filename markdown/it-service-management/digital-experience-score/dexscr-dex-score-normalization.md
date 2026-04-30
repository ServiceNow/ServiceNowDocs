---
title: DEX Score normalization for metric scores
description: Learn how normalization adjusts individual scores of each metric to a common scale, enabling comparison across different metrics.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Digital Experience Score​ reference, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# DEX Score normalization for metric scores

Learn how normalization adjusts individual scores of each metric to a common scale, enabling comparison across different metrics.

In Digital Experience Score​, the key metrics monitored from applications and devices are normalized by mapping the Good, Average, or Poor range of the actual metric value to the corresponding Good, Average, or Poor range definition on a scale of 100.

Normalization of metric values is done in two ways: One to maximize values and the other to minimize values.

<table id="table_pwr_jh4_zdc"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

To maximize the value

</td><td>

Maximize the value when higher values are better, for example, metric for WiFi reception rate. The following formula is used to get the normalized score:

 `Normalized value (Maximize) = L1 + ((M1 - L2) / (H2 - L2) x (H1 - L1))`

</td></tr><tr><td>

To minimize the value

</td><td>

Minimize the value when lower values are better, for example, metric for CPU usage. The following formula is used to get the normalized score:

 `Normalized value (Minimize) = H1 - ((M1 - L2) / (H2 - L2) x (H1 - L1))`

</td></tr></tbody>
</table>Where,

-   L1 = Low value of mapping range
-   H1 = High value of mapping range
-   M1 = Actual metric value
-   L2 = Low value of metric value range
-   H2 = High value of metric value range

You can customize the lower bound values for Good, Average, and Poor ranges. For more information, see [Customize metric definitions](../task/dexscr-customize-dex-score-metric-defs.md)

-   **Example for an application metric normalization \(maximize\)**

    Consider the following values for the metric WiFi reception rate:

    -   Actual metric value \(M1\): 400 \(falls in good range\) 
    -   Mapping range for good \(L1 and H1\): 75–100
    -   Metric value range for average \(L2 and H2\): 50–500 
    Then the application health metrics score is calculated as:

    Normalized value \(Maximize\) = `75 + ((400 - 50) / (500 - 50) x (100 - 75))` = 94 \(rounded off\).

-   **Example for a device metric normalization \(minimize\)**

    Consider the following values for the metric CPU Usage:

    -   Actual metric value: 79 \(falls in average range\)
    -   Mapping range for good \(L1 and H1\): 65–74
    -   Metric value range for average \(L2 and H2\): 55–84 
    Then the device health metrics score is calculated as:

    Normalized value \(Minimize\) = `74 - ((79 - 55) / (84 - 55) x (74 - 65))` = 66 \(rounded off\).


**Parent Topic:**[Digital Experience Score​ reference](../concept/dexscr-dex-score-reference.md)

**Related topics**  


[Define qualitative mapping for a DEX Score metric](../task/dexscr-define-qlty-metric-score-mapping.md)

[Metric scores in Digital Experience Score​](../concept/dexscr-dex-score-defs.md)

[DEX Score metrics calculation](dexscr-dex-score-metrics-calc.md)

