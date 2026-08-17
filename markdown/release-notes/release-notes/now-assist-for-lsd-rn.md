---
title: ServiceNow Otto for Legal Service Delivery \(LSD\) release notes
description: The ServiceNow ServiceNow Otto for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. ServiceNow Otto for Legal Service Delivery \(LSD\) was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
---

# ServiceNow Otto for Legal Service Delivery \(LSD\) release notes

The ServiceNow® ServiceNow Otto for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. ServiceNow Otto for Legal Service Delivery \(LSD\) was enhanced and updated in the Yokohama release.

## ServiceNow Otto for Legal Service Delivery \(LSD\) highlights for the Yokohama release

Yokohama Patch 11

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See  for more information.

**Important:** ServiceNow Otto for Legal Service Delivery \(LSD\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **Now LLM LTS support for ServiceNow Otto for Legal Service Delivery \(LSD\)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **New third-party AI model provider options available for all Now Assist applications**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## Changed in this release

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Role configuration required for agentic workflows and AI agents**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install ServiceNow Otto for Legal Service Delivery \(LSD\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Browser requirements

The ServiceNow Otto for Legal Service Delivery \(LSD\) application works with the latest stable versions of popular web browsers. To find the list of supported browsers, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/browser-support.md).

## Related ServiceNow applications and features

-   ****

    Use to connect employees and legal teams through a unified platform with intelligent workflows, streamlining legal requests and managing complex matters efficiently via the Legal Counsel Center.

-   ****

    Use the AI Admin Hub console to provide you with quick and easy access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Use to improve productivity and efficiency in your organization, deliver better self-service, suggest actions, provide answers, and empower your users to search more effectively.

-   ****

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows. These AI skills include case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/lsd-rn-landing-page.md)

