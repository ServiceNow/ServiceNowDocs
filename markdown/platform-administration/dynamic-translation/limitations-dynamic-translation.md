---
title: Limitations in Dynamic Translation
description: You must be aware of a few limitations when you integrate with a translation service provider to enable the Dynamic Translation experience.
locale: en-US
release: xanadu
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Limitations in Dynamic Translation

You must be aware of a few limitations when you integrate with a translation service provider to enable the Dynamic Translation experience.

## Length limitations for translation service providers

The following are the length limitations for translation service providers:

-   For Microsoft, the input text for translation cannot have more than 50,000 characters including spaces. The input text for detection also has a maximum of limit of 50,000 characters. For more information, see the [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/request-limits#character-and-array-limits-per-request).
-   For IBM, the size of the input text cannot exceed 50KB. For more information, see the [IBM Documentation](https://cloud.ibm.com/apidocs/language-translator#translate).

    **Important:** IBM has announced the deprecation of the IBM Watson Translator Service for IBM Cloud in all regions. As of June 10, 2023, the Language Translator tile will be removed from the IBM Cloud Platform for new customers; only existing customers will be able to access the product. As of June 10, 2024, the service will reach its End of Support date. As of December 10, 2024, the service will be withdrawn entirely and will no longer be available to any customers. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

-   For Google, the recommended maximum length of each request is 5,000 characters. The maximum size of the input text cannot exceed 30,000 code points. For more information, see the [Google Documentation](https://cloud.google.com/translate/quotas).

## Language support limitations for translation service providers

Not all source language translations are supported by translation service providers.

For information about language translations supported by Microsoft, see the Microsoft [documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/language-support).

For information about language translations supported by IBM, see the IBM [documentation](https://cloud.ibm.com/docs/language-translator?topic=language-translator-identifiable-languages) for identifiable languages, and the IBM [documentation](https://cloud.ibm.com/docs/language-translator?topic=language-translator-translation-models) for translation models.

**Important:** IBM has announced the deprecation of the IBM Watson Translator Service for IBM Cloud in all regions. As of June 10, 2023, the Language Translator tile will be removed from the IBM Cloud Platform for new customers; only existing customers will be able to access the product. As of June 10, 2024, the service will reach its End of Support date. As of December 10, 2024, the service will be withdrawn entirely and will no longer be available to any customers. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

For information about language translations supported by Google, see the Google [documentation](https://cloud.google.com/translate/docs/languages).

