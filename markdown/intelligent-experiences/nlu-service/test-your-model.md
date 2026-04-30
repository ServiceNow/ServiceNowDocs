---
title: Test your model
description: Test your Natural Language Understanding \(NLU\) model against its default test set. Testing helps determine how your model is performing with the current content.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Test and publish your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Test your model

Test your Natural Language Understanding \(NLU\) model against its default test set. Testing helps determine how your model is performing with the current content.

## Before you begin

-   Make sure that the NLU Model Builder - Core plugin, NLU Model Builder plugin, NLU Workbench - Advanced Features plugin and Predictive Intelligence plugin are all installed and activated.
-   Have a trained model for Virtual Agent or AI Search. For more information, see [Build and train your model](../concept/managing-model-content.md).
-   Have a test set for testing models. For more information, see [Test set creation and management](../concept/nlu-test-set-creation-management.md).
-   Role required: nlu\_editor, nlu\_admin, or admin. The editor must be assigned to the model.

## About this task

Run a test of your model using its default test set, which contains test utterances and their expected intents.

-   If an expected intent in your test set does not correspond to any intent in the model, the utterances with those intents are not used for testing. They are not included in the test results.
-   The mid-conversation responses of Dialog Acts can't be tried or tested in NLU Workbench.
-   When the model returns no prediction for utterances which are marked as `Not relevant`, that result will be counted as **Correct**.
-   If your test set does not cover at least 60% of intents in the model, the system will not recommend a confidence threshold. However, you can still run the test.

In this example scenario, you've trained your model and want to assess the performance.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then the name of the model you want to test.

3.  On the model overview's **Model details** tab, locate the card for the **Test and publish your model** phase, then click **View phase**.

4.  Select **Run new test**.

    **Note:** Other phases are unavailable during a test.

    ![Run new test on the Test and publish your model phase.](../images/test-your-model1.png)

5.  The **Confirm run new test** dialog box opens, so select **OK**.

    ![The dialog box to confirm Run new test.](../images/test-your-model2.png)

    The test begins and the **Testing is in progress...** page loads.


## Result

When the test is finished, the **Test and publish your model** page reloads. The **Test run date** field reflects the date and time of this test.

The **Overview** tab displays a chart of the test results. It also displays a list of the top 5 incorrect intents and the top 5 missed intents.

The **Detailed results** tab lists all of the test utterances and their prediction outcomes.

You can see previous test results by clicking **view the test history** on **Test and publish your model**, or by navigating to **Batch Testing** &gt; **Test results**.

## What to do next

Use the results to edit and improve your model's content. When you are satisfied with the results, publish your model to make it available to consuming applications such as Virtual Agent.

**Parent Topic:**[Test and publish your model](../concept/testing-your-model.md)

