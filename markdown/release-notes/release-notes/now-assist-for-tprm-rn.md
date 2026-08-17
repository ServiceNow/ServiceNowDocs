---
title: ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes
description: The ServiceNow Now Assist for TPRM application brings generative AI to Third-party Risk Management. ServiceNow Otto for Third-party Risk Management \(TPRM\) is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-11-07"
reading_time_minutes: 5
---

# ServiceNow Otto for Third-party Risk Management \(TPRM\) release notes

The ServiceNow® Now Assist for TPRM application brings generative AI to Third-party Risk Management. ServiceNow Otto for Third-party Risk Management \(TPRM\) is a new application in the Zurich release.

## ServiceNow Otto for Third-party Risk Management \(TPRM\) highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)

Starting with Zurich Patch 12, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Use generative AI to recommend TPRM issues for reviewer validation.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Use ServiceNow Otto for Third-party Risk Management \(TPRM\) to generate concise, AI-powered summaries of TPRM that can help with interpreting complex issue records.
-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.

See [ServiceNow Otto for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/exploring-now-assist-tprm.md) for more information.

**Important:** Now Assist for TPRM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Extended AI model support for Now Assist for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/supporting-information-now-assist-tprm.md)**

    Starting with Zurich Patch 12, ServiceNow Otto for Third-party Risk Management \(TPRM\) supports Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models in addition to previously supported models. Model availability depends on your ServiceNow Otto for Third-party Risk Management \(TPRM\) subscription, providing greater flexibility when selecting the AI model that meets your requirements.


-   **[Generate issue recommendations for TPRM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-recommendation-tprm-issue.md)**

    If you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the if you have the third‑party assessment reviewer role \[sn\_vdr\_risk\_asmt.vendor\_assessment\_reviewer\] and have installed the ServiceNow Otto for Third-party Risk Management \(TPRM\), you can use generative AI to automatically identify and recommend issues based on assessment responses. The TPRM issue management recommendation skill recommends issues with rationalized summaries. Recommended issues are presented for review and are created as standard TPRM issues only after user confirmation.


-   **[Generate a summary of a TPRM issue](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/create-a-summary-of-issue.md)**

    If you have the third-party assessor role \[sn\_vdr\_risk\_asmt.vendor\_assessor\] role and have installed the ServiceNow Otto for Third-party Risk Management \(TPRM\) for TPRM application, you can use generative AI to automatically summarize complex issue records. The TPRM Issue Summarization skill works across all issue states including New, Analyze, Review, Finalize, and Closed and can help reduce manual review time, improve consistency in issue descriptions and remediation guidance, and accelerate triage and reporting for customers managing high volumes of third-party risk data.

-   **[Some generative AI skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

## Changed in this release

-   **[ServiceNow Otto for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/exploring-now-assist-tprm.md)**

    Starting with Zurich Patch 12, Now Assist for Third-party Risk Management is now ServiceNow Otto® for TPRM. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

-   **[Default AI model for issue recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/supporting-information-now-assist-tprm.md)**

    Starting with Zurich Patch 12, the issue recommendation skill in ServiceNow Otto for Third-party Risk Management \(TPRM\) uses Azure OpenAI gpt-4-5-mini as the default model. This update changes the default model for issue recommendations. You can select alternative models, including the newly supported Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini, based on your requirements.

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   ****

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Install the Now Assist for TPRM application by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

After installing ServiceNow Otto for TPRM all ServiceNow Otto for TPRM skills are activated by default.

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console for access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-agent-studio.md)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the Now Assist panel conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **[Third-party Risk Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/third-party-risk-mgt-landing-page.md)**

    The ServiceNow® GRC: Third-party Risk Management \(TPRM\) application enables you to proactively identify, assess, and mitigate risks that are associated with your third-party relationships. TPRM provides a centralized process for managing your portfolio of third parties, assessing and scoring risk, and performing remediation.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/grc-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

