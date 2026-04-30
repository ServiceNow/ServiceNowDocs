---
title: Software Asset Management release notes
description: The ServiceNow Software Asset Management application systematically tracks, evaluates, and manages the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 11
---

# Software Asset Management release notes

The ServiceNow® Software Asset Management application systematically tracks, evaluates, and manages the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Xanadu release.

## Software Asset Management highlights for the Xanadu release

-   Gain insights into your software asset inventory from the first day, control version sprawl, and manage end of life \(EOL\) software products with the prescribed workflows.
-   Use the added support for the Nutanix virtualization technology to meet your license compliance requirements for Microsoft Windows Server, SQL Server, and Red Hat Enterprise Linux Server \(RHEL Server\).
-   Track and optimize IBM licenses across public clouds by using the IBM License Compliance for the Software Asset Management application.
-   Track and manage the indirect usage of SAP applications, avoiding any unexpected licensing costs by using the SAP Digital Access licensing model.

See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US) for more information.

**Important:** SaaS License Management, Data Collection for Oracle Global Licensing and Advisory Services, IBM License Compliance for Software Asset Management, ITAM Health Check, and Software Asset Management Guided Experiences are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Software Asset Management to Xanadu

After upgrading to the Microsoft Entra ID spoke 4.3 version, the **Microsoft Azure AD - Download Group Membership** directory job isn't executed for existing Microsoft Azure AD SSO or Directory integrations. This directory job also isn't created for new Microsoft Azure AD SSO or Directory integrations. Instead, the **Microsoft Azure AD - Download Groups** directory job downloads all groups and group memberships configured on Microsoft Azure AD.

## New in the Xanadu release

-   **[Direct integration support for the Tableau Cloud application](https://www.servicenow.com/docs/access?context=integrate-with-tableau-cloud&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Gain visibility into the subscriptions and reclaim stale licenses by integrating your ServiceNow instance with the Tableau Cloud application.

-   **[Gain a complete view of your GitHub Enterprise Cloud Subscriptions](https://www.servicenow.com/docs/access?context=integrate-github-cloud&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Take advantage of the enhanced ability to optimize your GitHub Enterprise Cloud subscriptions, including outside collaborators, pending invitations, and pending outside collaborators.

-   **[Minimize cost while optimizing Smartsheet subscriptions without the need for the Event Reporting add-on](https://www.servicenow.com/docs/access?context=create-integration-profile&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Optimize your Smartsheet subscriptions without the additional Smartsheet Event Reporting add-on. Use the Smartsheet integration to retrieve the last login information, enabling you to analyze the subscriptions that aren't used efficiently, reducing software spend for Smartsheet.

-   **[Integrate your SaaS applications with minimal user permissions](https://www.servicenow.com/docs/access?context=create-integration-profile&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Minimize security risks and protect information by granting access only to the necessary user or API permissions for optimizing SaaS licenses.

-   **[Get visibility into the login-based licenses of Salesforce CRM applications](https://www.servicenow.com/docs/access?context=integrate-with-salesforce-crm&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Gain insights into the number of Salesforce CRM login consumptions without the need to create user subscriptions.

-   **[License your organization for Oracle Java SE Universal with the Employee license metric](https://www.servicenow.com/docs/access?context=oracle-publisher-pack&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    License all your employees that are using Oracle Java SE Universal with the Employee license metric. The tier-based licensing model also supports licensing discounts.

-   **[Expand your analysis of asset information using the export capabilities in the Software Asset Workspace](https://www.servicenow.com/docs/access?context=sam-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Gain more insights and streamline operations with support for exporting asset information from the Software Asset Workspace.

-   **[Improve Software Asset Management licensing outcomes with actionable insights into discovered inventory](https://www.servicenow.com/docs/access?context=analytics-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Gain insights into discovered inventory, normalization, EOL software products, software version, and edition proliferation in your estate. Act to improve normalization, reduce version and edition proliferation, and remediate EOL software.

-   **[Expand your analysis of overlapping software usage with added insights from spend transactions](https://www.servicenow.com/docs/access?context=app-ration&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    View data related to spend transactions in the Overlapping usage view in Software Asset Workspace. You can gain insights into the combined data from applications including spend detection, Direct integration profiles, and SSO integration profiles.

-   **[Determine license compliance for Microsoft Windows Server, SQL Server, and RHEL Server deployed on Nutanix virtualization technology](https://www.servicenow.com/docs/access?context=software-recon-virt-tech&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Address your license compliance requirements for Microsoft Windows Server, SQL Server, and RHEL Server with deployments on Nutanix virtualization technology.

-   **[Reduce manual effort for managing Microsoft Windows Server Client Access Licenses \(CAL\) with automated usage tracking](https://www.servicenow.com/docs/access?context=user-device-license-consumption&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Track and manage the users and devices that are accessing your server software using ServiceNow® Discovery and use the automatic base CAL creation support for Microsoft Windows Server.

-   **[Optimize Microsoft Visio, Project Online, and Microsoft 365 Copilot subscriptions on the Microsoft 365 Admin Center](https://www.servicenow.com/docs/access?context=microsoft-o365&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Track the usage of Microsoft Visio, Project Online, and Microsoft 365 Copilot subscriptions through the Microsoft 365 Admin Center and create reclamation candidates for any unused subscriptions. Additionally, you can monitor blocked users across all subscriptions who are consuming licenses for potential removal.

-   **[Improve licensing accuracy for software suites with additional configuration for detecting software suites](https://www.servicenow.com/docs/access?context=software-suites-inference&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Improve licensing accuracy for software suites by setting an inference number for suite components. For newly created software models that include suite components, the **Number** inference option is selected by default.

-   **[Limit the License usage view to managed software](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Display software model results for only those software models that are associated with entitlements, limiting the License usage view to managed software.

-   **[Gain comprehensive insights into cluster configuration, licensing, and optimization](https://www.servicenow.com/docs/access?context=understand-sam-cluster&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Simplify cluster analysis by consolidating infrastructure, license usage, optimization, and cluster health data into a single, comprehensive view. This consolidation empowers Software Asset Management \(SAM\) managers to comprehend their cluster setup, examining details such as hosts, virtual machines, and software running on the cluster. Additionally, they gain insights into software license usage, optimization, and health issues. Equipped with this knowledge, SAM managers can make informed decisions that cover all aspects of their clusters.

-   **[Gain improved normalization coverage for similar discovery models through wide-net normalization](https://www.servicenow.com/docs/access?context=c_SAMDiscovery&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Achieve improved normalization of software products that have similar discovery models through wide-net normalization. With wide-net normalization, the Software Asset Management application uses a single normalization rule to normalize software products that share the same patterns for the discovered major version, discovered publisher, and discovered product. The Software Asset Management application can then immediately normalize your discovered software products without requiring the Content Service team to create additional normalization rules for similar discovery models. With this streamlined normalization process, you can reconcile and determine the license compliance of your software products more efficiently.

-   **[Manage content requests for software products directly through the Software Asset Management application](https://www.servicenow.com/docs/access?context=add-custom-software-products-workspace&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Submit, review, and disposition content requests for software products directly through the Software Asset Management application. If any publicly available software products don't exist in the Software Asset Management Content Library, you can add them to your ServiceNow instance as custom software products. By adding these custom software products to your instance, you can immediately use them in your downstream processes while automatically submitting corresponding content requests to the Content Service team. After these content requests are processed by the Content Service team, you can consolidate the custom software products with the software products that are added to the Software Asset Management Content Library.

-   **[Manage license compliance for Red Hat Enterprise Linux \(RHEL\) software across hybrid infrastructures](https://www.servicenow.com/docs/access?context=byol-concepts&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Use bring your own subscription \(BYOS\) support for Red Hat Enterprise Linux \(RHEL\) to determine the license compliance of your RHEL software across both on-premise and public cloud environments. Supported public cloud providers include AWS, Microsoft Azure, and Google Cloud Platform \(GCP\). Use your license compliance information to remediate any RHEL software installations that are non-compliant.

-   **[Optimize IBM licensing across public clouds by using the IBM License Compliance for Software Asset Management application](https://www.servicenow.com/docs/access?context=ibm-licensing-public-cloud-environments&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Use the IBM License Compliance for Software Asset Management application to track and measure IBM licenses across public clouds. Supported public cloud providers include AWS, Microsoft Azure, and Google Cloud Platform \(GCP\).

-   **[Optimize license costs for Microsoft Windows Server and Microsoft SQL Server deployments on your clusters](https://www.servicenow.com/docs/access?context=view-cost-based-licensing-optimizations-microsoft&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Use the Microsoft Core License Optimization reports to gain insight into the recommended cost-based licensing optimizations for your Microsoft clusters. Use this information to maximize cost savings across your Microsoft cluster deployments.

-   **[Manage licenses for indirect access to SAP applications using SAP Digital Access licensing model](https://www.servicenow.com/docs/access?context=sap-publisher-pack&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

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
-   **[Access software content data in National Security Cloud \(NSC\) Department of Defense \(DOD\) Impact Level 5 \(IL5\) deployments](https://www.servicenow.com/docs/access?context=c_SAMContentService&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    Access Software Asset Management Content Library data and receive regular software content updates for your NSC DOD IL5 deployments through the NSC DOD IL5 Content Data Service \(CDS\).

-   **[Gain increased visibility to Java landscape with enhanced ServiceNow Discovery application and reporting certified by Oracle Global License Advisory Services \(GLAS\)](https://www.servicenow.com/docs/access?context=download-oracle-glas-data&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    Access Oracle verified GLAS data by downloading Oracle Java reports populated by the ServiceNow Discovery application. The Discovery application also supports the discovery and evidence download of the Oracle database and middleware.


## UI changes

-   **[Reports displaying the combined data for SaaS and spend detection applications in the Overlapping usage view](https://www.servicenow.com/docs/access?context=app-ration&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    On the Overlapping usage view of Software Asset Workspace, the following widgets have been changed:

    -   Highest count in overlapping software application is replaced by Total count for SaaS and spend detection applications
    -   Highest spend in overlapping software application is replaced by Total spend for SaaS and spend detection applications
-   **[Report visualizations with details of published products on the License usage view](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    On the Publisher details page of the License usage view, the following widgets have been changed:

    -   True-up cost and Savings are replaced with score cards
    -   Software Model Statistics are removed
    -   Progress indicators are split into two widgets, with one widget showing only unlicensed entities

## Removed in this release

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

## Deprecations

-   In the Software installation \[cmdb\_sam\_sw\_install\] table, the Installs associated to lifecycle column is deprecated.
-   In the Software lifecycle Reports \[sam\_sw\_product\_lifecycle\_report\] table, the Installs column is deprecated. You can view the Software installation related list by selecting the Name column.

## Activation information

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugins, including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface. For details about the plugins and how to request them, see [Components installed with Software Asset Management Professional](https://www.servicenow.com/docs/access?context=sam-installed-components&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

In the ServiceNow AI Platform® Xanadu release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

For releases prior to Utah, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic user interface. For details about the plugins and how to request them, see [Request the Software Asset Management plugins](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US).

To activate Next Experience, make sure that the **glide.ui.polaris.experience** system property in your instance is set to true.

Install the following Software Asset Management applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences

## Related ServiceNow applications and features

-   **[Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your asset environment.

-   **[Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Enterprise Asset Management application enables you to manage the entire life cycle of your connected and non-connected enterprise assets. It provides a comprehensive end-to-end solution for maintaining enterprise assets, minimizing costly downtime, and maximizing enterprise asset usability.

-   **[Cloud Cost Management](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Cloud Cost Management application enables you to analyze all costs that are associated with your cloud assets. You can use this information to optimize operations and reduce your cloud spend.

-   **[Contract Management](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://www.servicenow.com/docs/access?context=c_Procurement&version=xanadu&pubname=xanadu-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Procurement application helps you to create purchase orders and to obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

