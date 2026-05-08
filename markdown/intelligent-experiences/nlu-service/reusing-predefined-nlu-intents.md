---
title: Reusing intents from prebuilt NLU models
description: Reuse Natural Language Understanding \(NLU\) intents by importing them from a prebuilt NLU model to other models. Reusing intents saves time when building your models.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: concept
last_updated: "2026-04-16"
reading_time_minutes: 2
breadcrumb: [NLU intents, Build and train your model, Model management, Natural Language Understanding, Enable AI experiences]
---

# Reusing intents from prebuilt NLU models

Reuse Natural Language Understanding \(NLU\) intents by importing them from a prebuilt NLU model to other models. Reusing intents saves time when building your models.

Prebuilt Virtual Agent NLU models provide language understanding needed for chatbot conversation flows in ITSM, CSM, and HR topics. Each NLU intent in these models maps to a single Virtual Agent conversation topic created in Virtual Agent Designer accordingly.

The prebuilt models are read-only, but contain validated intents that you can reuse in your NLU models. For example, the prebuilt HR model for Virtual Agent contains several intents regarding HR requests. Adding the intents to one of your models makes that model ready to respond to user inputs regarding HR.

## Prebuilt Virtual Agent model content

Each of the prebuilt Virtual Agent models uses language that's pertinent to their respective business unit \(BU\). The NLU that processes this language, built from a word corpus of 3 million words, is context-aware of general linguistic patterns and both ServiceNow and user-defined vocabularies.

The prebuilt models map to common conversation topics used by Virtual Agent chatbots across each of the three BUs. Those topics correspond with intents that perform BU-specific actions.

For more NLU and Virtual Agent context, refer to the following product documentation:

-   For ITSM context, see ITSM Virtual Agent.
-   For HR context, see Virtual Agent for HR Service Delivery.
-   For CSM context, see Customer Service Virtual Agent conversations.

## Virtual Agent and NLU plugins and roles

To access the prebuilt Virtual Agent models in the NLU Workbench, you must install and activate these plugins using the admin role.

<table id="table_tb3_pk5_f3b"><thead><tr><th>

Plugins

</th><th>

Descriptions

</th></tr></thead><tbody><tr><td>

-   CSM Virtual Agent conversations \[com.sn\_csm.virtualagent\]
-   Human Resources Scoped App: Virtual Agent Conversations \[com.sn\_hr\_virtual\_agent\]
-   ITSM Virtual Agent conversations \[com.snc.itsm.virtualagent\]

</td><td>

Enables Pre-built Virtual Agent topics, topic blocks, and ServiceNow NLU models for the Customer Service Management, HR Service Delivery, and IT Service Management applications.

 -   Requires the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin to be activated.
-   Automatically activates the NLU Workbench \(com.snc.nlu\_studio\) plugin.

</td></tr></tbody>
</table>## Creating NLU models that reuse predefined Virtual Agent intents

The prebuilt Virtual Agent models are set to read-only and can't be edited. However, the intents in these models can be imported into your new model, alongside any new intents you've created in your model. You can also copy the prebuilt model and use the intents as a foundation for a new model.

To reuse the intents from a prebuilt Virtual Agent model, choose the prebuilt model when importing intents. See [Import an NLU intent](../task/import-nlu-intent.md).

NLU models and their intents and entities are associated to an application scope. The scope can't be changed later, so verify your target application scope before you begin.

