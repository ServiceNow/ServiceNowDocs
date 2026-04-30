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

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Use labeling workflows to annotate UI templates.
-   Use structured output to constrain AI responses to predefined JSON schemas.
-   Improve overisght and compliance with AI Control Tower integration with your custom large language model.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Create a custom model to meet your specific needs and control behavior.
-   Customize ServiceNow skills by modifying the prompt, inputs, and providers.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Set up a security access control list to verify user authentication for Now Assist Skill Kit.
-   Use Document Intelligence as a tool when you create a skill.

-   Use UI Builder to deploy custom skills.
-   Use a custom data generator to create synthetic datasets.

See [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Now Assist Skill Kit is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Labelling](https://www.servicenow.com/docs/access?context=nadk-labelling&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)Use labeling workflows to annotate UI templates**

    Use the labeling framework to create and manage ground truth data. Published data collections can now be turned into labeling projects. Each record becomes a task assigned to labelers who annotate using pre-configured UI templates

-   **[s](https://www.servicenow.com/docs/access?context=configure-skill-prompt&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)Structured output support for AI responses**

    Enables consistent parsing in agentic workflows and reduces ambiguity in downstream automation.

-   **[Use multi-table data generator](https://www.servicenow.com/docs/access?context=use-multi-table-data-generator&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)New multi-table synthetic data generation option**

    You can generate related records across multiple tables in a single operation. You no longer need to generate each table separately and manually link records. Define your table relationships, set the cardinality and Now Assist Data Kit generates coherent, referentially linked records across all tables in one pass, with foreign key integrity maintained automatically. 

-   **[Create a model](https://www.servicenow.com/docs/access?context=create-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)AI Control Tower integration with custom LLMs.**

    Improve oversight and compliance for AI deployments with formal approval flows for custom models.

-   **[Now Assist Skill Kit roles](https://www.servicenow.com/docs/access?context=na-skill-kit-roles&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)Update to the abilities of the admin role**

    The sn\_skill\_builder.admin role is now broken into smaller, task-specific roles, including a custom LLM-specific admin role.


-   **[Create a model](https://www.servicenow.com/docs/access?context=create-model&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    When you bring your own model you can keep data in your own environment and fine-tune it to meet your specific needs.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[New skill deployment option](https://www.servicenow.com/docs/access?context=configure-skill-settings&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://www.servicenow.com/docs/access?context=na-data-kit-generate-data&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    When you create synthetic data, you can select what language you want to receive the data in.

-   **AI-assisted ground truth**

    Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://www.servicenow.com/docs/access?context=add-dataset&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Import data from a CSV file to create a dataset.

-   **[Create a custom data generator](https://www.servicenow.com/docs/access?context=create-custom-data-generator&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Create and use a custom data generator to create synthetic data.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Now Assist features are available with activation of any Now Assist plugins from ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=zurich&pubname=zurich-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability Management](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=zurich&pubname=zurich-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=zurich&pubname=zurich-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)
-   [Now Assist for Operational Technology Service Management \(OTSM\)](https://www.servicenow.com/docs/access?context=now-assist-for-operational-technology-service-management&version=zurich&pubname=zurich-operational-technology&ft:locale=en-US)
-   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US)
-   [Now Assist for Public Sector Digital Services \(PSDS\)](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=zurich&pubname=zurich-government-industry&ft:locale=en-US)
-   [Now Assist for Sales Force Automation \(SFA\)](https://www.servicenow.com/docs/access?context=now-assist-for-sales-and-order-management-som&version=zurich&pubname=zurich-order-management&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=zurich&pubname=zurich-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)
-   [Now Assist for Zero Copy Connector](https://www.servicenow.com/docs/access?context=now-assist-for-zero-copy-connector-for-erp&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US)

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Localization information

Now Assist supports Dynamic Translation for Zurich.

## Related ServiceNow applications and features

-   **[AI Search](https://www.servicenow.com/docs/access?context=overview-ais&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The ServiceNow® AI Search application provides a consumer-grade search engine for Service Portal, Now Mobile, and Virtual Agent. Intelligent query features help you quickly find the answers that you need.

-   **[Document Intelligence](https://www.servicenow.com/docs/access?context=document-intelligence-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow®Document Intelligence \(DocIntel\) application is an artificial intelligence \(AI\) solution that enables any organization to automate and accelerate the process of extracting data from documents. That data can easily be integrated into larger automation workflows to save time and resources.

-   **[Dynamic Translation](https://www.servicenow.com/docs/access?context=dynamic-translation-overview&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    The ServiceNow® Dynamic Translation application enables you to dynamically translate text entered in an application or in a chat window for a seamless localization experience.

-   **[Generative AI Controller](https://www.servicenow.com/docs/access?context=generative-ai-controller&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The ServiceNow® Generative AI Controller lets you integrate third-party large language models \(LLMs\) with your workflows.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)**

    The ServiceNow® Knowledge Management application enables the sharing of information in the Knowledge Base. The Knowledge Base contains articles that provide users with information such as self-help, troubleshooting, and task resolution.

-   **[Now Assist in Virtual Agent](https://www.servicenow.com/docs/access?context=now-assist-in-va-landing&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)**

    Use generative AI skills in your conversational experiences. Now Assist in Virtual Agent uses large language models \(LLMs\) to create a natural-language conversational experience that can improve the success of your self-service workflows.


**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

