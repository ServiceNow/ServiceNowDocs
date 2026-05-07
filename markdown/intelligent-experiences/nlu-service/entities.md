---
title: NLU entities
description: Entities provide your model with additional context when receiving user input. Add entities to your utterances and intents to improve the predictions of your Natural Language Understanding \(NLU\) model.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# NLU entities

Entities provide your model with additional context when receiving user input. Add entities to your utterances and intents to improve the predictions of your Natural Language Understanding \(NLU\) model.

Think of entities as the object of the action that the user wants to perform. The model interprets the utterance by matching it with an intent, but also uses entities to gather more details on the request.

For example, if a user types in `I have a critical issue with a slow laptop`, the system predicts a match to the intent \#TroubleshootSlowComputer. From this utterance, the model also identifies the following entities:

-   HARDWARE \(entity\) - laptop \(value\)
-   urgency \(entity\) - High \(value\)

![The Entities tab of the Build and train your model phase.](../images/entities01U.png)

NLU entities fall into two categories: system and user-defined. System entities such as DATE, TIME, and LOCATION are available by default in your instance. You can create your own user-defined entities to provide context relevant to your business.

There are five types of user-defined entities. Select one of the following links to learn more.

-   [Create a simple entity](../task/create-nlu-entities.md)
-   [Create a mapped entity](../task/create-mapped-entity-lookup-source.md)
-   [Create a pattern entity](../task/create-pattern-entity.md)
-   [Create a system-derived entity](../task/create-system-derived-entity.md)
-   [Create an open-ended entity](../task/create-open-ended-entity.md)

When you create entities, annotate them on utterances to provide examples to help your model learn. By annotating entities, you provide your model with linguistic associations and meaningful context for the system vocabulary. Annotations strengthen the relevance of entities and help your model perform the correct action in response to your users' inputs.

You add entities to your utterances when you are creating the intents. The entities then become associated to that intent, giving you the **Associated Intents** number.

## Regular expressions

Regular expressions \(regex\) help your model establish patterns that improve that model's ability to locate, match, and manage text. Use regular expressions with pattern entities to help your model understand formats such as email addresses, phone numbers, and incident numbers.

To learn more, see [Using regular expressions in entities](using-regular-expressions-nlu.md).

## Model availability

When you create an entity, you can choose to make the entity available for reuse by other intents in the model. If you didn't select the **Model availability** box when creating the entity, you can edit the entity afterwards.

On the Model details page, select **Entities**. Select the name of the entity to bring up the entity details page. Then, select the **Settings** tab.

![Settings tab of the Entity details page. Check the Model Availability box to make it available to all intents in the model.](../images/entities02.png "Entity settings page")

