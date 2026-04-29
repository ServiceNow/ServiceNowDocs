---
title: Create a simple entity
description: Create one or more simple entities from words in your utterance examples. An entity is an object of, or context for, an action.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create a simple entity

Create one or more simple entities from words in your utterance examples. An entity is an object of, or context for, an action.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model for Virtual Agent or AI Search.
-   Create or use an existing intent.
-   Role required: nlu\_editor, nlu\_admin, or admin. The nlu\_editor must be assigned to the model.

## About this task

Simple entities are words or phrases whose value can be extracted by your model. Simple entities are identified based on the context in which the entity is used in an utterance.

For the following example procedure, you've already created an intent that's titled SubmitAccessRequest and you're creating a simple entity for the type of access the user is requesting.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then the name of the model you want to add an entity to.

    For this example, you choose the NLU for Access Requests model.

3.  In the **Build and train your model** card, click **View phase**.

4.  In the intents tab, click the name of the intent.

    For this example, you click SubmitAccessRequest.

5.  Click a word in one of the utterances to bring up the entity window.

    For this example, click the word parking garage.

    ![Utterances tab of the intent details page with the entity window open.](../images/create-entites1.png)

6.  Click **Create New Entity**.

7.  In the Create a new entity screen, enter a name and select the **Simple** entity type.

    For this example, you enter `buildingaccess` for the **Entity Name**.

    ![Create a new entity window.](../images/create-entites2.png)

    **Note:** Select **Model availability** to make the entity available to every intent in the model. If you check the box, the entity shows in the **Associated Entities** tab.

8.  Click **Save**.

    The entity saves and the words in the utterance remain highlighted.


## What to do next

Your utterances can reference a vocabulary source by using the @ handle. If you have a list of values that are defined in a vocabulary source, you can annotate the @ handle as a simple entity to extract it rather than repeating the utterance for all of the values. The referenced vocabulary source can be a table or a list. For example, the following image shows how you invoke a vocabulary source that lists various conference room names.

![How to reference a vocabulary source from within an utterance.](../images/create-simple-entity0.png "Example utterance using a vocabulary source")

For more information, see [NLU vocabulary](../concept/using-nlu-vocabulary.md).

**Parent Topic:**[NLU entities](../concept/entities.md)

**Related topics**  


[Create a mapped entity](create-mapped-entity-lookup-source.md)

[Create a pattern entity](create-pattern-entity.md)

[Create a system-derived entity](create-system-derived-entity.md)

[Create an open-ended entity](create-open-ended-entity.md)

[Import entities](import-common-entities-nlu.md)

[Using regular expressions in entities](../concept/using-regular-expressions-nlu.md)

