---
title: Configure class recall for a classification solution
description: Create and apply a class recall parameter to an ML solution prior to training its data. For example, you set and apply this solution parameter to 90% recall for all records in the Email class.
locale: en-US
release: zurich
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring advanced settings for your ML solutions, Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Configure class recall for a classification solution

Create and apply a class recall parameter to an ML solution prior to training its data. For example, you set and apply this solution parameter to 90% recall for all records in the Email class.

## Before you begin

**Note:** Using advanced settings in your ML solutions is optional. If you choose to implement any of these settings, make sure you're well informed regarding the technology you're enabling in the solution, and that you have a use case that benefits from what the technology offers.

-   Create and save a classification solution definition or use an existing one.
-   Role required: admin or ml\_admin

## About this task

The class recall solution parameter enables you to steer a solution's training to bias a specific class. For example, classifying an incoming email as a Phish or not can be an important use case in a security-related machine learning solution. In this situation, it's very important to identify every Phish, and it may be acceptable to report a non-Phish as a Phish occasionally. However, no actual Phish should be classified as a non-Phish. In such situations, the recall metric must have a high value to minimize false negatives. High recall values might lead to lower percentages for precision and coverage.

You can apply a recall value to one class per solution definition.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solution Definitions**.

2.  Open a saved classification solution definition form.

    In this example scenario, you use an Incident Categorization solution definition form that you haven't trained yet.

    ![This image shows an example classification solution definition on which you apply the class recall parameter.](../images/configure-class-recall1.png)

3.  On the Advanced Solution Settings tab in the Related Links section of the form, select **New**.

    ![This image shows how to select the Solution Parameters option for creating the parameter.](../images/tf-idf-similarity-solution2.png)

4.  Create a parameter record.

    1.  In the **Solution Parameters** field, select the search icon.

    2.  In the ML Solution Parameters screen, select **Add class recall value while training**.

        ![How to create the parameter record by selecting a Search value, and then selecting the Class-Recall key Short Description.](../images/configure-class-recall2a.png)

    The Advanced Solution Setting \[ml\_advanced\_solution\_settings\] record appears.

    ![This image shows the Advanced Solution Setting record for Class Recall.](../images/configure-class-recall3.png)

5.  Add your values to the **User inputs** field, in the format `ClassName:RecallValue`.

    1.  Enter the name of the class for which you want to specify a recall value.

        In this scenario, you enter `Phish` for the **ClassName**.

    2.  Enter a colon character \(:\), then the Recall value.

        Enter `95` for the **RecallValue** in the example scenario.

    In other words you're specifying Phish as the target class, and 95 is the Recall percentage you're requesting the system to deliver during solution training \(`Phish:95`\).

    ![How to configure the User inputs field, where Phish is the target class, and 95% is the Recall percentage you're asking the system to deliver during solution training.](../images/configure-class-recall4.png)

6.  Select **Submit**.

    **Result:** Class recall is configured for your classification solution. Its solution parameter appears on the Advanced Solution Settings tab of your classification solution definition form.

    ![When you submit the record you created, the solution parameter for class recall appears on your solution definition form.](../images/configure-class-recall-result.png)


## What to do next

Train your saved classification solution so that your updates are incorporated.

**Related topics**  


[Create and train a classification solution](create-solution-definition.md)

[Configuring target metrics for a trained classification solution](../concept/configuring-target-metrics-trained-classification-solution.md)

[Configure TF-IDF for solutions](configure-tf-idf-classification-similarity.md)

