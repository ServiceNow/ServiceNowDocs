---
title: Assign an NLU editor to a model
description: Assign an editor to review your Natural Language Understanding \(NLU\) model translations and edit model content. Delegate the maintenance, testing, and optimization of model content to an editor.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Multilingual model management, Natural Language Understanding, Enable AI experiences]
---

# Assign an NLU editor to a model

Assign an editor to review your Natural Language Understanding \(NLU\) model translations and edit model content. Delegate the maintenance, testing, and optimization of model content to an editor.

## Before you begin

-   Create a model, or use an existing one. For translation review, create both primary and secondary \(translated\) models. For more information on multilingual model groups, see [Multilingual model management](../concept/multilingual-model-managent.md).
-   Assign the nlu\_editor role to users. See [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Role required: nlu\_admin. The nlu\_editor can't assign another editor to models.

## About this task

The nlu\_admin can delegate model content work to an nlu\_editor. Assign language specialists as editors to review the consistency between primary and secondary \(translated\) models, or further localize the translation by editing intents and utterances. Delegate the maintenance of an existing model's content, without affecting the model's published status.

The nlu\_editor can do the following, when assigned to a model:

-   Train and test the model.
-   [Export an NLU model](export-nlu-model.md) as CSV.
-   When a model or intent is in the **Needs review** state, the editor can mark it as **Reviewed**.
-   Modify the model's confidence threshold.
-   Edit the model name and description in **Settings**.
-   Review, edit, and approve translated utterances.
-   Add, edit, and delete training utterances.
-   Annotate training utterances \(add references to [NLU vocabulary](../concept/using-nlu-vocabulary.md) and [NLU entities](../concept/entities.md)\).
-   Update entity properties \(except the entity name in a secondary model\).
-   Add, edit, or delete the model's vocabulary.
-   View the **Vocabulary sources** module \(read only\).
-   Add, activate, and de-activate [NLU intents](../concept/intents.md) in primary and secondary models.
-   Resolve conflicting intents; also access the [Cross-model Conflict Review](../concept/nlu-intent-conflict-review-resolution.md) module.
-   View the [Irrelevance detection in NLU](../concept/irrelevance-detection-nlu.md) module.
-   Add, edit, or delete a test utterance in a test set; also access the [Multi-model Batch Testing](../concept/batch-testing-nlu.md) module.

**Note:** The editor must be assigned to a model and in the model's application scope to take these actions, unless otherwise indicated.

The nlu\_editor can't do the following:

-   Create, add, publish, or delete a model.
-   Duplicate a model.
-   Translate a model \(initiate a translated secondary model\).
-   Import primary model content to a secondary \(translated\) model.
-   Sync or edit vocabulary sources.
-   View model performance.
-   Provide feedback in [NLU Expert Feedback Loop](../concept/nlu-expert-feedback-loop.md).
-   Manage other editors, such as assigning an editor to a model or removing an editor from a model.

![In the Build and train your model phase, the Intents need review card is highlighted. In the list of the model's intents, three intents are marked as Needs review.](../images/assign-editor1U.png)

First, an admin assigns the nlu\_editor role to a user. Next, the NLU admin assigns the editor to a model.

When you assign an editor to a model, you must do so at the individual model level. You can't assign an editor at the model group level.

The following models can't be assigned to an editor:

-   Prebuilt models
-   Models that have a translation in progress

In this example procedure, you add an NLU editor to a secondary model that needs reviewing.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default. Select the appropriate tab for your model.

2.  Locate the name of your NLU model and scroll to the right end of its row.

    If your model is in a multilingual group, expand the group to find the individual model. Editors cannot be assigned to groups.

3.  Select the model's **More options** menu, then select **Manage editors** in the list.

    ![In the NLU Workbench, a model's More options menu is expanded and Manage editors is highlighted.](../images/assign-editor2V.png)

4.  In the **Add editors** window, use the drop-down list and search bar to add the names of the editors you want to assign to the model.

    ![In the Add editors window, the Editors field and the Add button are highlighted.](../images/assign-editor3V.png)

5.  Select **Add**.

    The editor is assigned to the model. A banner acknowledgement displays at the top of the screen. To add more editors, or remove editors, repeat this procedure.![A banner acknowledging that an editor was assigned to a model.](../images/assign-editor4V.png)


## What to do next

Assign more editors to the model, if necessary. You can assign up to four editors to a model at one time. To add more editors, or remove editors, repeat the above procedure.

As an NLU admin, ensure that your editors have what they need to properly review and edit models.

**Parent Topic:**[Multilingual model management](../concept/multilingual-model-managent.md)

