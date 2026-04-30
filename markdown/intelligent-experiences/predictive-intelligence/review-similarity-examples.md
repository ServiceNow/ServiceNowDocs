---
title: Review solution similarity examples
description: Review the similarity examples and scores generated during solution training to determine if the similarity score threshold is sufficient.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [View solution training progress, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Review solution similarity examples

Review the similarity examples and scores generated during solution training to determine if the similarity score threshold is sufficient.

## Before you begin

-   Train a similarity solution
-   Role required: admin or ml\_admin

## About this task

Solution training generates paired data record examples with a percentile score that represents the degree of similarity between the two records. The higher the score, the higher the similarity. A score of 100 indicates identical records and a score of 0 indicates dissimilar records.

The solution only returns similarity results that have a score that's higher than the threshold.

**Note:** The similarity filters specified in the solution definition aren't applied for similarity examples and are only applied during prediction.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, locate your solution and click the Reference Lookup icon.

    ![Lookup icon](../../../common/image/Form_ReferenceLookupIcon.png)

3.  Click **Open Record**.

4.  In the Related Links section, click **Similarity Examples**.

5.  Review the similarity examples and their threshold scores to determine the accuracy and coverage levels you want applied to your solution similarity results.

    The higher the similarity score, the more precise it is and the less coverage it offers. The lower the similarity score, the more coverage it has and the less precision it offers.

6.  Based on your review, determine whether to increase or decrease the similarity score threshold value for your similarity solution.


## What to do next

If you decide to adjust the score for your similarity solution, [update its similarity solution threshold](update-similarity-threshold.md).

