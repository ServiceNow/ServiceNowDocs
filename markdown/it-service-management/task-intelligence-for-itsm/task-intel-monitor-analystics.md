---
title: Monitoring and Analytics for Task Intelligence for ITSM
description: You can view the impacts of your trained incident prediction models. Monitor model performance overtime, track business value, and view what predictions your agents did and didn't use.
locale: en-US
release: yokohama
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Task Intelligence for ITSM, IT Service Management]
---

# Monitoring and Analytics for Task Intelligence for ITSM

You can view the impacts of your trained incident prediction models. Monitor model performance overtime, track business value, and view what predictions your agents did and didn't use.

To access the Task Intelligence Analytics dashboard, navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Monitoring**.

Use the **Model** drop-down list to select a model. Select **Apply** to open the model's configuration.

The Analytics dashboard contains the following sections:

-   Get an overview
-   See how your trained model is doing

## Get an overview

The Analytics dashboard uses visuals to represent the performance overview of the model.

-   **Number of predictions**

    The line graph shows the number of fields that the Incident categorization and Similar Incidents models predicted over time. As the model continues to learn, it can increase the number of predictions.

-   **Incident Mean time to resolve \(MTTR\)**

    The line graph shows the average amount of time that it takes to resolve incidents over time. As the model makes more predictions, the MTTR must decrease as the predictions help agents.


## See how your trained model is doing

The Analytics dashboard uses visuals to track how the model used predictions over time.

-   **Predictions agents accepted**

    The widget shows the correct predictions that your agents used during case management over time. If this number is trending downward, you can look to retrain your model. For more information on editing a trained model, see [Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md).

-   **Predictions agents replaced**

    The widget shows the incorrect predictions that your agents removed during case management over time. If this number is trending upward, you can look to retrain your model. For more information on editing a trained model, see [Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md).

-   **Predictions the model skipped**

    The widget shows the number of predictions that were skipped by the model based on the model, output field, and date range selection. For more information on editing a trained model, see [Edit an incident prediction model in Task Intelligence for ITSM](../task/edit-your-model.md).

-   **Performance overview**

    The performance overview table shows the mean percentage values for correct, incorrect, and skipped data for each combination of model and output field.

-   **Track usage of individual field predictions over time**

    The bar chart tracks the usage of the individual field predictions over time. Each bar in the chart shows three components, which are the predictions accepted, the predictions replaced, and the predictions that were skipped by the model. A red outline around each bar represents the total number of records for each day. To compare specific components, navigate to the legends and deselect the ones that you don't want to include so that you can have a more customized and focused comparison based on user preferences. By default, the view displays the number of predictions. However, you have the option to switch to the percentage view by toggling the Show Percentage option. In the percentage view, you can also access the information about the baseline that was replaced and accepted, which is derived from the training data. This option enables you to gain insights into the performance of the model with the baseline.


