---
title: Generative AI Controller release notes
description: The ServiceNow Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 6
---

# Generative AI Controller release notes

The ServiceNow® Generative AI Controller application enables you to use generative AI capabilities with third-party large language model \(LLM\) providers on the ServiceNow AI Platform. Generate and summarize content, analyze user sentiment, and write unique prompts. Generative AI Controller was enhanced and updated in the Zurich release.

## Generative AI Controller highlights for the Zurich release

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Generative AI event logs are now retained for 180 days, up from 30 days.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Connect your Azure OpenAI deployment to Generative AI Controller by configuring a custom resource path in your bring your own key \(BYOK\) model configuration.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Access the Gen AI log for debugging insights, with HR-related records remaining restricted.
-   Promote stability with the Long-Term Stable \(LTS\) model for generative AI.

-   Identify third-party LLM information, including model, version, and language.
-   Restrict LLM usage based on domain.

See [Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generative-ai-controller.md) for more information.

**Important:** Generative AI Controller is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Generative AI Controller to Zurich

Generative AI Controller is installed or updated when you install or update a Now Assist application. If you have issues installing or updating applications, see this [knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452) or open a support case.

## New in the Zurich release

-   **[Extended log retention for generative AI events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Retain records in the Generative AI Log \[sys\_generative\_ai\_log\] table for 180 days, up from 30 days, to stay compliant with retention requirements.


-   **[Configure a custom resource path for BYOK models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-custom-resource-path-byok.md)**

    Connect Generative AI Controller to your Azure OpenAI deployment by configuring a custom resource path in your bring your own key \(BYOK\) model configuration. Use this when your Azure OpenAI endpoint includes a path segment that Generative AI Controller does not add by default.


-   **[Administrator access to Gen AI log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Access the Gen AI log \[sys\_generative\_ai\_log\] table to gain insights for debugging purposes. HR-related records remain restricted to HR admins.

-   **[Enhanced AI asset inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Track the enhanced AI asset inventory through AI Control Tower using new metadata fields in the Model \[sys\_generative\_ai\_model\_config\] and Prompt \[sys\_generative\_ai\_config\] tables. Gain better visibility into AI asset status and life-cycle details, such as retirement dates.

-   **[Long-Term Stable model for generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/long-term-stable-models.md)**

    Promote stability and adoption for entitled users with a Long-Term Stable \(LTS\) model. The LTS model provides regulatory alignment, predictable behavior, and life cycle stability to integrate GenAI with confidence.


-   **[AI Model Version Mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Review the mappings between AI model versions and their providers in the Gen AI Model Version Mapping \[sys\_gen\_ai\_model\_version\_mapping\] table. This table shows the mappings between source and target models, along with associated metadata, such as skill type, model type, resource associations, and provider information.


-   **[Identify third-party LLM information](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Access the Gen AI Log Metadata \[sys\_gen\_ai\_log\_metadata\] table to identify which LLM model, version, and requested language was used to generate the AI content.

-   **[Restrict LLM usage based on the domain](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Enable or disable Now Assist for each domain so that you can restrict the use of LLMs and avoid using AI for data processing, if needed.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Direct action calls removed from Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md)**

    Starting with Zurich Patch 5, the Generative AI Controller \(GAIC\) no longer supports direct action calls in order to support the security requirements that all AI capabilities be protected by Access Control Lists \(ACLs\). To create custom generative AI functionality, use AI Skill Kit instead.

    -   Configure actions in the Generative AI Controller
    -   Generate Content to create AI-generated text responses
    -   QnA to answer user questions
    -   Summarize to shorten long or complex text
    -   Generic Prompt to generate ideas or content on any topic
    -   Sentiment Analysis to identify the sentiment of user input
    For more information, refer to [KB KB2716977: Generative AI Controller actions are no longer avaliable for custom workflows](https://support.servicenow.com/kb?sys_kb_id=6460540047ee7a9048cb2920326d4302&id=kb_article_view).


## Activation information

Generative AI Controller is a ServiceNow AI Platform feature that is available with activation of a Now Assist application. For details, see [Installing Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/installing-generative-ai-controller.md) and [Install plugins for ServiceNow Otto](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/install-now-assist-feature-plugins.md).

## Localization information

Generative AI Controller uses Microsoft Azure OEM for Dynamic Translation in Now Assist for multilanguage support. You can enable dynamic translation from the AI Admin Hub console. For more information, see [Microsoft Azure OEM for Dynamic Translation in Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/dynamic-translation-na-ms-azure-oem.md).

## Related ServiceNow applications and features

-   **[Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ci-use-agent-chat.md)**

    The ServiceNow® Agent Chat provides various features that agents and requesters can use to streamline the agent and end-user chat experience. Agent Chat also provides features that managers can use to monitor and assist agents.

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile®, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/c_CustomerServiceManagement.md)**

    The ServiceNow® Customer Service Management \(CSM\) application enables you to provide the service and support that your external customers need. For example, your customers can communicate and get help through the web, email, chat, telephone, and social media.

-   **[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation-overview.md)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/fsm-application-landing-page.md)**

    The ServiceNow® Facilities Service Management application enables you to manage work orders and related tasks, resources, skills, assets, and locations. Use this application to dispatch work order tasks and agents to the customer location for performing any kind of field work, such as installing, repairing, or maintaining equipment.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party LLMs with your workflows.

-   **[HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/hr-service-delivery.md)**

    The ServiceNow® HR Service Delivery application gives your employees the service experience that they deserve. By providing employees with a single place to manage their work needs while shielding them from back-end complexity, you can deliver a great experience to meet the demands of a current-day workforce.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management.md)**

    The ServiceNow® Knowledge Management application enables the sharing of information in the knowledge base. A knowledge base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[ITOM AIOps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/itom-health-landing-page.md)**

    The ServiceNow® ITOM AIOps product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

-   **[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/r_ITServiceManagement.md)**

    The ServiceNow® IT Service Management solution provides scalable workflows to manage and deliver IT services to your users all through a single cloud-based platform. The ITSM solution can help increase your agents' productivity, resolve issues quickly, and improve user satisfaction.

-   **[Now Assist for Security Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-security-incident-landing.md)**

    The Now Assist for Security Operations application permits security analysts to resolve security incidents faster with generative AI skills. Analysts and managers can condense long activity streams on security incidents into concise, easy-to-read summaries and automatically generate closure notes.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    ServiceNow® Workflow Studio enables you to integrate workflow authoring, configuring, and monitoring into a single page experience.

-   **[Configurable Workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/workspace-landing-page.md)**

    ServiceNow® Configurable Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

