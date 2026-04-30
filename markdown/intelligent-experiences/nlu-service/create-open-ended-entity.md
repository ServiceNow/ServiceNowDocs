---
title: Create an open-ended entity
description: Use an open-ended entity when you want to improve intent prediction accuracy. Open-ended entities help your model focus on the context of the utterances.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create an open-ended entity

Use an open-ended entity when you want to improve intent prediction accuracy. Open-ended entities help your model focus on the context of the utterances.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model for Virtual Agent or AI Search.
-   Create or use an existing intent.
-   Role required: nlu\_editor, nlu\_admin, or admin. The nlu\_editor must be assigned to the model.

## About this task

Open-ended entities tell the model to focus on the context of the entity rather than the entity itself. When you mark a word or phrase as open-ended, the system skips the entity and predicts the intent from the context that precedes or follows the entity in the utterance.

For example, in the utterance `I want to order an iPhone`, you annotate the words "an iPhone" as an open-ended entity. The model focuses on the context, predicting the user wants to order something. Since there are numerous things the user could want to order, naming all of them would be an unbearable task for the model author.

Using an open-ended entity instead of a simple entity helps the model focus on the rest of the utterance and not the entity. In the iPhone example, the entity itself is less relevant; so you want the system to ignore it.

In other scenarios you should use a simple entity, as there could be multiple intents where you shouldn't have the system ignore the entity.

**Note:** You can't annotate a vocabulary source \(referenced by @vocab\_source in an utterance\) as an open ended entity. You can only annotate a vocabulary source as a simple entity or a mapped entity. For example, if the utterance is “I want to order a laptop”, then the word “laptop” can be annotated as an open ended entity. However, if the utterance is “I want to order @laptop” where @laptop refers to a table vocabulary source or a list vocabulary source, it can't be annotated as an open ended entity.

For this example scenario, you've created an NLU model with an intent for your users to order company merchandise.

In the following example procedure, you create an entity from one of your utterances so the system can recognize it as open-ended and reusable in other NLU models in your instance.

**Note:** You can use only one open-ended entity per intent.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then select the name of your model.

3.  On the Model details page, click **Intents**.

4.  Select the name of the intent you want to add the entity to.

    For this example, you select the \#OrderMerch intent.

5.  In the Utterances tab, select a word or phrase of one of the utterances to bring up the entities window.

    For this example, you select a hoodie.

    ![Entity window in the Utterances tab of the Intent details page.](../images/create-open1.png "Entity window")

6.  Select **Create New Entity**

7.  On the Create a new entity screen, configure the fields.

    For this example, use the following configurations:

    -   **Entity Name**: `merch`
    -   **Type**: Select **Open-Ended**
    ![Create a new entity window for an open-ended entity.](../images/create-open2.png "Create entity")

8.  Select **Save**.

    The merch open-ended entity is annotated in the Utterances section of your model's Intent screen. When you point to its name, you can see that it persists as a new entity in the annotation details. This entity is reusable in all other NLU models in your instance.

    ![Entity window with your newly created open-ended entity.](../images/create-open3.png)


## What to do next

Train your model to save the entities. You can try your model to see if it interprets the utterance based on the context of the entity, rather than the entity itself.

For this example, you can test your model with a different merchandise item.

1.  Select **Try Model**.
2.  Enter `I want to order a polo`.
3.  Select **Go**.

![Utterances tab of the Intent details page with the Try model panel open. Try your model after training it to see if your new entity works.](../images/create-open4.png)

The model predicts the intent and shows that it used the merch entity for the a polo value.

**Parent Topic:**[NLU entities](../concept/entities.md)

**Related topics**  


[Create a simple entity](create-nlu-entities.md)

[Create a mapped entity](create-mapped-entity-lookup-source.md)

[Create a pattern entity](create-pattern-entity.md)

[Create a system-derived entity](create-system-derived-entity.md)

[Import entities](import-common-entities-nlu.md)

[Using regular expressions in entities](../concept/using-regular-expressions-nlu.md)

