---
title: Natural Language Understanding
description: ServiceNow Natural Language Understanding \(NLU\) provides an NLU Workbench and an NLU inference service that you can use to enable the system to learn and respond to human-expressed intent. By entering natural language examples into the system, you help it understand word meanings and contexts so it can infer user or system actions.
locale: en-US
release: australia
product: NLU Service
classification: nlu-service
topic_type: reference
last_updated: "2026-04-23"
reading_time_minutes: 4
breadcrumb: [Enable AI experiences]
---

# Natural Language Understanding

ServiceNow® Natural Language Understanding \(NLU\) provides an NLU Workbench and an NLU inference service that you can use to enable the system to learn and respond to human-expressed intent. By entering natural language examples into the system, you help it understand word meanings and contexts so it can infer user or system actions.

## Overview of Natural Language Understanding

For an overview of Natural Language Understanding, see [Exploring Natural Language Understanding](nlu-explore.md).

## NLU terminology

In NLU parlance, these terms identify the key language components the system uses to classify, parse, and otherwise process natural language content.

-   **Intent**

    Something a user wants to do or what you want your application to handle, such as granting access.

-   **Utterance**

    A natural language example of a user intent. For example, a text string in an incident's short description, a chat entry, or an email subject line. Utterances are used to build and train intents and should therefore not include several or ambiguous meanings or intents.

-   **Entity**

    The object of, or context for, an action. For example: a laptop, a user role, or a priority level.

-   **System entity**

    These are predefined in an instance and have highly reusable meanings, such as date, time, and location.

-   **User defined entity**

    These are created in the system by users and can be built from words in the utterances they create.

-   **Common Entity**

    A context commonly used and extracted via a pre-defined entity model, such as currency, organization, people, or quantity.

-   **Vocabulary**

    Vocabulary is used to define or overwrite word meanings. For example, you can assign the synonym “Microsoft” to the acronym “MS”.

-   **NLU Model**

    A collection of utterance examples and their associated intents and entities that the system uses as a reference to infer intents and entities in a new utterance. The NLU Workbench comes with pre-built NLU models for specific business units, such as an ITSM model. You can also create custom models.


## NLU Workbench

Use the NLU Workbench to create morphological representations of human language. These models enable you to create intents and entities expressed in natural language utterances. Any ServiceNow application can invoke an NLU model to get an inference of intents and entities in a given utterance.

Using the nlu\_admin role, you build your models in the NLU Workbench, where you create, train, test, and publish them iteratively.

For information on how to build and use an NLU model, see: [Create an NLU model](../task/create-nlu-modelx.md).

## NLU inference service

Natural Language Understanding provides an NLU inference service that helps the system to understand natural language and drive intelligent actions. This service trains and predicts intents and entities for a given user utterance in your model so that its text translates into machine-understandable formats, such as APIs and parameters.

The system uses an inference API to train NLU algorithms by using sample record data to identify intents and entities that are strong candidates for accurate prediction.

## NLU model consumption

Other ServiceNow® applications consume NLU model output, such as Virtual Agent.

For example, Virtual Agent administrators can configure a Virtual Agent Designer conversation flow to consume NLU models so that agent chatbots can better understand user statements in the conversation. For more information on how Virtual Agent consumes NLU models, see: [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-NLU.md).

## Get started

<table id="table_lhx_jch_czb" class="nav-card"><tbody><tr><td>

[Explore![](../../../reuse/icons/brand-icons/bus-explore.svg)Learn about NLU concepts and features.](nlu-explore.md)

</td><td>

[Use![](../../../reuse/icons/brand-icons/bus-sdlc.svg)Create, test, translate, and publish your NLU models.](nlu-models.md)

</td></tr><tr><td>

[Integrate![](../../../reuse/icons/brand-icons/bus-integration-and-apis.svg)Learn how Virtual Agent administrators can update NLU models from within Virtual Agent Designer.](virtual-agent-nlu-model-builder-integration.md)

</td><td>

[Reference![](../../../reuse/icons/brand-icons/bus-learn.svg)Learn about using models in different languages for use in other applications](nlu-language-support.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Virtual Agent &amp; NLU community page](https://www.servicenow.com/community/virtual-agent-nlu/ct-p/virtual-agent-natural-language)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

