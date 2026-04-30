---
title: Publish your NLU model
description: Publish your Natural Language Understanding \(NLU\) model to activate it and make it available for use in other applications that consume NLU.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Test and publish your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Publish your NLU model

Publish your Natural Language Understanding \(NLU\) model to activate it and make it available for use in other applications that consume NLU.

## Before you begin

-   Make sure that the - NLU Workbench - Core plugin, NLU Workbench plugin, and Predictive Intelligence plugin are all installed and activated.
-   Have a trained and tested NLU model.
-   Role required: admin or nlu\_admin

## About this task

For this procedure, you've already trained, tested, and refined your NLU model and are satisfied with the results.

If your model is already published, you can publish it again. However, you must train the model again before republishing.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then select the name of your model.

3.  On the Model overview page, locate **Test and publish your model**, then select **View phase**.

    **Note:** If the model hasn't been built or trained yet, the **Test and publish your model** phase is not available.

    ![The Test and publish your model phase on the model's overview page.](../images/publish-nlu-model05.png)

4.  On the **Test and publish your model** screen, select **Run new test** to assess the model using its default test set.

    Testing can be skipped, but model performance may not be optimal. If testing is skipped, a confirmation message displays, asking if you want to continue without testing. For more information on testing, see [Test and publish your model](../concept/testing-your-model.md).

5.  Click **Publish model**.

    ![Publish model button](../images/publish-nlu-model07.png)

    **Note:** If the model hasn't been tested yet, the **Publish model** button is white. If the model has already been tested, the button is green. If the last trained model is already published, the **Publish model** button is unavailable. Return to **Build and train your model** to train again.

    **Result:** The most recent version of your NLU model is published. The model is active and available for use in other ServiceNow applications, such as Virtual Agent. Publishing also replaces any older versions of the model that are currently in use by those applications.


**Parent Topic:**[Test and publish your model](../concept/testing-your-model.md)

