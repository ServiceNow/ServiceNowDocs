---
title: Software Asset Management release notes
description: The ServiceNow Software Asset Management application systematically tracks, evaluates, and manages the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 9
---

# Software Asset Management release notes

The ServiceNow® Software Asset Management application systematically tracks, evaluates, and manages the cost, utilization, compliance, and optimization for software and SaaS applications. The Software Asset Management application was enhanced and updated in the Yokohama release.

## Software Asset Management highlights for the Yokohama release

-   Leverage generative AI by using the Now Assist for Software Asset Management \(SAM\) application to create publisher summaries on software deployment, license compliance, configuration health, and optimization.
-   Manage the licenses for your Oracle Databases and WebLogic deployments on the Nutanix virtualization technology.
-   Integrate SAP Ariba and SAP S/4HANA Cloud with the Software Asset Management application to monitor and track software usage and subscriptions effectively.
-   Simplify the onboarding of your Software Asset Management \(SAM\) application by following the prescriptive guidance provided in the SAM Guided Setup and Microsoft 365 Guided Setup.
-   Track and optimize your IBM Cloud Pak licenses by using the Software Asset Management application.
-   Benefit from accessibility improvements to create a configurable workspace that supports Web Content Accessibility Guidelines \(WCAG\) 2.1 Level AA conformance.

See [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/c_SoftwareAssetMgmt.md) for more information.

**Important:** SaaS License Management, Data Collection for Oracle Global Licensing and Advisory Services, IBM License Compliance for Software Asset Management, ITAM Health Check, and Software Asset Management Guided Experiences are available in ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Software Asset Management to Yokohama

Starting from the Yokohama release, all the reconciliation script includes are being moved from the family release to the Software Asset Management store application \(com.sn\_itam\_samp\). When upgrading to Yokohama, if you have made customizations to reconciliation script includes, you must move your customizations to the new script includes. The old script includes will be deprecated.

When upgrading to Yokohama Patch 1 with the Software Asset Management \(sn\_itam\_samp\) 2.1.0 store application installed, you must delete the entitlements for the existing CrowdStrike integration profiles. Then, create new entitlements for various CrowdStrike products, such as CrowdStrike Falcon Endpoint Protection and CrowdStrike Falcon Discover, based on their license metrics. These metrics include the Reserved Hourly Average Sensor and Sensor Subscription, which are found under the CrowdStrike License Metric Group.

-   If any existing CrowdStrike profiles are in the Draft state, create new integration profiles and delete the existing ones.
-   If any existing CrowdStrike profiles are in the Published state, their state changes to Draft.

## New in the Yokohama release

-   **[Gain insights into your publisher license compliance by using Now Assist for Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/now-assist-sam.md)**

    Use generative AI to gain a comprehensive summary of publisher license compliance. The detailed publisher summaries enable you to understand the publisher license compliance details.

-   **[Manage Microsoft 365 license compliance and optimization through Microsoft 365 Guided Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/playbook-entitlementsetup-workspace.md)**

    Get a prescriptive guidance for the tasks that you must perform in the Software Asset Management application, Microsoft 365 admin center, and other applications to configure Microsoft 365. This Guided Setup organizes the configuration activities into various categories so that you can see the list of tasks that need to be performed.

-   **[Optimize Microsoft 365 subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/microsoft-o365.md)**

    Optimize how to manage Microsoft 365 licensing with these enhancements:

    -   Auto removal of licenses from the Microsoft 365 admin center by detecting low usage and overlapping subscriptions.
    -   Expanded support for usage-based optimization such as Microsoft 365 E3 Teams and Microsoft 365 government plans.
-   **[Optimize Microsoft Dynamics 365 subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/integrating-with-microsoft365.md)**
    -   Receive recommendations to save costs by removing low-usage subscriptions for MRS applications.
    -   Receive guidance on cost-saving strategies while purchasing multiple base subscription licenses for various Microsoft Dynamics 365 applications. Using a combination of base and attach licenses can provide a more cost-effective solution.
-   **[Simplify the activation process for SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/request-saas-license-management.md)**

    Simplify your activation process by optimizing your SaaS subscriptions. You can activate just the SaaS applications that you want to manage.

-   **[SaaS security permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/create-integration-profile.md)**

    While integrating your SaaS applications, you can now grant the minimum permissions required to enable key use cases, such as downloading subscriptions, calculating activity, and reclaiming subscriptions.

-   **[Optimize subscriptions for SAP Ariba](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/integrate-with-ariba.md)**

    Gain visibility to the subscriptions and reclaim stale licenses by integrating your ServiceNow instance with the SAP Ariba application.

-   **[Configure and map users from SaaS portals to ServiceNow AI Platform with ease](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/map-user-data.md)**

    Determine your licensed users by mapping user subscriptions from SaaS applications to users in ServiceNow AI Platform.

-   **[Optimize CrowdStrike subscriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/integrate-with-crowdstrike.md)**

    Software Asset Management now includes support for CrowdStrike products with license metrics such as Sensor Subscription and Reserved Hourly Average Sensor. The introduction of a new license metric group, CrowdStrike, improves data coverage and reconciliation. By managing the entitlements for various CrowdStrike products, including CrowdStrike Falcon Endpoint Protection, CrowdStrike Falcon Discover, and others, you can get better tracking and compliance.

-   **[Manage onboarding of products to support the Software Asset Management \(SAM\) application through SAM Guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/playbook-entitlementsetup-workspace.md)**

    Get step-by-step guidance on the activities that you must perform to onboard SaaS and on-premises products. The guided setup helps you to create or associate success goals, configure product integrations, create software entitlements, or run reconciliation to get the most out of the Software Asset Management application.

-   **[Manage license compliance for Oracle Database and WebLogic Server deployed on Solaris Logical Domain \(LDOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/oracle-licensing-hard-partitioned-environments.md)**

    Support Oracle Database and WebLogic Server licensing for Per Processor and Named User Plus \(NUP\) license metrics that are deployed on the hard-partitioned Solaris LDOM infrastructure, also known as Oracle VM Server for SPARC.

-   **[Manage compliance for SAP S/4HANA Cloud Public Edition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/integrate-with-hana.md)**

    Gain visibility to software usage information and subscriptions by integrating your Software Asset Management application with the SAP S/4HANA Cloud Public Edition. This integration supports the Full User Equivalent \(FUE\) license metric that is used to grant licenses for SAP cloud applications.

-   **[Determine license compliance for Oracle products deployed on Nutanix virtualization technology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/software-recon-virt-tech.md)**

    License Oracle Database Server, Options, and WebLogic Server with deployments on the Nutanix virtualization technology.

-   **[Support for revenue-based license metrics for SAP engines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/sap-publisher-pack.md)**

    Gain the ability to maintain licenses for higher value, revenue-based SAP engine products.

-   **[Leverage machine learning normalization for software recognition in protected government environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/ml-learning-sam.md)**

    Extend machine learning normalization capabilities to Government Community Cloud \(GCC\) and National Security Cloud \(NSC\) environments.

-   **[Leverage machine learning spend detection in protected government environments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/software-spend-detection.md)**

    Extend Software Spend Detection capabilities to Government Community Cloud \(GCC\) and National Security Cloud \(NSC\) environments.

-   **[Optimize licensing for IBM Cloud Paks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/licensing-ibm-cloud-paks.md)**

    Use the IBM License Compliance for Software Asset Management application to track and manage licenses for your IBM Cloud Paks.

-   **[Expand end of life \(EOL\) reporting by creating parent-child relationships between software products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/create-parent-child-relationships-between-software-products.md)**

    View, define, or update the parent-child relationships between your software products. Use these relationships to enable your child products to inherit life-cycle dates from their associated parent products.

-   **[View the Export Classification Control Numbers \(ECCNs\) for your software products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/view-eccn-software-mappings.md)**

    View the ECCNs that are mapped to your software products. Use this information to identify the products that are subject to U.S. export control regulations so that you can maintain export compliance across your products.

-   **[Create and manage entitlements for your Microsoft 365 From SA and Add-on user subscription licenses \(USLs\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/creating-m365-from-sa-add-on-entitlements.md)**

    Create entitlements to track and manage the From SA and Add-on licensing terms for your Microsoft 365 subscriptions. Specify the details of each license, including the license type, license cost, and number of purchased rights. Use this information to determine your license compliance so that you can optimize your licensing costs.

-   **[Improve your compliance position with insights on how your software installations get licensed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/install-licenseusage-journey.md)**

    Evaluate the installation to license consumption percentages and devise strategies for improving your license usage. Track your installation to license journey by connecting software installations to the licenses consumed and identifying the statuses such as licensed or unlicensed.

-   **[Gain an understanding of how licenses get calculated for your software assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/explanation-rights-post-recon.md)**

    Learn how the Software Asset Management application calculates the number of licenses that are required for your software assets with the factors that impact this process.

-   **[Increase the coverage of product life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/calculated-lifecycles.md)**

    Expand the life-cycle date calculations to include the custom general availability \(GA\) dates. Additionally, support is also available for the End of Extended Support phase and the End of Support and End of Life phases.


## Changed in this release

-   **[Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/auto-reflow.md)**

    The Software Asset configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.

-   **[Publisher optimizations dashboard for Microsoft](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/pub-opt-microsoft.md)**

    The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.


## Activation information

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugins including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface.

In the ServiceNow AI Platform® Yokohama release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

For releases prior to Utah, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic user interface. For details about the plugins and how to request them, see [Request Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/t_RequSoftwareAssetMgmt.md).

To activate Next Experience, make sure that the **glide.ui.polaris.experience** system property in your instance is set to true.

Install the following Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences

## Accessibility information

-   **Accessibility improvements**

    Accessibility improvements were completed to create a configurable workspace that supports WCAG 2.1 Level AA conformance.

-   **Reflow**

    The configurable workspace supports reflow, which enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels. Page layouts are transformed into a vertical, stacked view automatically when users increase browser zoom to 400%. This enhancement helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations. Reflow can be turned off with a system property for instances, experiences, and pages. See [Reflow for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-user-interface/auto-reflow.md) for details.


## Related ServiceNow applications and features

-   **[Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/ham-landing-page.md)**

    The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your asset environment.

-   **[Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/enterprise-asset-management.md)**

    The ServiceNow® Enterprise Asset Management application enables you to manage the entire life cycle of your connected and non-connected enterprise assets. It provides a comprehensive end-to-end solution for maintaining enterprise assets, minimizing costly downtime, and maximizing enterprise asset usability.

-   **[Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/cloud-insights-landing-page.md)**

    The ServiceNow® Cloud Cost Management application enables you to analyze all costs that are associated with your cloud assets. You can use this information to optimize operations and reduce your cloud spend.

-   **[Contract Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/c_ContractManagement.md)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-asset-management/c_Procurement.md)**

    The ServiceNow® Procurement application helps you to create purchase orders and to obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/it-asset-management-rn-landing.md)

