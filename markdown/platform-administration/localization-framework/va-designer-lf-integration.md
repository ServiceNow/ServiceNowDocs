---
title: Virtual Agent Designer integration with Localization Framework
description: The integration of Virtual Agent Designer with Localization Framework enables you to translate Virtual Agent NLU topics using the translation modes supported by Localization Framework with or without a localization task.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/localization-framework/va-designer-lf-integration.html
release: brazil
product: Localization Framework
classification: localization-framework
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore Localization Framework, Localization Framework, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Virtual Agent Designer integration with Localization Framework

The integration of Virtual Agent Designer with Localization Framework enables you to translate Virtual Agent NLU topics using the translation modes supported by Localization Framework with or without a localization task.

Starting with the Brazil release, Virtual Agent for NLU is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Localizing Virtual Agent NLU topics

The integration of Virtual Agent Designer with Localization Framework enables you to do the following tasks.

-   Select multiple languages from the available languages in the instance to configure settings with the Virtual Agent artifact. To configure localization settings, see [Localization Framework settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-framework/localization-settings.md).
-   Translate the content directly from the Virtual Agent Designer using the edit option.
-   Read, edit, machine translate, export, and import the content of the Virtual Agent topic from the Virtual Agent Designer if the Virtual Agent artifact is configured in the localization settings.

    **Note:**

    -   **Note:** You need the localization\_editor role to edit the translated content from the comparison UI of the Virtual Agent Designer directly. For more information about the localization\_editor role, see [Localization Framework Roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-framework/roles-localization-framework.md).

    -   Activate the Dynamic Translation plugin \(com.glide.dynamic\_translation\) to use machine translation in Localization Framework.
-   Request translations from Virtual Agent Designer.

    **Note:** Requesting translations creates localization tasks. You need the localization\_requester role to request translations.

-   Approve and publish the translated content.
-   Monitor the overall localization health of the Virtual Agent topics from the [Localization Insights dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-framework/localization-insights-dashboard.md).

For more information about localizing the Virtual Agent topics in the Virtual Agent Designer, see [Virtual Agent Localization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/localize-va-topic.md).

**Parent Topic:**[Explore Localization Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/localization-framework/exploring-localization-framework.md)

