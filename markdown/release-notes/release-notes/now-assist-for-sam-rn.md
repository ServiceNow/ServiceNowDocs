---
title: Now Assist for Software Asset Management \(SAM\) release notes
description: The ServiceNow Now Assist for Software Asset Management \(SAM\) application brings generative AI to IT Asset Management. Now Assist for SAM is a new application in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-02-18"
reading_time_minutes: 6
---

# Now Assist for Software Asset Management \(SAM\) release notes

The ServiceNow® Now Assist for Software Asset Management \(SAM\) application brings generative AI to IT Asset Management. Now Assist for SAM is a new application in the Yokohama release.

## Now Assist for Software Asset Management \(SAM\) highlights for the Yokohama release

Yokohama Patch 13

-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.
-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.
-   Automate user resolution with AI for SaaS license management to support efficiency and accuracy in subscription management.

Yokohama Patch 6

-   Automate and streamline the software asset request process by using an agentic workflow.
-   Automate the process of creating reclamation rules by identifying software products suitable for reclamation using an agentic workflow.
-   Automate evaluation of unused and underutilized software installations for potential reclamation by using an agentic workflow.

Yokohama Patch 3

-   Obtain crucial information on products to mitigate license compliance risks through product summaries on software deployment, license compliance, configuration health, and optimization.
-   Manage product license compliance via recommendations that guide you to take steps to ensure the necessary compliance requirements.

Yokohama Early Availability: Leverage generative AI by using the Now Assist for SAM application to create publisher summaries on software deployment, license compliance, configuration health, and optimization.

See [Now Assist for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-sam.md) for more information.

**Important:** Now Assist for SAM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/troubleshooting-saas-now-assist-sam.md)**

    Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.

-   **[Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/extract-entitlements-from-contracts-now-assist-sam.md)**

    Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.


-   **[Automate the creation of user resolution rules to accelerate reconciliation and ensure consistent user mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/automate-userresolution-saas-now-assist-sam.md)**

    Use generative AI to resolve user subscriptions by creating user resolution rules without manual intervention. AI automatically creates the user resolution rules, and these rules analyze and map incoming subscription data to corresponding user records in the Software Asset Management application.


-   **[New third-party AI model provider options available for all Now Assist applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/exploring-large-language-models.md)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Use an agentic workflow to automate software asset sourcing to improve operational efficiency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/using-now-assist-sam-ai-agents-usecases.md)**

    Use AI agents in the Help manage software request agentic workflow to automate sourcing of software assets either through automatic license allocation or by creating purchase orders.

-   **[Use an agentic workflow to create reclamation rules for enhancing software license utilization tracking and reducing waste](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-sam-create-software-reclamation-rule-workflow.md)**

    Use AI agents to automatically create reclamation rules for installed or subscription-based software, reducing the need for manual analysis of product usage and expenditure. The AI agent analyzes factors such as spend and utilization to suggest reclamation rules.

-   **[Use an agentic workflow to reclaim unused software to minimize compliance risk and optimize savings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-sam-evaluate-removal-candidate-workflow.md)**

    Use AI agents to automate reclamation of removal candidate for an installed or subscription-based software. The AI agent evaluates software removal candidates and provides suggestions for reclamation, based on intelligent checks that help ensure safe removal.


-   **[Gain insights into product compliance and optimization with AI-powered product summaries](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/summarize-product-compliance-now-assist-sam.md)**

    Get comprehensive product summaries to better understand your product compliance position across software deployment, license compliance, optimization, and configuration health. The AI-based product summaries simplify the complexity of license management and ensure adherence to publisher contracts.

-   **[Use AI-powered recommended actions to mitigate your license compliance risk](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/recommended-actions-now-assist-sam.md)**

    Use recommended actions to guide you through the appropriate steps to achieve compliance. Take actionable steps to address any configuration, maintenance, or optimization issues and gain faster compliance.


-   **[Gain insights into your publisher license compliance by using Now Assist for SAM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/summarize-publisher-compliance-now-assist-sam.md)**

    Use generative AI to gain a comprehensive summary of publisher license compliance. The detailed publisher summaries that cover software deployment, license compliance, optimization, and configuration health enable you to understand the publisher license compliance details.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install Now Assist for SAM by requesting it from the ServiceNow Store.

**Note:** To take full advantage of the Now Assist for SAM features, you need to install the Now Assist for SAM store application as well as upgrade to Yokohama Patch 3.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Now Assist for SAM application requires the Software Asset Management Pro plus or the Enterprise plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/ai-agent-studio.md)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use this conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-asset-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

