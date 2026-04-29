---
title: Artifact configurations
description: You can configure the required artifacts and use the Localization Framework to fulfill the translation requests.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure the Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Artifact configurations

You can configure the required artifacts and use the Localization Framework to fulfill the translation requests.

Any artifact configured in the Localization Framework application has its own record in the artifact configurations \[sn\_lf\_config\] table.

With the activation of the Localization Framework Installer plugin \(com.glide.localization\_framework.installer\), a record for Service Catalog item and Natural Language Understanding Model are automatically created and configured in Localization Framework.

A record for the Virtual Agent topic is also created and configured in the framework, since Virtual Agent is automatically enabled with the base system. For more information, see [Virtual Agent Lite](https://www.servicenow.com/docs/access?context=va-lite&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

Records for Document Template Block Content and HTML Document Template are created in the artifact configurations \[sn\_lf\_config\] table when you activate the Human Resources Scoped App: Lifecycle Events for Enterprise plugin \[com.sn\_hr\_lifecycle\_ent\]. For more information about activating this plugin, see [Activate Lifecycle Events for Enterprise](https://www.servicenow.com/docs/access?context=activate-hr-lifecycle-events-for-enterprise&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

You can also create and configure an artifact of your choice and a record for the same is created in the artifact configurations \[sn\_lf\_config\] table. For more information, see [Create and configure a custom artifact](../task/create-configure-custom-artifact.md).

-   **[Create and configure a custom artifact](../task/create-configure-custom-artifact.md)**  
Create and configure custom artifacts of your choice to use the Localization Framework functionality.
-   **[Create a processor script](../task/create-processor-script.md)**  
You can create a processor script to include in your custom artifact configuration to extract the translatable content and save the translated content.
-   **[Processor script functions](../reference/processor-script-functions.md)**  
The processor script contains functions that help you extract the translatable content and save the translated content which is included when you configure an artifact.
-   **[Create a UI action for the custom artifact](../task/create-ui-action-artifact.md)**  
Create a UI action to request translations for the custom artifact.
-   **[Read script helper functions for LFDocumentContentBuilder](../reference/lf-document-content-builder.md)**  
The LFDocumentContentBuilder provides utility functions to build document content. Use these functions to write the logic to extract the translatable content from any artifacts regardless of them using standard tables or not for translations.

**Parent Topic:**[Configure the Localization Framework](configuring-localization-framework.md)

