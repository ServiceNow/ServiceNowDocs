---
title: NLU models
description: Use NLU models to apply ServiceNow Natural Language Understanding on your instances. Create, manage, test, and publish NLU models with the NLU Workbench.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# NLU models

Use NLU models to apply ServiceNow Natural Language Understanding on your instances. Create, manage, test, and publish NLU models with the NLU Workbench.

![Diagram for how user input is transformed into a system action.](../images/nlu-modelsm3.png "Overview of how user input is transformed to a system action")

A model is a collection of utterances, intents, entities, and vocabulary that the system uses to respond to natural language inputs from your users. The model takes the natural language input from your users and matches it to actions to be performed by the system.

The utterances in your model data are examples of what your users might ask for. These examples are used to train your model to recognize which system actions to perform in response. These system actions are called intents.

## Usage, roles, and navigation

Use the nlu\_admin role to access the NLU Workbench.

Navigate to **NLU Workbench** &gt; **Models**.

There are three tabs on the NLU Workbench homepage: Virtual Agent, Issue Auto Resolution, and AI Search. The Virtual Agent tab opens by default. Select the correct tab for your application.

![The homepage view of the Natural Language Understanding Workbench.](../images/natural-language-understanding-homepage-V.png)

You can use the **Search** field to look for models by name.

The default setting of the **All Languages** filter displays all models regardless of their language. You can filter models by language using the list in **All Languages**. To learn more about the available languages, see [NLU language support](nlu-language-support.md).

If you have a multilingual grouped model, its row in the list of models has an arrow on the left side. Select the arrow to expand the group so that all language versions of the model are displayed. For more information on model languages and grouping, see [Multilingual model management](multilingual-model-managent.md).![A grouped model expanded to show two language models, one for English and one for Brazilian Portuguese.](../images/nlu-modelsV2.png)

The **Used In VA** column indicates whether a model has already been linked to another application such as Virtual Agent. For AI Search, this column indicates whether the model has already been linked to a Genius Result. Similarly, the **Mapped Intents** column displays a count of intents that have been mapped or linked to Virtual Agent topics.

Scroll down the NLU Workbench homepage to view the **Boost your model performance** section. This section displays cards you can use to access functions that are available to your model type.![The Boost your model performance section of the model homepage, with two cards displayed.](../images/nlu-modelsV3.png)

## Model applications

The output of your NLU models can be consumed by the ServiceNow applications Virtual Agent, Issue Auto Resolution, and AI Search. The NLU Workbench homepage organizes each application's models by tab. In the list of models, different columns are displayed depending on the application.

## NLU Models for Virtual Agent

For more information on Virtual Agent, see [Virtual Agent](https://www.servicenow.com/docs/access?context=virtual-agent-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

-   The tab for Virtual Agent displays a list of models. Select a model name to open an overview page for that model.
-   The **Show Prebuilt Models** toggle is off by default. Switch this toggle on to display read-only models that can be copied and used as the basis for your custom models.
-   The **Boost your model performance** section displays a total of 5 cards for functions available to Virtual Agent.

## NLU Models for IAR

Fewer functions and columns are displayed for IAR than for the other applications in NLU Workbench. This is because the IAR model is prebuilt and is configured in the IAR Admin console.

-   When you select the name of your IAR model in NLU Workbench, you are taken to IAR Tuning rather than to a model overview. For more information, see [Issue Auto Resolution Tuning in NLU](issue-auto-resolution-tuning-nlu.md).
-   The **Show Prebuilt Models** toggle is not displayed.
-   The **Create new model** button is not displayed because the prebuilt model is used directly.
-   The section **Boost your model performance** is not displayed.

For more information on setting up IAR, see [Using Issue Auto Resolution](https://www.servicenow.com/docs/access?context=auto-resolution-va&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## NLU Models for AI Search

-   There is one prebuilt model for AI Search. You can copy this model as the basis for a custom model.
-   The **Show Prebuilt Models** toggle is on by default.
-   The **Create new model** button is available.
-   The **Boost your model performance** section displays two cards for functions available to AI Search.

For an introduction to managing AI Search in the NLU Workbench, watch the following video. A video on how to manage AI Search in the NLU Workbench.

For more information, see the [AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=australia&pubname=australia-platform-administration&ft:locale=en-US) landing page.

## What you can do next

To learn more about model content and the model life-cycle, see [Model management](model-management-phases.md).

**Parent Topic:**[Exploring Natural Language Understanding](nlu-explore.md)

