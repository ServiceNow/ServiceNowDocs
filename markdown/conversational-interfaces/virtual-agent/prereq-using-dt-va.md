---
title: Prerequisites for using Dynamic Translation in Virtual Agent
description: To enable dynamic machine translation, install ServiceNow language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Localization options for Virtual Agent, Build and deploy, Virtual Agent, Conversational Interfaces]
---

# Prerequisites for using Dynamic Translation in Virtual Agent

To enable dynamic machine translation, install ServiceNow® language plugins and Dynamic Translation plugins. Then configure Dynamic Translation for your instance.

Before you can [enable dynamic machine translation](../task/enable-dynamic-lang-detection.md) for a language, you must install and configure Dynamic Translation on your instance.

1.  As an admin, install the following plugins:

    -   Glide Virtual Agent \(com.glide.cs.chatbot\)
    -   Dynamic Translation for Virtual Agent \(com.glide.cs.dynamic.translation.virtual\_agent\)
2.  [Activate language plugins](https://www.servicenow.com/docs/access?context=t_ActivateALanguage&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for each language that you want to deploy with dynamic translation.

    **Note:** Languages for Dynamic Translation are stored in the sys\_cs\_dynamic\_translation\_virtual\_agent table.

3.  \(Optional\) [Enable NLU languages in Virtual Agent settings](../task/enable-langs-va-gen-settings.md), if you are using NLU topic discovery.

    **Note:** NLU detection and discovery values are stored in the sys\_cs\_general\_settings table. As of Vancouver, ServiceNow NLU is the available NLU driver.

4.  \(Optional\) [Enable LLM languages in Now Assist Admin](../../now-assist-admin/task/enable-dynamic-translation-for-now-assist-applications.md) if you are using Now Assist in Virtual Agent.
5.  \(Optional\) Create exclusion rules for specific terms and content patterns within the [Exclusion Framework](https://www.servicenow.com/docs/access?context=dyn-translation-exclusion-framework&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

The following translation service providers are pre-configured once the plugins are installed:

-   Microsoft Azure
-   Microsoft Azure OEM
-   Google Translate

## Configuring other translation service providers

**Note:** The following content is only relevant to NLU conversations and live agent LLM conversations that use Dynamic Translation for Agent Chat.

You can configure any other translation service provider in the Dynamic Translation application as follows:

1.  [Integrate with a translation service provider](https://www.servicenow.com/docs/access?context=integrate-translation-service-provider&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

2.  [Create a translator configuration in Dynamic Translation](https://www.servicenow.com/docs/access?context=create-custom-translator&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

3.  [Create a language code mapping](https://www.servicenow.com/docs/access?context=create-language-code-mapping&version=australia&pubname=australia-platform-administration&ft:locale=en-US) to map translator language codes to the ServiceNow® language codes.


## Next step

[Configure Dynamic Translation service integration credentials](../task/configure-translation-srvc-integration-credentials.md)

**Parent Topic:**[Localization options for Virtual Agent](multi-language-options-va.md)

