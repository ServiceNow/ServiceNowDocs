---
title: NLU intents
description: Intents drive your models' responses by matching a system action to user inputs. Models with good intents help Virtual Agent and Search respond to your users accurately.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# NLU intents

Intents drive your models' responses by matching a system action to user inputs. Models with good intents help Virtual Agent and Search respond to your users accurately.

Think of intents as the core that drives the comprehension of natural language. Intents help the models translate utterances from your users into actions that the system can perform. Intents perform best if your utterances, entities, and vocabulary work together to support your model. Using vocabulary and realistic utterance examples can help the system to be more accurate when predicting intents.

When creating your Natural Language Understanding \(NLU\) model, you add intents to match user inputs with system actions. The more intents that a model has, the more actions it can take when it receives utterances from your users. Model intents can perform various actions, from creating hardware service requests to adding users to groups.

To access your model's intents, navigate to a model's overview page. In the **Build and train your model** phase, select **View phase**. The **Intents** tab shows by default.

![Intents tab of the Build and train your model phase](../images/intents05.png)

A model can contain up to 750 intents. However, models with over 300 intents or 4500 utterances, whichever comes first, take longer to train, test, and publish.

**Note:** As you create intents, keep in mind that they can sometimes impact each other. For example, you build and test an intent that works on one or two utterances. But when you test it in a larger intent environment, it might behave differently. To reduce the likelihood of such an event, you may want to create at least five intents in a model before you start proper testing.

To start adding content to your model, see [Create an NLU intent](../task/create-nlu-intent.md).

The **Enabled** column shows whether or not the intent is active in predictions. An NLU admin can deactivate an individual intent but keep it in the model.

However, if an intent is mapped to a published Virtual Agent topic:

-   You cannot deactivate the intent.
-   You cannot delete the intent.

After changing the **Enabled** status of an intent, retrain the model.

## Utterances

Intents contain training utterances, which are examples of inputs that the model may see from your users. Each intent in a model has its own utterances. When trained, the model learns to recognize similar utterances from your users and then respond with the matching intent.

Select an intent to access the intent details page. The **Utterances** tab lists all the utterances currently in the intent.

![Utterances tab for an example intent.](../images/intents06.png)

After adding utterances, you can edit, copy, move, or delete the utterances using the icons in the right column. You can move or delete multiple utterances by selecting the box on the left first and using the **Perform action on selected rows** button.

Here are some things to consider when adding utterances to intents:

-   A model must have at least 1 intent, with a minimum of 5 utterances in each intent.
-   An intent needs at least 5 utterances to begin training.
-   The system currently supports utterances up to 25 words or 200 characters. Utterances that exceed that limit fail to return an intent prediction.
-   The system currently supports up to 20,000 utterances in a single model.
-   Models with more than 4,500 utterances take longer to train, test, and publish.

Provide vocabulary for any words or phrases that are relevant to your organization or domain when adding utterances to your model. The vocabulary helps with intent prediction for words and phrases that your users are likely to use. You can use the @ symbol when adding an utterance to call on a vocabulary source. For more context and examples, see [NLU vocabulary](using-nlu-vocabulary.md).

## Associated entities

Your model uses entities to provide additional context and meaning when predicting user input. You add entities to the training utterances of your intent to provide the system with more information to perform the intended action.

![The Associated entities tab for an example intent.](../images/intents07.png)

For more information, see [NLU entities](entities.md).

## Intent issues

Building large models increases the chance that intents overlap, conflict, or fail to contain enough training utterances. For example, the utterance examples in one intent may end up identical to the examples in another intent. If your intents conflict, the model may not know which intent to predict when receiving user input.

If your model has issues or conflicts, the **Intents** page displays cards showing the number of intents affected. ![In the Intents tab of the Build and train your model phase, the issue cards are highlighted.](../images/resolve-intent-issues001V.png)

Select a card to see a filtered list of intents with that issue. Resolving issues ensures that your intents meet the requirements and work as intended.

For more information, see [Resolve intent issues](../task/resolve-intent-issues.md).

-   **[Create an NLU intent](../task/create-nlu-intent.md)**  
Create an intent for your Natural Language Understanding \(NLU\) model. Intents provide your model with a system action to perform when it receives user input.
-   **[Reusing intents from prebuilt NLU models](reusing-predefined-nlu-intents.md)**  
Reuse Natural Language Understanding \(NLU\) intents by importing them from a prebuilt NLU model to other models. Reusing intents saves time when building your models.
-   **[Import an NLU intent](../task/import-nlu-intent.md)**  
As you create intents for your Natural Language Understanding \(NLU\) model, you can also import and reuse intents from other models in the same application scope. Reusing intents saves time when building new models.
-   **[Resolve intent issues](../task/resolve-intent-issues.md)**  
Use the issue cards to identify intents that have conflicts, need reviewing, or need more utterances. Resolving intent issues ensures the intents in your Natural Language Understanding \(NLU\) models work properly.

**Parent Topic:**[Build and train your model](managing-model-content.md)

