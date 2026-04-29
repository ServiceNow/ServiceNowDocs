---
title: Create an NLU intent
description: Create an intent for your Natural Language Understanding \(NLU\) model. Intents provide your model with a system action to perform when it receives user input.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [NLU intents, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create an NLU intent

Create an intent for your Natural Language Understanding \(NLU\) model. Intents provide your model with a system action to perform when it receives user input.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Workbench - Advanced Features plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Ensure that you are in the same application scope as your model.
-   You can create intents for Virtual Agent and AI Search models in NLU Workbench.
-   Role required: admin or nlu\_admin

## About this task

This procedure shows you how to create an intent. To reuse intents from other models, see [Reusing intents from prebuilt NLU models](../concept/reusing-predefined-nlu-intents.md).

Here's an example of how intents can interact with the vocabulary in their training utterances.

-   Intent: \#AddMembersToDistributionList
-   Utterance A: "Please add Carlos Santana to the uxinfodev list"
-   Utterance B: "I'm mistakenly removed from the arlo-drury-directreports group"
-   Result: The system doesn't recognize uxinfodev or arlo-drury-directreports and can't use these words to predict the intent.
-   Solution: Add uxinfodev and arlo-drury-directreports as vocabulary items and add synonyms to them. The synonyms you provide help add more context to the utterance and the intent in which they reside. Your intent prediction confidence can be even higher if you also mark them as entities.

**Note:** Training utterances and utterances from your users have a limit of 25 words or 200 characters. Utterances that exceed that limit fail to return an intent prediction.

Do not include unrealistic terms such as "OrderLaptop" or "sfsdfasdfas" in training utterances. Utterances should be correct and natural examples in the model's language.

In the following example procedure, you're creating an intent and adding utterances that users might say when requesting information on payment. You've already created an NLU model that you've titled HR Model for Virtual Agent and you're creating an intent in that model.

## Procedure

1.  Set your application scope to your model's scope.

2.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

3.  Select the tab corresponding to your model's application, then select the name of the model you want to add an intent to.

    In this model example, you select your HR Model for Virtual Agent model.

4.  In the **Build and train your model** card, select **View phase**.

5.  Select **Intents**.

6.  Select **New Intent**.

7.  In the **Create an intent** window, add a name and description for the intent.

    ![Create an intent window. The intent name is required, but the description is optional.](../images/create-intent01.png "Creating an intent")

    In this example scenario, you enter `PayDiscrepancy` for the name. You can also add a description.

    **Note:** When you create an intent, the system adds a hashtag to the intent name.

8.  Select **Add intent**.

    The \#PayDiscrepancy intent screen appears, including sections for its utterances, associated entities, and settings. The intent draft status is also shown in the upper right corner of the Intent screen.

9.  In the **Utterances** tab, enter training utterance examples that are relevant to the intent.

    **Note:** The utterance examples that you provide must be unique and contain fewer than 25 words or 200 characters. Aim to add at least 15 utterances with as much variety between them as possible. You must add at least 5 utterances to begin training the model.

    In this scenario, you add the following utterances into the field and select **Add**

    ![Training utterance examples for the Pay Discrepancy intent. Add a minimum of 5 utterances to an intent.](../images/create-nlu-intent2.png)

    As you build and retrain your model iteratively, you can check how your updated intent affects the model's predictions. See [Train and try your NLU model](test-train-nlu-model.md).


## What to do next

Train your model to save your updates. For issues with intents, see [Resolve intent issues](resolve-intent-issues.md).

To improve your utterances, add entities to provide context. See [NLU entities](../concept/entities.md).

The available [Intent Discovery](../concept/intent-discovery.md) feature can help identify intents that would be possible to add, based on your historical data.

**Parent Topic:**[NLU intents](../concept/intents.md)

