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

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Protect your users by configuring settings for anonymization of personally identifiable information \(PII\) with the Data Privacy application.

See Generative AI Controller for more information.

**Important:** Generative AI Controller is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Generative AI Controller to Yokohama

Generative AI Controller is installed and updated when you install or update any Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) for steps that may address your issue. Otherwise, you can make a Support case.

## New in the Yokohama release

-   ****

    Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


-   **Administrator access to Gen AI log**

    Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. Records related to HR remain restricted to HR admins.

-   **Enhanced AI asset inventory**

    Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.


-   **AI Model Version Mappings**

    Review the mappings between AI model versions, their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. It shows mapping between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **Identify third-party LLM information**

    Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/generative-ai-controller-rn.md)**

    Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


-   **Global Model selection for conversational skills**

    Enable Now Assist Admins to choose between GPT4.o and Now Assist LLM model for data routing at a global level. This ensures compliance with any regional restrictions and helpful for APAC users who may face limitations with US-based models, such as GPT-4.0.


## Changed in this release

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **Configure Data Privacy and Data Discovery to protect the personally identifying information \(PII\) of your users.**

    Generative AI Controller has changed to use the Data Privacy application instead of the Sensitive Data Handler to help anonymize PII. The process for choosing what gets anonymized and how has shifted to different tables and forms that your administrator must configure for your organization.


## Deprecations

The dependency on Sensitive Data Handler has been removed. Regular expressions that are configured with Sensitive Data Handler are applied to the Data Privacy application with a fix script when you upgrade to Yokohama.

## Activation information

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see Installing Generative AI Controller and Install Now Assist plugins.

## Related ServiceNow applications and features

-   **[Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/ci-use-agent-chat.md)**

    The ServiceNow® Agent Chat provides various features that agents and requesters can use to streamline the agent and end-user chat experience. Agent Chat also provides features that managers can use to monitor and assist agents.

-   ****

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile®, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    The ServiceNow® Customer Service Management \(CSM\) application enables you to provide the service and support that your external customers need. For example, your customers can communicate and get the help through the web, email, chat, telephone, and social media.

-   ****

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/fsm-application-landing-page.md)**

    The ServiceNow® Field Service Management application enables you to manage work orders and related tasks, resources, skills, assets, and locations. Use this application to dispatch work order tasks and agents to the customer location for performing any kind of field work, such as install, repair, or maintain equipment.

-   ****

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   ****

    The ServiceNow® HR Service Delivery application gives your employees the service experience that they deserve. By providing employees with a single place to manage their work needs while shielding them from back-end complexity, you can deliver a great experience to meet the demands of a current-day workforce.

-   ****

    The ServiceNow® Knowledge Management \(KM\) application enables the sharing of information in the Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   ****

    The ServiceNow® ITOM Health product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

-   ****

    The ServiceNow® IT Service Management \(ITSM\) solution provides scalable workflows to manage and deliver IT services to your users all through a single cloud-based platform. The ITSM solution can help increase your agents' productivity, resolve issues quickly, and improve user satisfaction.

-   **[Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/security-operations-landing-page.md)**

    The Now Assist for Security Operations application permits security analysts to resolve security incidents faster with generative AI skills. Analysts and managers can condense long activity streams on security incidents into concise, easy-to-read summaries and automatically generate closure notes. Now Assist for Security Operations is a new application in the Xanadu release.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/workflow-studio.md)**

    ServiceNow® Workflow Studio enables you to integrate workflow authoring, configuring, and monitoring into a single page experience.

-   ****

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

