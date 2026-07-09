---
title: Now Assist release notes
description: The ServiceNow Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-09"
reading_time_minutes: 16
---

# Now Assist release notes

The ServiceNow® Now Assist experience brings generative AI to your organization. You can improve productivity and efficiency by delivering better self-service, recommending actions, delivering answers, and providing your users with AI Search. Now Assist was enhanced and updated in the Yokohama release.

## Now Assist highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Use the Now Assist context menu open prompt feature to create and edit knowledge articles.
-   Use Advanced settings to add conditions to hide or show the Now Assist Context Menu quick actions.
-   Create multiple Now Assist context menu configurations for the same field.
-   Use the Enable for extended tables option in parent table configuration, to enable or disable the inheritance model for the child table configurations.

[Yokohama Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-8.md)

-   Use the Now Assist Readiness Evaluation app to automate the implementation assessment process before implementing Now Assist agentic and generative AI.

[Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)

-   Enable administrators to set up a security access control list \(ACL\) that checks user authentication for Now Assist context menu skills and new setup options. This gives them control over who can use Now Assist context menu skills and actions, as well as the built-in options like shorten, elaborate, and change tone.

-   Use Google Gemini and Anthropic Claude on AWS as AI model providers for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.
-   Select your preferred large language model \(LLM\) provider for Now Assist out-of-box skills. Apart from Now LLM Service, the platform supports Azure OpenAI GPT-4.1 and GPT-4.1 mini, Google Gemini 2.0 Flash and 2.5 Pro, and AWS Anthropic Claude 3.7 Sonnet LLM providers with ServiceNow® third-party model strategy.
-   Select a display option for custom Now Assist context menu event with an option to suppress the modeless window.
-   View the numbered citation and links to the source of information when you use Now Assist context menu for Email reply recommendation.

[Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)

-   Access and monitor your Now Assist skills in the skill list or grid view. By toggling between the layouts, you can navigate from the Now Assist skills to specific products and then back to the skills page.
-   Identify and mark duplicate articles in the list view by using Now Assist in Knowledge Management and take action as required.
-   Apply the Now Assist Sentiment Analysis application to each record so that you can assess how satisfied your customers are. With this feature, you can make better decisions to improve customer experience.
-   Use the Now Assist context menu guided setup to create a Now Assist context menu configuration.
-   Use the Now Assist context menu to deploy the custom skills created using Now Assist skill kit.

-   Monitor how the Now Assist context menu is being used across the different applications with the new Now Assist context menu usage dashboard.
-   Customize the ServiceNow skills with new prompts or providers in the Now Assist Skill Kit for your specific business needs.
-   Enable your users to use voice to interact with the Now Assist panel by enabling the Voice Input setting.
-   Use the new Conversational Q&amp;A option in the Now Assist panel to achieve an enhanced and accurate query resolution.
-   Generate a record summary, share or copy the summary, and provide feedback by using the Summarize option in the Now Assist context menu.
-   Customize and choose between the casual, formal, or sympathetic tone by using the Now Assist context menu.

See [Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md) for more information.

For more Platform Now Assist feature release notes, see the following topics:

-   [AI Search release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/ai-search-rn.md)
-   [Document Intelligence release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/document-intelligence-rn.md)
-   [Now Assist Skill Kit release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/na-skill-kit-rn.md)
-   [Now Assist in Virtual Agent release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-va-rn.md)

**Important:** After purchasing a generative AI product, you can install it from ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist to Yokohama

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

## New in the Yokohama release

-   **[Monitor sensitive topic invocations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/reference-for-generative-ai-controller.md)**

    Access the Gen AI Metrics \[sys\_generative\_ai\_metric\] table to review the logged invocations of sensitive topics and gain insights into how these topics are being triggered and monitored.


-   **[Now Assist Readiness Evaluation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-readiness-evaluation-landing-page.md)**

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


-   **[Manage large language models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/manage-large-language-models.md)**

    Choose and update your preferred large language model \(LLM\) provider at the instance, skill or skill group level for Now Assist out-of-box skills with ServiceNow® third-party model strategy.

    Deactivate skills that are not compliant with any of the LLM providers and access the audit history to view updates by the AI steward.

-   **[Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-dynamic-translation-for-now-assist-applications.md)**

    Manage the default and supported languages by the different LLM providers under Multilingual service for translation.

-   ****

    Access the citations to the articles referenced from the knowledge base. Explore references and insert the suggested reply to your email.

-   **[Now Assist Guardian supports third-party LLMs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-guardian.md)**

    Extend guardrail support to third-party LLMs, such as Amazon Bedrock, Google Cloud \(AI Studio and Vertex\), and OpenAI to ensure any inappropriate content is logged and blocked during content generation.


-   **[Increase the maximum response token limit for custom skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configure-skill-prompt.md)**

    Increase the maximum response token limit for Now Assist custom skill beyond default value 1000 to support dynamic pricing based on output tokens and calculate the price for each skill executed per assist.


-   **[Exploring Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-now-assist-platform.md)**

    Access the Now Assist skills through an identifier tab on the Now Assist Admin console, and find the associated workflows.

    Navigate to your skills by using the intuitive list or grid view. The skill details are displayed, which means that you don't have to make additional selections.

    Access the Data privacy section under Now Assist Admin settings. View and edit the data privacy policies that apply to your Now Assist skills.

-   **Accessing the external content in Now Assist panel Q&amp;A capability**

    Get relevant answers to your questions from external content sources, such as Microsoft SharePoint, Google Drive, and Confluence Cloud, within the Now Assist panel, without manual indexing. Each response shows the source of information to reference later.

-   **[Enhanced log visibility](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-guardian.md)**
    -   Access the Generative AI Metric table \[sys\_generative\_ai\_metric\] to gain insights into the guardian logs and determine if they are for monitoring only or for both logging and blocking. Each guardrail shows its status value as Monitor, Block, or Off, to help administrators to manage their security policies.
    -   View the logs of masking that involve personal identifiable information \(PII\) in the Generative AI Metric table \[sys\_generative\_ai\_metric\]. You can identify which data is masked, the type of request, system response, processing time, errors, or error codes.
-   ****

    Define the output field destination so that you can select any multi-line text field from the base table You can customize incident forms and improve the usability of the resolution notes generation skill.

    Enable requesters to extract information from emails and email attachments to generate tasks. This email-to-task agentic workflow effectively addresses the challenge of task creation from emails.

-   **[Identify and review duplicate Knowledge articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/Now-Assist-identify-and-review-duplicate-articles.md)**

    Identify duplicate Knowledge articles by using Now Assist capabilities. You can review the list and deselect articles that you don’t consider to be duplicates.

-   **[Streaming responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Enable streaming responses on the Now Assist panel. Only synthesized responses are streamed.

-   **[Multiple Now Assist panels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Create separate, independent Now Assist panels that work across Next Experience and ServiceNow® Studio app shells.

-   **[Create Now Assist context Menu configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/create-now-assist-configuration-with-guided-setup.md)**

    Create a Now Assist context menu configuration for a streamlined custom skill deployment process with the help of a guided setup.


-   **[Now Assist Guardian analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-guardian.md)**

    Monitor the performance of offensive content and prompt injections guardrails with the help of the Now Assist Guardian analytics dashboard.

-   **[Configuring Now Assist settings and features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-na-landing.md)**

    For custom skills, explore an additional display option in the form of **Conversational experiences**. You can select Now Assist Virtual Agent to assist you with the display.

    Create and activate a Now Assist skill copy, and have both the original skill and its copy to remain active simultaneously.


-   **[Now Assist Context Menu usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-context-menu-dashboard.md)**

    View and monitor the use of the Now Assist context menu across the different applications. Gain insights into the usage patterns, frequency, and effectiveness of the context menu actions with the Now Assist context menu usage dashboard.

-   **[Customizing ServiceNow skills in the Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/clone-and-edit-servicenow-skill.md)**

    Clone the skills provided by ServiceNow in Now Assist applications by using the Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. By editing the prompt, you can choose the additional inputs to be considered by the large language model \(LLM\) and arrange the formatting and content of the LLM response. After the skill is edited, you can activate the edited skill in the Now Assist Admin console to enable it.

-   **[Enabling the voice input for the Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Enable the Voice Input setting for the Now Assist panel in the Now Assist Admin console. This setting gives users a voice-to-text input option to access the skills in the Now Assist panel in any supported language. After it’s enabled, the option is available in individual user accessibility preferences.

-   **[Setting your data overflow processing preferences to control your data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configure-na-data-overflow.md)**

    Set your data overflow processing preferences to control your data. By default, all Now Assist network traffic is managed within ServiceNow datacenters, but during periods of high traffic, the traffic is burst to Microsoft Azure datacenters. You can choose whether you want to opt out of cloud bursting from the Now Assist Admin console data overflow processing settings.

-   **Using multi-turn Q&amp;A in the Now Assist panel**

    Ask questions and get relevant answers directly in the Now Assist panel. The system remembers your previous questions for effortless follow-ups and pulls answers from multiple sources to give you the best results. You can select the source name in the response to access the full Knowledge article for more details.


-   **Using dashboard and visualization export in the Now Assist panel**

    Export Platform Analytics dashboards and data visualizations through conversations. You can select from several output formats, and download or email the files.


-   **[Summarize records with the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/summarize-with-now-assist-context-menu.md)**

    Generate summaries by using the Now Assist context menu for the Core UI and Workspace. You can also expand or collapse the summary card, regenerate the summary, copy and share the summary, or provide feedback.


-   **[Email recommendations using the Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/email-recommendations-nacm.md)**

    Select and choose the tone of your content with the change tone feature. You can select from the elaborate, shorten, casual, formal, or sympathetic tone.


## UI changes

-   **[Edit a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/edit-a-now-assist-skill.md)**

    You can now view the Helpful resources and Frequently asked questions \(FAQ\) tabs on the list view of the Now Assist skills page.

-   **[Email reply recommendation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills.md)**

    The email response creation skill offers guidance in choosing the most appropriate template based on the user's specific context. Additionally, it identifies the potential errors when a response isn't generated as intended.

-   **[Now Assist data sharing opt-out moved to Data sharing and processing tab.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md)**

    The opt-out button in the data sharing card from the Now Assist Admin Account page has moved to the Settings page on the **Data sharing and processing** tab.

-   **[Now Assist context menu](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-write-overview.md)**

    You can now open the Now Assist context menu by selecting the Now Assist context menu icon \(\[Omitted image "wwna-icon.png"\] Alt text: Now Assist Context menu icon.\) for effortless access.

    The Now Assist context menu enables users to automatically select a sentence, paragraph, or the entire content even if they initially make a partial selection. Administrators can configure the selection to be a sentence, paragraph, or the entire content.

    The dynamic header label next to the Now Assist context menu icon can be customized to display the query status.

    The new Now Assist context menu icon \(\[Omitted image "wwna-icon.png"\] Alt text: Context menu icon .\) was updated with an enhanced animation.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


-   **[Configure multilingual service for Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-dynamic-translation-for-now-assist-applications.md)**

    Enable translation settings is now Multilingual service in Now Assist admin console.

-   **[Default email client for email recommendation skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills.md)**

    The Seismic email client is enabled by default on Core UI with the activation of email recommendation. This client provides the Generative AI application features for creating email responses, draft management, and template management.

-   **[Now Assist panel response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)Now Assist panel response**

    With the carousel experience removed, the Now Assist panel now generates a synthesized response for any user inquiry. This response includes content from Knowledge articles, flows &amp; actions, skills, and links to those articles, instead of only the Now Assist panel skills.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)
-   [Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-development/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/now-assist-landing-cmdb.md)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-for-cwm-landing.md)
-   [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/build-workflows/now-assist-for-creator-landing.md)
-   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/customer-service-management/now-assist-csm.md)
-   [Now Assist for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assisit-employee-exp.md)
-   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/application-portfolio-management/now-assist-ea.md)
-   [Now Assist for Operational Sustainability \(formerly ESG\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/field-service-management/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-ham.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-hrsd.md)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/now-assist-for-irm.md)
-   [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-lsd-landing.md)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/operational-technology/now-assist-for-otm-landing.md)
-   [Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/order-management/now-assist-order-management.md)
-   [Now Assist for PSDS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/government-industry/now-assist-for-psds.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-security-incident-landing.md)
-   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-sam.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-business-management/now-assist-spm.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/telecom-media-technology/now-assist-spmc.md)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/governance-risk-compliance/now-assist-tprm.md)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/employee-service-management/now-assist-wsd-landing.md)
-   [Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/security-management/now-assist-for-vulnerability-response-landing.md)

## Additional requirements

The Next Experience UI Framework must be enabled before you can use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Accessibility information

-   **Voice Input for Now Assist**

    Administrators can enable an optional voice input setting for the Now Assist panel in the Now Assist Admin console. This feature gives users a voice-to-text input option to access the Now Assist skills in the panel in any supported language. For more information, see [Enable voice input for Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/enable-voice-input-for-now-assist-panel.md).

    Once enabled, the Enable voice input for the Now Assist panel option are available in individual user accessibility preferences. See [Configure Next Experience accessibility preferences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/next-experience-accessibility-preferences.md) for more information.

    Voice-to-text input can help users with mobility impairments access generative AI skills without using a keyboard. This feature can also be useful to blind or low-vision users, neurodivergent users, non-native language speakers, or mobile users on the go, such as field service agents.


## Localization information

Now Assist supports Dynamic Translation for Yokohama.

## Related ServiceNow applications and features

-   **[Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/conversational-interfaces/ci-use-agent-chat.md)**

    ServiceNow® Agent Chat provides various features that agents and requesters can use to streamline the agent and end-user chat experience. Agent Chat also provides features that managers can use to monitor and assist agents.

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/document-intelligence-landing.md)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an artificial intelligence \(AI\) solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/dynamic-translation-overview.md)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/servicenow-platform/knowledge-management.md)**

    The ServiceNow® Knowledge Management application enables the sharing of information in Knowledge Base. These Knowledge Base contain articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[Configurable Workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/workspace-landing-page.md)**

    ServiceNow® Workspace is a graphical user interface that puts multiple tools on one page, including the tools that agents use to find, research, and resolve issues.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

