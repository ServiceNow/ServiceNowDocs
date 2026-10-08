---
title: Configure AI settings in AI Admin Center \(Lux UI\)
description: Use AI admin features on the Settings page in AI Admin Center to configure AI settings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-configure-ai-settings.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 6
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [Using other AI applications from AI Admin Center, Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Configure AI settings in AI Admin Center \(Lux UI\)

Use AI admin features on the Settings page in AI Admin Center to configure AI settings.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to configure AI settings.

AI Admin Hub experiences and settings features are accessible on the Settings page. The features are grouped in AI Admin Center based on the type of action to perform.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Settings** \(\[Omitted image "icon-aiac-lux-nav-settings.png"\] Alt text: Settings icon.\) in the side navigation panel.

    The Settings page opens.

    \[Omitted image "ai-admin-center-lux-settings.png"\] Alt text: Settings page showing AI configuration options.

3.  Select a settings option.

    The following table lists the options on the Settings page.

<table id="table_lux_settings"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Account

</td><td>

Opens the Account page from AI Admin Hub.

 Review your ServiceNow AI license details to make sure that you're up to date on what's available to you.

 For more information, see [Review Now Assist account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/review-now-assist-account-information.md).

</td></tr><tr><td>

Automation opportunities

</td><td>

Opens the Automation opportunities settings page.

 Configure the data source, filters, schedule, and cost profile that AI Agent Advisor uses to identify automation opportunities and provide savings estimates for them.

 For more information, see [Set up a data source for analysis \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-set-up-data-source.md).

</td></tr><tr><td>

Multilingual service

</td><td>

Opens the Multilingual Service page from AI Admin Hub.

 Turn on multilingual service for user-entered text with native translation or Dynamic Translation in AI applications.

 For more information, see [Configure multilingual service for ServiceNow Otto applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/enable-dynamic-translation-for-now-assist-applications.md).

</td></tr><tr><td>

System Property Registry

</td><td>

Opens the System property registry page.

 View and edit the system properties for the AI applications in your instance.

 For more information, see [Manage system properties for AI applications in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-manage-system-properties.md).

</td></tr><tr><td>

AI Plugins

</td><td>

Opens the Plugins page from AI Admin Hub.

 Install AI plugins to enable generative AI on your instance.

 For more information, see [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

</td></tr><tr><td>

Usage alerts

</td><td>

Opens the Usage alerts page from AI Admin Hub.

 Create alert rules to track the usage of generative AI skills and notify you in the instance and by email when the set thresholds are reached.

</td></tr><tr><td>

Prompt Injection

</td><td>

Opens the Prompt Injection page from AI Admin Hub.

 Activate or deactivate prompt injection attack detection to protect all generative AI applications and AI-generated text and conversations on your instance from malicious inputs and unintended model behaviors.

 For more information, see [Configure prompt injection attack protection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-prompt-injection-attack-protection.md).

</td></tr><tr><td>

Offensiveness

</td><td>

Opens the Offensiveness page from AI Admin Hub.

 Activate offensiveness detection to log or block offensive content generated by AI skills and workflows.

 For more information, see [Activate offensiveness protection for generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-offensiveness-protection-for-generative-ai.md).

</td></tr><tr><td>

Guardrail Service Providers

</td><td>

Opens the Guardrail service providers page from AI Admin Hub.

 Choose the default service provider for AI Guardian. This provider is used by Offensiveness and Prompt Injection.

 For more information, see [Configuring a Guardrail Service Provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configuring-byog.md).

</td></tr><tr><td>

Model Providers

</td><td>

Opens the Manage model providers page from AI Admin Hub.

 Edit or customize the model provider for a skill or skill group at the instance level from the list of supported third-party model providers. You can also review the model policy set by your organization and view the change history.

 For more information, see [Manage model providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/edit-model-providers.md).

</td></tr><tr><td>

Model Versions

</td><td>

Opens the Manage model versions page from AI Admin Hub.

 Manage the version of the model providers across skills and instance levels. You can change and update versions for the base system and custom skills.

 For more information, see [Manage version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/manage-version.md).

</td></tr><tr><td>

Data privacy policies

</td><td>

Opens the Privacy policies page from AI Admin Hub.

 Configure privacy policies to anonymize data in AI applications.

 For more information, see [Configure Now Assist privacy policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-privacy-policies.md).

</td></tr><tr><td>

Data Sharing

</td><td>

Opens the Data sharing page from AI Admin Hub.

 Data sharing improves ServiceNow AI products. You can opt out of data sharing from this page.

 For more information, see [Opt out of data sharing for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md).

</td></tr><tr><td>

Data processing

</td><td>

Opens the Data overflow processing page from AI Admin Hub.

 Configure where AI data is processed during periods of high traffic.

 For more information, see [Configure Now Assist data overflow processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/configure-na-data-overflow.md).

</td></tr><tr><td>

ServiceNow Otto panel

</td><td>

Opens the ServiceNow Otto Panel page from AI Admin Hub.

 With the ServiceNow Otto panel, you can get assistance from generative AI experiences to solve customer issues faster. Use this conversational interface to summarize a chat, case, or incident, get help, or generate resolution notes so that you can get the context of this information more quickly.

 For more information, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md).

</td></tr><tr><td>

ServiceNow Otto context menu

</td><td>

Opens the ServiceNow Otto Context Menu page from AI Admin Hub.

 The ServiceNow Otto context menu uses generative AI to help agents summarize, create, and edit written content, thus streamlining their writing tasks.

 For more information, see [ServiceNow Otto context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-write-overview.md).

</td></tr></tbody>
</table>
