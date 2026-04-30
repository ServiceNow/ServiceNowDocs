---
title: Bulk Translation for knowledge articles
description: Perform bulk translations of knowledge articles in multiple languages using the Localization Framework application.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use translation management, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Bulk Translation for knowledge articles

Perform bulk translations of knowledge articles in multiple languages using the Localization Framework application.

The Bulk Translations feature extends the localization service in Knowledge Management to support customers across geographies by localizing knowledge articles in the language they speak. You can select multiple knowledge articles and translate them into different languages by using the ServiceNow® Localization Framework application. Once the translation process is complete, you can access the translated article from the Knowledge \[kb\_knowledge\] table. You can request translations for up to 200 articles at a time.

## Translation workflow

You can define a workflow to determine the actions required to complete a translation. For information, see [Workflows in the Localization Framework](https://www.servicenow.com/docs/access?context=workflow-localization-framework&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) .

## Preferences configuration

Through preferences, define the translations, workflow, and project preferences to request translation for activated languages. For more information, see [Configure the Localization Framework preferences](https://www.servicenow.com/docs/access?context=define-translation-preferences&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Artifact configuration

The Knowledge artifact is included in the Artifact Configurations \[sn\_lf\_config\] table and is active by default. For more information, see [Localization Framework support for Knowledge Base](https://www.servicenow.com/docs/access?context=lf-support-for-kb-articles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) .

## Translation validations

Translation validation enables you to review and manage the translation request before submitting knowledge articles for translation. The validations to be executed are:

-   The requested language is allowed in the knowledge base.
-   Blocks used in the article have translations present in the target language.
-   Source articles are not in the retired or outdated state.
-   The article's source language is different from the requested language.
-   The source article shouldn’t be a translated article.
-   The total number of selected articles is less than 200.

-   **[Use Bulk Translation for manual translation](use-bts-manual-translation.md)**  
Translate knowledge articles into different languages through bulk translations.
-   **[Use Bulk Translation for Dynamic Translation](bts-for-dynamic-translations.md)**  
Translate knowledge articles into different languages using machine translations.

**Parent Topic:**[Use translation management](../../../use-translation-management.md)

