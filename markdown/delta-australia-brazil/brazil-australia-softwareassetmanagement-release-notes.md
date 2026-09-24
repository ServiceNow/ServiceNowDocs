---
title: Combined Software Asset Management release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Software Asset Management from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-softwareassetmanagement-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined Software Asset Management release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Software Asset Management from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Software Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Software Asset Management to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Software Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Improved license compliance reporting for Smartsheet SaaS integration](https://www.servicenow.com/docs/access?context=integrate-with-smartsheet&family=australia&ft:locale=en-US)**

Improve visibility and compliance reporting of Smartsheet user licenses using the assigned seat type in the Smartsheet portal. The integration now retrieves users by seat type and creates subscription records for each category independently.

**Note:** The updated Smartsheet license reporting is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 17.6.0.

-   **[Use expanded Microsoft Entra ID Single Sign-On \(SSO\) license reclamation](https://www.servicenow.com/docs/access?context=saas-sso-integration&family=australia&ft:locale=en-US)**

Expand your Microsoft Entra ID SSO integrations to improve identification of inactive users and surface group-assigned users as reclamation candidates. Update SSO subscription reclamation logic to improve stale subscription detection.

**Note:** The expanded Microsoft Entra ID capability is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 17.6.0.

-   **[Onboard entitlements faster with additional predefined license metrics](https://www.servicenow.com/docs/access?context=c_SAMLicenseMetrics&family=australia&ft:locale=en-US)**

Reduce entitlement onboarding time by using additional predefined license metrics for supported publishers. These predefined license metrics help you track consumption, verify compliance, and reconcile deployments against entitlements. Review tier ranges and calculation factors on the new **License Metric Tier** tab of the Software entitlement page.

-   **[Analyze software spend transactions with AI in the Software Asset Workspace](https://www.servicenow.com/docs/access?context=spend-detection-ai-enhancements&family=australia&ft:locale=en-US)**

Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.


 -   **[Manage IBM sub-capacity licensing on Nutanix AHV \(Acropolis Hypervisor\)](https://www.servicenow.com/docs/access?context=ibm-licensing-vmware-vsphere-environment&family=australia&ft:locale=en-US)**

Gain visibility into IBM products deployed on Nutanix AHV virtualized environments, with consumption data for sub-capacity eligible metrics such as PVU, VPC, and RVU MAPC \(Managed Activated Processor Cores\). Licensing calculations align with IBM sub-capacity requirements, including 30-minute capacity scans that capture peak processor core capacity to help keep license positions audit-ready.

**Note:** IBM sub-capacity licensing on Nutanix AHV is available with IBM License Compliance for Software Asset Management 7.0.0 and later versions.

-   **[Gain visibility into the software asset life cycle with improved CMDB data quality](https://www.servicenow.com/docs/access?context=cmdb-sa-sam-use&family=australia&ft:locale=en-US)**

Audit your Software Asset Management CMDB for data quality gaps including missing edition/version details, cloud license inconsistencies, duplicate installs, and misaligned virtual-to-host relationships. Use the CMDB success advisor for Software Asset Management to systematically validate CI attributes, remediate duplicates, and establish consistent server mapping rules across your estate.


 -   **[Streamline entitlement import by resolving import errors with AI-suggested corrections](https://www.servicenow.com/docs/access?context=resolve-entitlement-import-error&family=australia&ft:locale=en-US)**

Reduce manual effort and improve data accuracy when reviewing entitlement import errors in the Software Asset Workspace by using AI skills. When publisher or product names in the standard entitlement import template don't match standard content, the Software normalization and Product match reviewer skills provide AI-suggested corrections for review. The feature also identifies potential duplicate entitlements, enabling you to review and dismiss them where appropriate.

-   **[Enhance SaaS application usage monitoring by integrating with the Agent Client Collector for Visibility Content \(ACC-VC\)](https://www.servicenow.com/docs/access?context=shadow-saas-analytics&family=australia&ft:locale=en-US)**

Monitor SaaS application usage across your organization by using URL monitoring data through the integration of your Software Asset Management application with ACC-VC. The SaaS Detection Report aggregates this usage data and distinguishes managed applications from the unmanaged ones. This enhancement provides actionable visibility to ServiceNow Otto for SAM managers into actual SaaS usage for software spend optimization.

**Note:** The ACC-VC integration with the Software Asset Management application is available with Software Asset Management - SaaS License Management 17.4.0 and later versions.


 -   **[Enhanced integration with OpenLM for tracking subscription and consumption licenses](https://www.servicenow.com/docs/access?context=concurrent-licenses&family=australia&ft:locale=en-US)**

Gain improved visibility into engineering application licenses across subscription-based and consumption models with the OpenLM integration. This capability provides support for named user allocation and usage tracking. Additionally, you can better monitor compliance risks and note denial patterns through actionable insights into automated processes and dashboards.

-   **[Leverage machine learning \(ML\) normalization for managing your software assets in protected government environments](https://www.servicenow.com/docs/access?context=ml-learning-sam&family=australia&ft:locale=en-US)**

Extend ML normalization capabilities to regulated markets for ServiceNow Protected Platform \(SPP\) in Singapore \(SG\) and Australia \(AU\).

-   **[Enhance the security of SAP ABAP on-premise integration using OAuth 2.0 authentication](https://www.servicenow.com/docs/access?context=add-sap-connection&family=australia&ft:locale=en-US)**

Benefit from enhanced OAuth 2.0 authentication for your SAP ABAP on-premise integrations with improved security. This capability provides a more secure, compliant, and future-proof method for integrating the Software Asset Management application with your SAP systems.

-   **[Improve your license management experience through the enhanced support for Oracle WebLogic Suite licensing](https://www.servicenow.com/docs/access?context=oracle-licensing-cloud-environments&family=australia&ft:locale=en-US)**

Access flexible licensing options that align with different deployment models and usage patterns through comprehensive license management with support for the Oracle WebLogic Suite for both Per Processor and Named User Plus \(NUP\) metrics. The enhanced support now covers the entire WebLogic product family, including the flagship Suite edition.

-   **[Improve software normalization outcomes with expanded pattern-based normalization rules rule](https://www.servicenow.com/docs/access?context=c_SAMDiscovery&family=australia&ft:locale=en-US)**

Streamline the software model discovery process by leveraging the expanded pattern-based normalization rule, which eliminates the need to manually update or create new normalization rules for every minor variation in software discovery models. This rule automatically recognizes and matches diverse patterns and variations in software model data. As a result, discovered publisher, product, version, and edition values are seamlessly aligned with the ServiceNow® repository.

-   **[Enhanced SQL server enterprise edition license compliance to support Server/CAL licensing model](https://www.servicenow.com/docs/access?context=mapping-ms-license-metrics&family=australia&ft:locale=en-US)**

Optimize licensing for legacy Microsoft SQL Server Enterprise Edition licenses under the Server+CAL licensing model with Software Assurance \(SA\) by using the enhanced licensing rule. A single server license can cover up to four virtual machines, provided that the combined processing power for these VMs does not exceed twenty hardware threads or cores at any given time.

-   **[Generate optimal software lifecycle reports using a guided playbook that ensures adherence to compliance and audit requirements.](https://www.servicenow.com/docs/access?context=guidedplaybook-sw-lifecycle-reports&family=australia&ft:locale=en-US)**

Simplify the creation of optimal software life-cycle reports through a guided playbook that assists in defining report scope, identifying gaps, and performing corrective actions. The playbook also integrates with the success portal, enabling you to establish and monitor success metrics, organize tasks and activities, and effectively track progress toward your objectives.

-   **[Streamline license management for Microsoft server product Installations and license usage via a single report](https://www.servicenow.com/docs/access?context=device-license-consumption-report&family=australia&ft:locale=en-US)**

Gain insights to a unified report for all Microsoft server product installations and license usage across license metrics. The Microsoft Server Infrastructure and License consumption report consolidates infrastructure data per device along with license usage and exemptions. Get detailed justifications for exemptions such as unlicensed or ignored installations, making it easier to monitor, analyze, and optimize your IT resources.


 -   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

-   **[Improve accuracy and productivity by extracting licensing data from contracts and generating software entitlements](https://www.servicenow.com/docs/access?context=extract-entitlements-from-contracts-now-assist-sam&family=australia&ft:locale=en-US)**

Leverage generative AI to upload contract documents and automatically extract licensing data, generating software entitlements. You can review and refine the entitlements prior to finalization. The entitlements are created and linked to the contract records, ensuring a streamlined and accurate process.

-   **[Benefit with an integrated troubleshooting experience for SaaS applications by resolving common issues using automated guidance](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&family=australia&ft:locale=en-US)**

Use generative AI to troubleshoot SaaS integrations with automated guidance and recommendations. By following the resolution guidance, you can significantly reduce downtime, lower the mean time to resolution \(MTTR\), and resolve complex SaaS issues without deep technical intervention.

-   **[Use an agentic workflow to automate Microsoft 365 license assignment to users to improve efficiency](https://www.servicenow.com/docs/access?context=now-assist-sam-fulfill-sw-asset-requests-workflow&family=australia&ft:locale=en-US)**

Use AI agents to assign Microsoft 365 licenses automatically to users on the Microsoft 365 Admin Center without manual intervention. The AI agent analyzes whether there are available licenses and automatically assigns those licenses to the Microsoft 365 Admin Center, ensuring accuracy and compliance.

-   **[Software Asset Management integration with Contract Management Pro](https://www.servicenow.com/docs/access?context=sam-integration-cmpro&family=australia&ft:locale=en-US)**

Gain centralized visibility into software contract life cycles and streamline contract management by extracting key metadata and obligations from an uploaded signed contract document using the agentic AI workflow. Additionally, you can optimize costs through proactive tracking of contract renewals, expirations, and contractual obligations by integrating Software Asset Management with the Contract Management Pro application. Note that only Software Asset Management Enterprise users can leverage this functionality.


 -   **[Improve user activity tracking with the GitHub integration](https://www.servicenow.com/docs/access?context=integrate-with-github&family=australia&ft:locale=en-US)**

Achieve more accurate user activity data and improved license reclamation for low or no-activity subscriptions by leveraging the enhanced GitHub integration for broader event coverage and extended retention.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Install the Software Asset Management application from the Product Hub](https://www.servicenow.com/docs/access?context=sam-product-hub&family=brazil&ft:locale=en-US)**

Streamline onboarding by installing Software Asset Management and its dependent applications from the Product Hub. The Product Hub is the central location to view and manage all applications included in your Software Asset Management subscription. Access product documentation, videos, release notes, and community links from the same place.

-   **[Set up the Software Asset Management application using the Configuration Console](https://www.servicenow.com/docs/access?context=config-console-sam&family=brazil&ft:locale=en-US)**

Reduce the time it takes to set up Software Asset Management after installing it from the Product Hub by using the Configuration Console, a one-stop shop for setup. Use predefined settings to smoothen the onboarding journey and configure software foundations, properties, AI skills, governance, team management, and data management from a single location. You can also use the AI conversational interface to configure groups, users, and Content Service setup.

-   **[Manage licenses for SAP S/4HANA Cloud, Private Edition](https://www.servicenow.com/docs/access?context=sap-publisher-pack&family=brazil&ft:locale=en-US)**

Establish an accurate license position for your SAP S/4HANA Cloud, Private Edition delivered through RISE with SAP, without manually tracking user classifications or engine and database consumption. Collect usage data from your private cloud systems and calculate your Full Usage Equivalent \(FUE\) license position automatically with the Software Asset Management publisher pack for SAP. Reduce audit exposure and avoid unexpected compliance costs by measuring private cloud compliance alongside your existing on-premises SAP systems.

-   **[Manage all reclamation candidates from a consolidated Reclamation tab on the License usage view in the Software Asset Workspace](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&family=brazil&ft:locale=en-US)**

Gain insights with a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows. Drill down from the **Reclamation** tab into individual removal candidates for each publisher or integration, without switching between separate reclamation views. This enhancement gives your asset team a complete picture of reclamation opportunities across your software estate.

-   **[Improved license compliance reporting for Smartsheet SaaS integration](https://www.servicenow.com/docs/access?context=integrate-with-smartsheet&family=brazil&ft:locale=en-US)**

Improve visibility and compliance reporting of Smartsheet user licenses using the assigned seat type in the Smartsheet portal. The integration now retrieves users by seat type and creates subscription records for each category independently.

**Note:** The updated Smartsheet license reporting is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 18.0.3.

-   **[Use expanded Microsoft Entra ID Single Sign-On \(SSO\) license reclamation](https://www.servicenow.com/docs/access?context=saas-sso-integration&family=brazil&ft:locale=en-US)**

Expand your Microsoft Entra ID SSO integrations to improve identification of inactive users and surface group-assigned users as reclamation candidates. Update SSO subscription reclamation logic to improve stale subscription detection.

**Note:** The expanded Microsoft Entra ID capability is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 18.0.3.

-   **[Automate suite license inference for improved compliance reporting](https://www.servicenow.com/docs/access?context=software-suites-inference&family=brazil&ft:locale=en-US)**

Enable automatic suite inference to calculate the optimal suite license for each software installation based on your actual footprint and entitlements. This feature reduces manual configuration required for the suite on the software model and improves compliance reporting.

-   **[Improve reporting of software installation inventory](https://www.servicenow.com/docs/access?context=deduplication-rule&family=brazil&ft:locale=en-US)**

Improve reporting of your software installation inventory by deploying rules that automatically consolidate duplicate product installations across your devices.

-   **[Onboard entitlements faster with additional predefined license metrics](https://www.servicenow.com/docs/access?context=c_SAMLicenseMetrics&family=brazil&ft:locale=en-US)**

Reduce entitlement onboarding time by using additional predefined license metrics for supported publishers. These predefined license metrics help you track consumption, verify compliance, and reconcile deployments against entitlements. Review tier ranges and calculation factors on the new **License Metric Tier** tab of the Software entitlement page.

-   **[Analyze software spend transactions with AI in the Software Asset Workspace](https://www.servicenow.com/docs/access?context=spend-detection-ai-enhancements&family=brazil&ft:locale=en-US)**

Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.


</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Software Asset Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[Manage software models with clearer licensing terminology](https://www.servicenow.com/docs/access?context=software-model-fields&family=australia&ft:locale=en-US)**

Understand licensing scope at a glance from the renamed column in the Software Model \[cmdb\_software\_product\_model\] table. The **License all installs accessed by clients** column is renamed to **License all installs**. The new name reflects that all installs meeting the software model's conditions are licensed, not only those tied to client access records.

-   **[Software Spend Detection Core UI](https://www.servicenow.com/docs/access?context=spend-detection-sam-workspace&family=australia&ft:locale=en-US)**

The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.


 -   **[Now Assist &gt; ServiceNow Otto announcement](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&family=australia&ft:locale=en-US)**

ServiceNow Otto introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.


 -   **[Large language models on the ServiceNow AI Platform](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=australia&ft:locale=en-US)**

The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.


 -   **[Delete button on the Product Workload Mapping form](https://www.servicenow.com/docs/access?context=integrate-with-crowdstrike&family=australia&ft:locale=en-US)**

A **Delete** button is available on the Product Workload Mapping form for CrowdStrike integration profiles to enable you to delete existing workload-to-software model mappings directly from the integration profile.

-   **[Product workload mappings and breakdown data lists on the License operations view](https://www.servicenow.com/docs/access?context=operations-workspace&family=australia&ft:locale=en-US)**

View the product workload mappings, usage, and consumption lists on the License operations view without requiring additional configuration.

-   **[Engineering application licenses, usages, and denials lists on the License operations view](https://www.servicenow.com/docs/access?context=operations-workspace&family=australia&ft:locale=en-US)**

View engineering application lists including licenses, usages, concurrent usage, denials, and unidentified publisher integration map on the License operations view for quick access.


 -   **[Troubleshoot button alongside the error message on the Integration profile form](https://www.servicenow.com/docs/access?context=troubleshooting-saas-now-assist-sam&family=australia&ft:locale=en-US)**

The **Troubleshoot** button is available for all SaaS integrations on the error message that is displayed when connection validation fails due to an error. When selected, the button triggers the generation of error summary and resolution guidance.


 -   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=sam-installed-components&family=australia&ft:locale=en-US)**

Use granular admin roles, such as sam\_admin and sam\_integrator, to complete administrative configuration tasks without requiring the full admin role. By using limited admin privileges that provide access to only certain tasks, you can help reduce security risks across your organization.


</td></tr><tr><td>

Brazil

</td><td>

-   **[Gain clearer visibility into SAP HANA user license types with the renamed License classification column](https://www.servicenow.com/docs/access?context=view-sapusers-workspace&family=brazil&ft:locale=en-US)**

The **Named user type** column is renamed to **License classification** in the SAP System Users \[samp\_sap\_system\_user\] table for improved visibility into SAP HANA user license types and entitlement reconciliation. The column appears on the SAP System Users related list of software models created for SAP S/4HANA products.

-   **[Manage SAP S/4HANA Cloud, Public Edition entitlements with the renamed User Subscription metric](https://www.servicenow.com/docs/access?context=c_SAMLicenseMetrics&family=brazil&ft:locale=en-US)**

The **Full Usage Equivalent** license metric for SAP S/4HANA Cloud, Public Edition is renamed to **User Subscription**, aligning with SAP's updated naming for this edition. The Full Usage Equivalent metric continues to apply to SAP S/4HANA Cloud, Private Edition. The calculation logic is unchanged.

-   **[Manage software models with clearer licensing terminology](https://www.servicenow.com/docs/access?context=software-model-fields&family=brazil&ft:locale=en-US)**

Understand licensing scope at a glance from the renamed column in the Software Model \[cmdb\_software\_product\_model\] table. The **License all installs accessed by clients** column is renamed to **License all installs**. The new name reflects that all installs meeting the software model's conditions are licensed, not only those tied to client access records.

-   **[Removal candidates tab replaced with the Reclamation tab in the License usage view](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&family=brazil&ft:locale=en-US)**

The **Reclamation** tab in the License usage view on the Software Asset Workspace presents a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows.

-   **[Software Spend Detection Core UI](https://www.servicenow.com/docs/access?context=spend-detection-sam-workspace&family=brazil&ft:locale=en-US)**

The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.


</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Software Asset Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Software Asset Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Software Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

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

Install the listed Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/store) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

    -   Software Asset Management - SaaS License Management
    -   Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)
    -   IBM License Compliance for Software Asset Management
    -   ITAM Health Check
    -   Software Asset Management Guided Experiences
    -   Software Asset Workspace

**Important:** Software Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

</td></tr><tr><td>

Brazil

</td><td>

-   **Activation information**

Software Asset Management is available with activation of the following plugins:

    -   **[Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\)](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&family=brazil&ft:locale=en-US)**

Activating this plugin automatically activates the following:

        -   Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\)
        -   Software Asset Workspace store application \(sn\_sam\_workspace\)
After you activate the Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\), you can't access the Software Asset Management Core UI.

    -   **[Basic Software Asset Management \(com.snc.sams\) plugin](https://www.servicenow.com/docs/access?context=t_SAMSetupSAMF&family=brazil&ft:locale=en-US)**

To access the foundation capabilities of Software Asset Management, activate the Basic Software Asset Management plugin. After you activate this plugin, activate the Software Asset Workspace store application \(sn\_sam\_workspace\) to complete the setup.


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Software Asset Management, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

[Australia Patch 5](https://www.servicenow.com/docs/access?context=australia-patch-5&family=australia&ft:locale=en-US)

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Otto for Software Asset Management \(SAM\). Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   Manage your IBM software estate on Nutanix AHV \(Acropolis Hypervisor\), including products deployed under sub-capacity licensing. Gain visibility into PVU, VPC, and RVU MAPC \(Managed Activated Processor Cores\) consumption to support compliance and cost optimization.

 [Australia Patch 3](https://www.servicenow.com/docs/access?context=australia-patch-3&family=australia&ft:locale=en-US)

-   Streamline the entitlement import process by resolving import errors using AI skills, for a faster import process and improved data accuracy.

 [Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   Streamline your Software Asset Management application implementation by automating entitlement extraction from contracts using AI, ensuring faster deployment.
-   Enhance your SaaS integration troubleshooting experience with user-friendly error explanations and resolution guidance for runtime job failures.
-   Automate the process of assigning available licenses to the Microsoft 365 Admin Portal by using an agentic workflow.
-   Leverage Obligation Management and AI-powered contract metadata and obligation extraction from an uploaded signed contract document in the Software Asset Workspace by using the combined capabilities of Software Asset Management and Contract Management Pro.

 Australia Patch 0

-   Streamline software lifecycle reporting and compliance management with a guided playbook.
-   Use a consolidated Microsoft licensing report that unifies device and infrastructure deployment details with license consumption calculations and transparent explanations.

 See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

-   Streamline and automate the software asset management tasks using ServiceNow Otto for Software Asset Management \(SAM\)
-   Automatically normalize your software assets with updates from the Software Asset Management content service.
-   Track and manage rights for your software products by creating or importing software entitlements.
-   Integrate with SaaS applications and SSO providers to track your SaaS subscription usage.
-   Track and manage financial transaction data for your software products to optimize your software spend.

 See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&family=brazil&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

