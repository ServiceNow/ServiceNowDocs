---
title: Success score calculation
description: To calculate the success score, formula indicators are provided. These indicators apply the multiplication operation to the data collected by the automated indicators to arrive at the final score.
locale: en-US
release: yokohama
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Change success score, Configure, Change Management, IT Service Management]
---

# Success score calculation

To calculate the success score, formula indicators are provided. These indicators apply the multiplication operation to the data collected by the automated indicators to arrive at the final score.

You can view the Change success score formula indicators in Performance Analytics under the indicator group **Change success score - multipliers**.

Review the following table to understand the default multipliers used in success score calculation.

|Automated indicator|Multiplier applied by formula indicator|
|-------------------|---------------------------------------|
|Successful changes|3|
|Successful changes with issues|-2|
|Unsuccessful changes|-5|
|P1 incident caused by change|-10|
|P2 incident caused by change|-5|
|P3 incident caused by change|-2|

-   **[Modify score calculation](../reference/modify-success-score-calculations.md)**  
Modify the multiplier values in the formula indicators to calculate the final success score.

**Parent Topic:**[Change success score](change-success-score.md)

