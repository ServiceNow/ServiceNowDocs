---
title: Limitations in Dynamic Translation
description: Learn about length and language support limitations when integrating with a machine translation service provider in Dynamic Translation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/dynamic-translation/limitations-dynamic-translation.html
release: brazil
product: Dynamic Translation
classification: dynamic-translation
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Reference for Dynamic Translation, Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Limitations in Dynamic Translation

Learn about length and language support limitations when integrating with a machine translation service provider in Dynamic Translation.

## Length limitations for machine translation service providers

The following are the length limitations for some translation service providers. If you use a different third-party provider, check that provider's documentation.

-   For Google, the recommended maximum length of each request is 5,000 characters. The maximum size of the input text can't exceed 30,000 code points. For more information, see the [Google Documentation](https://cloud.google.com/translate/quotas).
-   For Microsoft, the input text for translation can't have more than 50,000 characters including spaces. The input text for detection also has a maximum of limit of 50,000 characters. For more information, see the [Microsoft Documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/request-limits#character-and-array-limits-per-request).

## Language support limitations for translation service providers

Not all translation service providers support the same languages that ServiceNow AI Platform supports.

For information about languages supported by Google for translation, see the Google [documentation](https://cloud.google.com/translate/docs/languages).

For information about languages supported by Microsoft for translation, see the Microsoft [documentation](https://docs.microsoft.com/en-us/azure/cognitive-services/translator/language-support).

**Parent Topic:**[Reference for Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-translation/reference-for-dynamic-translation.md)

