---
title: Import entities
description: Reuse entities that you have created across your other Natural Language Understanding \(NLU\) models. Importing entities saves time and helps improve the intents in your model.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [NLU entities, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Import entities

Reuse entities that you have created across your other Natural Language Understanding \(NLU\) models. Importing entities saves time and helps improve the intents in your model.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, NLU Common Model plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   Create or use an existing NLU model.
-   Create or use existing intents and entities.
-   Role required: nlu\_editor, nlu\_admin, or admin. The nlu\_editor must be assigned to the model.

## About this task

New entities are usually created inside an individual intent. To help save time and improve your intents, you can also reuse entities from your other models by importing them. After importing entities into a model, annotate the model's utterances using the new entities.

**Note:** All models include several system entities by default.

In this example procedure, you are importing several entities to a new model.

## Procedure

1.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab corresponding to your model's application, then select the name of the model you want to add entities to.

3.  In the **Build and train your model** phase, select the **Entities** tab.

4.  Select **Import entity**.

    ![On the Entities tab of the Build and train your model phase, the Import entity button is highlighted.](../images/import-entities1U.png)

5.  In the Import Entity window, select the entities you want to import.

    In this example, you click the drop-down arrow for Application: HR Service Delivery NLU Model for Virtual Agent Conversations. Select the four entities.

    ![Import Entity window. The applications refer to other models.](../images/import-entites2.png)

    **Note:** Importing entities does not import any utterances that are annotated with those entities. You must annotate your current model's utterances using the new imported entities, then retrain the model.

6.  Click **Import**.

    The selected entities import to the model. The entities appear under **User Defined Entities** in the Entities tab. By default, **Model Availability** will be enabled so that all intents in the model can use the entity.

    ![Entities tab of the Manage your model content page with your imported entities.](../images/import-entities3.png)


## What to do next

Use the imported entities to annotate the utterances of the model. Train your model to save your changes.

**Related topics**  


[Import an NLU intent](import-nlu-intent.md)

