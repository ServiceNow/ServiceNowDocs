---
title: Limitations in Dynamic Translation
description: You must be aware of a few limitations when you integrate with a translation service provider to enable the Dynamic Translation experience.
locale: en-US
release: zurich
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer]
---

# Limitations in Dynamic Translation

You must be aware of a few limitations when you integrate with a translation service provider to enable the Dynamic Translation experience.

## Length limitations for translation service providers

The following are the length limitations for translation service providers:

-   For Google, the recommended maximum length of each request is 5,000 characters. The maximum size of the input text cannot exceed 30,000 code points. For more information, see the [Google Documentation](https://cloud.google.com/translate/quotas).
-   For Microsoft, the input text for translation cannot have more than 50,000 characters including spaces. The input text for detection also has a maximum of limit of 50,000 characters. For more information, see the [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/request-limits#character-and-array-limits-per-request).

## Language support limitations for translation service providers

Not all translation service providers support the same languages that ServiceNow AI Platform supports.

For information about languages supported by Google for translation, see the Google [documentation](https://cloud.google.com/translate/docs/languages).

For information about languages supported by Microsoft for translation, see the Microsoft [documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/language-support).

