---
title: \(Legacy\) Prerequisites for using Dynamic Translation in Virtual Agent for NLU
description: To enable dynamic machine translation, install ServiceNow language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/prereq-using-dt-va-nlu.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Localization options for NLU conversations, Build and deploy NLU conversations, \(Legacy\) Virtual Agent for NLU, Conversational Interfaces]
---

# \(Legacy\) Prerequisites for using Dynamic Translation in Virtual Agent for NLU

To enable dynamic machine translation, install ServiceNow® language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.

Before you can [enable dynamic machine translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/virtual-agent/enable-dynamic-lang-detection.md) for a language, you must install and configure Dynamic Translation on your instance.

1.  As an admin, install the following plugins:

    -   Glide Virtual Agent \(com.glide.cs.chatbot\)
    -   Dynamic Translation for Virtual Agent \(com.glide.cs.dynamic.translation.virtual\_agent\)
2.  [Activate language plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/t_ActivateALanguage.md) for each language that you want to deploy with dynamic translation.

    **Note:** Languages for Dynamic Translation are stored in the sys\_cs\_dynamic\_translation\_virtual\_agent table.

3.  [\(Legacy\) Enable NLU languages in Virtual Agent settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/enable-langs-va-gen-settings.md).

    **Note:** NLU detection and discovery values are stored in the sys\_cs\_general\_settings table. As of Vancouver, ServiceNow NLU is the available NLU driver.

4.  \(Optional\) Create exclusion rules for specific terms and content patterns within the [Exclusion Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dyn-translation-exclusion-framework.md).

The following translation service providers are pre-configured once the plugins are installed:

-   Microsoft Azure
-   Microsoft Azure OEM
-   Google Translate

## Configuring other translation service providers

You can configure any other translation service provider in the Dynamic Translation application as follows:

1.  [Integrate with a translation service provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/integrate-translation-service-provider.md).

2.  [Create a translator configuration in Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/create-custom-translator.md).

3.  [Create a language code mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/create-language-code-mapping.md) to map translator language codes to the ServiceNow® language codes.


## Next step

[\(Legacy\) Configure Dynamic Translation service integration credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/configure-translation-srvc-integration-credentials.md)

**Parent Topic:**[\(Legacy\) Localization options for Virtual Agent for NLU](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/multi-language-options-va.md)

