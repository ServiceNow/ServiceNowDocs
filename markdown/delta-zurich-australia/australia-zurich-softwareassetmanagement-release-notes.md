---
title: Combined Software Asset Management release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Software Asset Management from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-softwareassetmanagement-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 18
breadcrumb: [Products combined by family]
---

# Combined Software Asset Management release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Software Asset Management from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Software Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Software Asset Management to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Starting from the Zurich release, the following workflows are migrated to Flow Designer as flows:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

When upgrading to the Zurich release, a fix script identifies whether the workflows were customized. If you haven't customized the workflows before the upgrade, the fix script deactivates the legacy workflows from the instance and deploys the Flow Designer flows on the instance post-upgrade. If you have customized the impacted workflows in the previous release, the fix script doesn’t deploy the Flow Designer flows on the instance post-upgrade. You can view and access the impacted workflows in the instance after the upgrade. However, the deprecated workflows are considered as custom code and ServiceNow doesn’t support those workflows.

 Starting from the Zurich release, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is moved from the family release to the Software Asset Workspace store application. After upgrading to Zurich, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is inactivated and the Software Asset Workspace store application \(sn\_sam\_workspace\) is enabled in the instance.

 When upgrading to the Software Asset Management – SaaS License Management plugin \(sn\_sam\_saas\_int\) version 16.0.6 or later in the Zurich release, verify that the Software Asset Workspace store app \(sn\_sam\_workspace\) is updated to version 9.0.4.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Software Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Retrieve detailed subscription and consumption data across your entire organization with the Docusign integration](https://www.servicenow.com/docs/access?context=integrate-with-docusign-org&family=zurich&ft:locale=en-US)**

Get insights into detailed subscription and consumption data across your organization by integrating Docusign with the Software Asset Management application. You can now access data at both the account and organization levels, giving you a centralized view of envelope activity and usage. This enhancement helps you better monitor Docusign consumption and optimize your license use.

-   **[Streamline the authentication process for Salesforce CRM integration](https://www.servicenow.com/docs/access?context=integrate-with-salesforce-crm&family=zurich&ft:locale=en-US)**

Experience seamless data flow between the Software Asset Management application and Salesforce CRM. This updated feature supports the OAuth 2.0 Client Credentials grant type, eliminating manual authentication, and uses a secure machine-to-machine method to ensure efficient and uninterrupted data exchange.

-   **[Manage license compliance and optimization for Adobe Cloud services through Adobe Guided Setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&family=zurich&ft:locale=en-US)**

Simplify setting up Adobe SaaS integration using the Adobe Guided Setup. The Guided Setup provides step-by-step guidance to set up the Adobe integration with the Software Asset Management application that supports license compliance and optimization for Adobe Cloud services.

-   **[Gain the flexibility to exclude certain SaaS subscriptions \(users and subscription identifiers\) from license calculations](https://www.servicenow.com/docs/access?context=subscription-exclusions&family=zurich&ft:locale=en-US)**

Optimize your licensing costs with the ability to exclude certain low-value and high-volume subscriptions from ServiceNow's licensing calculations.

-   **[Optimize subscription licensing for specific SaaS offerings and editions via Single Sign-On \(SSO\) integrations](https://www.servicenow.com/docs/access?context=integrate-with-azure-ad&family=zurich&ft:locale=en-US)**

Leverage the enhanced SSO integration that supports tracking subscriptions for specific SaaS offerings and editions. This update enables you to map SSO groups to software models for the specific offerings or editions and optimally license users based on their access.

-   **[Improve the security of Microsoft-related integrations with the enhanced support for application type permissions](https://www.servicenow.com/docs/access?context=microsoft-publisher-pack&family=zurich&ft:locale=en-US)**

Enhance Microsoft SaaS integration security with the added support for application-type permissions. This feature includes SSO integration with Microsoft Entra ID, Microsoft Dynamics 365 and Power Apps, and Microsoft 365.

-   **[Monitor database memory for your SAP HANA Database with SAP HANA Database integration](https://www.servicenow.com/docs/access?context=add-sap-connection&family=zurich&ft:locale=en-US)**

Manage memory allocations and licensing costs for your SAP HANA Database by integrating with the Software Asset Management application. Data populated through this approach helps in effective license reconciliation based on the peak memory usage of the SAP HANA Database.

-   **[Receive more frequent updates from the Software Asset Management Content Service](https://www.servicenow.com/docs/access?context=sam-content-updates&family=zurich&ft:locale=en-US)**

Gain the benefit of twice-weekly shipments of the Content Library. This increase in the update frequency delivers faster Content Service to your ServiceNow instance.

-   **[Improve reclamation candidate selection for Microsoft 365 by considering mailbox and OneDrive sizes](https://www.servicenow.com/docs/access?context=o365-usage-activity&family=zurich&ft:locale=en-US)**

Enhance the process of reclamation candidate selection for Microsoft 365 downgrade opportunities by considering three key factors: product usage, mailbox storage, and Microsoft OneDrive storage. Considering all these aspects enables more accurate and effective reclamation decisions.

-   **[Leverage the Flow Designer for reclamation workflow updates](https://www.servicenow.com/docs/access?context=reclaiming-software-sam&family=zurich&ft:locale=en-US)**

Manage the reclamation process using the functionality migrated to the Flow Designer. The Flow Designer migration includes additional error handling features to enable a more intuitive and efficient way to manage the reclamation process.

-   **[Automatically identify and license Microsoft SQL Server high availability configurations](https://www.servicenow.com/docs/access?context=microsoft-sql-server-ha-configurations&family=zurich&ft:locale=en-US)**

Use the Software Asset Management publisher pack for Microsoft to automatically identify and license Microsoft SQL Server deployments in high availability configurations, such as Always On availability groups. This capability enables the Software Asset Management application to automatically classify each replica within a configuration as either active or passive, resulting in more accurate license compliance for Microsoft SQL Server.

-   **[Manage licensing for Microsoft Server products on Microsoft Hyper-V virtualization technology](https://www.servicenow.com/docs/access?context=microsoft-server-licensing-hyper-v-virtualization-technology&family=zurich&ft:locale=en-US)**

Use the Software Asset Management publisher pack for Microsoft to track and manage licensing for Microsoft Server products, such as Microsoft Windows Server and Microsoft SQL Server, on Microsoft Hyper-V virtualization technology. Track license usage and determine your license compliance position so that you can better optimize your licensing costs.

-   **[Apply preferred licensing assignments to Microsoft software products that are deployed on clusters](https://www.servicenow.com/docs/access?context=apply-preferred-licensing-assignments-microsoft-clusters&family=zurich&ft:locale=en-US)**

Define and apply preferred cluster licensing assignments to the Microsoft software products that are deployed on your hypervisor clusters. By using a preferred cluster licensing assignment, you can choose whether you want to license these software products at either the physical host layer or the virtual layer, helping you better align with your organization’s predetermined licensing strategy. Built-in validations help verify that your licensing strategy setup complies with the relevant Microsoft licensing requirements.

-   **[Manage the life-cycle risks of a software product based on its add-on or optional support](https://www.servicenow.com/docs/access?context=software-models-and-entitlements&family=zurich&ft:locale=en-US)**

Gain insight into the extended life cycle of a software product when you purchase an add-on or optional support. Each time you indicate that a software product has an add-on or optional support, the Software Asset Management application extends the life-cycle dates of that product, as defined by the add-on or optional support. Use these extended life-cycle dates to identify and plan for your end-of-life \(EOL\) risks.

-   **[Manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\)](https://www.servicenow.com/docs/access?context=vmware-publisher-pack&family=zurich&ft:locale=en-US)**

Following the updates to VMware's licensing policy, use the Software Asset Management publisher pack for VMware to track and manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\), which are updated suite-based product offerings for VMware vSphere. With these updated product offerings, you can measure compliance and optimize licensing for multiple VMware vSphere products under a single subscription.

In addition, the publisher pack can account for the number of cores and the licensing minimums when calculating licensing requirements for VVS and VVEP.

-   **[Gain expanded insight into the content library information through content dashboard analytics](https://www.servicenow.com/docs/access?context=content-search-portal&family=zurich&ft:locale=en-US)**

Gain in-depth information related to various content tables and trends in content change from the enhanced Content Library portal. The introduction of numeric widgets, line graphs, bar charts, and content-specific tabs provides complete visibility to content shipped and analyze content coverage. The expanded search feature with additional filter options lets you view the records for a particular period or release.

-   **[Efficiently manage user allocations in bulk using group allocations](https://www.servicenow.com/docs/access?context=group-user-allocation&family=zurich&ft:locale=en-US)**

Allocate licenses to user groups instead of individual users for a software entitlement using the group allocation feature for the user-based licensing metric software. Group allocation feature enables Software Asset Management managers to streamline and manage the license allocation process efficiently. User allocation is created for the group members based on the availability of unallocated licenses. Any changes made to the composition of the user group automatically updates the license allocation.

-   **[Use the enhanced License Usage view for expanded insights on your license compliance](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&family=zurich&ft:locale=en-US)**

Conduct a deeper analysis of your publisher compliance using both the list view and the card view in the License usage view. You can save and share the data by exporting the list view in multiple file formats. View integrated health check results, license usage analysis, and learn why a retired or stale CI is using a license. Furthermore, to avoid clutter on the Publisher details page, software model results are only shown for software models that have entitlements.

-   **[Seamlessly continue with the entitlement import process even when PPNs are missing](https://www.servicenow.com/docs/access?context=import-entitlements-workspace&family=zurich&ft:locale=en-US)**

Continue with the entitlement import process by automatically creating software models when both PPNs and software models are missing. Software models are automatically generated based on the publisher and product details.

-   **[Use flexible reporting capabilities to gain deeper insights into your Effective License Position \(ELP\)](https://www.servicenow.com/docs/access?context=elp-grouping-byconsumption&family=zurich&ft:locale=en-US)**

Improve analysis of your ELP with flexible reporting on reconciliation results. Reports can be run on existing reconciliation groups or customer-defined groups, and the report data can be organized by unique combinations of group, subgroup, publisher, product, version, and edition. For each combination, the average cost is calculated and provides the total number of required licenses. The results are presented in a structured format for easy analysis and reporting.


</td></tr><tr><td>

Australia

</td><td>

-   **[Streamline entitlement import by resolving import errors with AI-suggested corrections](https://www.servicenow.com/docs/access?context=resolve-entitlement-import-error&family=australia&ft:locale=en-US)**

Reduce manual effort and improve data accuracy when reviewing entitlement import errors in the Software Asset Workspace by using AI skills. When publisher or product names in the standard entitlement import template don't match standard content, the Software normalization and Product match reviewer skills provide AI-suggested corrections for review. The feature also identifies potential duplicate entitlements, enabling you to review and dismiss them where appropriate.

-   **[Enhance SaaS application usage monitoring by integrating with the Agent Client Collector for Visibility - Content \(ACC-VC\)](https://www.servicenow.com/docs/access?context=shadow-saas-analytics&family=australia&ft:locale=en-US)**

Monitor SaaS application usage across your organization by using URL monitoring data through the integration of your Software Asset Management application with ACC-VC. The SaaS Detection Report aggregates this usage data and distinguishes managed applications from the unmanaged ones. This enhancement provides actionable visibility to SAM managers into actual SaaS usage for software spend optimization.

**Note:** The ACC-VC integration with the Software Asset Management application is available with Software Asset Management - SaaS License Management 17.4.0 and later versions.


[Australia Patch 1](https://www.servicenow.com/docs/access?context=australia-patch-1&family=australia&ft:locale=en-US)

-   **[ServiceNow product tiers](https://www.servicenow.com/docs/access?context=ai-native-sku-overview&family=australia&ft:locale=en-US)**

The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets and create your own
Depending on your entitlements, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.

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


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Software Asset Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Publisher optimizations for Microsoft](https://www.servicenow.com/docs/access?context=pub-opt-microsoft&family=zurich&ft:locale=en-US)**

The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.

-   **[Publisher optimizations for SAP](https://www.servicenow.com/docs/access?context=pub-opt-sap&family=zurich&ft:locale=en-US)**

The Publisher Optimizations dashboard for SAP has been updated with a report on SAP HANA Database monthly peak usage.


</td></tr><tr><td>

Australia

</td><td>

-   **[Granular configuration admin roles](https://www.servicenow.com/docs/access?context=sam-installed-components&family=australia&ft:locale=en-US)**

Use granular admin roles, such as sam\_admin and sam\_integrator, to complete administrative configuration tasks without requiring the full admin role. By using limited admin privileges that provide access to only certain tasks, you can help reduce security risks across your organization.


</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Software Asset Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Software Asset Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Starting from the Zurich release, the following workflows are being prepared for future deprecation:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

Software Asset Management is available with activation of the following plugins:

-   **Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\)**

Activating this plugin automatically activates the following:

    -   Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\)
    -   Software Asset Workspace store application \(sn\_sam\_workspace\)
After you activate the Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\), you can't access the Software Asset Management Core UI.

-   **Software Asset Management Foundation plugin \(com.snc.sams\)**

To access the foundation capabilities of Software Asset Management, activate this plugin. After you activate the Software Asset Management Foundation plugin, activate the Software Asset Workspace store application \(sn\_sam\_workspace\) to complete the setup.


 In the ServiceNow AI Platform® Zurich release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

 Install the following Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/store) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=zurich&ft:locale=en-US).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences
-   Software Asset Workspace

</td></tr><tr><td>

Australia

</td><td>

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

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   ****

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

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

Zurich

</td><td>

-   Streamline Adobe integration with the Software Asset Management application using the Adobe Guided Setup.
-   Integrate SAP HANA Database with the Software Asset Management application to monitor the memory allocations and licensing costs for your SAP HANA Database measurement.
-   Track and optimize licensing for Microsoft Server products on Microsoft Hyper-V virtualization technology by using the Software Asset Management publisher pack for Microsoft.
-   Track and optimize licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\) by using the Software Asset Management publisher pack for VMware.
-   Gain the flexibility to retrieve both subscription and consumption data at the organization level using the enhanced Docusign integration with the Software Asset Management application.

 See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

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

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

