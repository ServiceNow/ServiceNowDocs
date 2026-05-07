---
title: Creating models
description: Creating models is the first step to taking advantage of Natural Language Understanding \(NLU\) in your instances. Create models for Virtual Agent and AI Search in the NLU Workbench.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Model management, Natural Language Understanding, Enable AI experiences]
---

# Creating models

Creating models is the first step to taking advantage of Natural Language Understanding \(NLU\) in your instances. Create models for Virtual Agent and AI Search in the NLU Workbench.

You create NLU models for consumption by the ServiceNow applications Virtual Agent or AI Search.

**Note:** For Issue Auto Resolution, a prebuilt model is provided for you to configure.

To start creating models, set your scope to the application scope you want for your new model. Then navigate to **NLU Workbench** &gt; **Models**. The Virtual Agent tab opens by default. Select the appropriate tab for the model you want to create.

![In the Virtual Agent tab of the NLU Homepage, the Create new model button is highlighted.](../images/creating-models1V.png)

## New model creation

When you select the **Create new model** button, a modal opens to display your model creation options. Start by selecting one of the icons:![The modal for 'How do you want to create your model?' displays three selectable tiles: Use prebuilt model, Import data from a CSV, Start from blank.](../images/creating-models2V.png)

-   [Create an NLU model using a pre-built model](../task/create-nlu-model-prebuilt.md): Copy a prebuilt model and its contents as a starting point for your new model.
-   [Create an NLU model from a CSV file](../task/create-nlu-model-csv.md): Upload a CSV file containing a list of intents and corresponding utterances.
-   [Create an NLU model from blank](../task/create-nlu-modelx.md): Build a model from scratch and add intents and utterances as you go.

After creating, add content to your model. The intents, utterances, entities, and vocabulary you add helps improve the model's ability to interpret natural language. See [Build and train your model](managing-model-content.md).

## Duplicating, exporting, and updating

After creating a model, you have options to use that model across other models and instances. With the NLU Workbench, you can perform the following actions with your models:

-   [Duplicate an NLU model](../task/clone-nlu-model.md): Copy a model to create a model with the same content.
-   [Export an NLU model](../task/export-nlu-model.md): Export a model as a CSV file containing the associated utterances and intents. Share the model or use it to create one.
-   [Add an NLU model to an update set](../task/add-model-update-set.md): Add a model and its artifacts to an update set to transfer the model across instances.

