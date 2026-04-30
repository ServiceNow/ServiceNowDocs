---
title: Now Assist release notes
description: The ServiceNow Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-11-19"
reading_time_minutes: 11
---

# Now Assist release notes

The ServiceNow® Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Xanadu release.

## Now Assist highlights for the Xanadu release

[Xanadu Patch 10](../quality/xanadu-patch-10.md)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

[Xanadu Patch 3](../quality/xanadu-patch-3.md)

-   Protect your users from offensive content, prompt injection attacks, and filtered subjects in AI-generated content with Now Assist Guardian.
-   Use the native translation capabilities of the Now LLM Service models to speak to users in their preferred languages.
-   Troubleshoot Now Assist skills from the Now Assist Admin console to locate the sources of configuration problems.
-   Monitor the usage and performance of generative AI features and capabilities offered under Now Assist from the Analytics tab in the Now Assist Admin console.
-   Use the multi-language capabilities of Now Assist to generate a Knowledge article for an incident, case, or other supported task type in a language other than English.
-   Enable agents to utilize the generative AI capabilities of Now Assist to shorten or elaborate content in a Knowledge article using the context menu feature.
-   Now Assist context menu enhancements.

[Xanadu Patch 1](../quality/xanadu-patch-1.md)

-   Support users who speak different languages with multi-language, dynamic translation.
-   Make finding tables and lists easier and more efficient by using the navigation platform skill in the Now Assist panel.
-   Write with Now Assist to provide chat and email suggestions for agents based on the content of a conversation.
-   Enable developers to create their own custom skills by using the Now Assist Skill Kit.
-   Generate a Knowledge Base article from a selection of similar cases or incidents to help address related concerns in a single article with Now Assist in Knowledge Management.

See [Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for more information.

For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](../now-platform-administration/ai-search-rn.md)
-   [Document Intelligence release notes](document-intelligence-rn.md)
-   [Generative AI Controller release notes](generative-ai-controller-rn.md)
-   [Now Assist in Virtual Agent release notes](../now-platform-capabilities/now-assist-va-rn.md)

**Important:** After purchasing a generative AI product, you can install it from the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist to Xanadu

If you customized UI actions or other items that are associated with Now Assist skills, confirm that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

## New in the Xanadu release

-   **[Now Assist Readiness Evaluation](https://www.servicenow.com/docs/access?context=now-assist-readiness-evaluation-landing-page&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Readiness Evaluation app to help you evaluate your organization's readiness to implement agentic and generative AI Now Assist capabilities.

    Assessments for agentic AI include:

    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
    Assessments for generative AI include:

    -   AI Search
    -   Virtual Agent \(VA\)
    -   IT Service Management \(ITSM\)
    -   Customer Service Management \(CSM\)
    -   HR Service Delivery \(HRSD\)
    Results shown are estimates. You should evaluate results provided by Now Assist Readiness Evaluation for accuracy and appropriateness for your use case.


-   **[Now Assist Guardian adds guardrails to log, block, and redirect unwanted content](https://www.servicenow.com/docs/access?context=now-assist-guardian&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Protect your users from offensive content, certain kinds of prompt injection attacks, and sensitive topics by logging attempts, blocking content, or redirecting to a new Virtual Agent topic.

-   **[Translation for Now Assist with native translation](https://www.servicenow.com/docs/access?context=translation-for-now-assist&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the native translation capabilities of the Now LLM Service models or to translate user-generated and LLM-generated content into the preferred languages of your users.

-   **[Troubleshoot a Now Assist skill](https://www.servicenow.com/docs/access?context=troubleshoot-a-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Run diagnostics on certain Now Assist skills to identify common configuration errors that help to prevent your skills from working as intended.

-   **[Analyze Now Assist performance](https://www.servicenow.com/docs/access?context=now-assist-analytics&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Analytics dashboard to monitor the usage and performance of generative AI features and capabilities offered under Now Assist.

-   **[Configure and use a retriever with Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=add-retriever&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Augment and add context to your prompts with AI Search results from custom retriever inputs.

-   **[Get prompt assistance with Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=use-prompt-assistance&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Use prompt assistance to get a jump-start with your prompt development by selecting an example from the prompt library or using Now Assist to generate one.

-   **[Evaluate skill prompts](https://www.servicenow.com/docs/access?context=evaluate-prompt&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Evaluate your prompts created within Now Assist Skill Kit using data collections created within Now Assist Data Kit. Evaluations return information on the correctness and faithfulness of the responses from running the custom skill.

-   **[View skill run test history](https://www.servicenow.com/docs/access?context=test-prompt-template&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    View the history of your test results to assist your understanding of how changes to the prompt have adjusted the outcome.

-   **[Generate a Knowledge article using multi-language support](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-multilanguage-support&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Generate a Knowledge article for an incident, case, or other supported task type in languages other than English using the multi-language capabilities of Now Assist.

-   **[Edit an article using the Now Assist context menu](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-using-context-menu&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Use generative AI capabilities of Now Assist to shorten or elaborate content within a Knowledge article.

-   **[Use Now Assist Data Kit to add a dataset to the data catalog](https://www.servicenow.com/docs/access?context=now-assist-data-kit-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Create a data collection and select the sampling data for publication. Once published, the evaluation data is available in Now Assist Skill Kit.

-   **[Now Assist context menu](https://www.servicenow.com/docs/access?context=now-assist-write-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**
    -   Write with Now Assist is now called the Now Assist context menu.
    -   Explain the assessed and calculated change request risk with the Now Assist context menu in workspaces and UI16.
    -   Use the **Elaborate** and **Shorten** content editing capabilities of the Now Assist context menu in Knowledge articles.
    -   Configure the maximum number of content refinement calls using the Now Assist context menu.
    -   Use the Now Assist context menu recommendations to compose an email and complete the drafts.

-   **[Dynamic theming enables different themes to be applied to chat summarization cards](https://www.servicenow.com/docs/access?context=now-assist-chat-summary&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Support dynamic theming for chat summarization cards.

-   **[Write with Now Assist](https://www.servicenow.com/docs/access?context=now-assist-write-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    Enable your agents to use Write with Now Assist for generative AI-powered text generation and editing assistance. This feature helps to improve and streamline their writing responsibilities.

-   **Use Now Assist [Platform skills](https://www.servicenow.com/docs/access?context=na-platform-skills&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**
    -   Use generative AI Platform skills in the Platform workflow starting with the Xanadu release to enhance and streamline your user experience.
    -   Enter search commands in plain language to retrieve and filter records and tables by using the [Navigation](https://www.servicenow.com/docs/access?context=now-assist-global-navigation&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) skill.
-   **Use [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US) for Generative AI app developers**

    Create and activate custom prompts and skills for your Now Assist agent use cases.

-   **Generate a knowledge article from multiple cases or incidents with [Now Assist in Knowledge Management](https://www.servicenow.com/docs/access?context=Now-Assist-generate-article-coreui&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Draft Knowledge articles quickly from a configurable workspace or the classic environment based on similar cases or incidents with  Now Assist. Knowledge articles can be generated by selecting from a list of similar cases or incidents, case or incident numbers, or even by searching keywords specific to a case or incident.


## UI changes

-   **[Write with Now Assist has been renamed as the Now Assist context menu](https://www.servicenow.com/docs/access?context=now-assist-write-overview&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    The Now Assist context menu uses generative AI to help agents create and edit written content, which streamlines writing tasks.

-   **[New step in chat summarization guided setup](https://www.servicenow.com/docs/access?context=configure-chat-summarization-in-the-now-assist-admin-console&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    You can now use the **Customize output** step to choose between paragraph and bulleted list formats.

-   **[Service Portal and Virtual Agent display Genius Result answer cards in a carousel](https://www.servicenow.com/docs/access?context=use-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    When a search returns multiple Genius Result answers, Service Portal and Virtual Agent display Genius Result answer cards in a carousel instead of a list. The modified UI lets you scroll through multiple Genius Result answers while keeping your search query's regular results more accessible on the results screen.

-   **[Legal disclaimer in Now Assist panel and Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=using-now-assist-in-va&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The following text appears at the top of any Now Assist panel or Now Assist in Virtual Agent conversation: `Answers generated by AI. Review for accuracy.`


## Changed in this release

-   **[New conditions available in Define Availability step of guided setup for chat reply recommendation](https://www.servicenow.com/docs/access?context=configure-a-now-assist-skill&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    When activating or editing the chat reply recommendation skill, you can now add conditions to determine who can use the skill.


-   **[__Get started__ step added to guided setup for resolution note generation](https://www.servicenow.com/docs/access?context=now-assist-rn-summarization&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    A step has been added to the guided setup for the resolution notes generation skill to remind you to update any customized code that is associated with the skill after a new release.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=xanadu&pubname=xanadu-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=xanadu&pubname=xanadu-government-industry&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=xanadu&pubname=xanadu-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=xanadu&pubname=xanadu-telecom-media-technology&ft:locale=en-US)

For more information, see [Install Now Assist plugins](https://www.servicenow.com/docs/access?context=install-now-assist-feature-plugins&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US).

## Additional requirements

The Next Experience UI Framework must be enabled to use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Xanadu.

## Related ServiceNow applications and features

-   **[Agent Chat](https://www.servicenow.com/docs/access?context=ci-use-agent-chat&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)**

    The ServiceNow® Agent Chat provides various features that agents and requesters can use to streamline the agent and end-user chat experience. Agent Chat also provides features that managers can use to monitor and assist agents.

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile®, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=xanadu&pubname=xanadu-customer-service-management&ft:locale=en-US)**

    The ServiceNow® Customer Service Management \(CSM\) application enables you to provide the service and support that your external customers need. For example, your customers can communicate and get the help through the web, email, chat, telephone, and social media.

-   **[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    The ServiceNow® Field Service Management application enables you to manage work orders and related tasks, resources, skills, assets, and locations. Use this application to dispatch work order tasks and agents to the customer location for performing any kind of field work, such as install, repair, or maintain equipment.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=xanadu&pubname=xanadu-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   **[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery&version=xanadu&pubname=xanadu-employee-service-management&ft:locale=en-US)**

    The ServiceNow® HR Service Delivery application gives your employees the service experience that they deserve. By providing employees with a single place to manage their work needs while shielding them from back-end complexity, you can deliver a great experience to meet the demands of a current-day workforce.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Knowledge Management \(KM\) application enables the sharing of information in the Knowledge Base. A Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[ITOM Health](https://www.servicenow.com/docs/access?context=itom-health-landing-page&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The ServiceNow® ITOM Health product includes the ServiceNow® Event Management and ServiceNow® Metric Intelligence applications, which help you track and maintain the health of services in your organization.

-   **[IT Service Management](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US)**

    The ServiceNow® IT Service Management \(ITSM\) solution provides scalable workflows to manage and deliver IT services to your users all through a single cloud-based platform. The ITSM solution can help increase your agents' productivity, resolve issues quickly, and improve user satisfaction.

-   **[Security Operations](https://www.servicenow.com/docs/access?context=security-operations-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Now Assist for Security Operations application permits security analysts to resolve security incidents faster with generative AI skills. Analysts and managers can condense long activity streams on security incidents into concise, easy-to-read summaries and automatically generate closure notes. Now Assist for Security Operations is a new application in the Xanadu release.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables you to integrate workflow authoring, configuring, and monitoring into a single page experience.

-   **[Configurable Workspace UI](https://www.servicenow.com/docs/access?context=workspace-landing-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues.


**Parent Topic:**[Intelligent Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist release notes](../now-assist/now-assist-rn-landing.md)

