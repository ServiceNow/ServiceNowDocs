---
title: Now Assist Skill Kit release notes
description: The ServiceNow Now Assist Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. Now Assist Skill Kit was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Now Assist Skill Kit release notes

The ServiceNow® Now Assist Skill Kit application enables AI developers to create custom skills and to have greater flexibility with the generative AI capabilities of Now Assist. Now Assist Skill Kit was enhanced and updated in the Zurich release.

## Now Assist Skill Kit highlights for the Zurich release

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Use labeling workflows to annotate UI templates.
-   Use structured output to constrain AI responses to predefined JSON schemas.
-   Improve overisght and compliance with AI Control Tower integration with your custom large language model.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Create a custom model to meet your specific needs and control behavior.
-   Customize ServiceNow skills by modifying the prompt, inputs, and providers.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Set up a security access control list to verify user authentication for Now Assist Skill Kit.
-   Use Document Intelligence as a tool when you create a skill.

-   Use UI Builder to deploy custom skills.
-   Use a custom data generator to create synthetic datasets.

See [Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skill-kit-landing.md) for more information.

**Important:** Now Assist Skill Kit is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Labelling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/nadk-labelling.md)Use labeling workflows to annotate UI templates**

    Use the labeling framework to create and manage ground truth data. Published data collections can now be turned into labeling projects. Each record becomes a task assigned to labelers who annotate using pre-configured UI templates

-   **[s](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-skill-prompt.md)Structured output support for AI responses**

    Enables consistent parsing in agentic workflows and reduces ambiguity in downstream automation.

-   **[Use multi-table data generator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/use-multi-table-data-generator.md)New multi-table synthetic data generation option**

    You can generate related records across multiple tables in a single operation. You no longer need to generate each table separately and manually link records. Define your table relationships, set the cardinality and Now Assist Data Kit generates coherent, referentially linked records across all tables in one pass, with foreign key integrity maintained automatically. 

-   **[Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-model.md)AI Control Tower integration with custom LLMs.**

    Improve oversight and compliance for AI deployments with formal approval flows for custom models.

-   **[Now Assist Skill Kit roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-skill-kit-roles.md)Update to the abilities of the admin role**

    The sn\_skill\_builder.admin role is now broken into smaller, task-specific roles, including a custom LLM-specific admin role.


-   **[Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/create-model.md)**

    When you bring your own model you can keep data in your own environment and fine-tune it to meet your specific needs.


-   **[New third-party AI model provider options available for all AI applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for generative AI skills and AI agents, in addition to Now LLM Service and Azure OpenAI.

-   **[New skill deployment option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configure-skill-settings.md)**

    Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/na-data-kit-generate-data.md)**

    When you create synthetic data, you can select what language you want to receive the data in.

-   **AI-assisted ground truth**

    Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/add-dataset.md)**

    Import data from a CSV file to create a dataset.

-   **Create a custom data generator**

    Create and use a custom data generator to create synthetic data.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Zurich Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Now Assist features are available with activation of any Now Assist plugins from ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-apo.md)
-   [Now Assist for App Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise.md)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/now-assist-landing-cmdb.md)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-for-cwm-landing.md)
-   [Now Assist for Creator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/now-assist-for-creator-landing.md)
-   [Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/now-assist-csm.md)
-   [Now Assist for Employee Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assisit-employee-exp.md)
-   [Now Assist for Enterprise Architecture \(EA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-portfolio-management/now-assist-ea.md)
-   [Now Assist for Operational Sustainability Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/environmental-social-governance/now-assist-for-esg.md)
-   [Now Assist for Field Service Management \(FSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/now-assist-fsm.md)
-   [Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/financial-services-operations/now-assist-for-financial-services-operations.md)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-ham.md)
-   [Now Assist for Health and Safety](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hs-landing.md)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-hrsd.md)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-for-irm.md)
-   [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-operations-management/now-assist-itom.md)
-   [Now Assist for IT Service Management \(ITSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/now-assist-itsm.md)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-lsd-landing.md)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-otm-landing.md)
-   [Now Assist for Operational Technology Service Management \(OTSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/operational-technology/now-assist-for-operational-technology-service-management.md)
-   [Now Assist for Order Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/now-assist-order-management.md)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/government-industry/now-assist-for-psds.md)
-   [Now Assist for Sales Force Automation \(SFA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/order-management/now-assist-for-sales-and-order-management-som.md)
-   [Now Assist for Security Incident Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-security-incident-landing.md)
-   [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam.md)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-slo.md)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/source-to-pay-operations/now-assist-spo.md)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-business-management/now-assist-spm.md)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/telecom-media-technology/now-assist-spmc.md)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/governance-risk-compliance/now-assist-tprm.md)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/employee-service-management/now-assist-wsd-landing.md)
-   [Now Assist for Vulnerability Response](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/security-management/now-assist-for-vulnerability-response-landing.md)
-   [Now Assist for Zero Copy Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/now-assist-for-zero-copy-connector-for-erp.md)

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Zurich.

## Related ServiceNow applications and features

-   **[AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/overview-ais.md)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/document-intelligence-landing.md)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an artificial intelligence \(AI\) solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/dynamic-translation-overview.md)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Generative AI Controller](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/generative-ai-controller.md)**

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management.md)**

    The ServiceNow® Knowledge Management application enables the sharing of information in the Knowledge Base. The Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[Now Assist in Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/now-assist-in-va-landing.md)**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

