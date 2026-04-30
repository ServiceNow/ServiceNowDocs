---
title: Software Asset Management release notes
description: The ServiceNow Software Asset Management application systematically tracks, evaluates, and manages the cost, utilization, compliance, and optimization for software and SaaS applications. Software Asset Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 11
---

# Software Asset Management release notes

The ServiceNow® Software Asset Management application systematically tracks, evaluates, and manages the cost, utilization, compliance, and optimization for software and SaaS applications. Software Asset Management was enhanced and updated in the Zurich release.

## Software Asset Management highlights for the Zurich release

-   Streamline Adobe integration with the Software Asset Management application using the Adobe Guided Setup.
-   Integrate SAP HANA Database with the Software Asset Management application to monitor the memory allocations and licensing costs for your SAP HANA Database measurement.
-   Track and optimize licensing for Microsoft Server products on Microsoft Hyper-V virtualization technology by using the Software Asset Management publisher pack for Microsoft.
-   Track and optimize licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\) by using the Software Asset Management publisher pack for VMware.
-   Gain the flexibility to retrieve both subscription and consumption data at the organization level using the enhanced Docusign integration with the Software Asset Management application.

See [Software Asset Management](https://www.servicenow.com/docs/access?context=c_SoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US) for more information.

**Important:** Software Asset Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading Software Asset Management to Zurich

Starting from the Zurich release, the following workflows are migrated to Flow Designer as flows:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

When upgrading to the Zurich release, a fix script identifies whether the workflows were customized. If you haven't customized the workflows before the upgrade, the fix script deactivates the legacy workflows from the instance and deploys the Flow Designer flows on the instance post-upgrade. If you have customized the impacted workflows in the previous release, the fix script doesn’t deploy the Flow Designer flows on the instance post-upgrade. You can view and access the impacted workflows in the instance after the upgrade. However, the deprecated workflows are considered as custom code and ServiceNow doesn’t support those workflows.

Starting from the Zurich release, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is moved from the family release to the Software Asset Workspace store application. After upgrading to Zurich, the Software Asset Workspace plugin \(com.sn\_sam\_workspace\) is inactivated and the Software Asset Workspace store application \(sn\_sam\_workspace\) is enabled in the instance.

When upgrading to the Software Asset Management – SaaS License Management plugin \(sn\_sam\_saas\_int\) version 16.0.6 or later in the Zurich release, verify that the Software Asset Workspace store app \(sn\_sam\_workspace\) is updated to version 9.0.4.

## New in the Zurich release

-   **[Retrieve detailed subscription and consumption data across your entire organization with the Docusign integration](https://www.servicenow.com/docs/access?context=integrate-with-docusign-org&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Get insights into detailed subscription and consumption data across your organization by integrating Docusign with the Software Asset Management application. You can now access data at both the account and organization levels, giving you a centralized view of envelope activity and usage. This enhancement helps you better monitor Docusign consumption and optimize your license use.

-   **[Streamline the authentication process for Salesforce CRM integration](https://www.servicenow.com/docs/access?context=integrate-with-salesforce-crm&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Experience seamless data flow between the Software Asset Management application and Salesforce CRM. This updated feature supports the OAuth 2.0 Client Credentials grant type, eliminating manual authentication, and uses a secure machine-to-machine method to ensure efficient and uninterrupted data exchange.

-   **[Manage license compliance and optimization for Adobe Cloud services through Adobe Guided Setup](https://www.servicenow.com/docs/access?context=playbook-entitlementsetup-workspace&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Simplify setting up Adobe SaaS integration using the Adobe Guided Setup. The Guided Setup provides step-by-step guidance to set up the Adobe integration with the Software Asset Management application that supports license compliance and optimization for Adobe Cloud services.

-   **[Gain the flexibility to exclude certain SaaS subscriptions \(users and subscription identifiers\) from license calculations](https://www.servicenow.com/docs/access?context=subscription-exclusions&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Optimize your licensing costs with the ability to exclude certain low-value and high-volume subscriptions from ServiceNow's licensing calculations.

-   **[Optimize subscription licensing for specific SaaS offerings and editions via Single Sign-On \(SSO\) integrations](https://www.servicenow.com/docs/access?context=integrate-with-azure-ad&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Leverage the enhanced SSO integration that supports tracking subscriptions for specific SaaS offerings and editions. This update enables you to map SSO groups to software models for the specific offerings or editions and optimally license users based on their access.

-   **[Improve the security of Microsoft-related integrations with the enhanced support for application type permissions](https://www.servicenow.com/docs/access?context=microsoft-publisher-pack&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Enhance Microsoft SaaS integration security with the added support for application-type permissions. This feature includes SSO integration with Microsoft Entra ID, Microsoft Dynamics 365 and Power Apps, and Microsoft 365.

-   **[Monitor database memory for your SAP HANA Database with SAP HANA Database integration](https://www.servicenow.com/docs/access?context=add-sap-connection&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Manage memory allocations and licensing costs for your SAP HANA Database by integrating with the Software Asset Management application. Data populated through this approach helps in effective license reconciliation based on the peak memory usage of the SAP HANA Database.

-   **[Receive more frequent updates from the Software Asset Management Content Service](https://www.servicenow.com/docs/access?context=sam-content-updates&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Gain the benefit of twice-weekly shipments of the Content Library. This increase in the update frequency delivers faster Content Service to your ServiceNow instance.

-   **[Improve reclamation candidate selection for Microsoft 365 by considering mailbox and OneDrive sizes](https://www.servicenow.com/docs/access?context=o365-usage-activity&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Enhance the process of reclamation candidate selection for Microsoft 365 downgrade opportunities by considering three key factors: product usage, mailbox storage, and Microsoft OneDrive storage. Considering all these aspects enables more accurate and effective reclamation decisions.

-   **[Leverage the Flow Designer for reclamation workflow updates](https://www.servicenow.com/docs/access?context=reclaiming-software-sam&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Manage the reclamation process using the functionality migrated to the Flow Designer. The Flow Designer migration includes additional error handling features to enable a more intuitive and efficient way to manage the reclamation process.

-   **[Automatically identify and license Microsoft SQL Server high availability configurations](https://www.servicenow.com/docs/access?context=microsoft-sql-server-ha-configurations&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use the Software Asset Management publisher pack for Microsoft to automatically identify and license Microsoft SQL Server deployments in high availability configurations, such as Always On availability groups. This capability enables the Software Asset Management application to automatically classify each replica within a configuration as either active or passive, resulting in more accurate license compliance for Microsoft SQL Server.

-   **[Manage licensing for Microsoft Server products on Microsoft Hyper-V virtualization technology](https://www.servicenow.com/docs/access?context=microsoft-server-licensing-hyper-v-virtualization-technology&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Use the Software Asset Management publisher pack for Microsoft to track and manage licensing for Microsoft Server products, such as Microsoft Windows Server and Microsoft SQL Server, on Microsoft Hyper-V virtualization technology. Track license usage and determine your license compliance position so that you can better optimize your licensing costs.

-   **[Apply preferred licensing assignments to Microsoft software products that are deployed on clusters](https://www.servicenow.com/docs/access?context=apply-preferred-licensing-assignments-microsoft-clusters&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Define and apply preferred cluster licensing assignments to the Microsoft software products that are deployed on your hypervisor clusters. By using a preferred cluster licensing assignment, you can choose whether you want to license these software products at either the physical host layer or the virtual layer, helping you better align with your organization’s predetermined licensing strategy. Built-in validations help verify that your licensing strategy setup complies with the relevant Microsoft licensing requirements.

-   **[Manage the life-cycle risks of a software product based on its add-on or optional support](https://www.servicenow.com/docs/access?context=software-models-and-entitlements&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Gain insight into the extended life cycle of a software product when you purchase an add-on or optional support. Each time you indicate that a software product has an add-on or optional support, the Software Asset Management application extends the life-cycle dates of that product, as defined by the add-on or optional support. Use these extended life-cycle dates to identify and plan for your end-of-life \(EOL\) risks.

-   **[Manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\)](https://www.servicenow.com/docs/access?context=vmware-publisher-pack&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Following the updates to VMware's licensing policy, use the Software Asset Management publisher pack for VMware to track and manage licensing for VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\), which are updated suite-based product offerings for VMware vSphere. With these updated product offerings, you can measure compliance and optimize licensing for multiple VMware vSphere products under a single subscription.

    In addition, the publisher pack can account for the number of cores and the licensing minimums when calculating licensing requirements for VVS and VVEP.

-   **[Gain expanded insight into the content library information through content dashboard analytics](https://www.servicenow.com/docs/access?context=content-search-portal&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Gain in-depth information related to various content tables and trends in content change from the enhanced Content Library portal. The introduction of numeric widgets, line graphs, bar charts, and content-specific tabs provides complete visibility to content shipped and analyze content coverage. The expanded search feature with additional filter options lets you view the records for a particular period or release.

-   **[Efficiently manage user allocations in bulk using group allocations](https://www.servicenow.com/docs/access?context=group-user-allocation&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Allocate licenses to user groups instead of individual users for a software entitlement using the group allocation feature for the user-based licensing metric software. Group allocation feature enables Software Asset Management managers to streamline and manage the license allocation process efficiently. User allocation is created for the group members based on the availability of unallocated licenses. Any changes made to the composition of the user group automatically updates the license allocation.

-   **[Use the enhanced License Usage view for expanded insights on your license compliance](https://www.servicenow.com/docs/access?context=sam-workspace-workbench&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Conduct a deeper analysis of your publisher compliance using both the list view and the card view in the License usage view. You can save and share the data by exporting the list view in multiple file formats. View integrated health check results, license usage analysis, and learn why a retired or stale CI is using a license. Furthermore, to avoid clutter on the Publisher details page, software model results are only shown for software models that have entitlements.

-   **[Seamlessly continue with the entitlement import process even when PPNs are missing](https://www.servicenow.com/docs/access?context=import-entitlements-workspace&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Continue with the entitlement import process by automatically creating software models when both PPNs and software models are missing. Software models are automatically generated based on the publisher and product details.

-   **[Use flexible reporting capabilities to gain deeper insights into your Effective License Position \(ELP\)](https://www.servicenow.com/docs/access?context=elp-grouping-byconsumption&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    Improve analysis of your ELP with flexible reporting on reconciliation results. Reports can be run on existing reconciliation groups or customer-defined groups, and the report data can be organized by unique combinations of group, subgroup, publisher, product, version, and edition. For each combination, the average cost is calculated and provides the total number of required licenses. The results are presented in a structured format for easy analysis and reporting.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **[Group Allocations tab on the software model form](https://www.servicenow.com/docs/access?context=software-model-fields&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US#section_rcp_zm4_hfc)**

    The Group Allocations tab on the software model form lists all the group allocation records created for allocating an assignment group to the software entitlement.

-   **[Group column on the User Allocations list](https://www.servicenow.com/docs/access?context=software-entitlement-fields&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US#section_kf5_lhp_drb)**

    The Group column in the User Allocations list indicates whether the user allocation is done individually or as part of a group assignment to the software entitlement. The group's name is populated when the user allocation is automatically created with the group assignment. An empty value is populated when the user allocation record is individually created.

-   **[Resume reclaim button on the Removal Candidate form](https://www.servicenow.com/docs/access?context=add-sw-removal-workspace&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The **Resume reclaim** button is available when the state of the reclamation candidate is **Attention Required**. When selected, the **Resume reclaim** button runs a verification to check the completeness of data for processing.


## Changed in this release

-   **[Publisher optimizations for Microsoft](https://www.servicenow.com/docs/access?context=pub-opt-microsoft&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Publisher Optimizations dashboard for Microsoft has been updated to support additional subscriptions.

-   **[Publisher optimizations for SAP](https://www.servicenow.com/docs/access?context=pub-opt-sap&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The Publisher Optimizations dashboard for SAP has been updated with a report on SAP HANA Database monthly peak usage.


## Deprecations

Starting from the Zurich release, the following workflows are being prepared for future deprecation:

-   Reclamation workflow
-   Procurement Process Flow - Auto allocation enabled

## Activation information

Software Asset Management is available with activation of the Activate all Software Asset Management Professional plugin, including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\). Activating this plugin automatically activates the Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\) and the Software Asset Workspace store app \(sn\_sam\_workspace\). After the new plugin is activated, you can't access the classic user interface.

In the ServiceNow AI Platform® Zurich release, there's limited support for the Software Asset Management classic user interface. While it remains active in your instance, including when you upgrade to a new ServiceNow AI Platform® release, you can move to the new workspace for an intuitive and personalized experience.

For releases before Utah, if you activated the older Software Asset Management Professional plugin \(com.sn\_samp\_master\), the Software Asset Workspace is available with activation of the Software Asset Workspace plugin \(com.sn\_sam\_workspace\). After the Workspace plugin is activated, you can't revert to the classic user interface. For details about the plugins and how to request them, see [Request Software Asset Management](https://www.servicenow.com/docs/access?context=t_RequSoftwareAssetMgmt&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

Install the following Software Asset Management applications by requesting them from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/store) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   Software Asset Management - SaaS License Management
-   Data Collection for Oracle Global Licensing and Advisory Services \(GLAS\)
-   IBM License Compliance for Software Asset Management
-   ITAM Health Check
-   Software Asset Management Guided Experiences
-   Software Asset Workspace

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Hardware Asset Management](https://www.servicenow.com/docs/access?context=ham-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Hardware Asset Management application provides advanced workflow, automation, and mobile capabilities to track and manage your technology asset environment.

-   **[Enterprise Asset Management](https://www.servicenow.com/docs/access?context=enterprise-asset-management&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Enterprise Asset Management application manages the entire life cycle of your enterprise's connected and non-connected assets, which enables you to maintain and maximize the life of your assets while minimizing any costly downtime.

-   **[Cloud Cost Management](https://www.servicenow.com/docs/access?context=cloud-insights-landing-page&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Cloud Cost Management application enables you to analyze all costs that are associated with your cloud assets. You can use this information to optimize operations and reduce your cloud spend.

-   **[Contract Management](https://www.servicenow.com/docs/access?context=c_ContractManagement&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Contract Management application enables you to track and manage your contracts.

-   **[Procurement](https://www.servicenow.com/docs/access?context=c_Procurement&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US)**

    The ServiceNow® Procurement application helps you create purchase orders and obtain items for fulfilling service catalog requests.


**Parent Topic:**[IT Asset Management release notes](it-asset-management-rn-landing.md)

