---
title: Train and try your NLU model
description: Train and try your model iteratively so that its intents and entities are validated, compiled, and saved to your model.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Train and try your NLU model

Train and try your model iteratively so that its intents and entities are validated, compiled, and saved to your model.

## Before you begin

-   Make sure that the NLU Workbench - Core plugin, NLU Workbench plugin, and Predictive Intelligence plugin are all installed and activated.
-   Create an NLU model. For more information, see [Creating models](../concept/creating-models.md).
-   Create one or more NLU intents and their associated entities for your model. For more information, see [NLU intents](../concept/intents.md).
-   If any utterance references a table vocabulary source, ensure that the source has been synchronized so that its values are available to your model. For more information see [Sync a table vocabulary source](sync-table-vocabulary-source.md).
-   Role required: nlu\_editor, nlu\_admin, or admin. The NLU editor must be assigned to the model.

## About this task

Training your model saves any changes you made to the content, and checks for conflicts or errors. Training also makes a model available for publishing.

After training, you can try your model by manually entering individual utterances to see what intents are predicted.

**Note:** To run a test of your model against a list of test utterances, see [Test and publish your model](../concept/testing-your-model.md).

The mid-conversation responses of Dialog Acts can't be tried or tested in NLU Workbench.

In this example scenario, you've already built sufficient model content by adding intents, utterances, entities, and their associated annotations. Following the example procedure, you first train your NLU model. Then you try your model by manually entering utterances so you can check the prediction results and confidence scores.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then select the name of your model.

3.  In the **Model details** tab of the model overview, make sure there is enough content in Intents, Entities, and Vocabulary.

4.  On the **Build and train your model** card on the model overview, select **View phase**.

    ![The Build and train your model phase card, on the model overview.](../images/managing-model-content2.png)

5.  When the **Build and train your model** phase opens, ensure that the **Train model** tab is selected.

    Result: The **Train model** tab displays the last time the model was trained, and also summarizes content changes since the last training, if any.![The Build and train your model phase view with the Train and try panel highlighted.](../images/test-train-nlu-model1.png)

6.  Select the **Train** button.

    Result: The system displays a progress bar during training. When finished, the system displays one of two recommendations:

    -   When less than 60% of the model's intents are covered in the default test set, the system recommends adding more test utterances. See [Test set creation and management](../concept/nlu-test-set-creation-management.md).![The recommendation to add test utterances, shown after training.](../images/test-train-nlu-model2.png)
    -   When over 60% of the model's intents are covered in the default test set, the system recommends proceeding to testing. See [Test and publish your model](../concept/testing-your-model.md).![The recommendation to proceed to testing, shown after training.](../images/test-train-nlu-model3.png)
7.  To manually try individual utterances, select the **Try model** tab.

8.  In the text field under **Enter an utterance to test**, type an utterance and select **Go**.

    ![The Try model section with results displayed.](../images/test-train-nlu-model4.png)


## Result

In this example, you entered `I need to update my home address` as the utterance to try.

1.  The system displays the model's confidence threshold, which is 76% in this example.
2.  Under **Top prediction\(s\)**, the system displays all intents that were predicted with a confidence score greater than the threshold.
3.  In the example, the intent UpdateAddress is predicted with a confidence score of 97%, which is greater than the threshold of 76%.

The **Try model** results also display thumbs-up and thumbs-down icons for you to provide feedback. For more information, see [Test panel feedback](../concept/test-model-panel-feedback.md).

## What to do next

-   Continue trying various utterances to check that your updates to model content are effective. See [Compare draft and published versions of your NLU model](compare-draftmodel-to-last-published-version.md).
-   To test your model against a list of test utterances, use its default test set in the [Test and publish your model](../concept/testing-your-model.md) phase, or navigate to [Multi-model Batch Testing](../concept/batch-testing-nlu.md).
-   To adjust the model's confidence threshold, use the **Settings** tab on the model's overview page. For more information, see [NLU model settings](../concept/nlu-model-settings.md).
-   If you're satisfied with the results of your testing, [Publish your NLU model](publish-nlu-model.md).

**Parent Topic:**[Build and train your model](../concept/managing-model-content.md)

