---
title: Test and publish your model
description: Assess the performance of your NLU model to identify areas for improvement. Then publish your model to make it available to other applications such as Virtual Agent.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Model management, Natural Language Understanding, Enable AI experiences]
---

# Test and publish your model

Assess the performance of your NLU model to identify areas for improvement. Then publish your model to make it available to other applications such as Virtual Agent.

## Summary usage

Test your Virtual Agent or AI Search model against its default test set to see how the model responds. Test results provide information you can use to improve your model.

**Note:** Testing your model requires the Multi-model Batch Testing feature, available with the NLU Workbench - Advanced Features application from ServiceNow® Store. For more information, see [Install NLU Workbench - Advanced Features](../task/install-nlu-workbench-adv-features.md).

To test your model, navigate to **NLU Workbench** &gt; **Models**. Select the tab for your model's application, then select the name of the model. In the **Test and publish your model** card, select **View phase.** ![Test and publish your model phase card](../images/testing-your-model001.png)

## Overview of testing and publishing your model

The **Test and publish your model** phase opens in the **Overview** page by default. Buttons for **Run new test** and **Publish model** are located here.

![Test and publish your model overview page](../images/testing-your-model002.png)

**Overview** provides information about a previous test run, with bar charts summarizing the test results.

If you have earlier test runs, you can view those by selecting from the **Test run date** list.

![Test run date pulldown](../images/testing-your-model003.png)

To drill down into the test results table, select the **Detailed results** tab. Each test utterance is listed in **Detailed results**, with its prediction.

## Understanding test results

The test results show how your model responded to the utterances in the test set.

![Test results for a model test in the NLU Workbench.](../images/testing-your-model02.png)

The bar chart shows the prediction percentages for correct, correct among multiple, missed, and incorrect:

<table id="table_cyz_yt3_3qb"><thead><tr><th>

Percentage

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Correct

</td><td>

The percentage of utterances for which your model correctly predicted the intent. When the model predicts no intent for utterances marked as `Not relevant`, that result is counted as Correct.

</td></tr><tr><td>

Correct among multiple

</td><td>

For utterances that had more than one intent predicted.

 The percentage of utterances for which the model correctly predicted the intent or intents, but also predicted intents that did not belong to the utterance.

</td></tr><tr><td>

Missed

</td><td>

The percentage of utterances for which your model did not predict an intent, even though there was an expected intent.

</td></tr><tr><td>

Incorrect

</td><td>

The percentage of utterances for which your model predicted an intent that was not correct.

</td></tr></tbody>
</table>Testing can affect the model's confidence threshold. The confidence threshold determines how confident a model must be to predict an intent for an utterance. For more information on confidence thresholds, see [NLU model settings](nlu-model-settings.md).

For information about utterances which should not have any intent predicted, see [Irrelevance detection in NLU](irrelevance-detection-nlu.md).

## Publish model

The **Publish model** button makes the current version of the model available to other applications such as Virtual Agent.

**Note:** If the model has not been trained, the **Publish model** button is unavailable. Return to the **Build and train your model** phase to train the model before publishing.

For more information on publishing your model, see [Publish your NLU model](../task/publish-nlu-model.md).

## Multi-model Batch Testing

In the **Test and publish your model** phase, you test your model against its default test set. With Multi-model Batch Testing, you can test against other test sets, test multiple models at once, and see your test results. To use Multi-model Batch Testing, navigate to **NLU Workbench** &gt; **NLU Advanced Features** &gt; **Multi-model Batch Testing**.

For more information, see [Multi-model Batch Testing](batch-testing-nlu.md).

For more information about test sets, see:

-   [Create a test set](../task/import-batch-test-set.md)
-   [Test set creation and management](nlu-test-set-creation-management.md)

For information about the process of testing, see [Test your model](../task/test-your-model.md).

