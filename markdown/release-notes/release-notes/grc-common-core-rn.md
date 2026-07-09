---
title: Common Governance, Risk, and Compliance feature release notes
description: The ServiceNow Integrated Risk Management \(IRM\) application helps enable your organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Integrated Risk Management was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Common Governance, Risk, and Compliance feature release notes

The ServiceNow® Integrated Risk Management \(IRM\) application helps enable your organization to continue to provide its business services during adverse operational events, such as a pandemic, extreme weather, or hacking. Integrated Risk Management was enhanced and updated in the Australia release.

## Integrated Risk Management highlights for the Australia release

-   Automatic redirection from GRC notification links to the appropriate workspace view based on the recipient's persona and access permissions.
-   The Tasks page now loads faster by showing an instant overview of task counts and progressively loading detailed tasks.

See  for more information.

**Important:** Integrated Risk Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   ****

    After upgrading GRC to version 22.0.1, notification links in GRC applications automatically route you to the appropriate workspace view based on your persona and access permissions. If you don't have workspace access, links default to the classic view.

-   ****

    After upgrading GRC to version 22.0.1, the Tasks page loads faster with performance improvements. Task counts display first as an at-a-glance summary, followed by detailed task lists that load progressively. Task data refreshes at regular intervals to keep information current. These improvements provide better scalability for users with high task volumes across multiple task sources.


## UI changes

-   ****

    The Task page now includes a timestamp showing when the task data was last refreshed. Additionally, a notification now displays when the page is refreshing data in the background.


## Changed in this release

-   ****

    After upgrading GRC to version 22.3.6, notification links use dynamic routing rules to redirect you to the correct page, for workspaces where dynamic routing is configured.


-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

-   **Default AI model for issue summarization skill**

    After upgrading to version 22.4.0, the Issue Summarization skill in Now Assist skills for Risk &amp; Sustainability uses Azure OpenAI gpt-5.4-mini as the default model. This update changes the default model for issue summarizations. You can select alternative models, including the newly supported Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini, based on your requirements.


## Activation information

Install Integrated Risk Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Plugin information

-   **New plugins**

    The following plugins are new in Australia:

    -   Integrated risk management foundation \(com.sn\_ai\_irm\_fdn\)
    -   Integrated risk management advanced \(com.sn\_ai\_irm\_adv\)
    -   Integrated risk management prime \(com.sn\_ai\_irm\_prm\)
-   **Renamed or changed plugins**

    Now Assist for IRM has been replaced by:

    -   Enhanced Features for IRM Professional \(sn\_irm\_pro\_plus\)
    -   Enhanced Features for IRM Enterprise \(sn\_irm\_ent\_plus\)
    Contact your ServiceNow administrator to verify which application applies to your instance. All existing functionality and AI agents continue to work in both applications.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/grc-rn-landing.md)

