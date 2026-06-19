---
title: Prerequisites for using Dynamic Translation in Virtual Agent
description: To enable dynamic machine translation, install ServiceNow language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/virtual-agent/prereq-using-dt-va.html
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Prerequisites for using Dynamic Translation in Virtual Agent

To enable dynamic machine translation, install ServiceNow® language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.

Before you can [enable dynamic machine translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/enable-dynamic-lang-detection.md) for a language, you must install and configure Dynamic Translation on your instance.

1.  As an admin, install the following plugins:

    -   Glide Virtual Agent \(com.glide.cs.chatbot\)
    -   Dynamic Translation for Virtual Agent \(com.glide.cs.dynamic.translation.virtual\_agent\)
2.  Activate language plugins for each language that you want to deploy with dynamic translation.

    **Note:** Languages for Dynamic Translation are stored in the sys\_cs\_dynamic\_translation\_virtual\_agent table.

3.  \(Optional\) [Enable NLU languages in Virtual Agent settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/enable-langs-va-gen-settings.md), if you are using NLU topic discovery.

    **Note:** NLU detection and discovery values are stored in the sys\_cs\_general\_settings table. As of Vancouver, ServiceNow NLU is the available NLU driver.

4.  \(Optional\) [Enable LLM languages in Now Assist Admin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/enable-dynamic-translation-for-now-assist-applications.md) if you are using Now Assist in Virtual Agent.
5.  \(Optional\) Create exclusion rules for specific terms and content patterns within the Exclusion Framework.

The following translation service providers are pre-configured once the plugins are installed:

-   Microsoft Azure
-   Microsoft Azure OEM
-   Google Translate

## Configuring other translation service providers

**Note:** The following content is only relevant to NLU conversations and live agent LLM conversations that use Dynamic Translation for Agent Chat.

You can configure any other translation service provider in the Dynamic Translation application as follows:

1.  Integrate with a translation service provider.

2.  Create a translator configuration in Dynamic Translation.

3.  Create a language code mapping to map translator language codes to the ServiceNow® language codes.


## Next step

[Configure Dynamic Translation service integration credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/configure-translation-srvc-integration-credentials.md)

**Parent Topic:**[Localization options for Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/conversational-interfaces/virtual-agent/multi-language-options-va.md)

