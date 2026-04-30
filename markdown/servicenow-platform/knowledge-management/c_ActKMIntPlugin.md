---
title: Activate the knowledge management internationalization plugin
description: To enable translation of knowledge articles, you must activate multiple plugins.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate the knowledge management internationalization plugin

To enable translation of knowledge articles, you must activate multiple plugins.

-   Knowledge Management Advanced \(com.snc.knowledge\_advanced\) plugin. For more information, see [Activate the Knowledge Management Advanced plugin](../task/activate-knowledge-advanced-plugin.md)
-   I18N:Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\) plugin. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).
-   Internationalization plugins for each appropriate language. For more information, see [Activate a language](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    **Note:**

    -   Activating internationalization plugins for the available languages automatically activates the I18N: Internationalization plugin \(com.glide.i18n\) that instead activates the I18N: Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\) plugin.
    -   Beginning with the San Diego release, you can request ServiceNow personnel to customize your Languages \[sys\_language\] table. You can create translations of knowledge articles into any combination of language and region configured in the table. These combinations must be in compliance with the Internet Engineering Task Force \(IETF\) BCP-47 standard. For more information, see [The region subtag](https://www.w3.org/International/articles/language-tags/#region)​.

## Installed components

The I18N:Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\) plugin installs the following components:

-   A relationship named Translated Versions that creates a related list on the Knowledge form showing other articles that have the same parent article.
-   A business rule named knowledge query that automatically filters the knowledge portal and search results based on the user's selected language.
-   A UI macro named kb languages.
-   Two fields, named Language and Parent, in the Knowledge \[kb\_knowledge\] table and the Knowledge form.

## Knowledge form changes

The I18N:Knowledge Management Internationalization Plugin v2 \(com.glideapp.knowledge.i18n2\) plugin adds the following fields to the Knowledge form:

-   **Language**: Language in which you are creating the knowledge article. The list is populated based on the languages enabled for the selected knowledge base.
-   **Parent**: The article number that represents the base language article. This setting keeps translations of the same article related to each other. Consider choosing the same language consistently for the parent article.

    **Note:** The **Parent** field tracks translations of articles.


Additionally, the Translated Versions related list is automatically added to the Knowledge form after you save an article.

**Parent Topic:**[Configuring Knowledge Management](../../../configuring-knowledge-management.md)

