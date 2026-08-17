---
title: ServiceNow Otto for Software Asset Management \(SAM\) release notes
description: The ServiceNow ServiceNow Otto for Software Asset Management \(SAM\) application brings generative AI to IT Asset Management. ServiceNow Otto for SAM was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-05"
reading_time_minutes: 8
---

# ServiceNow Otto for Software Asset Management \(SAM\) release notes

The ServiceNow® ServiceNow Otto for Software Asset Management \(SAM\) application brings generative AI to IT Asset Management. ServiceNow Otto for SAM was enhanced and updated in the Zurich release.

## ServiceNow Otto for SAM highlights for the Zurich release

[Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)- ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Software Asset Management \(SAM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

[Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)

-   Streamline the entitlement import process by resolving import errors using AI skills, for a faster import process and improved data accuracy.

[Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)

-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.
-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.

[Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)

-   Automate the process of assigning available licenses to the Microsoft 365 Admin Portal by using an agentic workflow.

[Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)

-   Review changes to usage measurement.

[Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)

-   Some AI skills, AI agents, and agentic workflows are now turned on by default.
-   Automate user resolution with AI for SaaS license management to support efficiency and accuracy in subscription management.

[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   Automate and streamline the software asset request process by using an agentic workflow.
-   Automate the process of creating reclamation rules by identifying software products suitable for reclamation using an agentic workflow.
-   Automate the evaluation of unused and underused software installations for potential reclamation by using an agentic workflow.
-   Additional role configuration required for agentic workflows and AI agents included with your applications.

See [ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam.md) for more information.

**Important:** Now Assist for SAM is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Streamline entitlement import by resolving import errors with AI-suggested corrections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/resolve-entitlement-import-error.md)**

    Reduce manual effort and improve data accuracy when reviewing entitlement import errors in the Software Asset Workspace by using AI skills. When publisher or product names in the standard entitlement import template don't match standard content, the Software normalization and Product match reviewer skills provide AI-suggested corrections for review. The feature also identifies potential duplicate entitlements, enabling you to review and dismiss them where appropriate.


-   **[Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/extract-entitlements-from-contracts-now-assist-sam.md)**

    Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.

-   **[Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/troubleshooting-saas-now-assist-sam.md)**

    Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.


-   **[Use an agentic workflow to automate Microsoft 365 license assignment to users to improve efficiency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam-fulfill-sw-asset-requests-workflow.md)**

    Use AI agents to assign Microsoft 365 licenses automatically to users on the Microsoft 365 Admin Center without manual intervention. The AI agent analyzes whether there are available licenses and automatically assigns those licenses to the Microsoft 365 Admin Center, ensuring accuracy and compliance.


-   **[Automate the creation of user resolution rules to accelerate reconciliation and ensure consistent user mappings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/automate-userresolution-saas-now-assist-sam.md)**

    Use generative AI to resolve user subscriptions by creating user resolution rules without manual intervention. AI automatically creates the user resolution rules, and these rules analyze and map incoming subscription data to corresponding user records in the Software Asset Management application.


[Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)

-   **[Use an agentic workflow to automate software asset sourcing to improve operational efficiency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/using-now-assist-sam-ai-agents-usecases.md)**

    Use AI agents in the Help manage software request agentic workflow to automate software asset sourcing, either through automatic license allocation or by creating purchase orders.


-   **[Use an agentic workflow to create reclamation rules for enhancing software license utilization tracking and reducing waste](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam-create-software-reclamation-rule-workflow.md)**

    Use AI agents to create reclamation rules automatically for installed or subscription-based software, reducing manual analysis of product use and cost. The AI agent analyzes factors such as spend and utilization to suggest reclamation rules.


-   **[Use an agentic workflow to reclaim unused software to minimize compliance risk and optimize savings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/now-assist-sam-evaluate-removal-candidate-workflow.md)**

    Use AI agents to automate the reclamation process for installed or subscription-based software. The AI agent evaluates software removal candidates and provides suggestions for reclamation based on intelligent checks that help ensure safe removal.

-   **[Configure ACLs for AI agents and agentic workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-security-implementation.md)**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## UI changes

-   **[Troubleshoot button alongside the error message on the Integration profile form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-asset-management/troubleshooting-saas-now-assist-sam.md)**

    The **Troubleshoot** button is available for alls SaaS integrations on the error message that is displayed when connection validation fails due to an error. When selected, the button triggers the generation of error summary and resolution guidance.


-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Now Assist &gt; ServiceNow Otto announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


-   **[Changes to Now Assist usage measurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**

    Starting with Australia Early Access, AI usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: AI Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some generative AI skills, AI agents, and agentic workflows are turned on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md)**

    The skills are automatically available to appropriate role users for the application, such as ITIL roles on incident forms or change forms. This change simply activates the skill and does not touch the roles that may be needed to use the skill. The new default behavior works as follows:

    -   New customers: When you install an AI product, designated skills and agentic workflows are turned on automatically.
    -   Existing customers who are upgrading \(starting with Australia Early Access\): Any previously unconfigured skill, agent, or agentic workflow is turned on automatically \(the AI asset was never configured and turned on, then turned off again\). Previously configured skills and agentic workflows that were turned on, then off, remain inactive.
-   **[Role configuration required for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/aia-role-masking.md)**

    Agentic workflows and AI agents included with your applications require additional security configuration. If you select **Users with selected roles** for your user access security controls for an agentic workflow or AI agent, you must add the installed roles, or they will not execute. See the documentation for the agentic workflow or AI agent for the specific roles you must add.


## Activation information

Install Now Assist for SAM by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[AI Admin Hub console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/configuring-now-assist.md)**

    Use the AI Admin Hub console for quick and effortless access to the important information that you need to set up, configure, and monitor Now Assist applications and features.

-   **[AI Agent Studio overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/ai-agent-studio.md)**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **[ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-panel-overview.md)**

    Use the Now Assist panel conversational interface in ServiceNow® Software Asset Workspace to interact with and get assistance from generative AI.

-   **[Now Assist skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills.md)**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/it-asset-management-rn-landing.md)

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)

