---
title: Run a multi-model batch test
description: Test multiple Natural Language Understanding \(NLU\) models against a test set. Evaluate the quality of your models and refine them to improve intent prediction.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Multi-model Batch Testing, NLU Workbench - Advanced Features, Natural Language Understanding, Enable AI experiences]
---

# Run a multi-model batch test

Test multiple Natural Language Understanding \(NLU\) models against a test set. Evaluate the quality of your models and refine them to improve intent prediction.

## Before you begin

-   Make sure that the NLU Workbench - Core plugin, NLU Workbench plugin, NLU Workbench - Advanced Features plugin and Predictive Intelligence plugin are all installed and activated.
-   Have one or more trained models for Virtual Agent or AI Search.
-   Have a test set containing test utterances with expected intents. See [Create a test set](import-batch-test-set.md) or [Test set creation and management](../concept/nlu-test-set-creation-management.md).
-   Role required: nlu\_admin or admin. When assigned to a model, the nlu\_editor role can run tests and modify test utterances for that model.

## About this task

In **Multi-model Batch Testing**, you can use a test set that is not the model's default test set.

Also, you can test up to ten models at one time using **Multi-model Batch Testing**. However, tests with fewer models run more quickly.

When testing multiple models, your test set must cover at least 25% of the total intents of all the models. Use test sets that contain utterances the models are likely to encounter in Virtual Agent or AI Search.

**Note:** If an expected intent in your test set doesn't match any intent in your models, that expected intent and its test utterances are skipped. They aren't counted or displayed in test results.

To test a single model against its default test set, use the **Test and publish your model** phase on the model's overview page. For more information, see [Test and publish your model](../concept/testing-your-model.md).

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **NLU Advanced Features** &gt; **Multi-model Batch Testing**.

2.  Click **Run a test**.

3.  In the **Run new batch test** window, select your models from the list.

    ![The window for Run a new batch test.](../images/run-batch-test2.png)

4.  Select a test set from the list.

5.  Click **Run**.

    ![The list view of batch test results.](../images/run-batch-test3.png)

    Your new test shows in the **Test results** list with a **Testing...** Status.


## What to do next

When the batch test is finished, its Status changes to **Done**. You can click the name of the test set to view the test results.

Use the results to adjust and improve your models. Then, run the test again to assess the performance.

Batch testing may affect confidence threshold recommendations. For more information, see [NLU model settings](../concept/nlu-model-settings.md).

