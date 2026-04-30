---
title: Generative AI Controller release notes
description: The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. You can reduce complexity and enhance the user experience in your organization by generating and summarizing content, analyzing user sentiment, and writing unique prompts. Generative AI Controller was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 7
---

# Generative AI Controller release notes

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. You can reduce complexity and enhance the user experience in your organization by generating and summarizing content, analyzing user sentiment, and writing unique prompts. Generative AI Controller was enhanced and updated in the Yokohama release.

## Generative AI Controller highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Protect your users by configuring settings for anonymization of personally identifiable information \(PII\) with the Data Privacy application.

See [Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Generative AI Controller is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Generative AI Controller to Yokohama

Generative AI Controller is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

## New in the Yokohama release

-   **[Administrator access to Gen AI log](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. Records related to HR remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.


-   **[AI Model Version Mappings](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Review the mappings between AI model versions, their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. It shows mapping between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **[Identify third-party LLM information](https://www.servicenow.com/docs/access?context=reference-for-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](generative-ai-controller-rn.md)**

    Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


-   **[Global Model selection for conversational skills](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Configure Data Privacy and Data Discovery to protect the personally identifying information \(PII\) of your users.](https://www.servicenow.com/docs/access?context=configure-now-assist-data-privacy&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Generative AI Controller has changed to use the Data Privacy application instead of the Sensitive Data Handler to help anonymize PII. The process for choosing what gets anonymized and how has shifted to different tables and forms that your administrator must configure for your organization.


## Deprecations

The dependency on Sensitive Data Handler has been removed. Regular expressions that are configured with Sensitive Data Handler are applied to the Data Privacy application with a fix script when you upgrade to Yokohama.

## Activation information

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see [Installing Generative AI Controller](https://www.servicenow.com/docs/access?context=installing-generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) and [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Related ServiceNow applications and features

-   **[Agent Chat](https://www.servicenow.com/docs/access?context=ci-use-agent-chat&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    The ServiceNow® Agent Chat provides various features that agents and requesters can use to streamline the agent and end-user chat experience. Agent Chat also provides features that managers can use to monitor and assist agents.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile®, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The ServiceNow® Customer Service Management \(CSM\) application enables you to provide the service and support that your external customers need. For example, your customers can communicate and get the help through the web, email, chat, telephone, and social media.

-   **[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    The ServiceNow® Field Service Management application enables you to manage work orders and related tasks, resources, skills, assets, and locations. Use this application to dispatch work order tasks and agents to the customer location for performing any kind of field work, such as install, repair, or maintain equipment.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   **[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)**

    The ServiceNow® HR Service Delivery application gives your employees the service experience that they deserve. By providing employees with a single place to manage their work needs while shielding them from back-end complexity, you can deliver a great experience to meet the demands of a current-day workforce.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Knowledge Management \(KM\) application enables the sharing of information in the Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[ITOM AIOps](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    The ServiceNow® ITOM AIOps product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

-   **[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    The ServiceNow® IT Service Management \(ITSM\) solution provides scalable workflows to manage and deliver IT services to your users all through a single cloud-based platform. The ITSM solution can help increase your agents' productivity, resolve issues quickly, and improve user satisfaction.

-   **[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)**

    The Now Assist for Security Operations application permits security analysts to resolve security incidents faster with generative AI skills. Analysts and managers can condense long activity streams on security incidents into concise, easy-to-read summaries and automatically generate closure notes. Now Assist for Security Operations is a new application in the Xanadu release.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables you to integrate workflow authoring, configuring, and monitoring into a single page experience.

-   **[Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

