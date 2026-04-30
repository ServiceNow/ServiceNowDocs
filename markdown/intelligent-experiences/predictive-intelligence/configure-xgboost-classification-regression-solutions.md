---
title: Configure XGBoost for classification or regression solutions
description: Apply XGBoost encoding to optimize the training for your classification or regression solutions.
locale: en-US
release: yokohama
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-01-16"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure XGBoost for classification or regression solutions

Apply XGBoost encoding to optimize the training for your classification or regression solutions.

## Before you begin

-   Create a classification solution definition or use an existing one.
-   Create a regression solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

XGBoost is an optional gradient boosting framework that uses multiple decision trees and supports both Paragraph Vector-based text and TF-IDF distance-based text. LogR is the default distance-based model algorithm.

Configuring advanced settings on your ML solutions is optional. If you choose to configure any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that you have a use case that benefits from what the technology offers.

In this example scenario, you apply XGBoost to both a classification solution and a regression solution.

**Note:** The regression framework is deprecated in the Yokohama release. You can continue to use existing regression solutions but you can't create new ones.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open a classification solution definition form.

3.  On the Advanced Solution Settings tab in the Related Links section of the form, select **New**.

    ![This image shows how to select the Solution Parameters option for creating the parameter.](../images/tf-idf-similarity-solution2.png)

4.  Create a parameter record.

    1.  In the **Solution Parameters** field, select the search icon.

    2.  In the ML Solution Parameters screen, select **Use XGBoost algo for classification model training**.

    ![How to create the parameter record by selecting the Search button, and then selecting the XGBoost key Short Description.](../images/config-xgboost-classification-or-regression1.png)

5.  Select **Submit**.

    The Advanced Solution Setting record screen refreshes.

    ![This image shows the new Advanced Solution Setting record you created.](../images/config-xgboost-classification-or-regression2.png)

6.  Select **Submit**.

    **Result:** XGBoost is configured for your classification solution. Its solution parameter appears on the Advanced Solution Settings tab of your classification definition form.

    ![The Advanced Solution Setting parameter for XGBoost as configured on your classification solution definition form.](../images/config-xgboost-classification-or-regression3.png)

    **Note:** Follow the steps below if you want to configure XGBoost on a regression solution.

7.  Navigate to **Predictive Intelligence** &gt; **Regression** &gt; **Solution Definitions** \(available only if you had created a regression solution before the regression framework was deprecated\).

8.  In this second scenario, you open a regression solution definition form.

9.  Repeat the steps from the previous classification solution example, except this time you're using a regression solution.

10. Select **Submit**.

    **Result:**

    XGBoost is configured for your regression solution. Its solution parameter appears on the Advanced Solution Settings tab of your regression solution definition form.


**Related topics**  


[Create and train a classification solution](create-solution-definition.md)

[Create and train a regression solution](create-regression-solution.md)

