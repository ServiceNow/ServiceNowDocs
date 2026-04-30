---
title: Configure class recall for a classification solution
description: Create and apply a class recall parameter to an ML solution prior to training its data. For example, you set and apply this solution parameter to 90% accuracy for all records you train in the Email class.
locale: en-US
release: xanadu
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure class recall for a classification solution

Create and apply a class recall parameter to an ML solution prior to training its data. For example, you set and apply this solution parameter to 90% accuracy for all records you train in the Email class.

## Before you begin

**Note:** Configuring advanced settings on your ML solutions is optional. If you choose to configure any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that you have a use case that benefits from what the technology offers.

-   Create and save a classification solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

The class recall solution parameter enables you to steer a solution's training to bias a specific class. For example, classifying an incoming email as a Phish or not can be an important use case in a security-related machine learning solution. In this situation, it's very important to identify every Phish, and it may be okay to report a non-Phish as a Phish occasionally. However, no real Phish should be classified as a non-Phish. In such situations, the recall metric must have a high value, which might lead to lower percentages for precision and coverage.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open a saved classification solution definition form.

    In this example scenario, you use an Incident Categorization solution definition form that you haven't trained yet.

    ![This image shows an example classification solution definition on which you apply the class recall parameter.](../images/configure-class-recall1.png)

3.  On the Advanced Solution Settings tab in the Related Links section of the form, click **New**.

    ![This image shows how to select the Solution Parameters option for creating the parameter.](../images/tf-idf-similarity-solution2.png)

4.  Create a parameter record.

    1.  In the **Solution Parameters** field, click the search icon.

    2.  In the ML Solution Parameters screen, select **Add class recall value while training**.

        ![How to create the parameter record by selecting a Search value, and then selecting the Class-Recall key Short Description.](../images/configure-class-recall2a.png)

5.  Click **Submit**.

    The Advanced Solution Setting record appears.

    ![This image shows the Advanced Solution Setting record for Class Recall.](../images/configure-class-recall3.png)

6.  Configure the **User inputs** field.

    1.  Enter the class name on which you want to track the Recall value.

        In this scenario, you enter `Phish` for the **ClassName**.

    2.  Enter the Recall value.

        Enter `90` for the **RecallValue**.

    Here you're specifying Phishas the target class, and 95 is the recall percentage you're requesting the system to deliver during solution training.

    ![How to configure the User inputs field, where Spam is the target class, and 90% is the prediction accuracy you're asking the system to deliver during solution training.](../images/configure-class-recall4.png)

7.  Click **Submit**.

    **Result:** Class recall is configured for your classification solution. Its solution parameter appears on the Advanced Solution Settings tab of your classification solution definition form.

    ![When you submit the record you created, the class recall solution parameter appears on your clustering solution definition form.](../images/configure-class-recall-result.png)


## What to do next

Train your saved classification solution.

**Related topics**  


[Create and train a classification solution](create-solution-definition.md)

[Configuring target metrics for a trained classification solution](../concept/configuring-target-metrics-trained-classification-solution.md)

[Configure TF-IDF for solutions](configure-tf-idf-classification-similarity.md)

