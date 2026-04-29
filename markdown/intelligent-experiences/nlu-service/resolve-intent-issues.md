---
title: Resolve intent issues
description: Use the issue cards to identify intents that have conflicts, need reviewing, or need more utterances. Resolving intent issues ensures the intents in your Natural Language Understanding \(NLU\) models work properly.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [NLU intents, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Resolve intent issues

Use the issue cards to identify intents that have conflicts, need reviewing, or need more utterances. Resolving intent issues ensures the intents in your Natural Language Understanding \(NLU\) models work properly.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Workbench - Advanced Features plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   You can resolve conflicts for Virtual Agent and AI Search models.
-   Role required: nlu\_admin or admin. When assigned to a model, the nlu\_editor can resolve intent issues for that model.

## About this task

When a trained model contains intents with issues, the issue cards are displayed on the intents tab of **Build and train your model** page. Select each card to filter the list of intents for that issue. ![In the Build and train your model phase, the highlighted cards notify the user about several issues with this model's intents.](../images/resolve-intent-issues001V.png)

The cards display different issues:

-   **intents have low utterance count**: Intent doesn’t contain the required minimum of 5 training utterances. This card also displays when the intent contains less than the recommended count of 15 utterances.
-   **intents have low test utterance count**: The default test set does not have enough test utterances for the intent. This card displays when the count of test utterances for an intent is below the recommended 15.
-   **intents have critical conflicts**: Intent contains training utterances that overlap with utterances in another intent.

    **Note:** Utterances which are marked as `Not relevant`may also conflict with utterances assigned to intents. For more information, see [Irrelevance detection in NLU](../concept/irrelevance-detection-nlu.md).

-   **intents need review**: Intent was translated but must be reviewed by an nlu\_admin or nlu\_editor.

The issue cards are hidden under the following circumstances:

-   The model is a pre-built model
-   The model is in a draft state and not trained
-   The model contains no conflicts
-   A successful conflict report doesn't exist for the latest trained version
-   The NLU Workbench - Advanced Features plugin isn't installed

Resolve issues in the following ways:

|Issue|Resolution|
|-----|----------|
|intents have low utterance count|Add more training utterances to the intent. Intents need at least 5 utterances. The recommended count is at least 15 utterances.|
|intents have low test utterance count|Add more test utterances for the intent to the model's default test set. The recommended count is at least 15.|
|intents have critical conflicts|Remove or edit any utterances so that each utterance applies to only one intent.|
|intents need review|Have an nlu\_admin or nlu\_editor review the intent. For more information, see [Enable or disable a secondary model intent](enable-disable-secondary-model-intent.md).|

In this example procedure, you are resolving critical conflicts in one of your intents. You built a Virtual Agent model for handling HR requests, but two of your intents, GeneralHRInquiry and CreateHRGeneralInquiryCase included similar utterances.

## Procedure

1.  Ensure that you are in the same application scope as your model, and navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then select the name of your model.

3.  In the **Build and train your model** card, click **View phase**.

4.  On the intents tab, click the **intents have critical conflicts** card.

    The intents list filters and shows the intents with critical conflicts.

5.  Click the intent name you want to resolve.

    In this example, you click the GeneralHRInquiry intent.

6.  Click the **Conflicts** tab.

    The conflicts tab appears and lists the conflicting utterances. The utterances for the current intent show on the left. The conflicting utterances for the other intent appear on the right.

    **Note:** You can hide moderate conflicts to focus on the critical conflicts. You can also ignore conflicts. However, be sure to fix all conflicts for best performance.

    ![Conflicts tab of an intent screen with critical conflicts. Changes made on this screen are saved automatically.](../images/resolve-intent-issues01.png)

7.  Point to the utterance that you want to edit or remove.

    ![Utterances that are conflicting with each other. You can edit or delete an utterance from that intent.](../images/resolve-intent-issues02.png)

    In this example procedure, click the trash icon to remove the utterance from the CreateHRGeneralInquiryCase intent.

    The utterance is removed from the intent.

    **Note:** Any changes you make automatically save.


## What to do next

Utterances designated as `Irrelevant` or `Not relevant`may also conflict with training utterances. Irrelevant utterances are displayed as though they are in their own intent named **NO\_INTENT**. However, these utterances cannot be edited or deleted in Conflicts. Copy the utterance to the Irrelevance Detection module to edit or delete. For more information, see [Irrelevance detection in NLU](../concept/irrelevance-detection-nlu.md).

Continue to resolve all conflicts. When finished, train your model to see a list of updated conflicts, if any. Resolve all intent issues prior to testing and publishing your model.

**Parent Topic:**[NLU intents](../concept/intents.md)

