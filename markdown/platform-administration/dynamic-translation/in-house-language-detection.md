---
title: Language Detection spoke
description: ServiceNow Language Detection Service spoke provides a single subflow and action to detect the language of the given text using the ServiceNow language detection service.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2025-01-22"
reading_time_minutes: 1
breadcrumb: [Translating with Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Language Detection spoke

ServiceNow Language Detection Service spoke provides a single subflow and action to detect the language of the given text using the ServiceNow language detection service.

The ServiceNow Language Detection Service spoke is an in-house language detection service offered by the ServiceNow platform.

The ServiceNow Language Detection Service spoke plugin \(com.glide.language\_detection\_spoke\) is available with the activation of Dynamic Translation plugin \(com.glide.dynamic\_translation\).

This spoke creates an entry named ServiceNow in the Translator Configurations \(sn\_dt\_translator\_configuration\) table. By default, this entry is active and marked as default for detection. You can opt to configure your own language detection service.

## Subscription

This spoke requires any ServiceNow subscription that is Professional or above, and includes Dynamic Translation.

## Supported versions

API versions v3 and v4.

## Spoke subflow

The spoke provides the subflow in the Published state to integrate with the ServiceNow language detection service.

<table id="table_lcb_s4x_vnb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Inputs

</td></tr><tr><td>

Detect Language \[detect\_language\_v3\] or \[detect\_language\_v4\]

</td><td>

Detects the languages of texts using ServiceNow Language Detection Service.The v4 flows for Dynamic Translation are supported from the Xanadu Patch 3 release. For more information, see [Migrate customized Translator Configurations to v4 flows](../task/migrate-v4-dynamic-translation.md).

</td></tr></tbody>
</table>## Spoke action

The spoke provides the action in the Published state to integrate with the ServiceNow language detection service.

<table id="table_kfs_zxy_vnb"><thead><tr><th>

Subflow

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Inputs

</td></tr><tr><td>

Detect Language \[detect\_language\_v3\] or \[detect\_language\_v4\]

</td><td>

Detects the languages of texts using ServiceNow Language Detection Service. The v4 flows for Dynamic Translation are supported from the Xanadu Patch 3 release. For more information, see [Migrate customized Translator Configurations to v4 flows](../task/migrate-v4-dynamic-translation.md).

</td></tr></tbody>
</table>The ServiceNow Language Detection service uses the following Dynamic Translation APIs to detect the language of the input texts:

-   getDetectedLanguage: Provides text to identify the languages.
-   getDetectedLanguages: Provides texts to identify the languages.

For more information, see [DynamicTranslation API](dyn-translation-apis.md).

