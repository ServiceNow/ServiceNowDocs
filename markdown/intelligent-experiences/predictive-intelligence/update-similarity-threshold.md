---
title: Update your similarity score threshold
description: After you review the similarity examples provided by the system, update your solution similarity score threshold if you want the results returned by the solution to be more or less similar.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create and train a similarity solution, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Update your similarity score threshold

After you review the similarity examples provided by the system, update your solution similarity score threshold if you want the results returned by the solution to be more or less similar.

## Before you begin

-   Review the Similarity Score Threshold values for your similarity examples.
-   Role required: admin or ml\_admin

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, locate your solution and click the Reference Lookup icon \(i\).

3.  Click **Open Record**.

4.  In the Solution Statistics section, enter a new numerical value that represents a percentage in the **Similarity Score Threshold** field.

    For example, imagine that the current score is 80. In your similarity example review you decided to increase the accuracy of your similarity recommendations at the cost of lowering the prediction coverage. So you update the field by entering the higher score of 90.

5.  In the Context Menu, click **Save**.

    Your solution uses the new threshold value that you assigned to it and returns similar results that have a score higher than 90. If you set the score to 90, the degree of similarity in your word corpus is accurate at least 91% of the time.


