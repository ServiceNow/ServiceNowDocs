---
title: Update your similarity score threshold
description: After you review the similarity examples provided by the system, update your solution similarity score threshold if you want the results returned by the solution to be more or less similar.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and train a similarity solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Update your similarity score threshold

After you review the similarity examples provided by the system, update your solution similarity score threshold if you want the results returned by the solution to be more or less similar.

## Before you begin

-   Review your similarity examples and their scores. For more information see [Review solution similarity examples](review-similarity-examples.md).
-   Role required: ml\_admin or admin

## About this task

A deployed solution returns records only when the similarity score is higher than the **Similarity Score Threshold** value:

-   The higher the threshold value, the higher the precision and the lower the coverage.
-   The lower the threshold value, the lower the precision and the higher the coverage.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, locate your solution by filtering for the Solution Name, and open its active version.

3.  On the solution form, locate and open the **Solution Statistics** tab.

4.  In the **Similarity Score Threshold** field, enter a new numerical value that represents a percentage.

    For example, imagine that the current threshold is 80. In your similarity example review you decided to increase the accuracy of your similarity recommendations at the cost of lowering the prediction coverage. So you update the field by entering the higher value of 90.

5.  In the form's context menu \(Additional actions\), select **Save**.

    Your solution uses the new threshold value that you assigned to it and returns similar results that have a score higher than 90. If you set the threshold to 90, the similarity score must be 91% or above to return records.


