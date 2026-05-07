---
title: Create an NLU model from blank
description: Create a Natural Language Understanding \(NLU\) model from scratch. Start with an empty model to have full control over the model's content.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create an NLU model from blank

Create a Natural Language Understanding \(NLU\) model from scratch. Start with an empty model to have full control over the model's content.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   You can create NLU models for Virtual Agent and AI Search.
-   Role required: nlu\_admin or admin

## About this task

In this example procedure, you're building an NLU model to help Virtual Agent understand human-expressed intent regarding Human Resources.

## Procedure

1.  Set your scope to the application scope you want for your model.

2.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

3.  Select the tab for the type of model you want to create, such as AI Search.

4.  Select the **Create new model** button.

5.  In the **Add some details** window, select the **Start from blank** button.

6.  In the define details page, enter a unique **Name** and **Short description**.

    ![Window for creating an NLU model from blank. Fill in the model details such as the language and purpose.](../images/create-model-x.png)

    In this example scenario, you enter `HR Model for Virtual Agent` for the name and `Natural language for Human Resources user requests` for the description.

7.  Select the language and purpose from the drop-down lists.

    In this example scenario, select `English` and `Virtual Agent`.

8.  Select a business area for your model.

9.  Select **Next**.

    Your model starts building. When complete, select **View model** to open the **Model details** page for your new model.


## What to do next

![Model details page after creating a model from blank.](../images/create-nlu-model-blank03.png "Model details page")

Your new model contains no content. Select **Add content** to begin adding intents, entities, and vocabulary. For more information, see [Build and train your model](../concept/managing-model-content.md).

Add test utterances and intents to build the model's default test set. For more information, see [Test set creation and management](../concept/nlu-test-set-creation-management.md).

