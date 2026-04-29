---
title: Dynamic Translation spoke
description: The Dynamic Translation spoke provides actions to enable the ability to translate multiple texts from one language into one or more languages and detect the language of multiple texts seamlessly.
locale: en-US
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Translating with Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic Translation spoke

The Dynamic Translation spoke provides actions to enable the ability to translate multiple texts from one language into one or more languages and detect the language of multiple texts seamlessly.

The Dynamic Translation APIs are accessible across the ServiceNow platform through the following access points:

-   Server
-   Platform Client
-   Portal Client

In the Australia release, the Dynamic Translation spoke enables you to access the Dynamic Translation APIs from the Workflow Studio.

The Dynamic Translation Spoke is a plugin \(com.glide.dynamic\_translation.spoke\) that is available with activation of the Dynamic Translation plugin \(com.glide.dynamic\_translation\).

The Dynamic Translation spoke contains actions that are built corresponding to the Dynamic Translation APIs.

The following actions are built in the Australia release in Dynamic Translation spoke:

|Action Name|API|
|-----------|---|
|Detect Language|getDetectedLanguage\(\)|
|Detect Languages|getDetectedLanguages\(\)|
|Translate Text|getTranslation\(\)|
|Translate Texts|getTranslations\(\)|
|Is Dynamic Translation Enabled|isDynamicTranslationEnabled\(\)|

For more information about accessing the actions from the Workflow Studio, see [Access Dynamic Translation spoke actions from Workflow Studio](../task/access-dt-spoke-actions.md).

