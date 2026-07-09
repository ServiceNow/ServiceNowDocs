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

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

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

See [Now Assist Skill Kit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skill-kit-landing.md) for more information.

**Important:** Now Assist Skill Kit is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Now Assist Skill Kit to Yokohama

If you customized UI actions or other items that are associated with Now Assist skills, ensure that your customized code is updated with the new skill releases. Otherwise, certain functions may not work as expected.

If you run into issues when you're upgrading a Now Assist product, see [KB1637452: Issues and mitigation for Now Assist \(Generative AI\) Applications and Plugin updates](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1637452). You may need to log in to view the article.

## New in the Yokohama release

-   **[New skill deployment option](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configure-skill-settings.md)**

    Deploy skills using UI Builder.

-   **[Choose a language for data generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/na-data-kit-generate-data.md)**

    When you create synthetic data, you can select what language you want to receive the data in.

-   **[AI-assisted ground truth](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/add-ground-truth.md)**

    Use AI to assist creating ground truth for your data.

-   **[Import data with a CSV file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/add-dataset.md)**

    Import data from a CSV file to create a dataset.

-   **Create a custom data generator**

    Create and use a custom data generator to create synthetic data.


-   **[Customize ServiceNow skills in Now Assist Skill Kit to tailor skills to meet your specific business requirements.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/clone-and-edit-servicenow-skill.md)**

    Eligible skills provided in ServiceNow Now Assist applications can be cloned in Now Assist Skill Kit so that you can edit the prompt or change the AI service provider. Editing the prompt enables you to arrange the formatting and content of the large language model \(LLM\) response. After the skill is edited, activate the edited skill in the Now Assist Admin console to enable it.

-   **[Add and manage tools visually in the new Tools editor, including decision branching, to execute different tools for your skill.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/add-a-tool.md)**

    Adding decision branches between tools enables you to define the conditions that must be met for a tool to run. If no conditions are met, the default branch's step is executed.


## UI changes

-   **[Now Assist Skill Kit add tools function moved to Tool editor tab.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/add-a-tool.md)**

    The ability to add and edit tools for Now Assist Skill Kit previously appeared on the **Prompt editor** tab. It now appears on the **Tool editor** tab.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Now Assist features are available with activation of any Now Assist plugin from the ServiceNow Store. The following plugins are available:

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

The Next Experience UI Framework must be enabled to use the Now Assist panel.

## Browser requirements

Now Assist supports various browsers, including Google Chrome and Microsoft Edge. Now Assist isn’t supported in Microsoft Internet Explorer.

## Accessibility information

Admins can enable an optional Voice Input setting for the Now Assist panel that enables users to interact with the panel using their voice or in voice assist mode.

## Localization information

Now Assist supports Dynamic Translation for Yokohama.

**Parent Topic:**[AI Experiences release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/intelligent-experiences-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

