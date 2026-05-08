---
title: Software Asset Management release notes
description: The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications.The Software Asset Management application was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 8
---

# Software Asset Management release notes

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications.The Software Asset Management application was enhanced and updated in the Australia release.

## Software Asset Management highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.
-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.
-   Automate the process of assigning available licenses to the Microsoft 365 Admin Portal by using an agentic workflow.
-   Leverage Obligation Management and AI-powered contract metadata and obligation extraction from an uploaded signed contract document in the Software Asset Workspace by using the combined capabilities of Software Asset Management and Contract Management Pro.

Australia Patch 0

-   Streamline software lifecycle reporting and compliance management with a guided playbook.
-   Use a consolidated Microsoft licensing report that unifies device and infrastructure deployment details with license consumption calculations and transparent explanations.

See Software Asset Management for more information.

**Important:** Software Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   **ServiceNow product tiers**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements**

    Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.

-   **Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance**

    Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.

-   **Use an agentic workflow to automate Microsoft 365 license assignment to users to improve efficiency**

    Use AI agents to assign Microsoft 365 licenses automatically to users on the Microsoft 365 Admin Center without manual intervention. The AI agent analyzes whether there are available licenses and automatically assigns those licenses to the Microsoft 365 Admin Center, ensuring accuracy and compliance.

-   **Software Asset Management integration with Contract Management Pro**

    Gain centralized visibility into software contract life cycles and streamline contract management by extracting key metadata and obligations from an uploaded signed contract document using the agentic AI workflow. Additionally, you can optimize costs through proactive tracking of contract renewals, expirations, and contractual obligations by integrating Software Asset Management with the Contract Management Pro application. Note that only Software Asset Management Enterprise users can leverage this functionality.


-   **Improve user activity tracking with the GitHub integration**

    Achieve more accurate user activity data and improved license reclamation for low or no-activity subscriptions by leveraging the enhanced GitHub integration for broader event coverage and extended retention.

-   **Enhanced integration with OpenLM for tracking subscription and consumption licenses**

    Gain improved visibility into engineering application licenses across subscription-based and consumption models with the OpenLM integration. This capability provides support for named user allocation and usage tracking. Additionally, you can better monitor compliance risks and note denial patterns through actionable insights into automated processes and dashboards.

-   **Leverage machine learning \(ML\) normalization for managing your software assets in protected government environments**

    Extend ML normalization capabilities to regulated markets for ServiceNow Protected Platform \(SPP\) in Singapore \(SG\) and Australia \(AU\).

-   **Enhance the security of SAP ABAP on-premise integration using OAuth 2.0 authentication**

    Benefit from enhanced OAuth 2.0 authentication for your SAP ABAP on-premise integrations with improved security. This capability provides a more secure, compliant, and future-proof method for integrating the Software Asset Management application with your SAP systems.

-   **Improve your license management experience through the enhanced support for Oracle WebLogic Suite licensing**

    Access flexible licensing options that align with different deployment models and usage patterns through comprehensive license management with support for the Oracle WebLogic Suite for both Per Processor and Named User Plus \(NUP\) metrics. The enhanced support now covers the entire WebLogic product family, including the flagship Suite edition.

-   **Improve software normalization outcomes with expanded pattern-based normalization rules rule**

    Streamline the software model discovery process by leveraging the expanded pattern-based normalization rule, which eliminates the need to manually update or create new normalization rules for every minor variation in software discovery models. This rule automatically recognizes and matches diverse patterns and variations in software model data. As a result, discovered publisher, product, version, and edition values are seamlessly aligned with the ServiceNow® repository.

-   **Enhanced SQL server enterprise edition license compliance to support Server/CAL licensing model**

    Optimize licensing for legacy Microsoft SQL Server Enterprise Edition licenses under the Server+CAL licensing model with Software Assurance \(SA\) by using the enhanced licensing rule. A single server license can cover up to four virtual machines, provided that the combined processing power for these VMs does not exceed twenty hardware threads or cores at any given time.

-   **Generate optimal software lifecycle reports using a guided playbook that ensures adherence to compliance and audit requirements.**

    Simplify the creation of optimal software life-cycle reports through a guided playbook that assists in defining report scope, identifying gaps, and performing corrective actions. The playbook also integrates with the success portal, enabling you to establish and monitor success metrics, organize tasks and activities, and effectively track progress toward your objectives.

-   **Streamline license management for Microsoft server product Installations and license usage via a single report**

    Gain insights to a unified report for all Microsoft server product installations and license usage across license metrics. The Microsoft Server Infrastructure and License consumption report consolidates infrastructure data per device along with license usage and exemptions. Get detailed justifications for exemptions such as unlicensed or ignored installations, making it easier to monitor, analyze, and optimize your IT resources.


## UI changes

-   **Troubleshoot button alongside the error message on the Integration profile form**

    The **Troubleshoot** button is available for all SaaS integrations on the error message that is displayed when connection validation fails due to an error. When selected, the button triggers the generation of error summary and resolution guidance.


-   **Delete button on the Product Workload Mapping form**

    A **Delete** button is available on the Product Workload Mapping form for CrowdStrike integration profiles to enable you to delete existing workload-to-software model mappings directly from the integration profile.

-   **Product workload mappings and breakdown data lists on the License operations view**

    View the product workload mappings, usage, and consumption lists on the License operations view without requiring additional configuration.

-   **Engineering application licenses, usages, and denials lists on the License operations view**

    View engineering application lists including licenses, usages, concurrent usage, denials, and unidentified publisher integration map on the License operations view for quick access.


## Changed in this release

-   **Granular configuration admin roles**

    Use granular admin roles, such as sam\_admin and sam\_integrator, to complete administrative configuration tasks without requiring the full admin role. By using limited admin privileges that provide access to only certain tasks, you can help reduce security risks across your organization.


## Activation information

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugin, including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace store app \(sn\_sam\_workspace\).

**Note:** After the new plugin is activated, you can't access the classic user interface.

The ServiceNow AI Platform® in the Australia release has limited support for the Software Asset Management classic user interface. However, it remains active in your instance, including when you upgrade to a newer ServiceNow AI Platform® release.

Install the listed Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/store) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences
-   Software Asset Workspace

## Related ServiceNow applications and features

-   **AI Agent Studio**

    Use AI Agent Studio to create, manage, or test AI agents and agentic workflows so that you can create self-executing workflows to help you achieve your business goals.

-   **Now Assist skills**

    Use the ServiceNow® Now Assist products to provide generative AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **Hardware Asset Management**

    The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment.

-   **Enterprise Asset Management**

    The ServiceNow® Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtime.

-   **Cloud Cost Management**

    The ServiceNow® Cloud Cost Management application enables you to analyze all costs that are associated with your cloud assets. You can use this information to optimize operations and reduce your cloud spend.

-   **Contract Management**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **Procurement**

    The ServiceNow® Procurement application helps you create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

