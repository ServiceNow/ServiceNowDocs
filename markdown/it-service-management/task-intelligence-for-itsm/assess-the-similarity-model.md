---
title: Assess the similarity model
description: Assess the results from the model training and view sample results to see the similar records predicted for incidents. Reviewing the results gives you a preview of how your model will perform after being deployed. Based on the sample results, select the prediction preference.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-service-management/task-intelligence-for-itsm/assess-the-similarity-model.html
release: xanadu
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Set up similar records prediction model, Create a similar records prediction model in Task Intelligence for ITSM, Managing Task Intelligence for ITSM models, Task Intelligence for ITSM, IT Service Management]
---

# Assess the similarity model

Assess the results from the model training and view sample results to see the similar records predicted for incidents. Reviewing the results gives you a preview of how your model will perform after being deployed. Based on the sample results, select the prediction preference.

## Before you begin

You must train your model with various data. For more information on how to train your model, see [Train the similarity model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/task-intelligence-for-itsm/train-the-similarity-model.md)

Role required: sn\_ti\_admin.tia\_admin or admin 

## About this task

The model has flexible options. Based on the sensitivity and requirements of each incident record, you can do the following actions:

-   Recommend the similar records for the incidents.
-   Monitor and run the prediction model for the incidents in the background only.
-   Turn off the predictions for the incidents.

## Procedure

1.  View the number value in the **Estimated number of records used for training** section. 

    The number helps you predict how your model performs when deployed.

2.  Select **View sample results** to see the similar records predicted for each incident. 

3.  Choose one of the following options from the **Prediction preference** drop-down list for each field.

<table id="choicetable_lzr_gyr_zyb"><thead><tr><th align="left" id="d89667e104">

Options

</th><th align="left" id="d89667e107">

Description

</th></tr></thead><tbody><tr><td id="d89667e113">

**Recommendations**

</td><td>

Shows the top recommendations based on the similarity patterns. Agents can choose to accept or reject the recommendation. You can configure the number of recommended values using Advanced Recommended actions for ITSM. For more information, see [Recommended Actions for ITSM in Service Operations Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/service-operations-workspace/recommended-actions-for-itsm-in-service-operations-workspace.md).

</td></tr><tr><td id="d89667e138">

**Turn off predictions**

</td><td>

Stops the model from performing any predictions.

</td></tr><tr><td id="d89667e147">

**Monitor only**

</td><td>

Monitors and runs the model in the background only without making any predictions on the incident form.

</td></tr></tbody>
</table>    \[Omitted image "TI\_Assess\_the\_similarity\_model\_page.png"\] Alt text: Access the model page

4.  Select **Save &amp; continue**.


**Parent Topic:**[Set up similar records prediction model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-service-management/task-intelligence-for-itsm/set-up-similar-records-prediction-model.md)

