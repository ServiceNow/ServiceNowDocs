---
title: Virtual Agent and NLU Workbench integration
description: Virtual Agent administrators can access and update their NLU models from within the Virtual Agent Designer user interface.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Natural Language Understanding, Enable AI experiences]
---

# Virtual Agent and NLU Workbench integration

Virtual Agent administrators can access and update their NLU models from within the Virtual Agent Designer user interface.

![Diagram of NLU and Virtual Agent authoring.](../images/nlu-va-integration.png)

**Note:** If you have Now Assist in Virtual Agent, you can continue to use your existing NLU topics and migrate them into new LLM topics using the topic migration feature within Virtual Agent Designer. For more information on topic migration, see [Migrate NLU topics to LLM topics](https://www.servicenow.com/docs/access?context=migrate-nlu-llm&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Integration setup tasks, roles, and details

As Virtual Agent administrators create and configure their conversation topics, they must first create their NLU model and its associated intents in the NLU Workbench. This action requires they use the NLU Workbench and the admin or nlu\_admin role.

In addition, they must also complete the following tasks in Virtual Agent **General Settings**.

-   Enable NLU.
-   Select the NLU service provider.
-   If using language-specific NLU models, enable the languages for those models.

Virtual Agent administrators must also apply their NLU model to a conversation topic by completing the following tasks in Virtual Agent Designer:

-   In **Topic Properties**, select the NLU model, the NLU intent, and the topic switching behavior.
-   For input controls used in the topic flow, set the NLU properties for entity extraction.

Optionally, admins can activate Dialog Acts to enable Virtual Agent to respond flexibly when users make a modification in mid-conversation. Currently available response types are Modify, Affirm, and Negate, based on the last 5 exchanges in the conversation. Dialog Acts can be configured for English only, in Topic Properties. For more information see [Dialog Acts for Virtual Agent](https://www.servicenow.com/docs/access?context=c_dialog-acts&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

After the NLU model is complete and associated with a Virtual Agent conversation topic, administrators with the virtual\_agent\_admin or admin role can do the following from within the Virtual Agent Designer user interface.

-   Update NLU intent utterances.
-   Train, test, and publish the NLU model.

For more information, see [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent](https://www.servicenow.com/docs/access?context=va-NLU&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US).

## Publishing topics from Virtual Agent

When your model is published in the NLU Workbench, it's ready to use in Virtual Agent Designer. When editing a topic, click the **Properties** tab to select a model and intent to map to that topic.

![Natural Language Understanding section of the Properties tab of Virtual Agent Designer.](../images/nlu-va-integrationT3.png)

When you click **Publish**, the model and intent are mapped to that topic and published seamlessly.

Publishing a topic with a mapped intent fails for the following reasons:

-   Model isn't trained, or training is in progress.
-   The last trained model is already published with a VA topic.
-   The intent is not enabled in the model.

**Parent Topic:**[Natural Language Understanding](nlu-landing.md)

