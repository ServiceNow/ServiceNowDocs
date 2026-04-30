---
title: Explore Localization Framework
description: Learn more about the Localization Framework app that enables a systematic localization process, so you can provide a seamless user experience in multiple languages.
locale: en-US
release: xanadu
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2024-11-20"
reading_time_minutes: 3
breadcrumb: [Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Explore Localization Framework

Learn more about the Localization Framework app that enables a systematic localization process, so you can provide a seamless user experience in multiple languages.

## Localization Framework overview

The Localization Framework streamlines the process of adapting and translating ServiceNow instances to meet the needs of different regions and languages. With this application, users can create and manage translation projects, assign tasks to translators, and track progress. The Localization Framework also supports the creation of language packs, which contain translated content for specific languages. Organizations can ensure that their ServiceNow instances are accessible and user-friendly for users around the world by reducing the time and effort needed for localization.

![Localization projects submitted by a Requestor are reviewed by a Localization manager. A Translator fulfills the assignment before approval and publishing by a Translation manager.](../image/Exploring-LF-infographic.png "The localization process")

## Localization Framework benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Define and use custom language artifacts, in addition to installing artifact-specific product plugins.|[Artifact configurations](framework-configuration.md)|Administrators|
|Tailor Localization Framework workflows and translation preferences|[Localization Framework settings](localization-settings.md)|Administrators|
|Request translations|[Request translations](using-localization-framework.md)|Administrators, editors,managers, and requestors|
|Manage translation projects|[Create a localization project](../task/create-localization-project.md)|Managers|
|Bundle translation projects together|[Add a localization request item to a project](../task/add-lritm-to-project.md)|Managers|
|Perform translation projects|[Fulfill a localization task](../task/fulfill-localization-task.md)|Fulfillers|
|Approve and publish localizations and translations|[Approve a localization task](../task/approve-localization-task.md)|Fulfillers|
|Use artifacts in localization, with support for Virtual Agent and several other ServiceNow products.|[Supported artifacts in Localization Framework](supported-artifacts-lf.md)|Administrators, managers, and users|

**Note:** Localization Framework does not support Domain Separation.

-   **[Supported artifacts in Localization Framework](supported-artifacts-lf.md)**  
Localization Framework extends its framework capabilities to certain artifacts and translates the content of the artifact items.
-   **[Localization Framework support for Service Catalog items](lf-support-for-catalog-items.md)**  
Localization Framework enables translation of Service Catalog items when a catalog item is requested for translation into a language and a localization requested item \(LRITM\) is created.
-   **[Virtual Agent Designer integration with Localization Framework](va-designer-lf-integration.md)**  
The integration of Virtual Agent Designer with Localization Framework enables you to translate Virtual Agent topics using the translation modes supported by Localization Framework with or without a localization task.
-   **[Localization Framework support for Natural Language Understanding models](lf-support-for-nlu.md)**  
Localization Framework integrates with NLU Workbench to translate the Natural Language Understanding models along with their associated intents, utterances, and entities into multiple languages.
-   **[Localization Framework support for Surveys](lf-support-for-surveys.md)**  
Localization Framework enables the translation of surveys items when a translation request for a survey is created and when a localization requested item \(LRITM\) is created.
-   **[Localization Framework support for Knowledge Base](lf-support-for-kb-articles.md)**  
Localization Framework enables the translation of Knowledge Base \(KB\) articles when a KB article is requested for translation into a language and when a localization requested item \(LRITM\) is created.
-   **[Localization Framework support for email notifications](lf-support-for-email-notif.md)**  
Localization Framework enables the translation of emails \(notification, template, and layout\) when an email artifact is requested for translation into a language and when a localization requested item \(LRITM\) is created.
-   **[Localization Framework support for HR Service Delivery](lf_support-for-hr.md)**  
Localization Framework extends its framework capabilities to Document Templates and Document Template Block Contents in HR Service Delivery.
-   **[Localization Framework Roles](../reference/roles-localization-framework.md#)**  
Localization Framework uses different roles to manage different aspects of the application.
-   **[Workflows in the Localization Framework](../reference/workflow-localization-framework.md)**  
Workflows define actions for completing a localization task. Each localization task undergoes the workflow configured for its target language to complete the task.

**Parent Topic:**[ServiceNow AI Platform translation and localization](../../managing-data/concept/translation-and-localization.md)

