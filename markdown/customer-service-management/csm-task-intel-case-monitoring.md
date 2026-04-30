---
title: View Task Intelligence Analytics
description: View the Task Intelligence for CSM Analytics dashboard to monitor the model performance over time, track the business value, and see what predictions your agents did or didn't use.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Use Task Intelligence for Customer Service, Automate and optimize, Using Customer Service Management, Customer Service Management]
---

# View Task Intelligence Analytics

View the Task Intelligence for CSM Analytics dashboard to monitor the model performance over time, track the business value, and see what predictions your agents did or didn't use.

The dashboard uses visual representations to provide you with an overview of how each model is performing. You can see the number of predictions from each model and the overall mean time that it takes to resolve the cases in your organization.

The following example shows the Get an overview and See how your trained model is doing sections within the dashboard.

![View the analytics dashboard and monitor machine learning models. For the text description, see the following sections.](../image/task-intelligence-analytics.png "Task Intelligence Analytics dashboard")

## Get an overview

The dashboard contains visual representations that provide you with the business value of the model.

-   **Number of predictions**

    The line graph shows the number of correct predictions that agents have accepted over time for all the categorization models combined. If the sentiment and language models are activated, the correct predictions for those models are shown as well. As the model continues to learn, it can increase the number of predictions that agents accept.

-   **Mean time to resolve \(MTTR\)**

    The line graph shows the average amount of time that it takes to resolve cases over time. As the model makes more predictions, the MTTR should decrease as the predictions help your agents.


The Task Intelligence Analytics page includes the following data about the predicted fields and how they impact your business:

-   The number of predicted fields.
-   The number of predictions that agents used.
-   The number of predictions that agents changed.

## See how your trained model is doing

The dashboard uses visual representations to help you monitor the utilization of predictions by the model over time. By selecting a specific model and output field, you can view the number of predictions that were accepted or replaced by the agent and compare them to the baseline.

-   **Predictions agents accepted**

    The widget shows the correct predictions that your agents used during case management over time. If this number is trending downward, you can look to retrain your model.

-   **Predictions agents replaced**

    The widget shows the incorrect predictions that your agents removed during case management over time. If this number is trending upward, you can look to retrain your model.

-   **Predictions the model skipped**

    The widget shows the number of predictions that were skipped by the model based on the model, output field, and date range selection.

-   **Performance overview**

    The performance overview table shows the mean percentage values for correct, incorrect, and skipped data for each combination of model and output field.

-   **Track usage of individual field predictions over time**

    The bar chart tracks the usage of the individual field predictions over time. Each bar in the chart shows three components, which are the predictions accepted, the predictions replaced, and the predictions that were skipped by the model. A red outline around each bar represents the total number of records for each day. To compare specific components, navigate to the legends and deselect the ones that you don't want to include so that you can have a more customized and focused comparison based on user preferences. By default, the view displays the number of predictions. However, you have the option to switch to the percentage view by toggling the **Show Percentage** option. In the percentage view, you can also access the information about the baseline that was replaced and accepted, which is derived from the training data. This option enables you to gain insights into the performance of the model with the baseline.

-   **Track usage of model predictions over time**

    The bar chart monitors the usage of the model over time and is similar to the bar chart in the “Track usage of individual field predictions over time” data. The field selections enable users to compare predictions over time across a maximum of three fields.


**Note:**

-   When you refresh the page, the configurations, model selection, fields, usage type, and Show percentage toggle selection are retained.
-   The Model and Output field options support multi-select functionality so that you can compare the average number of training records and analyze how your agents use the predictions of different models. When multiple models are selected, the Compare how agents used models' predictions section enables your agents to compare the selected models across different usage types. The chart also supports toggling between the count and percentage. It also displays the baselines for accepted and replaced predictions when you’re using the percentage model.

## Using Task Intelligence analytics

Navigate to **All** &gt; **Task Intelligence for Customer Service** &gt; **Monitoring** to access the Task Intelligence Analytics page.

You can view the analytics for all of your models or each individual model. To select a model, do the following actions:

1.  Select **Model** to access analytics for an individual model.
2.  Select a model from the list of models that have been created from the Task Intelligence Admin Console.
3.  Select **Apply**.

To clear the selected model, select **Model** and then select **Clear**.

