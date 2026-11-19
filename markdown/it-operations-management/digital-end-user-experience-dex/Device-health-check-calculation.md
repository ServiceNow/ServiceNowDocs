---
title: Device heath check calculation
description: Device health checks classify the performance of each device health category and subcategory as Good, Average, or Poor based on weighted averages of performance indicators.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/digital-end-user-experience-dex/Device-health-check-calculation.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [DEX Self-service reference, Reference, Digital End-User Experience, IT Operations Management]
---

# Device heath check calculation

Device health checks classify the performance of each device health category and subcategory as Good, Average, or Poor based on weighted averages of performance indicators.

## Calculating device health and performance

The performance of each device health category is classified as Good, Average, or Poor based on the weighted average of performance indicators from its associated subcategories.

The performance of each subcategory is classified as Good, Average, or Poor based on the weighted average of performance indicators from associated device metrics.

|Performance indicators|Weight|Upper bound|Lower bound|
|----------------------|------|-----------|-----------|
|Good|1|1.67|1|
|Average|2|2.33|1.67|
|Poor|5|5|2.33|

-   **Formula used to calculate the subcategory performance indicators**

    `Sub-category performance indicator= (weight of evaluation metrics performance indicator)/total number of evaluation metrics for the subcategory)`

    where,

    -   Evaluation metric performance indicator: Performance indicator \(Good, Average, Poor\) of the evaluation metrics' value as defined in the metric definition table. For details on metric definitions, see [Customize metric definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/digital-end-user-experience-dex/dexscr-customize-dex-score-metric-defs.md).
    -   Weight: Weight of the performance indicator. After all the subcategories are marked as Good, Average, and Poor. The performance of the category is calculated by the weighted average of subcategories performance indicator.
-   **Score range definition**

    The following defines the performance range and its corresponding classification:

    -   Good: Performance indicator average value in the range of \(1, 1.67\)
    -   Average: Performance indicator average value in the range of \(1.67, 2.33\)
    -   Poor: Performance indicator average value in the range of \(2.33, 5\)
-   **Formula used to calculate the parent category performance indicator:**

    `Category performance indicator= (sum of sub-category performance indicator weights)/total number of sub-categories)`

-   **Example**

    Consider the following example of calculating the performance indicator for the Device performance category, which has the following subcategories:

    |Subcategory|Metric|Metric value|Subcategory performance metric calculation|Subcategory performance indicator|
    |-----------|------|------------|------------------------------------------|---------------------------------|
    |Disk Space|Disk Usage|90|Subcategory performance indicator = 5 \(Weight of Poor indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Poor|
    |Battery Health|Battery health|Good|Subcategory performance indicator = 1 \(Weight of Good indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Good|
    |Computer Restart|Device uptime|1|Subcategory performance indicator = 1 \(Weight of Good indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Good|

    Performance indicator for Device performance category.

    -   Subcategory performance indicators = Poor, Average, Good
    -   Sum of weight of subcategory performance indicators: \(5 + 1 + 1\) = 7 Performance indicator = 7 / 3 \(number of subcategories\) = 2.33
    -   The device performance category is Poor \(because 2.33 falls in the Poor range\)

