---
title: Import an NLU intent
description: As you create intents for your Natural Language Understanding \(NLU\) model, you can also import and reuse intents from other models in the same application scope. Reusing intents saves time when building new models.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [NLU intents, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Import an NLU intent

As you create intents for your Natural Language Understanding \(NLU\) model, you can also import and reuse intents from other models in the same application scope. Reusing intents saves time when building new models.

## Before you begin

-   Make sure that the NLU Workbench plugin, NLU Workbench - Core plugin, and Predictive Intelligence plugin are all installed and activated on your instance.
-   You can import intents for Virtual Agent and AI Search models.
-   Verify that the application scope of your source model and target model are the same.
-   Role required: nlu\_editor, nlu\_admin, or admin

## About this task

When you import an intent, the following associated items are also imported:

-   training utterances, with their entity annotations
-   entities

The following items are not included when importing an intent:

-   test utterances in the default test set
-   regular and pattern vocabulary

**Note:** You cannot import intents in the following situations:

-   When the model already has an intent with the same name as the intent you are trying to import.
-   When the model already has an entity with the same name but different attributes as what you are trying to import.

In this example scenario, you are building the content of your NLU model and you want to enhance the model by reusing intents from another model.

## Procedure

1.  Ensure that you are in the target application scope, and navigate to **All** &gt; **NLU Workbench** &gt; **Models**.

    The Virtual Agent tab opens by default.

2.  Select the tab for your model's application, then select the name of the model you want to add an intent to.

3.  In the model overview page, find the **Build and train your model** phase and select **View phase**.

4.  In the **Intents** tab, select **Import intents**.

    ![On the intents tab of the Build and train your model phase, the Import intents button is highlighted.](../images/import-intent01U.png)

    The **Import intents** screen appears, showing a list of NLU models from which you can select intents to import.

5.  Locate the intents you want to import, and select their check boxes.

    ![The Import Intents list displays intent names, the models they belong to, the count of associated training utterances, and the count of associated entities.](../images/import-intent02.png)

    In this scenario, you select the **OpenITTicket** intent in the ITSM NLU Model for Virtual Agent Conversations model.

6.  Select **Import**.

    **Result:** The **\#OpenITTticket** intent appears in the intents list of your target model. By importing this particular intent, you have added 29 additional training utterances to your model.


## What to do next

Review the annotations of the newly imported training utterances. Add vocabulary annotation if needed.

Train your model to save your updates. For issues with intents, see [Resolve intent issues](resolve-intent-issues.md).

If there are any secondary language models associated to your target model, consider importing and translating the new content. See [Import primary model content to a secondary model](import-primary-model-content-to-secondary-model.md).

For information about prebuilt Virtual Agent models that you can import from, see [Reusing intents from prebuilt NLU models](../concept/reusing-predefined-nlu-intents.md).

**Parent Topic:**[NLU intents](../concept/intents.md)

