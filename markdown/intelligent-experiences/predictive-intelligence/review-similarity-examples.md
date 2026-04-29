---
title: Review solution similarity examples
description: Review the similarity examples generated during solution training to determine whether the similarity score threshold meets your business requirements.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View solution training progress, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Review solution similarity examples

Review the similarity examples generated during solution training to determine whether the similarity score threshold meets your business requirements.

## Before you begin

-   Train a similarity solution
-   Role required: ml\_admin or admin

## About this task

Solution training generates a set of paired record examples. Each pair includes a percentile score that estimates the degree of similarity between the two records. The higher the score, the higher the similarity, as follows:

-   A score of 100 indicates identical records.
-   A score of 0 indicates dissimilar records.

A deployed solution returns records only when the score is higher than the **Similarity Score Threshold** value:

-   The higher the threshold value, the higher the precision and the lower the coverage.
-   The lower the threshold value, the lower the precision and the higher the coverage.

On domain-separated instances, the following procedure displays records from all domains to ML admins. However, when solutions are applied in your forms and flows, similarity predictions are domain-aware. Examples from other domains on the instance are not displayed to users.

**Note:** The similarity filters specified in the solution definition aren't applied for similarity examples and are applied only during prediction.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, locate your solution by filtering for the Solution Name, and open the active version.

3.  In the Related Links section of the form, select **Similarity Examples**.

    A list of paired records opens on the Similarity Examples \(ml\_similarity\_example\) table. By default the rows are sorted by the **Similarity Score** column in descending order.

4.  Review the similarity examples for accuracy and coverage.

    Based on your review, determine whether to increase or decrease the Similarity Score Threshold value of your solution.


## What to do next

If you decide to adjust the Similarity Score Threshold for your similarity solution, see [update its similarity solution threshold](update-similarity-threshold.md).

