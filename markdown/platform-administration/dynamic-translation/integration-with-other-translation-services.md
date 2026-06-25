---
title: Integration with other translation services
description: Enable machine translation on your instance by integrating third-party translator services with Dynamic Translation. You can configure one or more translation service providers of your choice.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/dynamic-translation/integration-with-other-translation-services.html
release: australia
product: Dynamic Translation
classification: dynamic-translation
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Dynamic Translation, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Integration with other translation services

Enable machine translation on your instance by integrating third-party translator services with Dynamic Translation. You can configure one or more translation service providers of your choice.

Translator services are listed in the Translator Configurations \[sn\_dt\_translator\_configuration\] table. By default several third-party translators are partially preconfigured in this table. You can complete the configuration of a default translator by providing your account credentials and connections.

Alternatively, you can also create a custom spoke. In addition to your account credentials and connections, you must configure flows and any needed language code mappings for your custom translator. See [Integrate with a translation service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/integrate-translation-service-provider.md).

Also listed in the Translator Configurations table is a default record for the **ServiceNow** translator. This translator can be used for language detection only, not for translation, so its **Mark as default for translation** check box is not selectable. This optional language detection service is included in your Dynamic Translation subscription.

**Note:** If you activate dynamic translation in the Generative AI Controller, a fully preconfigured spoke to [Microsoft Azure OEM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/dynamic-translation-na-ms-azure-oem.md) Translator Service is added as a row in Translator Configurations.

-   **[Integrate with a translation service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/integrate-translation-service-provider.md)**  
Integrate with a third-party translation provider of your choice for machine translation of user-generated text.
-   **[Google Cloud Translator Service Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/google-translator-spoke.md)**  
Provides subflows and actions to dynamically translate the user-entered text, and to detect the language of the text using the Google translation service.
-   **[Microsoft Azure Translator Service spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/microsoft-translation-spoke.md)**  
Microsoft Azure Translator Service spoke provides subflows and actions to detect and translate user-entered text, using the Microsoft machine translation service. Dynamic Translation supports detection and translation of single texts and multiple texts.
-   **[Migrate customized Translator Configurations to v3 flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/migrate-v3-dynamic-translation.md)**  
Implement the contract with subflows using complex objects in the input and output fields for dynamic translation of text.
-   **[Migrate customized Translator Configurations to v4 flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/dynamic-translation/migrate-v4-dynamic-translation.md)**  
Migrate your customized translator configurations to v4 flows. Version 4 flows for Dynamic Translation are available from the Xanadu Patch 3 release.

**Parent Topic:**[ServiceNow AI Platform translation and localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-localization/translation-and-localization.md)

**Related topics**  


[Configuring Dynamic Translation]()

[Reference for Dynamic Translation]()

