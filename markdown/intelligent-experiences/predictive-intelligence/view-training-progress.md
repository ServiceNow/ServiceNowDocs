---
title: View solution training progress
description: View your solution training progress or statistics to determine if a solution is available, or how long the next training cycle might take to complete.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# View solution training progress

View your solution training progress or statistics to determine if a solution is available, or how long the next training cycle might take to complete.

## Before you begin

Role required: admin or ml\_admin

## About this task

Solution training involves these steps.

1.  Fetching files for training. The system downloads the training records and sends them to the nearest training service.
2.  Preparing the data. The system removes duplicate records from the training set.
3.  Training the solution. The training service trains the solution.
4.  Uploading the trained solution. The training service uploads the solution as attachment records.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solutions** or **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions**.

2.  In the ML Solutions list, select the solution whose progress or statistics you want to view.

    For example, select **Incident Categorization** to see the training history.

3.  In the **Related Links** section, click **Show training progress**.

    Training times vary based on the number of records and classes within the training set. The more records and classes you use, the longer the training can take. For example, a data set containing 100,000 records and several hundred classes can take around five hours to complete.

    The system shows a Training Progress pop-up window.

    ![Solution training progress pop-up window showing that training succeeded.](../images/solution-training-progress.png)


## What to do next

For classification solutions, see [Review classification solution statistics](review-solution-statistics.md).

For similarity solutions, see [Review similarity solution examples and scores](review-similarity-examples.md).

