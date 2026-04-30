---
title: Build and train your model
description: After creating a model, build the model's content by adding intents, entities, vocabulary, and test set utterances. Your NLU model content determines how the model responds to user inputs.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Model management, Natural Language Understanding, Enable AI experiences]
---

# Build and train your model

After creating a model, build the model's content by adding intents, entities, vocabulary, and test set utterances. Your NLU model content determines how the model responds to user inputs.

Models are made up of the following content:

-   Intents: An action the user wants to do or wants the application to do.
-   Entities: Object or context for an action.
-   Vocabulary: Add vocabulary to help your model understand the range of words in your users' utterances.
-   Test set: To assess model performance, add test utterances and the intents that you expect to be predicted for those utterances.

To access the model content, navigate to **NLU Workbench** &gt; **Models**. The Virtual Agent tab opens by default. Select the tab for your model's application and then select the name of the model to open the **Model details** page. In the **Build and train your model** card, select **View phase**.

![The phase for Build and train your model](../images/managing-model-content2.png)

## Intents

When your model receives user input, it uses an intent to perform a system action. For example, a user types in `I have a critical issue with a slow laptop`. The model matches the utterance input to the intent \#TroubleshootSlowComputer. If the intent is linked to a Virtual Agent topic, it triggers further action.

Intents contain training utterances, or examples of user inputs that would trigger the system action. Provide realistic utterances that the model might encounter from your users. The quality of training utterances affects the accuracy of your model.

For more information, see [NLU intents](intents.md).

## Entities

Your intents use entities to provide additional context for the model when receiving inputs. In the computer example, the laptop is the entity, or object of, the action.

NLU entities fall into two categories: system-defined and user-defined. System entities such as DATE, TIME, and LOCATION are available by default in your instance. You can create your own user-defined entities to provide additional associations and meaning for your business requirements.

All entities are reusable across other NLU models. However, you must add them to a training utterance for each model to use them.

For more information, see [NLU entities](entities.md).

## Vocabulary

Your users' input may contain a wide variety of words and phrases. Also, your model may not understand some terms used in specialized domains or business areas.

To improve your model's ability to understand a wide range of user input, you can define synonyms by creating vocabulary items.

For example, your model includes an entity for the term computer. When a user types in `I need a new computer`, the model knows how to respond. However, if a user enters `laptop` or `workstation`, the model might fail to predict the intent. You can add vocabulary to the model to train it to understand synonyms and variations.

You can also use tables and lists as vocabulary sources. Your models can look up the vocabulary sources when predicting intents.

For more information, see [NLU vocabulary](using-nlu-vocabulary.md).

## Test set

Your model contains a default test set that you can use to evaluate the model’s performance. Initially the test set is empty, ready to be populated with your content. Add test utterances and their expected intents to build the test set.

For more information, see [Test set creation and management](nlu-test-set-creation-management.md).

## Test panel

Access the test panel by clicking **Train model** or **Try model** in the **Build and train your model** phase. Training incorporates new content into your model. With **Try model**, you can manually enter individual utterances to test what intents the model predicts for them.

For more information, see [Train and try your NLU model](../task/test-train-nlu-model.md).

You can also use the test panel to provide feedback on your model's predictions. Your feedback helps improve intent prediction. See [Test panel feedback](test-model-panel-feedback.md).

## Settings

Use the **Settings** tab to edit the name, short description, and confidence threshold of the model. You can't change the language or purpose of the model.

![Settings tab of an example model.](../images/managing-model-contentT1.png)

For more information on the confidence threshold, see [Test and publish your model](testing-your-model.md). For more information on Settings, see [NLU model settings](nlu-model-settings.md).

-   **[NLU intents](intents.md)**  
Intents drive your models' responses by matching a system action to user inputs. Models with good intents help Virtual Agent and Search respond to your users accurately.
-   **[NLU entities](entities.md)**  
Entities provide your model with additional context when receiving user input. Add entities to your utterances and intents to improve the predictions of your Natural Language Understanding \(NLU\) model.
-   **[NLU vocabulary](using-nlu-vocabulary.md)**  
Use NLU vocabulary items to help the system recognize the various ways your users express their requests. Use vocabulary sources to help the system recognize objects in tables or lists, such as names of conference rooms or catalog items.
-   **[Test set creation and management](nlu-test-set-creation-management.md)**  
Use the default test set of your NLU model to test the model's performance and accuracy. Manage your test set over time by building or updating its content in the NLU Workbench.
-   **[Train and try your NLU model](../task/test-train-nlu-model.md)**  
Train and try your model iteratively so that its intents and entities are validated, compiled, and saved to your model.
-   **[Test panel feedback](test-model-panel-feedback.md)**  
When testing your NLU model on the Try model section of the test panel, use this feature to provide feedback on the model's intent predictions.

**Parent Topic:**[Model management](model-management-phases.md)

