---
title: Translating with Dynamic Translation
description: Translate user-generated content live on your instance to streamline communication for your agents and end users.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Translating with Dynamic Translation

Translate user-generated content live on your instance to streamline communication for your agents and end users.

A common use case for Dynamic Translation

After you activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\), you can do the following tasks using a translation service provider:

-   Detect the language of the input text
-   Translate user-entered text from a source language to a target language

For information on activating this plugin, see [Activate Dynamic Translation](../task/activate-dynamic-translation.md).

## Default translation service providers for Dynamic Translation

By default, Dynamic Translation supports the following Microsoft and Google service providers for machine translation.

-   Connections and credential aliases and the corresponding connection attributes.

    **Note:** You should create a connection for each translation service provider and specify the credential information.

-   IntegrationHub subflows and actions for these spokes.
    -   Microsoft Azure Translator Service spoke
    -   Google Cloud Translator Service spoke
-   Translator configurations

**Note:** The Google Cloud Translator Service spoke for Dynamic Translation must be installed from ServiceNow Store.

## Using Dynamic Translation

When your admin has configured Dynamic Translation, look for the translate icon \(![Translate icon.](../image/Translation.png)\) next to fields on forms and in workspaces.

