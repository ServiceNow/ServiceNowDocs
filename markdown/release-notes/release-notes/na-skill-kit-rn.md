---
title: Now Assist Skill Kit release notes
description: The ServiceNow Now Assist Skill Kit application enables AI developers to create custom skills and to have greater flexibility with Now Assist's generative AI capabilities. Now Assist Skill Kit was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Now Assist Skill Kit release notes

The ServiceNow® Now Assist Skill Kit application enables AI developers to create custom skills and to have greater flexibility with Now Assist's generative AI capabilities. Now Assist Skill Kit was enhanced and updated in the Yokohama release.

## Now Assist Skill Kit highlights for the Yokohama release

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Yokohama Patch 6

-   Use UI Builder to deploy custom skills.
-   Import data into Now Assist Skill Kit with a CSV file.
-   Use AI to create ground truth for your data.
-   Use a custom data generator to create synthetic datasets.

-   Users can create synthetic data in Now Assist Data Kit.
-   Generated synthetic data can be saved as a dataset.
-   Add and manage tools of a custom skill, visually in the new Tools editor, including conditional execution of tools.
-   Customize ServiceNow skills with new prompts or providers in Now Assist Skill Kit to suit your specific business needs.

See [Now Assist Skill Kit](https://www.servicenow.com/docs/access?context=now-assist-skill-kit-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US) for more information.

**Important:** Now Assist Skill Kit is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist Skill Kit to Yokohama

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

## New in the Yokohama release

-   **[New skill deployment option](https://www.servicenow.com/docs/access?context=configure-skill-settings&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://www.servicenow.com/docs/access?context=na-data-kit-generate-data&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    When you create synthetic data, you can select what language you want to receive the data in.

-   **[AI-assisted ground truth](https://www.servicenow.com/docs/access?context=add-ground-truth&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://www.servicenow.com/docs/access?context=add-dataset&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Import data from a CSV file to create a dataset.

-   **[Create a custom data generator](https://www.servicenow.com/docs/access?context=create-custom-data-generator&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Create and use a custom data generator to create synthetic data.


-   **[Customize ServiceNow skills in Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://www.servicenow.com/docs/access?context=clone-and-edit-servicenow-skill&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the large language model \(LLM\) response. After the skill is edited, activate the edited skill in the Now Assist Admin console to enable it.

-   **[Add and manage tools visually in the new Tools editor, including decision branching, to execute different tools for your skill.](https://www.servicenow.com/docs/access?context=add-a-tool&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Adding decision branches between tools enables you to define the conditions that must be met for a tool to run. If no conditions are met, the default branch's step is executed.


## UI changes

-   **[Now Assist Skill Kit add tools function moved to Tool editor tab.](https://www.servicenow.com/docs/access?context=add-a-tool&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The ability to add and edit tools for Now Assist Skill Kit previously appeared on the **Prompt editor** tab. It now appears on the **Tool editor** tab.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

-   [Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for App Engine](https://www.servicenow.com/docs/access?context=add-ai-to-custom-apps-with-now-assist-for-app-engine-enterprise&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)
-   [Now Assist for Configuration Management Database \(CMDB\)](https://www.servicenow.com/docs/access?context=now-assist-landing-cmdb&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Now Assist for Collaborative Work Management \(CWM\)](https://www.servicenow.com/docs/access?context=now-assist-for-cwm-landing&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Creator](https://www.servicenow.com/docs/access?context=now-assist-for-creator-landing&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)
-   [Now Assist for Customer Service Management \(CSM\)](https://www.servicenow.com/docs/access?context=now-assist-csm&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)
-   [Now Assist for Employee Experience](https://www.servicenow.com/docs/access?context=now-assisit-employee-exp&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)
-   [Now Assist for Operational Sustainability \(formerly ESG\)](https://www.servicenow.com/docs/access?context=now-assist-for-esg&version=yokohama&pubname=yokohama-environmental-social-governance&ft:locale=en-US)
-   [Now Assist for Field Service Management \(FSM\)](https://www.servicenow.com/docs/access?context=now-assist-fsm&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)
-   [Now Assist for Financial Services Operations \(FSO\)](https://www.servicenow.com/docs/access?context=now-assist-for-financial-services-operations&version=yokohama&pubname=yokohama-financial-services-operations&ft:locale=en-US)
-   [Now Assist for Hardware Asset Management \(HAM\)](https://www.servicenow.com/docs/access?context=now-assist-ham&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Health and Safety](https://www.servicenow.com/docs/access?context=now-assist-hs-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for HR Service Delivery \(HRSD\)](https://www.servicenow.com/docs/access?context=now-assist-hrsd&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Integrated Risk Management \(IRM\)](https://www.servicenow.com/docs/access?context=now-assist-for-irm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for IT Operations Management \(ITOM\)](https://www.servicenow.com/docs/access?context=now-assist-itom&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)
-   [Now Assist for IT Service Management \(ITSM\)](https://www.servicenow.com/docs/access?context=now-assist-itsm&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)
-   [Now Assist for Legal Service Delivery \(LSD\)](https://www.servicenow.com/docs/access?context=now-assist-lsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Operational Technology Manager \(OTM\)](https://www.servicenow.com/docs/access?context=now-assist-for-otm-landing&version=yokohama&pubname=yokohama-operational-technology&ft:locale=en-US)
-   [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)
-   [Now Assist for PSDS](https://www.servicenow.com/docs/access?context=now-assist-for-psds&version=yokohama&pubname=yokohama-government-industry&ft:locale=en-US)
-   [Now Assist for Security Incident Response](https://www.servicenow.com/docs/access?context=now-assist-security-incident-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)
-   [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)
-   [Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=yokohama&pubname=yokohama-source-to-pay-operations&ft:locale=en-US)
-   [Now Assist for Strategic Portfolio Management \(SPM\)](https://www.servicenow.com/docs/access?context=now-assist-spm&version=yokohama&pubname=yokohama-it-business-management&ft:locale=en-US)
-   [Now Assist for Telecommunications, Media and Technology \(TMT\)](https://www.servicenow.com/docs/access?context=now-assist-spmc&version=yokohama&pubname=yokohama-telecom-media-technology&ft:locale=en-US)
-   [Now Assist for Third-party Risk Management \(TPRM\)](https://www.servicenow.com/docs/access?context=now-assist-tprm&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US)
-   [Now Assist for Workplace Service Delivery \(WSD\)](https://www.servicenow.com/docs/access?context=now-assist-wsd-landing&version=yokohama&pubname=yokohama-employee-service-management&ft:locale=en-US)
-   [Now Assist for Vulnerability Response](https://www.servicenow.com/docs/access?context=now-assist-for-vulnerability-response-landing&version=yokohama&pubname=yokohama-security-management&ft:locale=en-US)

## Additional requirements

The Next Experience UI Framework must be enabled to use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Accessibility information

Admins can enable an optional Voice Input setting for the Now Assist panel that enables users to interact with the panel using their voice or in voice assist mode.

## Localization information

Now Assist supports Dynamic Translation for Yokohama.

**Parent Topic:**[AI Experiences release notes](intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

