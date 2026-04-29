---
title: Localization Framework support for Natural Language Understanding models
description: Localization Framework integrates with NLU Workbench to translate the Natural Language Understanding models along with their associated intents, utterances, and entities into multiple languages.
locale: en-US
release: australia
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Localization Framework support for Natural Language Understanding models

Localization Framework integrates with NLU Workbench to translate the Natural Language Understanding models along with their associated intents, utterances, and entities into multiple languages.

## Localizing Natural Language Understanding models

The integration of Localization Framework with NLU Workbench enables you to do the following tasks.

-   Auto-configure the NLU Model artifact in the Artifacts Configuration \[sn\_lf\_config\] table with the activation of the Localization Framework plugin \(com.glide.localization\_framework.installer\).
-   Select multiple languages from the available languages in the instance to configure settings with Natural Language Understanding models artifacts. To configure localization settings, see [Localization Framework settings](localization-settings.md).
-   Request translations for Natural Language Understanding Models and translate the content of the localization task using the translation modes.

    **Note:** Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\) to use machine translation in Localization Framework.

-   Translate the content of the Natural Language Understanding models directly from the NLU Workbench.

    **Note:** Only users with the localization\_editor role can translate content on the comparison UI of the Natural Language Understanding model in the NLU Workbench. For more information about the localization\_editor role, see [Localization Framework Roles](../reference/roles-localization-framework.md#).

-   Approve and publish the translated content.

**Note:** The localization of Natural Language Understanding models requires mapping between the Natural Language Understanding models in one language and their counterpart in other languages to use the localization framework support.

For more information about localizing Natural Language Understanding models, see [Translate NLU Models](https://www.servicenow.com/docs/access?context=translate-multilingual-model&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

**Parent Topic:**[Explore Localization Framework](exploring-localization-framework.md)

