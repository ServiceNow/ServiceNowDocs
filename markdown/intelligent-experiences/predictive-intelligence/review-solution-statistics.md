---
title: Review classification solution statistics
description: The Solution Statistics dashboard in Predictive Intelligence has been deprecated in the Xanadu release. It provided precision and coverage statistics for each class in a classification solution.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [View solution training progress, Creating and training solutions, Predictive Intelligence, Enable AI experiences]
---

# Review classification solution statistics

The Solution Statistics dashboard in Predictive Intelligence has been deprecated in the Xanadu release. It provided precision and coverage statistics for each class in a classification solution.

## Before you begin

-   Role required: admin, ml\_admin, or ml\_report\_user

## About this task

**Important:** With the Xanadu release, the Solution Statistics dashboard is deprecated. Upgrading customers can continue to use their existing Solutions Statistics dashboards from the application menu. For new customers onboarding with the Xanadu release, the Solutions Statistics dashboard is not available. The following information is provided for legacy context.

The Solution Statistics dashboard lists the precision, coverage, and distribution for each class of active solutions. The system uses the classes with the highest number of records when it builds a solution. The number of classes predicted may be less than 50, and may skip a class if there is not enough historical data to build a solution that can predict the class confidently.

The Solution Statistics dashboard is different from the Solution Statistics tab in an ML Solution record. For more information, see [Create and train a classification solution](create-solution-definition.md).

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Statistics**.

2.  From **Filter by solution**, select the solution whose statistics you want to review.

3.  From **Filter by version**, select the solution version whose statistics you want to review.

4.  Click **Apply.**

    The system updates the dashboard based on the filters selected.

    ![Bar graph of classification solution statistics](../images/solution-statistics-example-madrid.png)

5.  Identify classes with unwanted combinations of precision, coverage, and distribution values.

    For example, identify classes that have low precision or coverage but a high distribution.

6.  Identify any missing classes you want the model to include.

    For example, identify any missing incident categories from the Incident classification solution.


## What to do next

If you're satisfied with the solution you've reviewed, the latest version is already active and ready to use. If you're not satisfied, you can choose a different version of the solution and make it active. You can also tune and retune the solution by configuring the class precision and coverage to use acceptable values.

