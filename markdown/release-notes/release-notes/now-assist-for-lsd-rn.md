---
title: Now Assist for Legal Service Delivery \(LSD\) release notes
description: The ServiceNow Now Assist for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. Now Assist for Legal Service Delivery \(LSD\) was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Now Assist for Legal Service Delivery \(LSD\) release notes

The ServiceNow® Now Assist for Legal Service Delivery \(LSD\) application leverages generative AI capabilities to summarize a legal request or legal matter so that you understand the context, refresh the summary, and post the summary to the work notes. This summary helps you to understand the context faster. Now Assist for Legal Service Delivery \(LSD\) was enhanced and updated in the Yokohama release.

## Now Assist for Legal Service Delivery \(LSD\) highlights for the Yokohama release

Yokohama Patch 11

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

See [Explore Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-exploring&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Legal Service Delivery \(LSD\) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Now LLM LTS support for Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-llm-model-updates&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## Changed in this release

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install Now Assist for Legal Service Delivery \(LSD\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

The Now Assist for Legal Service Delivery \(LSD\) application works with the latest stable versions of popular web browsers. To find the list of supported browsers, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Related ServiceNow applications and features

-   **[Legal Service Delivery](https://www.servicenow.com/docs/access?context=legal-management-overview&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    Use to connect employees and legal teams through a unified platform with intelligent workflows, streamlining legal requests and managing complex matters efficiently via the Legal Counsel Center.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and easy access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use to improve productivity and efficiency in your organization, deliver better self-service, suggest actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide generative AI skills to meet the needs of users in different workflows. These AI skills include case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[Legal Service Delivery release notes](lsd-rn-landing-page.md)

