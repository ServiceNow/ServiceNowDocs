---
title: Reviewing your ML solution training jobs
description: Use the ML Solutions \(ML Training Jobs view\) module to monitor the training status and progress for Predictive Intelligence solutions. The module displays training jobs for both user interface and API solutions.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Reviewing your ML solution training jobs

Use the ML Solutions \(ML Training Jobs view\) module to monitor the training status and progress for Predictive Intelligence solutions. The module displays training jobs for both user interface and API solutions.

## Background and usage

When you submit an ML solution or ML solution definition for training, it goes to a ServiceNow data center for processing to predict and deliver a data outcome. Depending on the solution size, the training can take hours or sometimes days to complete. The ML Training Jobs view helps you stay on top of all in-progress and completed ML solution training jobs in your instance.

To access this view, you use the admin or ml\_admin role and the following navigation path: **Predictive Intelligence** &gt; **Training Jobs**.

**Note:** The ML scheduler limits the number of trainings an instance can commit to 50 new ML training requests per instance within a 24 hour window. This excludes scheduled re-training requests. In addition, clustering and similarity updates are also excluded from this limit, even if the new training requests exceed 50 within a 24 hour window.

## ML Training Jobs view summary

The view shows all ML training jobs grouped by the four Predictive Intelligence capability frameworks: classification, similarity, clustering, and regression.

Each record displays values such as solution name, version, training state, and training completion percentage.

If you don't have any training jobs for a particular capability, the list doesn't display a group for that capability. For example, in this scenario, there is no group for regression because you don't have any regression solutions that you've submitted for training yet.

![How to navigate to the MLTraining Jobs view.](../images/reviewing-ml-solutions-training-jobs1.png)

Select the Solution Name to see the details of the ML solution, as demonstrated in the images below.

![Select the name of an ML solution to open its detailed record.](../images/reviewing-ml-solutions-training-jobs2.png)

![The ML solution form with details. The Solution Name highlighted here is the same as the one you selected in the previous image.](../images/reviewing-ml-solutions-training-jobs3.png)

