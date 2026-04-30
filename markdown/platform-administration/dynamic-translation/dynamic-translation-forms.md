---
title: Dynamic translation on forms and activity streams
description: For a seamless localization experience on forms and activity streams, you can dynamically translate text based on the preferred language of a user​.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Translating with Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Dynamic translation on forms and activity streams

For a seamless localization experience on forms and activity streams, you can dynamically translate text based on the preferred language of a user​.

## Dynamic translation on forms

You can translate the field values on forms on the ServiceNow AI Platform and the configurable workspaces. For more information on Dynamic Translation support for configurable workspaces, see [Dynamic Translation support for configurable workspace](https://www.servicenow.com/docs/access?context=dynamic-translation-support-in-your-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

To enable dynamic translation at the field-level on Platform forms, see [Enable dynamic translation for a field](../task/configure-field-translation.md). After dynamic translation is enabled, select the translate icon \(![Translate icon](../image/Translation.png)\) to show or hide the translated content.

## Dynamic translation in activity streams

You can enable dynamic translation in activity streams on the ServiceNow AI Platform, configurable workspace, and Service Portal. For more information on Dynamic Translation support for configurable workspaces, see [Dynamic Translation support for configurable workspace](https://www.servicenow.com/docs/access?context=dynamic-translation-support-in-your-workspace&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Use the dynamic translation properties to enable or prevent the option for dynamic translation in the activity stream of the tables you list. When enabled, select the translate icon \(![Translate icon](../image/Translation.png)\) to show or hide the translated content for each comment or work note in the activity stream. For more information, see [Dynamic Translation properties](../reference/dynamic-translation-properties.md).

## Length limitations for translation service providers

The following are the length limitations for translation service providers:

-   For Microsoft, the input text for translation cannot have more than 50,000 characters including spaces. The input text for detection also has a maximum of limit of 50,000 characters. For more information, see the [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/request-limits#character-and-array-limits-per-request).
-   For IBM, the size of the input text cannot exceed 50KB. For more information, see the [IBM Documentation](https://cloud.ibm.com/apidocs/language-translator#translate).

    **Important:** IBM has announced the deprecation of the IBM Watson Translator Service for IBM Cloud in all regions. As of June 10, 2023, the Language Translator tile will be removed from the IBM Cloud Platform for new customers; only existing customers will be able to access the product. As of June 10, 2024, the service will reach its End of Support date. As of December 10, 2024, the service will be withdrawn entirely and will no longer be available to any customers. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

-   For Google, the recommended maximum length of each request is 5,000 characters. The maximum size of the input text cannot exceed 30,000 code points. For more information, see the [Google Documentation](https://cloud.google.com/translate/quotas).

**Note:** Starting with the Rome release, you can use Dynamic Translation without the snc-internal role.

