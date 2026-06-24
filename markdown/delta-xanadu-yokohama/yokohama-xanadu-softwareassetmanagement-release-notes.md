---
title: Combined Software Asset Management release notes for upgrades from Xanadu to Yokohama
description: Consolidated page of all release notes for Software Asset Management from Xanadu to Yokohama.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/delta-xanadu-yokohama/yokohama-xanadu-softwareassetmanagement-release-notes.html
release: yokohama
topic_type: reference
last_updated: "2026-06-24"
reading_time_minutes: 19
breadcrumb: [Products combined by family]
---

# Combined Software Asset Management release notes for upgrades from Xanadu to Yokohama

Consolidated page of all release notes for Software Asset Management from Xanadu to Yokohama.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Software Asset Management release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Yokohama.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Software Asset Management to Yokohama

Before you upgrade to Yokohama, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

After upgrading to the Microsoft Entra ID spoke 4.3 version, the **Microsoft Azure AD - Download Group Membership** directory job isn't executed for existing SSO or Directory integrations. This directory job also isn't created for new SSO or Directory integrations. Instead, the **Microsoft Azure AD - Download Groups** directory job downloads all groups and group memberships configured on .

</td></tr><tr><td>

Yokohama

</td><td>

Starting from the Yokohama release, all the reconciliation script includes are being moved from the family release to the Software Asset Management store application \(com.sn\_itam\_samp\). When upgrading to Yokohama, if you have made customizations to reconciliation script includes, you must move your customizations to the new script includes. The old script includes will be deprecated.

 When upgrading to Yokohama Patch 1 with the Software Asset Management \(sn\_itam\_samp\) 2.1.0 store application installed, you must delete the entitlements for the existing CrowdStrike integration profiles. Then, create new entitlements for various CrowdStrike products, such as CrowdStrike Falcon Endpoint Protection and CrowdStrike Falcon Discover, based on their license metrics. These metrics include the Reserved Hourly Average Sensor and Sensor Subscription, which are found under the CrowdStrike License Metric Group.

-   If any existing CrowdStrike profiles are in the Draft state, create new integration profiles and delete the existing ones.
-   If any existing CrowdStrike profiles are in the Published state, their state changes to Draft.

</td></tr></tbody>
</table>## New features

Between your current release family and Yokohama, new features were introduced for Software Asset Management.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[Direct integration support for the Tableau Cloud application](https://www.servicenow.com/docs/access?context=integrate-with-tableau-cloud&family=xanadu&ft:locale=en-US)**

Gain visibility into the subscriptions and reclaim stale licenses by integrating your ServiceNow instance with the Tableau Cloud application.

-   **[Gain a complete view of your GitHub Enterprise Cloud Subscriptions](https://www.servicenow.com/docs/access?context=integrate-github-cloud&family=xanadu&ft:locale=en-US)**

Take advantage of the enhanced ability to optimize your GitHub Enterprise Cloud subscriptions, including outside collaborators, pending invitations, and pending outside collaborators.

-   **[Minimize cost while optimizing Smartsheet subscriptions without the need for the Event Reporting add-on](https://www.servicenow.com/docs/access?context=create-integration-profile&family=xanadu&ft:locale=en-US)**

Optimize your Smartsheet subscriptions without the additional Smartsheet Event Reporting add-on. Use the Smartsheet integration to retrieve the last login information, enabling you to analyze the subscriptions that aren't used efficiently, reducing software spend for Smartsheet.

-   **[Integrate your SaaS applications with minimal user permissions](https://www.servicenow.com/docs/access?context=create-integration-profile&family=xanadu&ft:locale=en-US)**

Minimize security risks and protect information by granting access only to the necessary user or API permissions for optimizing SaaS licenses.

-   **[Get visibility into the login-based licenses of Salesforce CRM applications](https://www.servicenow.com/docs/access?context=integrate-with-salesforce-crm&family=xanadu&ft:locale=en-US)**

Gain insights into the number of Salesforce CRM login consumptions without the need to create user subscriptions.

-   **[License your organization for Oracle Java SE Universal with the Employee license metric](https://www.servicenow.com/docs/access?context=oracle-publisher-pack&family=xanadu&ft:locale=en-US)**

License all your employees that are using Oracle Java SE Universal with the Employee license metric. The tier-based licensing model also supports licensing discounts.

-   **[Expand your analysis of asset information using the export capabilities in the Software Asset Workspace](https://www.servicenow.com/docs/access?context=sam-workspace&family=xanadu&ft:locale=en-US)**

Gain more insights and streamline operations with support for exporting asset information from the Software Asset Workspace.

-   **[Improve Software Asset Management licensing outcomes with actionable insights into discovered inventory](https://www.servicenow.com/docs/access?context=analytics-workspace&family=xanadu&ft:locale=en-US)**

Gain insights into discovered inventory, normalization, EOL software products, software version, and edition proliferation in your estate. Act to improve normalization, reduce version and edition proliferation, and remediate EOL software.

-   **[Expand your analysis of overlapping software usage with added insights from spend transactions](https://www.servicenow.com/docs/access?context=app-ration&family=xanadu&ft:locale=en-US)**

View data related to spend transactions in the Overlapping usage view in Software Asset Workspace. You can gain insights into the combined data from applications including spend detection, Direct integration profiles, and SSO integration profiles.

-   **[Determine license compliance for Microsoft Windows Server, SQL Server, and RHEL Server deployed on Nutanix virtualization technology](https://www.servicenow.com/docs/access?context=software-recon-virt-tech&family=xanadu&ft:locale=en-US)**

Address your license compliance requirements for Microsoft Windows Server, SQL Server, and RHEL Server with deployments on Nutanix virtualization technology.

-   **[Reduce manual effort for managing Microsoft Windows Server Client Access Licenses \(CAL\) with automated usage tracking](https://www.servicenow.com/docs/access?context=user-device-license-consumption&family=xanadu&ft:locale=en-US)**

Track and manage the users and devices that are accessing your server software using ServiceNow® Discovery and use the automatic base CAL creation support for Microsoft Windows Server.

-   **[Optimize Microsoft Visio, Project Online, and Microsoft 365 Copilot subscriptions on the Microsoft 365 Admin Center](https://www.servicenow.com/docs/access?context=microsoft-o365&family=xanadu&ft:locale=en-US)**

Track the usage of Microsoft Visio, Project Online, and Microsoft 365 Copilot subscriptions through the Microsoft 365 Admin Center and create reclamation candidates for any unused subscriptions. Additionally, you can monitor blocked users across all subscriptions who are consuming licenses for potential removal.

-   **[Improve licensing accuracy for software suites with additional configuration for detecting software suites](https://www.servicenow.com/docs/access?context=software-suites-inference&family=xanadu&ft:locale=en-US)**

Improve licensing accuracy for software suites by setting an inference number for suite components. For newly created software models that include suite components, the **Number** inference option is selected by default.

-   **[Limit the License usage view to managed software](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&family=xanadu&ft:locale=en-US)**

Display software model results for only those software models that are associated with entitlements, limiting the License usage view to managed software.

-   **[Gain comprehensive insights into cluster configuration, licensing, and optimization](https://www.servicenow.com/docs/access?context=understand-sam-cluster&family=xanadu&ft:locale=en-US)**

Simplify cluster analysis by consolidating infrastructure, license usage, optimization, and cluster health data into a single, comprehensive view. This consolidation empowers Software Asset Management \(SAM\) managers to comprehend their cluster setup, examining details such as hosts, virtual machines, and software running on the cluster. Additionally, they gain insights into software license usage, optimization, and health issues. Equipped with this knowledge, SAM managers can make informed decisions that cover all aspects of their clusters.

-   **[Gain improved normalization coverage for similar discovery models through wide-net normalization](https://www.servicenow.com/docs/access?context=c_SAMDiscovery&family=xanadu&ft:locale=en-US)**

Achieve improved normalization of software products that have similar discovery models through wide-net normalization. With wide-net normalization, the Software Asset Management application uses a single normalization rule to normalize software products that share the same patterns for the discovered major version, discovered publisher, and discovered product. The Software Asset Management application can then immediately normalize your discovered software products without requiring the Content Service team to create additional normalization rules for similar discovery models. With this streamlined normalization process, you can reconcile and determine the license compliance of your software products more efficiently.

-   **[Manage content requests for software products directly through the Software Asset Management application](https://www.servicenow.com/docs/access?context=add-custom-software-products-workspace&family=xanadu&ft:locale=en-US)**

Submit, review, and disposition content requests for software products directly through the Software Asset Management application. If any publicly available software products don't exist in the Software Asset Management Content Library, you can add them to your ServiceNow instance as custom software products. By adding these custom software products to your instance, you can immediately use them in your downstream processes while automatically submitting corresponding content requests to the Content Service team. After these content requests are processed by the Content Service team, you can consolidate the custom software products with the software products that are added to the Software Asset Management Content Library.

-   **[Manage license compliance for Red Hat Enterprise Linux \(RHEL\) software across hybrid infrastructures](https://www.servicenow.com/docs/access?context=byol-concepts&family=xanadu&ft:locale=en-US)**

Use bring your own subscription \(BYOS\) support for Red Hat Enterprise Linux \(RHEL\) to determine the license compliance of your RHEL software across both on-premise and public cloud environments. Supported public cloud providers include AWS, Microsoft Azure, and Google Cloud Platform \(GCP\). Use your license compliance information to remediate any RHEL software installations that are non-compliant.

-   **[Optimize IBM licensing across public clouds by using the IBM License Compliance for Software Asset Management application](https://www.servicenow.com/docs/access?context=ibm-licensing-public-cloud-environments&family=xanadu&ft:locale=en-US)**

Use the IBM License Compliance for Software Asset Management application to track and measure IBM licenses across public clouds. Supported public cloud providers include AWS, Microsoft Azure, and Google Cloud Platform \(GCP\).

-   **[Optimize license costs for Microsoft Windows Server and Microsoft SQL Server deployments on your clusters](https://www.servicenow.com/docs/access?context=view-cost-based-licensing-optimizations-microsoft&family=xanadu&ft:locale=en-US)**

Use the Microsoft Core License Optimization reports to gain insight into the recommended cost-based licensing optimizations for your Microsoft clusters. Use this information to maximize cost savings across your Microsoft cluster deployments.

-   **[Manage licenses for indirect access to SAP applications using SAP Digital Access licensing model](https://www.servicenow.com/docs/access?context=sap-publisher-pack&family=xanadu&ft:locale=en-US)**

Track the usage of SAP applications through a third-party application or a non- SAP intermediary software by using the SAP Digital Access model. In this licensing model, the usage of SAP applications is licensed by the count of documents created by the third-party application. The documents include the following:

    -   Sales
    -   Invoices
    -   Purchase Orders
    -   Service &amp; Maintenance
    -   Manufacturing
    -   Quality Management
    -   Time Management
    -   Financial
    -   Material
-   **[Access software content data in National Security Cloud \(NSC\) Department of Defense \(DOD\) Impact Level 5 \(IL5\) deployments](https://www.servicenow.com/docs/access?context=c_SAMContentService&family=xanadu&ft:locale=en-US)**

Access Software Asset Management Content Library data and receive regular software content updates for your NSC DOD IL5 deployments through the NSC DOD IL5 Content Data Service \(CDS\).

-   **[Gain increased visibility to Java landscape with enhanced ServiceNow Discovery application and reporting certified by Oracle Global License Advisory Services \(GLAS\)](https://www.servicenow.com/docs/access?context=download-oracle-glas-data&family=xanadu&ft:locale=en-US)**

Access Oracle verified GLAS data by downloading Oracle Java reports populated by the ServiceNow Discovery application. The Discovery application also supports the discovery and evidence download of the Oracle database and middleware.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Gain insights into your publisher license compliance by using Now Assist for Software Asset Management](https://www.servicenow.com/docs/access?context=now-assist-sam&family=yokohama&ft:locale=en-US)**

Use generative AI to gain a comprehensive summary of publisher license compliance. The detailed publisher summaries enable you to understand the publisher license compliance details.

-   **[Manage Microsoft 365 license compliance and optimization through Microsoft 365 Guided Setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&family=yokohama&ft:locale=en-US)**

Get a prescriptive guidance for the tasks that you must perform in the Software Asset Management application, Microsoft 365 admin center, and other applications to configure Microsoft 365. This Guided Setup organizes the configuration activities into various categories so that you can see the list of tasks that need to be performed.

-   **[Optimize Microsoft 365 subscriptions](https://www.servicenow.com/docs/access?context=microsoft-o365&family=yokohama&ft:locale=en-US)**

Optimize how to manage Microsoft 365 licensing with these enhancements:

    -   Auto removal of licenses from the Microsoft 365 admin center by detecting low usage and overlapping subscriptions.
    -   Expanded support for usage-based optimization such as Microsoft 365 E3 Teams and Microsoft 365 government plans.
-   **[Optimize Microsoft Dynamics 365 subscriptions](https://www.servicenow.com/docs/access?context=integrating-with-microsoft365&family=yokohama&ft:locale=en-US)**
    -   Receive recommendations to save costs by removing low-usage subscriptions for MRS applications.
    -   Receive guidance on cost-saving strategies while purchasing multiple base subscription licenses for various Microsoft Dynamics 365 applications. Using a combination of base and attach licenses can provide a more cost-effective solution.
-   **[Simplify the activation process for SaaS License Management](https://www.servicenow.com/docs/access?context=request-saas-license-management&family=yokohama&ft:locale=en-US)**

Simplify your activation process by optimizing your SaaS subscriptions. You can activate just the SaaS applications that you want to manage.

-   **[SaaS security permissions](https://www.servicenow.com/docs/access?context=create-integration-profile&family=yokohama&ft:locale=en-US)**

While integrating your SaaS applications, you can now grant the minimum permissions required to enable key use cases, such as downloading subscriptions, calculating activity, and reclaiming subscriptions.

-   **[Optimize subscriptions for SAP Ariba](https://www.servicenow.com/docs/access?context=integrate-with-ariba&family=yokohama&ft:locale=en-US)**

Gain visibility to the subscriptions and reclaim stale licenses by integrating your ServiceNow instance with the SAP Ariba application.

-   **[Configure and map users from SaaS portals to ServiceNow AI Platform with ease](https://www.servicenow.com/docs/access?context=map-user-data&family=yokohama&ft:locale=en-US)**

Determine your licensed users by mapping user subscriptions from SaaS applications to users in ServiceNow AI Platform.

-   **[Optimize CrowdStrike subscriptions](https://www.servicenow.com/docs/access?context=integrate-with-crowdstrike&family=yokohama&ft:locale=en-US)**

Software Asset Management now includes support for CrowdStrike products with license metrics such as Sensor Subscription and Reserved Hourly Average Sensor. The introduction of a new license metric group, CrowdStrike, improves data coverage and reconciliation. By managing the entitlements for various CrowdStrike products, including CrowdStrike Falcon Endpoint Protection, CrowdStrike Falcon Discover, and others, you can get better tracking and compliance.

-   **[Manage onboarding of products to support the Software Asset Management \(SAM\) application through SAM Guided setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&family=yokohama&ft:locale=en-US)**

Get step-by-step guidance on the activities that you must perform to onboard SaaS and on-premises products. The guided setup helps you to create or associate success goals, configure product integrations, create software entitlements, or run reconciliation to get the most out of the Software Asset Management application.

-   **[Manage license compliance for Oracle Database and WebLogic Server deployed on Solaris Logical Domain \(LDOM\)](https://www.servicenow.com/docs/access?context=oracle-licensing-hard-partitioned-environments&family=yokohama&ft:locale=en-US)**

Support Oracle Database and WebLogic Server licensing for Per Processor and Named User Plus \(NUP\) license metrics that are deployed on the hard-partitioned Solaris LDOM infrastructure, also known as Oracle VM Server for SPARC.

-   **[Manage compliance for SAP S/4HANA Cloud Public Edition](https://www.servicenow.com/docs/access?context=integrate-with-hana&family=yokohama&ft:locale=en-US)**

Gain visibility to software usage information and subscriptions by integrating your Software Asset Management application with the SAP S/4HANA Cloud Public Edition. This integration supports the Full User Equivalent \(FUE\) license metric that is used to grant licenses for SAP cloud applications.

-   **[Determine license compliance for Oracle products deployed on Nutanix virtualization technology](https://www.servicenow.com/docs/access?context=software-recon-virt-tech&family=yokohama&ft:locale=en-US)**

License Oracle Database Server, Options, and WebLogic Server with deployments on the Nutanix virtualization technology.

-   **[Support for revenue-based license metrics for SAP engines](https://www.servicenow.com/docs/access?context=sap-publisher-pack&family=yokohama&ft:locale=en-US)**

Gain the ability to maintain licenses for higher value, revenue-based SAP engine products.

-   **[Leverage machine learning normalization for software recognition in protected government environments](https://www.servicenow.com/docs/access?context=ml-learning-sam&family=yokohama&ft:locale=en-US)**

Extend machine learning normalization capabilities to Government Community Cloud \(GCC\) and National Security Cloud \(NSC\) environments.

-   **[Leverage machine learning spend detection in protected government environments](https://www.servicenow.com/docs/access?context=software-spend-detection&family=yokohama&ft:locale=en-US)**

Extend Software Spend Detection capabilities to Government Community Cloud \(GCC\) and National Security Cloud \(NSC\) environments.

-   **[Optimize licensing for IBM Cloud Paks](https://www.servicenow.com/docs/access?context=licensing-ibm-cloud-paks&family=yokohama&ft:locale=en-US)**

Use the IBM License Compliance for Software Asset Management application to track and manage licenses for your IBM Cloud Paks.

-   **[Expand end of life \(EOL\) reporting by creating parent-child relationships between software products](https://www.servicenow.com/docs/access?context=create-parent-child-relationships-between-software-products&family=yokohama&ft:locale=en-US)**

View, define, or update the parent-child relationships between your software products. Use these relationships to enable your child products to inherit life-cycle dates from their associated parent products.

-   **[View the Export Classification Control Numbers \(ECCNs\) for your software products](https://www.servicenow.com/docs/access?context=view-eccn-software-mappings&family=yokohama&ft:locale=en-US)**

View the ECCNs that are mapped to your software products. Use this information to identify the products that are subject to U.S. export control regulations so that you can maintain export compliance across your products.

-   **[Create and manage entitlements for your Microsoft 365 From SA and Add-on user subscription licenses \(USLs\)](https://www.servicenow.com/docs/access?context=creating-m365-from-sa-add-on-entitlements&family=yokohama&ft:locale=en-US)**

Create entitlements to track and manage the From SA and Add-on licensing terms for your Microsoft 365 subscriptions. Specify the details of each license, including the license type, license cost, and number of purchased rights. Use this information to determine your license compliance so that you can optimize your licensing costs.

-   **[Improve your compliance position with insights on how your software installations get licensed](https://www.servicenow.com/docs/access?context=install-licenseusage-journey&family=yokohama&ft:locale=en-US)**

Evaluate the installation to license consumption percentages and devise strategies for improving your license usage. Track your installation to license journey by connecting software installations to the licenses consumed and identifying the statuses such as licensed or unlicensed.

-   **[Gain an understanding of how licenses get calculated for your software assets](https://www.servicenow.com/docs/access?context=explanation-rights-post-recon&family=yokohama&ft:locale=en-US)**

Learn how the Software Asset Management application calculates the number of licenses that are required for your software assets with the factors that impact this process.

-   **[Increase the coverage of product life cycles](https://www.servicenow.com/docs/access?context=calculated-lifecycles&family=yokohama&ft:locale=en-US)**

Expand the life-cycle date calculations to include the custom general availability \(GA\) dates. Additionally, support is also available for the End of Extended Support phase and the End of Support and End of Life phases.


</td></tr></tbody>
</table>## Changes

Between your current release family and Yokohama, some changes were made to existing Software Asset Management features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **[Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US)**

The Software Asset configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.

-   **[Publisher optimizations dashboard for Microsoft](https://www.servicenow.com/docs/access?context=pub-opt-microsoft&family=yokohama&ft:locale=en-US)**

The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.


</td></tr></tbody>
</table>## Removed

Between your current release family and Yokohama, some Software Asset Management features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

The following legacy dashboards are no longer available for new Xanadu users who have activated the Software Asset Management Professional \(com.snc.samp\) plugin or upgraded to Xanadu without activating the Software Asset Management Professional \(com.snc.samp\) plugin prior to Xanadu.

-   Office 365 and Adobe Cloud dashboard
-   Software Asset Analytics dashboard
-   Software Publisher Analytics dashboard
-   SaaS Overview dashboard
-   Software Asset Management dashboard
-   Engineering License Overview dashboard
-   Normalization and Content Service dashboard
-   Software Asset Management Foundation dashboard
-   Overlapping Software dashboard

**Note:** If you activated the Software Asset Management Professional \(com.snc.samp\) plugin prior to Xanadu but didn't activate the Workspace plugin \(com.sn\_sam\_workspace\), you have access to the legacy dashboards. If you activate the Workspace plugin, you aren't able to access the legacy dashboards from the **Software Asset** navigation menu in your instance. You can, however, access the legacy dashboards from the **Dashboards** navigation menu.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Yokohama, some Software Asset Management features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   In the Software installation \[cmdb\_sam\_sw\_install\] table, the Installs associated to lifecycle column is deprecated.
-   In the Software lifecycle Reports \[sam\_sw\_product\_lifecycle\_report\] table, the Installs column is deprecated. You can view the Software installation related list by selecting the Name column.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugins, including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface. For details about the plugins and how to request them, see [Components installed with Software Asset Management Professional](https://www.servicenow.com/docs/access?context=sam-installed-components&family=xanadu&ft:locale=en-US).

 In the ServiceNow AI Platform® Xanadu release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

 For releases prior to Utah, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic user interface. For details about the plugins and how to request them, see [Request the Software Asset Management plugins](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&family=xanadu&ft:locale=en-US).

 To activate Next Experience, make sure that the **glide.ui.polaris.experience** system property in your instance is set to true.

 Install the following Software Asset Management applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=xanadu&ft:locale=en-US).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences

</td></tr><tr><td>

Yokohama

</td><td>

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugins, including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface.

 In the ServiceNow AI Platform® Yokohama release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

 For releases prior to Utah, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic user interface. For details about the plugins and how to request them, see [Request Software Asset Management](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&family=yokohama&ft:locale=en-US).

 To activate Next Experience, make sure that the **glide.ui.polaris.experience** system property in your instance is set to true.

 Install the following Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=yokohama&ft:locale=en-US).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

-   **Accessibility improvements**

Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://www.servicenow.com/docs/access?context=auto-reflow&family=yokohama&ft:locale=en-US) for details.


</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Software Asset Management we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

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

Xanadu

</td><td>

-   Gain insights into your software asset inventory from the first day, control version sprawl, and manage end of life \(EOL\) software products with the prescribed workflows.
-   Use the added support for the Nutanix virtualization technology to meet your license compliance requirements for Microsoft Windows Server, SQL Server, and Red Hat Enterprise Linux Server \(RHEL Server\).
-   Track and optimize IBM licenses across public clouds by using the IBM License Compliance for the Software Asset Management application.
-   Track and manage the indirect usage of SAP applications, avoiding any unexpected licensing costs by using the SAP Digital Access licensing model.

 See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Leverage generative AI by using the Now Assist for Software Asset Management \(SAM\) application to create publisher summaries on software deployment, license compliance, configuration health, and optimization.
-   Manage the licenses for your Oracle Databases and WebLogic deployments on the Nutanix virtualization technology.
-   Integrate SAP Ariba and SAP S/4HANA Cloud with the Software Asset Management application to monitor and track software usage and subscriptions effectively.
-   Simplify the onboarding of your Software Asset Management \(SAM\) application by following the prescriptive guidance provided in the SAM Guided Setup and Microsoft 365 Guided Setup.
-   Track and optimize your IBM Cloud Pak licenses by using the Software Asset Management application.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

 See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&family=yokohama&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/delta-xanadu-yokohama/rn-combined-intro.md)

