---
title: NLU model settings
description: Change your NLU model's name, description, or confidence threshold on the Settings page of the model overview.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Model management, Natural Language Understanding, Enable AI experiences]
---

# NLU model settings

Change your NLU model's name, description, or confidence threshold on the **Settings** page of the model overview.

Access the model's settings by navigating to **All** &gt; **NLU Workbench** &gt; **Models**. Select the tab for your model's application, then your model's name. On the model's overview, select the **Model settings** tab. ![Model settings on the model's overview page](../images/nlu-model-settings1.png)

## Model settings

In the upper section of the model settings page, you can change the model's name, short description, and business area. You cannot change the model's language, purpose, or scope. To make a model with a different language, purpose, or scope, see [Creating models](creating-models.md).

By default, the **Ignore punctuation** check box is active. Ignoring punctuation makes it so that there is less variance between predicted intents and confidence scores for utterances with slightly different punctuation. For best results, keep the check box active.

## Model threshold settings

Here you can adjust how the confidence threshold works in your model.

A threshold is a confidence score represented by a percentage. The confidence threshold of a model determines what intents from that model will be predicted for a given utterance. For example, if the model threshold is 65%, then an intent will be predicted for an utterance only when the intent has a confidence score that is at least 65%. Setting a threshold that is too low may increase the false positives by predicting intents that should not be a match for an utterance. On the other hand, a model threshold that is too high may filter out intents that you do want to get predicted. Finding the ideal threshold improves your model's ability to predict intents correctly.

There are two types of model threshold settings:

-   **Automatic** - Allow the system to choose the optimal confidence threshold for your model. The value is updated dynamically based on test results. This happens in the **Test and publish your model** phase, where your model's default test set is used.
-   **Manual** - You can manually set the confidence threshold. The system may also recommend a better threshold for the model during testing. You can choose to accept recommendations.

Prebuilt models come with a tuned threshold. The confidence threshold on prebuilt models was chosen specifically for that model.

Test results include a model threshold recommendation only if they meet the following requirements:

-   The test set has a Test Coverage score of at least 60%, with at least 5 test utterances per intent. For more information, see [Test set creation and management](nlu-test-set-creation-management.md).
-   The test set has at least 100 utterances.
-   The model is not a prebuilt model.
-   The recommended threshold would have better results than the current threshold.

![Test results page with the bar charts for the current and recommended thresholds.](../images/testing-your-model03.png)

Test results with a recommended threshold contain a second graphic. The second graphic shows the prediction percentages with the recommended thresholds applied.

Applying the threshold recommendation may improve the prediction percentages of your model. Select **Apply recommendations** to change the threshold. The system automatically retrains the model, and the test results show the prediction percentages with the new threshold.

**Parent Topic:**[Model management](model-management-phases.md)

