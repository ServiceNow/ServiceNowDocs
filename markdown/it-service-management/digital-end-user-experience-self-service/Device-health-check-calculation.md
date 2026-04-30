---
title: Device heath check calculation
description: Device health calculation and categorization of performance as Good, Average, or Poor.
locale: en-US
release: zurich
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Employee Self-service, Digital End-User Experience, IT Service Management]
---

# Device heath check calculation

Device health calculation and categorization of performance as Good, Average, or Poor.

## Calculating device health and performance

Performance for each device health category is classified as Good, Average, or Poor by calculating the weighted average of performance indicators from its associated subcategories.

Performance for each subcategory of a device health category is classified as Good, Average, or Poor by calculating the weighted average of performance indicators from associated device metrics.

|Performance Indicators|Weight|Upper bound|Lower bound|
|----------------------|------|-----------|-----------|
|Good|1|1.67|1|
|Average|2|2.33|1.67|
|Poor|5|5|2.33|

-   **Formula used to calculate the subcategory performance indicators**

    `Sub-category performance indicator= (weight of evaluation metrics performance indicator)/total number of evaluation metrics for the subcategory)`

    where,

    -   Evaluation metric performance indicator: Performance indicator \(Good, Average, Poor\) of the evaluation metrics' value as defined in the metric definition table. For more information, see [Customize metric definitions](../../dex-score/task/dexscr-customize-dex-score-metric-defs.md).
    -   Weight: Weight of the performance indicator. After all the subcategories are marked as Good, Average, and Poor. The performance of the category is calculated by the weighted average of subcategories performance indicator.
-   **Score range definition**

    The following defines the performance range and its corresponding classification:

    -   Good if the performance indicator average value lies in the range of \(1, 1.67\)
    -   Average performance indicator average value lies in the range of \(1.67, 2.33\)
    -   Poor performance indicator average value lies in the range of \(2.33, 5\)
-   **Formula used to calculate the parent category performance indicator:**

    `Category performance indicator= (sum of sub-category performance indicator weights)/total number of sub-categories)`

-   **Example**

    Consider the following example for the calculating the performance indicator for **Device performance category** that has the following subcategories:

    |Subcategory|Metric|Metric value|Subcategory performance metric calculation|Subcategory Performance indicator|
    |-----------|------|------------|------------------------------------------|---------------------------------|
    |Disk Space|Disk Usage|90|Subcategory performance indicator = 5 \(Weight of Poor indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Poor|
    |Battery Health|Battery health|Good|Subcategory performance indicator = 1 \(Weight of Good indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Good|
    |Computer Restart|Device uptime|1|Subcategory performance indicator = 1 \(Weight of Good indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Good|

    Performance indicator for Device performance category.

    -   Subcategory performance indicators = Poor, Average, Good
    -   Sum of weight of subcategory performance indicators: \(5 + 1 + 1\) = 7 Performance indicator = 7 / 3 \(no. Of subcategories\) = 2.33
    -   The device performance category is Poor \(as 2.33 falls under the Poor range\)

