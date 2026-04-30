---
title: Creating and training solutions
description: Use one of the Predictive Intelligence \(PI\) frameworks to create and train machine-learning solutions. Each framework delivers a different solution type for training the system to predict, recommend, and organize data outcomes.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: concept
last_updated: "2026-03-27"
reading_time_minutes: 3
breadcrumb: [Predictive Intelligence, Enable AI experiences]
---

# Creating and training solutions

Use one of the Predictive Intelligence \(PI\) frameworks to create and train machine-learning solutions. Each framework delivers a different solution type for training the system to predict, recommend, and organize data outcomes.

## Types of solutions

The three PI frameworks provide different solutions that can be invoked by any application through a prediction API to make a prediction. Create and train your own solutions using your previous data. Navigate to **All** &gt; **Predictive Intelligence** &gt; **Homepage** to view and create solutions.

Select the best framework for your desired prediction:

-   Classification solutions:

    Sets field values during record creation to automatically categorize and route work based on past records. See [Create and train a classification solution](../task/create-solution-definition.md).

-   Similarity solutions:

    Identifies similarities between new and existing records to recommend resolutions. See [Create and train a similarity solution](../task/create-similarity-solution.md).

-   Clustering solutions:

    Groups similar records into clusters to identify patterns and major incidents. See [Create and train a clustering solution](../task/create-clustering-solution.md).

-   Regression solutions:

    **Note:** From the Washington DC release, support for creating new regression solutions was removed. You can still edit and train existing regression solutions, but you won't be able to initiate new ones.

    Uses historic data to predict numeric outputs, such as estimating the time it takes to resolve an incident or case. See [Create and train a regression solution](../task/create-regression-solution.md).


## Selecting data records for training your solution

A solution is only as good as the record data you use to train it. In general, a good training dataset has these characteristics.

-   The solution definition input fields are available to users when creating records. To make predictions at record creation, the solution must have the input field values at record creation.
-   The solution definition output field is a choice field. To make more accurate predictions, limit the output field to a finite set of possible values.
-   The training records only contain correct values for the output field. To make more accurate predictions, filter out any records that have unreliable output field values. For example, if recently closed incidents are subject to review and change for a month, filter out any recently closed incidents.
-   The training records contain multiple examples of each output field value that you want the solution to predict. To provide more record coverage, include multiple examples of each output field value.
-   The training records include common variations of the input fields. To provide more record coverage, include multiple examples of input field values.

## Exporting your solution for training

To train a solution, you export its solution definition and associated records to a centralized training server within the same datacenter. When the training completes, the training server exports the solution back to your instance and deletes all of your training data from the server. Each datacenter has its own dedicated training server and the data doesn't leave the datacenter. Confirm that your configuration aligns with your compliance requirements.

Predictions occur on a centralized prediction server within the same datacenter as the instance. The trained model artifacts are sent from the instance server to the prediction server when the prediction is invoked for the first time. After that, the trained model artifacts are cached on the prediction server for subsequent predictions.

**Note:** All communication between the instance and the training service occurs within the same datacenter firewall. Even so, all communications occur over HTTPS.

## Solution training troubleshooting

For troubleshooting common training issues, see the [Predictive Intelligence Common issues \[KB781893\]](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0781893) article in the Now Support Knowledge Base.

