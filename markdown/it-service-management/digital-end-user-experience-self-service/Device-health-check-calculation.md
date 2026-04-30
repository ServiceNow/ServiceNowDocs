---
title: Device heath check calculation
description: Learn how the device health is being calculated and marked with Good, Average, or Poor performance indicators.
locale: en-US
release: yokohama
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: reference
last_updated: "2025-04-28"
reading_time_minutes: 2
breadcrumb: [Digital End-user Experience Self-service Reference, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Device heath check calculation

Learn how the device health is being calculated and marked with Good, Average, or Poor performance indicators.

## Calculating Device health check

Each category of the selected device is marked as Good, Average, or Poor by calculating the weighted average of the sub-categories associated with the parent category.

Each sub-category’s performance is marked as Good, Average, or Poor by calculating the weighted average of the performance indicators of device metrics associated with the sub-category.

|Performance Indicators|Weight|Upper bound|Lower bound|
|----------------------|------|-----------|-----------|
|Good|1|1.67|1|
|Average|2|2.33|1.67|
|Poor|5|5|2.33|

-   **Formula used to calculate the sub-category performance indicators**

    `Sub-category performance indicator= (weight of evaluation metrics performance indicator)/total number of evaluation metrics for the subcategory)`

    where,

    -   Evaluation metric performance indicator: Performance indicator \(Good, Average, Poor\) of the evaluation metrics' value as defined in the metric definition table. For more information, see [Customize metric definitions](../../dex-score/task/dexscr-customize-dex-score-metric-defs.md).
    -   Weight: Weight of the performance indicator. After all the sub-categories are marked as Good, Average, and Poor. The performance of the category is calculated by weighted average of sub-categories performance indicator.
-   **Score range definition**

    The following defines the performance range and its corresponding classification:

    -   Good if performance indicator average value lies in range of \(1, 1.67\)
    -   Average performance indicator average value lies in range of \(1.67, 2.33\)
    -   Poor performance indicator average value lies in range of \(2.33, 5\)
-   **Formula used to calculate the parent category performance indicator:**

    `Category performance indicator= (sum of sub-category performance indicator weights)/total number of sub-categories)`

-   **Example**

    Consider the following example for the calculating the performance indicator for **Device performance category** which has the below sub-categories:

    |Sub-category|Metric|Metric value|Sub-category performance metric calculation|Sub-category Performance indicator|
    |------------|------|------------|-------------------------------------------|----------------------------------|
    |Disk Space|Disk Usage|90|Sub-category performance indicator = 5 \(i.e Weight of Poor indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Poor|
    |Battery Health|Battery health|Good|Sub-category performance indicator = 1 \(i.e Weight of Good indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Good|
    |Computer Restart|Device uptime|1|Sub-category performance indicator = 1 \(i.e Weight of Good indicator\) / 1 \(total no. of evaluation metrics for the subcategory\)|Good|

    Performance indicator for Device performance category.

    -   Sub-category performance indicators = Poor, Average, Good
    -   Sum of weight of Sub-category performance indicators: \(5 + 1 + 1\) = 7 Performance indicator = 7 / 3 \(no. Of sub-categories\) = 2.33
    -   Device performance category is Poor \(as 2.33 falls under the Poor range\)

