---
title: Software Asset Management release notes
description: The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.The September 2026 introduces AI-powered spend detection, enhanced publisher integrations for Smartsheet, and Microsoft Entra ID, and additional predefined license metrics.The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 13
---

# Software Asset Management release notes

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

## About Software Asset Management

[Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Software Asset Management \(SAM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Manage your IBM software estate on Nutanix AHV \(Acropolis Hypervisor\), including products deployed under sub-capacity licensing. Gain visibility into PVU, VPC, and RVU MAPC \(Managed Activated Processor Cores\) consumption to support compliance and cost optimization.

[Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)

-   Streamline the entitlement import process by resolving import errors using AI skills, for a faster import process and improved data accuracy.

[Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)

-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.
-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.
-   Automate the process of assigning available licenses to the Microsoft 365 Admin Portal by using an agentic workflow.
-   Leverage Obligation Management and AI-powered contract metadata and obligation extraction from an uploaded signed contract document in the Software Asset Workspace by using the combined capabilities of Software Asset Management and Contract Management Pro.

Australia Patch 0

-   Streamline software lifecycle reporting and compliance management with a guided playbook.
-   Use a consolidated Microsoft licensing report that unifies device and infrastructure deployment details with license consumption calculations and transparent explanations.

See [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SoftwareAssetMgmt.md) for more information.

## Activation and other requirements

**Important:** Software Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Software Asset Management is available with activation of the following plugins:

    -   **Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\)**

        Activating this plugin automatically activates the following:

        -   Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\)
        -   Software Asset Workspace store application \(sn\_sam\_workspace\)
        After you activate the Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\), you can't access the Software Asset Management Core UI.

    -   **Software Asset Management Foundation plugin \(com.snc.sams\)**

        To access the foundation capabilities of Software Asset Management, activate this plugin. After you activate the Software Asset Management Foundation plugin, activate the Software Asset Workspace store application \(sn\_sam\_workspace\) to complete the setup.

    The ServiceNow AI Platform® in the Australia release has limited support for the Software Asset Management classic user interface. However, it remains active in your instance, including when you upgrade to a newer ServiceNow AI Platform® release.

    Install the listed Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/store) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

    -   Software Asset Management - SaaS License Management
    -   Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)
    -   IBM License Compliance for Software Asset Management
    -   ITAM Health Check
    -   Software Asset Management Guided Experiences
    -   Software Asset Workspace

**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/it-asset-management-rn-landing.md)

## September 2026

The September 2026 introduces AI-powered spend detection, enhanced publisher integrations for Smartsheet, and Microsoft Entra ID, and additional predefined license metrics.

### What's new

-   **[Improved license compliance reporting for Smartsheet SaaS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/integrate-with-smartsheet.md)**

    Improve visibility and compliance reporting of Smartsheet user licenses using the assigned seat type in the Smartsheet portal. The integration now retrieves users by seat type and creates subscription records for each category independently.

    **Note:** The updated Smartsheet license reporting is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 17.6.0.

-   **[Use expanded Microsoft Entra ID Single Sign-On \(SSO\) license reclamation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-sso-integration.md)**

    Expand your Microsoft Entra ID SSO integrations to improve identification of inactive users and surface group-assigned users as reclamation candidates. Update SSO subscription reclamation logic to improve stale subscription detection.

    **Note:** The expanded Microsoft Entra ID capability is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 17.6.0.

-   **[Onboard entitlements faster with additional predefined license metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SAMLicenseMetrics.md)**

    Reduce entitlement onboarding time by using additional predefined license metrics for supported publishers. These predefined license metrics help you track consumption, verify compliance, and reconcile deployments against entitlements. Review tier ranges and calculation factors on the new **License Metric Tier** tab of the Software entitlement page.

-   **Analyze software spend transactions with AI in the Software Asset Workspace**

    Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.


### What's changed

-   **[Manage software models with clearer licensing terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-model-fields.md)**

    Understand licensing scope at a glance from the renamed column in the Software Model \[cmdb\_software\_product\_model\] table. The **License all installs accessed by clients** column is renamed to **License all installs**. The new name reflects that all installs meeting the software model's conditions are licensed, not only those tied to client access records.

-   **Software Spend Detection Core UI**

    The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.


## August 2026

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

### What's new

-   **[Manage IBM sub-capacity licensing on Nutanix AHV \(Acropolis Hypervisor\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/ibm-licensing-vmware-vsphere-environment.md)**

    Gain visibility into IBM products deployed on Nutanix AHV virtualized environments, with consumption data for sub-capacity eligible metrics such as PVU, VPC, and RVU MAPC \(Managed Activated Processor Cores\). Licensing calculations align with IBM sub-capacity requirements, including 30-minute capacity scans that capture peak processor core capacity to help keep license positions audit-ready.

    **Note:** IBM sub-capacity licensing on Nutanix AHV is available with IBM License Compliance for Software Asset Management 7.0.0 and later versions.

-   **[Gain visibility into the software asset life cycle with improved CMDB data quality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cmdb-sa-sam-use.md)**

    Audit your Software Asset Management CMDB for data quality gaps including missing edition/version details, cloud license inconsistencies, duplicate installs, and misaligned virtual-to-host relationships. Use the CMDB success advisor for Software Asset Management to systematically validate CI attributes, remediate duplicates, and establish consistent server mapping rules across your estate.


### What's changed

-   **[Now Assist &gt; ServiceNow Otto announcement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/platform-now-assist-landing.md)**

    Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


## July 2026

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

### What's changed

-   **[Large language models on the ServiceNow AI Platform®](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/exploring-large-language-models.md)**

    The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


## June 2026

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

### What's new

-   **[Streamline entitlement import by resolving import errors with AI-suggested corrections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/resolve-entitlement-import-error.md)**

    Reduce manual effort and improve data accuracy when reviewing entitlement import errors in the Software Asset Workspace by using AI skills. When publisher or product names in the standard entitlement import template don't match standard content, the Software normalization and Product match reviewer skills provide AI-suggested corrections for review. The feature also identifies potential duplicate entitlements, enabling you to review and dismiss them where appropriate.

-   **[Enhance SaaS application usage monitoring by integrating with the Agent Client Collector for Visibility Content \(ACC-VC\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/shadow-saas-analytics.md)**

    Monitor SaaS application usage across your organization by using URL monitoring data through the integration of your Software Asset Management application with ACC-VC. The SaaS Detection Report aggregates this usage data and distinguishes managed applications from the unmanaged ones. This enhancement provides actionable visibility to ServiceNow Otto for SAM managers into actual SaaS usage for software spend optimization.

    **Note:** The ACC-VC integration with the Software Asset Management application is available with Software Asset Management - SaaS License Management 17.4.0 and later versions.


## Australia General Availability

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

### What's new

-   **[Enhanced integration with OpenLM for tracking subscription and consumption licenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/concurrent-licenses.md)**

    Gain improved visibility into engineering application licenses across subscription-based and consumption models with the OpenLM integration. This capability provides support for named user allocation and usage tracking. Additionally, you can better monitor compliance risks and note denial patterns through actionable insights into automated processes and dashboards.

-   **[Leverage machine learning \(ML\) normalization for managing your software assets in protected government environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/ml-learning-sam.md)**

    Extend ML normalization capabilities to regulated markets for ServiceNow Protected Platform \(SPP\) in Singapore \(SG\) and Australia \(AU\).

-   **[Enhance the security of SAP ABAP on-premise integration using OAuth 2.0 authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/add-sap-connection.md)**

    Benefit from enhanced OAuth 2.0 authentication for your SAP ABAP on-premise integrations with improved security. This capability provides a more secure, compliant, and future-proof method for integrating the Software Asset Management application with your SAP systems.

-   **[Improve your license management experience through the enhanced support for Oracle WebLogic Suite licensing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/oracle-licensing-cloud-environments.md)**

    Access flexible licensing options that align with different deployment models and usage patterns through comprehensive license management with support for the Oracle WebLogic Suite for both Per Processor and Named User Plus \(NUP\) metrics. The enhanced support now covers the entire WebLogic product family, including the flagship Suite edition.

-   **[Improve software normalization outcomes with expanded pattern-based normalization rules rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/c_SAMDiscovery.md)**

    Streamline the software model discovery process by leveraging the expanded pattern-based normalization rule, which eliminates the need to manually update or create new normalization rules for every minor variation in software discovery models. This rule automatically recognizes and matches diverse patterns and variations in software model data. As a result, discovered publisher, product, version, and edition values are seamlessly aligned with the ServiceNow® repository.

-   **[Enhanced SQL server enterprise edition license compliance to support Server/CAL licensing model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/mapping-ms-license-metrics.md)**

    Optimize licensing for legacy Microsoft SQL Server Enterprise Edition licenses under the Server+CAL licensing model with Software Assurance \(SA\) by using the enhanced licensing rule. A single server license can cover up to four virtual machines, provided that the combined processing power for these VMs does not exceed twenty hardware threads or cores at any given time.

-   **[Generate optimal software lifecycle reports using a guided playbook that ensures adherence to compliance and audit requirements.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/guidedplaybook-sw-lifecycle-reports.md)**

    Simplify the creation of optimal software life-cycle reports through a guided playbook that assists in defining report scope, identifying gaps, and performing corrective actions. The playbook also integrates with the success portal, enabling you to establish and monitor success metrics, organize tasks and activities, and effectively track progress toward your objectives.

-   **[Streamline license management for Microsoft server product Installations and license usage via a single report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/device-license-consumption-report.md)**

    Gain insights to a unified report for all Microsoft server product installations and license usage across license metrics. The Microsoft Server Infrastructure and License consumption report consolidates infrastructure data per device along with license usage and exemptions. Get detailed justifications for exemptions such as unlicensed or ignored installations, making it easier to monitor, analyze, and optimize your IT resources.


### What's changed

-   **[Delete button on the Product Workload Mapping form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/integrate-with-crowdstrike.md)**

    A **Delete** button is available on the Product Workload Mapping form for CrowdStrike integration profiles to enable you to delete existing workload-to-software model mappings directly from the integration profile.

-   **[Product workload mappings and breakdown data lists on the License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/operations-workspace.md)**

    View the product workload mappings, usage, and consumption lists on the License operations view without requiring additional configuration.

-   **[Engineering application licenses, usages, and denials lists on the License operations view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/operations-workspace.md)**

    View engineering application lists including licenses, usages, concurrent usage, denials, and unidentified publisher integration map on the License operations view for quick access.


## April 2026

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

### What's new

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/extract-entitlements-from-contracts-now-assist-sam.md)**

    Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.

-   **[Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/troubleshooting-saas-now-assist-sam.md)**

    Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.

-   **[Use an agentic workflow to automate Microsoft 365 license assignment to users to improve efficiency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/now-assist-sam-fulfill-sw-asset-requests-workflow.md)**

    Use AI agents to assign Microsoft 365 licenses automatically to users on the Microsoft 365 Admin Center without manual intervention. The AI agent analyzes whether there are available licenses and automatically assigns those licenses to the Microsoft 365 Admin Center, ensuring accuracy and compliance.

-   **[Software Asset Management integration with Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/sam-integration-cmpro.md)**

    Gain centralized visibility into software contract life cycles and streamline contract management by extracting key metadata and obligations from an uploaded signed contract document using the agentic AI workflow. Additionally, you can optimize costs through proactive tracking of contract renewals, expirations, and contractual obligations by integrating Software Asset Management with the Contract Management Pro application. Note that only Software Asset Management Enterprise users can leverage this functionality.


### What's changed

-   **[Troubleshoot button alongside the error message on the Integration profile form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/troubleshooting-saas-now-assist-sam.md)**

    The **Troubleshoot** button is available for all SaaS integrations on the error message that is displayed when connection validation fails due to an error. When selected, the button triggers the generation of error summary and resolution guidance.


## Australia Early Availability

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Australia release.

### What's new

-   **[Improve user activity tracking with the GitHub integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/integrate-with-github.md)**

    Achieve more accurate user activity data and improved license reclamation for low or no-activity subscriptions by leveraging the enhanced GitHub integration for broader event coverage and extended retention.


### What's changed

-   **[Granular configuration admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/sam-installed-components.md)**

    Use granular admin roles, such as sam\_admin and sam\_integrator, to complete administrative configuration tasks without requiring the full admin role. By using limited admin privileges that provide access to only certain tasks, you can help reduce security risks across your organization.


