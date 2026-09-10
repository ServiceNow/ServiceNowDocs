---
title: Dynamic Translation release notes
description: The ServiceNow Dynamic Translation application enables translation of user-generated text by using third-party translation service providers. Dynamic Translation was enhanced and updated in the Yokohama release.The ServiceNow Dynamic Translation application enables translation of user-generated text by using third-party translation service providers. Dynamic Translation was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 1
---

# Dynamic Translation release notes

The ServiceNow® Dynamic Translation application enables translation of user-generated text by using third-party translation service providers. Dynamic Translation was enhanced and updated in the Yokohama release.

## About Dynamic Translation

-   Preserve text, such as product names or technical terms, during machine translation with the Exclusion Framework feature.
-   The APIs used by default translator configurations are upgraded to v4. If you want to use v4 APIs with customized translator configurations, you must migrate them manually.
-   The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is removed.

See [Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/dynamic-translation-overview.md) for more information.

## Activation and other requirements

**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-platform-admin-rn-landing.md)

## Yokohama

The ServiceNow® Dynamic Translation application enables translation of user-generated text by using third-party translation service providers. Dynamic Translation was enhanced and updated in the Yokohama release.

### What's new

-   **[Exclusion Framework in Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/dyn-translation-exclusion-framework.md)**

    Preserve text such as product names or technical terms during machine translation. With Exclusion Framework, you can specify words and patterns that shouldn't be translated.

-   **[The APIs used by default Translator Configurations are upgraded to v4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/migrate-v3-dynamic-translation.md)**

    The APIs used by default translator configurations are automatically upgraded to v4. If you want to use v4 APIs with customized translator configurations, you must migrate them manually. The previous v3 is still supported.


### What's deprecated or removed

The spoke for IBM Watson Translator Service for IBM Cloud \(com.glide.ibm\_translation\_spoke\) is no longer available because IBM has withdrawn this translation service. For more information, see [IBM Watson Language Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/ibm-translation-spoke.md).

