---
title: Irrelevance detection in NLU
description: Keep Virtual Agent chats focused with Irrelevance detection. Use the Irrelevance detection feature to train your NLU model to avoid making predictions for utterances that are not relevant.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Model management, Natural Language Understanding, Enable AI experiences]
---

# Irrelevance detection in NLU

Keep Virtual Agent chats focused with Irrelevance detection. Use the Irrelevance detection feature to train your NLU model to avoid making predictions for utterances that are not relevant.

## Summary information

The Irrelevance detection feature improves the prediction accuracy of NLU models by training them to ignore certain utterances. These utterances from your users may not apply to any intent, so should not get any prediction.

To ensure that models do not predict an intent when they are not supposed to, you can mark utterances as `Not relevant`. These marked utterances are included as part of model training. When the published model encounters similar utterances from your users, no intent is matched or predicted.

The Irrelevance detection table is where you can manage utterances marked as `Not relevant`.

## Roles, Usage, and Navigation

Use the nlu\_admin or admin role to access Irrelevance Detection. The nlu\_editor role is also able to access Irrelevance Detection, but must be assigned to a model to edit that model's contents.

Irrelevance Detection is available for Virtual Agent models only.

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**. The Virtual Agent tab opens by default.
2.  Scroll down the list of Virtual Agent models to the **Boost your model performance** section.
3.  Scroll horizontally to locate the card **Keep chats focused**, and select its button **Go to irrelevance detection**.![In NLU Workbench, on the Virtual Agent tab, the card Keep chats focused is highlighted.](../images/irrelevance-detection-nlu020V.png)

**Note:** The instance URL for this feature is &lt;instance-name&gt;.servicenow.com/now/nlu-workbench/irrelevant-utterances.

## Adding utterances to Irrelevance detection

There are several methods for adding utterances to **Irrelevance detection**:

-   The Virtual Agent chat log: In the Expert Feedback Loop in NLU Workbench, when you review an utterance collected from the Virtual Agent chat log, you can mark it as `Not relevant`. The system will ask whether it should be irrelevant to a particular model, or to all models. After adding, these utterances may display as **NO\_INTENT** in Expert Feedback Loop.

    For more information on Expert Feedback Loop in NLU, see [NLU Expert Feedback Loop](nlu-expert-feedback-loop.md).

    These utterances have a Source of **VA Chat Logs** in the Irrelevance detection table.

-   Manual input: In Irrelevance detection, type your utterance in the **Type utterances here** field, then select **Add**. The system will ask whether it should be irrelevant to a particular model, or to all models.

    These utterances have a Source of **Manual** in the Irrelevance detection table.

-   Importing: When you use a CSV or XLSX \(Excel Workbook\) file to import training utterances and their intents, you can indicate irrelevant utterances by leaving the Intent column empty. These utterances may display as **NO\_INTENT** in areas such as Expert Feedback Loop and Conflict Review.

    For more information on importing utterances and intents, see [Create an NLU model from a CSV file](../task/create-nlu-model-csv.md).

    These utterances have a Source of **Manual** in the Irrelevance detection table.


## Behavior of irrelevant utterances

There are two types of irrelevant utterances: those associated to one specific model, or those irrelevant to any model. A model can have a maximum of 200 irrelevant utterances associated to it.

Following are details of how these two types and the 200-count maximum interact.

When a model is submitted for training, at most 200 irrelevant utterances are submitted with it. First, irrelevant utterances directly associated to that model are submitted. Then, utterances which are designated as not relevant to any model are submitted. The total of these types does not exceed 200.

If a model has 200 irrelevant utterances associated to it, and a new irrelevant utterance is added, then the model's oldest utterance is dropped. The new irrelevant utterance could be of either type \(not relevant to the specific model, or not relevant to any model\).

A model cannot have more irrelevant utterances than normal training utterances.

## Conflict review

If an utterance is marked as irrelevant, and there is a similar utterance in an intent, the model does not make a prediction for that utterance. In other words, irrelevant utterances take precedence over training utterances.

Because irrelevant utterances impact the model's predictions, they are displayed as conflicts when they overlap with training utterances.

There are two locations where conflicts with irrelevant utterances are highlighted:

-   The Cross-model Conflict Review module. For more information about this module, see [Cross-model Conflict Review](nlu-intent-conflict-review-resolution.md).

    **Note:** The Cross-model Conflict Review module is available with the NLU Workbench - Advanced Features application from ServiceNow® Store. For more information, see [NLU Workbench - Advanced Features](nlu-workbench-advanced-features.md).

-   The Conflicts tab of an intent. For more information on conflicts in an intent, see [Resolve intent issues](../task/resolve-intent-issues.md).

For the purpose of reviewing conflicts, irrelevant utterances are displayed as though they are in their own intent, named **NO\_INTENT**.

Note that irrelevant utterances cannot be edited or deleted on the conflict page. Copy the irrelevant utterance from the conflict page to the Irrelevance detection page to modify or delete the utterance.

## More information

-   In test sets, aim to include about 10% of test utterances as irrelevant. This helps to assess how your model handles utterances that should not have an intent predicted. When you import training or test utterances from a CSV or XLSX \(Excel Workbook\) file, you can indicate that an utterance is irrelevant by leaving the Intent column empty.
-   When testing models against test sets, results are considered Correct if no intent is predicted for an irrelevant utterance.
-   Utterances that were marked as `Not relevant` can be re-assigned later. For example, if a new intent is created, existing irrelevant utterances can be manually assigned to the new intent. They then become part of the normal training utterances.

    To re-assign an utterance in Irrelevance detection, expand the list in the **Corrected intent** column and select the appropriate intent. Be sure to select the **Save feedback** button after re-assignment. Also be sure to retrain the model to incorporate these updates into the model.

-   Irrelevant utterances are not associated to particular intents within a model. They are either associated to one model, or marked as not relevant to any model.
-   The utterances which are marked as not relevant to any model are submitted as part of the training data for each model. In other words, these apply to all models.
-   Model training is necessary to incorporate `Not relevant`utterances. Training any model adds newly marked utterances to all models.
-   Utterances can be deleted or edited in the Irrelevance detection table.
-   Irrelevant utterances should have content that is different from utterances associated to an intent.

**Parent Topic:**[Model management](model-management-phases.md)

