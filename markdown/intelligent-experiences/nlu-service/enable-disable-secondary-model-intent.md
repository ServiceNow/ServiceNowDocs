---
title: Enable or disable a secondary model intent
description: Enable and disable intents in your Natural Language Understanding \(NLU\) models to make them active or inactive. Disable intents while editors or admins edit, review, or update its content and translations.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Multilingual model management, Natural Language Understanding, Enable AI experiences]
---

# Enable or disable a secondary model intent

Enable and disable intents in your Natural Language Understanding \(NLU\) models to make them active or inactive. Disable intents while editors or admins edit, review, or update its content and translations.

## Before you begin

Role required: nlu\_admin or nlu\_editor

## About this task

NLU admins and NLU editors can enable or disable intents in secondary models. If an intent is disabled, the model doesn't use it to make predictions. However, it also can't be accessed by any ServiceNow application using the model, such as Virtual Agent or Search.

An intent's state is represented in the **Enabled** column.

![Intents list with one intent that is enabled, and one intent that is not. Intents that are not enabled display as grayed out.](../images/enable-disable01.png "Intents list")

Enabling of intents works in the following ways:

-   Intents created in primary models are active by default.
-   Intents from primary models are automatically created, but not enabled, in their secondary models \(pending import\).
-   Disabling an intent in the primary model disables the corresponding intent in all secondary models.
-   If an intent is disabled in the primary model, the intent can't be re-enabled in a secondary model.
-   Enabling a disabled intent in the primary model does not enable the corresponding intents in the secondary models.
-   Disabling intents in secondary models has no effect on the primary model or other secondary models.
-   Secondary model intents that are marked with Needs review are disabled by default.
-   If you disable a primary model intent that is mapped to a Virtual Agent \(VA\) topic, a confirmation message appears.
-   If you disable a secondary model intent that is mapped to a VA topic, a confirmation message appears.
-   NLU admins can enable and disable intents in any model.
-   NLU editors can enable and disable intents only for models they are assigned to.

Disabling intents gives editors time to review the intent translations and update them if needed. When you’re satisfied with the content, enable the intent to make it accessible to other NLU models and ServiceNow applications.

In this review example, you have a list of disabled intents in the Needs review state. The goal of this task is to review the translated content for a secondary model. When you complete your review, or if the content is fine as it is, you click Mark as reviewed. This moves the intent into the Reviewed state. You can also undo the Mark as reviewed state for an intent by clicking the **Unmark Reviewed** button, but only if you remain on the Intent screen. If you leave the screen prematurely, the **Unmark Reviewed** button disappears, and you won't be able to retrieve it.

![You can switch back and forth between the Reviewed and Unmark Reviewed states for an intent, as long as you do so within the same session.](../images/enable-disable-secondary-model-intent00.png "Switch between the Reviewed and Unmark Reviewed states for an intent")

The editorial review also includes the Vocabulary section on the Model screen, where vocabulary that has been translated from the primary model to the secondary model is marked with an orange dot and the Needs review state. You can edit or delete the vocabulary items, even if they are in review. After you review the vocabulary and update the translations if needed, you can mark all of them at once by clicking the Mark all reviewed button. This action makes the orange dot disappear from the Vocabulary section of the Model screen.

**Note:** The **Train** and **Try** buttons on the Model screen are disabled until the vocabulary is reviewed, and the intents in the Needs review state are either reviewed or disabled.

![The orange dot represents items or groups of items that are in the Needs Review state.](../images/enable-disable-secondary-model-intent000.png "Items that require review")

In this example scenario, you have applied the Use Software translation mode to translate a secondary model into the Japanese language. Because the translation hasn't been reviewed yet, the system marks the intents and the model with the Needs review state. When a model is in the Needs review state, it can't be trained, tested, or published. When it moves out of the Needs review state, you can then train and test the model.

**Note:** An NLU editor can't create or publish a model. Only the NLU admin has permission to do this.

In this example procedure, you're reviewing the intents in a model one at a time.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

2.  Locate one of your secondary models that has already been translated.

    In this example scenario, you locate the Virtual Agent Conversation Setup JA model, as shown in the image below.

    In the Intents section of the model, there's a list of five intents that are marked with the Needs review state. Above the list of intents, there's also a box that shows a running count of the intents that need review.

    ![The Needs Review state lets users know that the translation must be reviewed by an NLU editor or NLU admin.](../images/enable-disable-secondary-model-intent1.png "The needs review state")

3.  Click an intent Name so you can access the intent content.

    In this scenario, you click the **\#End Conversations** intent name.

4.  Review the secondary language translations of the model utterances, entities, and vocabulary, then update the content as needed.

    When you finish your review of the intent, the Mark as reviewed button appears.

5.  Click **Mark as reviewed**.

    **Result**: The system updates the **\#End Conversations** intent from the Mark as reviewed state to the Reviewed state. In addition, the reviewed intents box changes its running count from 0 of 5 to 1 of 5.

6.  If you're satisfied with your intent review, click the **Enable** button so the intent is available and can be accessed by any application, such as Virtual Agent \(VA\) or Search.


## What to do next

Repeat Steps 1 through 6 for the four remaining intents in the list. As each intent review completes and is marked with the Reviewed state, the running count in the intents reviewed box increases toward 5 of 5.

**Parent Topic:**[Multilingual model management](../concept/multilingual-model-managent.md)

