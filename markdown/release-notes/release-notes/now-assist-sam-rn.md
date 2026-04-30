---
title: Now Assist for Software Asset Management \(SAM\) release notes
description: The ServiceNow Now Assist for Software Asset Management \(SAM\) application brings generative AI to IT Asset Management. Now Assist for SAM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-05"
reading_time_minutes: 7
---

# Now Assist for Software Asset Management \(SAM\) release notes

The ServiceNow® Now Assist for Software Asset Management \(SAM\) application brings generative AI to IT Asset Management. Now Assist for SAM was enhanced and updated in the Zurich release.

## Now Assist for SAM highlights for the Zurich release

[Zurich Patch 8](../quality/zurich-patch-8.md)

-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.
-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Automate the process of assigning available licenses to the Microsoft 365 Admin Portal by using an agentic workflow.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills, agents, and agentic workflows are now turned on by default.
-   Automate user resolution with AI for SaaS license management to support efficiency and accuracy in subscription management.

[Zurich Patch 1](../quality/zurich-patch-1.md)

-   Automate and streamline the software asset request process by using an agentic workflow.
-   Automate the process of creating reclamation rules by identifying software products suitable for reclamation using an agentic workflow.
-   Automate the evaluation of unused and underused software installations for potential reclamation by using an agentic workflow.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

See [Now Assist for Software Asset Management \(SAM\)](https://www.servicenow.com/docs/access?context=now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

**Important:** Now Assist for SAM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements](https://www.servicenow.com/docs/access?context=extract-entitlements-from-contracts-now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.

-   **[Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.


-   **[Use an agentic workflow to automate Microsoft 365 license assignment to users to improve efficiency](https://www.servicenow.com/docs/access?context=now-assist-sam-fulfill-sw-asset-requests-workflow&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use AI agents to assign Microsoft 365 licenses automatically to users on the Microsoft 365 Admin Center without manual intervention. The AI agent analyzes whether there are available licenses and automatically assigns those licenses to the Microsoft 365 Admin Center, ensuring accuracy and compliance.


-   **[Automate the creation of user resolution rules to accelerate reconciliation and ensure consistent user mappings](https://www.servicenow.com/docs/access?context=automate-userresolution-saas-now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use generative AI to resolve user subscriptions by creating user resolution rules without manual intervention. AI automatically creates the user resolution rules, and these rules analyze and map incoming subscription data to corresponding user records in the Software Asset Management application.


[Zurich Patch 1](../quality/zurich-patch-1.md)

-   **[Use an agentic workflow to automate software asset sourcing to improve operational efficiency](https://www.servicenow.com/docs/access?context=using-now-assist-sam-ai-agents-usecases&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use AI agents in the Help manage software request agentic workflow to automate software asset sourcing, either through automatic license allocation or by creating purchase orders.


-   **[Use an agentic workflow to create reclamation rules for enhancing software license utilization tracking and reducing waste](https://www.servicenow.com/docs/access?context=now-assist-sam-create-software-reclamation-rule-workflow&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use AI agents to create reclamation rules automatically for installed or subscription-based software, reducing manual analysis of product use and cost. The AI agent analyzes factors such as spend and utilization to suggest reclamation rules.


-   **[Use an agentic workflow to reclaim unused software to minimize compliance risk and optimize savings](https://www.servicenow.com/docs/access?context=now-assist-sam-evaluate-removal-candidate-workflow&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use AI agents to automate the reclamation process for installed or subscription-based software. The AI agent evaluates software removal candidates and provides suggestions for reclamation based on intelligent checks that help ensure safe removal.

-   **[Configure ACLs for AI agents and agentic workflows](https://www.servicenow.com/docs/access?context=aia-security-implementation&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## UI changes

-   **[Troubleshoot button alongside the error message on the Integration profile form](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Troubleshoot** button is available for all SaaS integrations on the error message that is displayed when connection validation fails due to an error. When selected, the button triggers the generation of error summary and resolution guidance.


-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills, agents, and agentic workflows are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://www.servicenow.com/docs/access?context=aia-role-masking&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Agentic workflows and AI agents included with Now Assist applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they won't execute. Data access settings must also include these roles. See the documentation for the agentic workflow or AI agent for the specific roles you must add. After the roles are configured, users must have the specified role to invoke the agentic workflow or AI agent.


## Activation information

Install Now Assist for SAM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Now Assist Admin console](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio](https://www.servicenow.com/docs/access?context=ai-agent-studio&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist panel conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

