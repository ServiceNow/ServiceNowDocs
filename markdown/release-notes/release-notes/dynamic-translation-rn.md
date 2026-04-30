---
title: Dynamic Translation release notes
description: The ServiceNow Dynamic Translation application enables translation of user-generated text by using the translation service providers configured in Dynamic Translation. Dynamic Translation was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-07"
reading_time_minutes: 1
---

# Dynamic Translation release notes

The ServiceNow® Dynamic Translation application enables translation of user-generated text by using the translation service providers configured in Dynamic Translation. Dynamic Translation was enhanced and updated in the Xanadu release.

## Dynamic Translation highlights for the Xanadu release

-   Using Exclusion Framework, prevent certain words such as product names from being machine translated.
-   The IBM Watson Translator Service Spoke has been withdrawn and is no longer available.
-   The Microsoft Azure Translator service increased the maximum length of a translation request from 10,000 characters to 50,000 characters.

See [Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) for more information.

**Important:**

IBM has announced deprecation of the IBM Watson Translator service. With the Xanadu release, this integration is no longer available in the ServiceNow® Store.

## New in the Xanadu release

-   **[Exclusion Framework in Dynamic Translation](https://www.servicenow.com/docs/access?context=dyn-translation-exclusion-framework&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Exclusion Framework enables you to prevent machine translation of certain words and terms. You can specify words, such as official product names, that you want to shield from the translation process. You can also input regex to prevent translation of patterns such as sys ids.

-   **[The flows used by default Translator Configurations are upgraded to v4](https://www.servicenow.com/docs/access?context=migrate-v4-dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    With the Xanadu Patch 3 release, the flows used by default translator configurations are automatically upgraded to v4. If you want to use v4 flows and APIs with customized translator configurations, you must migrate them manually. The previous v3 is still supported.


## Changed in this release

-   **[Character maximum has increased for MS translation requests](https://www.servicenow.com/docs/access?context=limitations-dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    For users of the Microsoft Azure Translator service: the maximum character limit for a translation request has increased to 50,000. The maximum character limit for a detection request remains 50,000.


## Deprecations

With the Xanadu release, the IBM Watson Translator Service integration is no longer available in the ServiceNow® Store. For more information, see [https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes](https://cloud.ibm.com/docs/language-translator?topic=language-translator-release-notes).

## Activation information

Dynamic Translation is a ServiceNow AI Platform feature that is available with activation of the Dynamic Translation plugin \(com.glide.dynamic\_translation\). For details, see [Activate Dynamic Translation](https://www.servicenow.com/docs/access?context=activate-dynamic-translation&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Localization Framework](https://www.servicenow.com/docs/access?context=localization-framework-landing&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The Localization Framework application standardizes and enhances the translation process of artifacts across the platform through configurable workflows.

-   **[Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Localization Framework uses ServiceNow® Integration Hub spokes to connect to translation service providers.


**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

