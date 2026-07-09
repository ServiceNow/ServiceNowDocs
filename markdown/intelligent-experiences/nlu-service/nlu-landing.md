---
title: Natural Language Understanding
description: ServiceNow Natural Language Understanding \(NLU\) provides an NLU Workbench and an NLU inference service that you can use to enable the system to learn and respond to human-expressed intent. By entering natural language examples into the system, you help it understand word meanings and contexts so it can infer user or system actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/intelligent-experiences/nlu-service/nlu-landing.html
release: yokohama
product: NLU Service
classification: nlu-service
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Enable AI experiences]
---

# Natural Language Understanding

ServiceNow® Natural Language Understanding \(NLU\) provides an NLU Workbench and an NLU inference service that you can use to enable the system to learn and respond to human-expressed intent. By entering natural language examples into the system, you help it understand word meanings and contexts so it can infer user or system actions.

## Overview of Natural Language Understanding

\[Omitted image "natural-language-understanding-homepage-Q.png"\] Alt text: This image shows you the user input flow in the NLU model build process.

This image shows you the user input flow in the NLU model build process.

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


This image illustrates how Natural Language Understanding processes and renders utterance examples into intents and entities in the system.

\[Omitted image "natural-language-understanding-examples.png"\] Alt text: This image shows you how Natural Language Understanding processes and renders utterance examples into intents and entities in the system.

## NLU Workbench

Use the NLU Workbench to create morphological representations of human language. These models enable you to create intents and entities expressed in natural language utterances. Any ServiceNow application can invoke an NLU model to get an inference of intents and entities in a given utterance.

Using the nlu\_admin role, you build your models in the NLU Workbench, where you create, train, test, and publish them iteratively.

\[Omitted image "natural-language-understanding-modeling-Q.png"\] Alt text: This image shows you how the NLU Authoring API helps NLU administrators build their NLU models.

For information on how to build and use an NLU model, see: [Create an NLU model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/create-nlu-modelx.md).

## NLU inference service

Natural Language Understanding provides an NLU inference service that helps the system to understand natural language and drive intelligent actions. This service trains and predicts intents and entities for a given user utterance in your model so that its text translates into machine-understandable formats, such as APIs and parameters.

\[Omitted image "natural-language-understanding-inference-Q.png"\] Alt text: This image shows you how the system uses an NLU inference API to extract intents and entities for a given utterance. \[Omitted image ""\] Alt text: This image shows you how the system uses an NLU inference API to extract intents and entities for a given utterance.

Here, the system uses an inference API to train NLU algorithms by using sample record data to identify intents and entities that are strong candidates for accurate prediction.

## NLU model consumption

Other ServiceNow® applications consume NLU model output, such as Virtual Agent.

\[Omitted image "natural-language-understanding-consumption.png"\] Alt text: This image shows you how the Virtual Agent application consumes Natural Language Understanding.

For example, Virtual Agent administrators can configure a Virtual Agent Designer conversation flow to consume NLU models so that agent chatbots can better understand user statements in the conversation. For more information on how Virtual Agent consumes NLU models, see: [Natural Language Understanding \(NLU\) topic discovery in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/va-NLU.md).

## Get started

<table id="table_lhx_jch_czb" class="nav-card"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn about NLU concepts and features.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/nlu-explore.md)

</td><td>

[Use\[Omitted image "bus-sdlc.svg"\] Alt text:Create, test, translate, and publish your NLU models.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/nlu-models.md)

</td><td>

[Integrate\[Omitted image "bus-integration-and-apis.svg"\] Alt text:Learn how Virtual Agent administrators can update NLU models from within Virtual Agent Designer.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/virtual-agent-nlu-model-builder-integration.md)

</td></tr><tr><td>



</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Learn about using models in different languages for use in other applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/nlu-language-support.md)

</td><td>

 

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Virtual Agent &amp; NLU community page](https://www.servicenow.com/community/virtual-agent-nlu/ct-p/virtual-agent-natural-language)
-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

-   **[Exploring Natural Language Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/nlu-explore.md)**  
ServiceNow® Natural Language Understanding \(NLU\) provides an NLU Workbench and an NLU inference service that you can use to enable the system to learn and respond to human-expressed intent. By entering natural language examples into the system, you help it understand word meanings and contexts so it can infer user or system actions.
-   **[Model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/model-management-phases.md)**  
Manage your NLU model's life cycle in the NLU Workbench. Model management phases guide you through the iterative process of building, testing, and publishing your model.
-   **[Multilingual model management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/multilingual-model-managent.md)**  
Use multilingual Natural Language Understanding \(NLU\) models for the system to understand user input in several languages. The NLU Workbench helps you manage and maintain a consistent structure for content across languages to provide a unified experience.
-   **[Virtual Agent and NLU Workbench integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/virtual-agent-nlu-model-builder-integration.md)**  
Virtual Agent administrators can access and update their NLU models from within the Virtual Agent Designer user interface.
-   **[NLU Workbench - Advanced Features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/nlu-service/nlu-workbench-advanced-features.md)**  
NLU Workbench - Advanced Features expands the functionality of NLU Workbench to help you manage and improve your models.

**Parent Topic:**[Enable AI experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/intelligent-experiences/ai-products.md)

