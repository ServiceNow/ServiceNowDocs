---
title: Create an NLU model using a pre-built model
description: Use the prebuilt Natural Language Understanding \(NLU\) models in the NLU Workbench to create a new one.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating models, Model management, Natural Language Understanding, Enable AI experiences]
---

# Create an NLU model using a pre-built model

Use the prebuilt Natural Language Understanding \(NLU\) models in the NLU Workbench to create a new one.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   You can create NLU models for Virtual Agent and AI Search.
-   Role required: nlu\_admin or admin.

## About this task

In this example procedure, you're building an NLU model based on the prebuilt HR NLU for VA model. You base your model on the prebuilt model, then edit or add to the model content to meet your business requirements.

Your new model contains intents, entities, and vocabulary from the prebuilt model. The new model also contains an empty default test set, ready to be populated with test utterances.

## Procedure

1.  Set your scope to the application scope you want for your new model.

2.  Navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

3.  Select the tab for the type of model you want to create, such as AI Search.

4.  Select the **Create new model** button.

5.  In the **How do you want to create your model?** window, select **Use prebuilt model**.

6.  On the **Add some details** window, fill in the **Name** and **Short description** for the model.

    ![Define details page for creating a model using a pre-built model.](../images/create-nlu-model-pre2.png)

    In this example scenario, you enter `Human Resources VA Model` for the name and `Virtual Agent Model for responding to HR Requests` for the short description.

7.  Select the language and purpose from the drop-down lists.

    In this example scenario, you select `English` and `Virtual Agent`.

8.  Select the business area for the model.

    In this example scenario, you select `HR`.

9.  Click **Next**.

10. Select the prebuilt model from the drop-down list.

    ![Select a pre-built model screen.](../images/create-nlu-model-pre3.png)

    In this example scenario, you select `HR NLU for VA`.

11. Select **Next**.

12. On the **Select intents** screen, select the prebuilt intents to add to your model.

    ![Select intents screen with several intents selected.](../images/create-nlu-model-pre4.png)

    In this example scenario, you select 10 intents from the list.

    **Note:** You can select all the prebuilt intents by checking the **Intent** box at the top of the list.

13. Select **Next**.

    Your model starts building. After completion, select **View model** to open the **Model details** page for your new model.


## What to do next

Add more intents and training utterances to continue building the model. Update entities and vocabulary to help the model understand inputs from your users. For more information, see [Build and train your model](../concept/managing-model-content.md).

Add test utterances and intents to build the model's default test set. For more information, see [Test set creation and management](../concept/nlu-test-set-creation-management.md).

