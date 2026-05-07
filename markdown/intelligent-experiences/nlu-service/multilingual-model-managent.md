---
title: Multilingual model management
description: Use multilingual Natural Language Understanding \(NLU\) models for the system to understand user input in several languages. The NLU Workbench helps you manage and maintain a consistent structure for content across languages to provide a unified experience.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-04-21"
reading_time_minutes: 5
breadcrumb: [Natural Language Understanding, Enable AI experiences]
---

# Multilingual model management

Use multilingual Natural Language Understanding \(NLU\) models for the system to understand user input in several languages. The NLU Workbench helps you manage and maintain a consistent structure for content across languages to provide a unified experience.

## Primary and secondary languages

A primary language is the source language you choose when creating a model. These models are considered primary models. Primary models can then be translated into different languages. Those translated models are referred to as secondary models. The languages in which they are translated are referred to as secondary languages.

The NLU Workbench home displays primary and secondary language models nested under the model name. Select the arrow to the left of the model name to expand the language group.

![On the NLU Workbench homepage, VA tab, one grouped model is expanded to show two different languages.](../images/nlu-modelsV2.png)

Multilingual model management provides a way for you to group, oversee, and update your NLU models. The designation for the model language works as follows:

-   Primary models have a language you assign to them during model creation and listed as English \(Primary\). The language of the primary model is the source language for the translations that follow later in the secondary models.
-   Secondary models are translated copies of the primary model. Each secondary model uses a different language, such as Brazilian Portuguese, Polish, or Finnish.
-   Any supported language can be the primary language for a primary model or the secondary language for a secondary model.
-   Within a model group, you can't have two secondary models that use the same language.

For more information on the languages available in NLU, see [NLU language support](nlu-language-support.md).

## Implementing language grouping

Grouping languages is optional but helps with organizing various language versions of models. There are two methods for ensuring that model languages are grouped:

-   You can add a language to a primary model in the model's More options menu, which automatically creates a secondary language model with translation options. For more information on adding and translating a language, see [Translate a multilingual model](../task/translate-multilingual-model.md).
-   You can access the instance model migration page directly by visiting `<instance_name>.service-now.com/$nlu-studio.do#/model-migration`. For more information on language grouping using this method, see [Model language grouping](../reference/model-language-grouping.md).

## Primary and secondary model interactions

To ensure consistency within a model group, the names of intents and entities in all secondary models are the same as the content in the primary model. New intents can only be created in a primary model. Creating an intent in a primary model adds the intent to all the secondary models within the model group, but without any utterances in them. New intents are inactive by default. New entities can also be created in secondary models for languages that support entities. Adding an entity in a primary model creates it across all secondary models within the model group, if valid.

When you add an intent to a primary model, the intent is added to all of its secondary models. Every intent in a secondary model is mapped to its corresponding intent in the primary model. The mapping of intents ensures that any application that uses these intents can access all the secondary intents through their corresponding primary intents.

When you delete an intent or entity in a primary model, its corresponding intents and entities are also deleted in its secondary models. Therefore, the secondary models follow the status of the primary model content. Although you can't delete intents in secondary models, you can deactivate them.

For more information on intent interactions, see [Import primary model content to a secondary model](../task/import-primary-model-content-to-secondary-model.md).

You can't delete an entity created in a secondary model if it's a copy of a corresponding entity created in the primary model. However, you can add or delete an entity in a secondary model if it doesn't have a corresponding entity in the primary model.

Whenever you translate a model or add intents and entities to secondary models, the model must be reviewed. Secondary models marked with **Needs review** must be manually reviewed before publishing.

![Models page in the NLU Workbench with secondary models that need reviewing.](../images/multilingual-model02.png "Viewing secondary models that need reviewing")

If every intent in a secondary model is deactivated, then the **Train** and **Try** buttons are also deactivated in the model. However, even if only one intent is enabled in the model, then you can train and test the model. Ensure that some intents are enabled in your secondary models to translate them.

**Note:** When training and testing, prediction scores for similar utterances across primary and secondary models can be different. The context comes across differently among languages due to inherent structural variations.

When looking at a model, you can navigate between languages in the model group. On a Model details page, use the **Model language** drop-down list to navigate to other models.

![Model details page with the Model language drop-down list.](../images/multilingual-model05.png "Viewing model languages list")

## Duplicating grouped models and model groups

Using the nlu\_admin role, you can duplicate primary models, secondary models, and entire model groups. You can duplicate just the primary model or a set of secondary models from among the model group.

Following is a list of system behaviors you may encounter when you duplicate these models.

-   If you duplicate a secondary model that's in a model group, the duplicated version becomes a separate primary model that is outside that model group.
-   All intents are duplicated. The duplicated intent maintains the same **Enabled** status as the original intent.
-   When duplicating a primary model, you can duplicate a set of secondary models, or all of the secondary models along with it. This action creates a model group comprised of duplicated versions with the respective original models marked as the source models.
-   When duplicating a model group, you can choose an existing secondary model to be the primary model for the duplicated group.
-   If you select a secondary model in an existing model group as a new primary model while duplicating the group, all the deactivated entities are enabled for the duplicated version of the secondary model. The secondary model becomes the primary model in the new duplicated model group.
-   If you duplicate a primary model without any secondary model, the duplicated version becomes a separate primary model.

For more information, see [Duplicate an NLU model](../task/clone-nlu-model.md).

