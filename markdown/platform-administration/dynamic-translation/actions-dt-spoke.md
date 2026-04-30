---
title: Actions in Dynamic Translation spoke
description: Actions in the Dynamic Translation spoke are built to access the Dynamic Translation APIs from Workflow Studio.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Actions in Dynamic Translation spoke

Actions in the Dynamic Translation spoke are built to access the Dynamic Translation APIs from Workflow Studio.

<table id="table_lj3_3bz_vnb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Detect Language \[detect\_language\]

</td><td>

Detects the language of the text using the configured translator.

</td></tr><tr><td>

Detect Languages \[detect\_languages\]

</td><td>

Detects the languages of multiple texts using the configured translator.

</td></tr><tr><td>

Is Dynamic Translation Enabled \[is\_dynamic\_translation\_enabled\]

</td><td>

Checks whether the Dynamic Translation plugin \(com.glide.dynamic\_translation\) is installed and configured for a Translation Service Provider.-   If the input is empty, checks whether a default Translation Service Provider is configured.
-   If a translator is provided, checks whether that Translation Service Provider is configured.

</td></tr><tr><td>

Translate Text \[translate\_text\]

</td><td>

Translates text to multiple languages using the configured translation service provider. The action can translate a text string into multiple target languages.

</td></tr><tr><td>

Translate Texts \[translate\_texts\]

</td><td>

Translate texts to multiple languages using the configured translation service provider. The action can translate an array of texts into multiple target languages.

</td></tr></tbody>
</table>## Standard Error Codes

When an error occurs, error codes populate with the reason for the error. Refer to the following information for the standard error codes that appear while you work on the Dynamic Translation spoke actions corresponding to the Dynamic Translation APIs.

-   [Dynamic Translation - Scoped](https://www.servicenow.com/docs/access?context=DynamicTranslation&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)
-   [Dynamic Translation - Client](https://www.servicenow.com/docs/access?context=DynamicTranslationClientAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

