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

[Yokohama Patch 11](../quality/yokohama-patch-11.md)

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

See [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US) for more information.

**Important:** Now Assist for SAM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Automate the creation of user resolution rules to accelerate reconciliation and ensure consistent user mappings](https://www.servicenow.com/docs/access?context=automate-userresolution-saas-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use generative AI to resolve user subscriptions by creating user resolution rules without manual intervention. AI automatically creates the user resolution rules, and these rules analyze and map incoming subscription data to corresponding user records in the Software Asset Management application.


-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.

-   **[Use an agentic workflow to automate software asset sourcing to improve operational efficiency](https://www.servicenow.com/docs/access?context=using-now-assist-sam-ai-agents-usecases&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use AI agents in the Help manage software request agentic workflow to automate sourcing of software assets either through automatic license allocation or by creating purchase orders.

-   **[Use an agentic workflow to create reclamation rules for enhancing software license utilization tracking and reducing waste](https://www.servicenow.com/docs/access?context=now-assist-sam-create-software-reclamation-rule-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use AI agents to automatically create reclamation rules for installed or subscription-based software, reducing the need for manual analysis of product usage and expenditure. The AI agent analyzes factors such as spend and utilization to suggest reclamation rules.

-   **[Use an agentic workflow to reclaim unused software to minimize compliance risk and optimize savings](https://www.servicenow.com/docs/access?context=now-assist-sam-evaluate-removal-candidate-workflow&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use AI agents to automate reclamation of removal candidate for an installed or subscription-based software. The AI agent evaluates software removal candidates and provides suggestions for reclamation, based on intelligent checks that help ensure safe removal.


-   **[Gain insights into product compliance and optimization with AI-powered product summaries](https://www.servicenow.com/docs/access?context=summarize-product-compliance-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Get comprehensive product summaries to better understand your product compliance position across software deployment, license compliance, optimization, and configuration health. The AI-based product summaries simplify the complexity of license management and ensure adherence to publisher contracts.

-   **[Use AI-powered recommended actions to mitigate your license compliance risk](https://www.servicenow.com/docs/access?context=recommended-actions-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use recommended actions to guide you through the appropriate steps to achieve compliance. Take actionable steps to address any configuration, maintenance, or optimization issues and gain faster compliance.


-   **[Gain insights into your publisher license compliance by using Now Assist for SAM](https://www.servicenow.com/docs/access?context=summarize-publisher-compliance-now-assist-sam&version=yokohama&pubname=yokohama-it-asset-management&ft:locale=en-US)**

    Use generative AI to gain a comprehensive summary of publisher license compliance. The detailed publisher summaries that cover software deployment, license compliance, optimization, and configuration health enable you to understand the publisher license compliance details.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install Now Assist for SAM by requesting it from the ServiceNow Store.

**Note:** To take full advantage of the Now Assist for SAM features, you need to install the Now Assist for SAM store application as well as upgrade to Yokohama Patch 3.

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Additional requirements

The Now Assist for SAM application requires the Software Asset Management Pro plus or the Enterprise plus license.

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

