---
title: Software Asset Management release notes
description: The ServiceNow Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. See the following sections for release notes by version.The Brazil Early Availability release introduces streamlined onboarding through the Product Hub and Configuration Console, along with license management for SAP S/4HANA Cloud, Private Edition. It also delivers enhanced publisher integrations for Smartsheet, and Microsoft Entra ID, additional predefined license metrics, enhanced deduplication feature, and automated suite inference.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/software-asset-management-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Asset Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Software Asset Management release notes

The ServiceNow® Software Asset Management application enables you to systematically track, evaluate, and manage the cost, utilization, compliance, and optimization for software and SaaS applications. See the following sections for release notes by version.

## About Software Asset Management

-   Streamline and automate the software asset management tasks using ServiceNow Otto for Software Asset Management \(SAM\)
-   Automatically normalize your software assets with updates from the Software Asset Management content service.
-   Track and manage rights for your software products by creating or importing software entitlements.
-   Integrate with SaaS applications and SSO providers to track your SaaS subscription usage.
-   Track and manage financial transaction data for your software products to optimize your software spend.

See [Software Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_SoftwareAssetMgmt.md) for more information.

## Activation and other requirements

-   **Activation information**

    Software Asset Management is available with activation of the following plugins:

    -   **[Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/t_RequSoftwareAssetMgmt.md)**

        Activating this plugin automatically activates the following:

        -   Activate all Software Asset Management Professional plugin \(com.sn\_samp\_master\)
        -   Software Asset Workspace store application \(sn\_sam\_workspace\)
        After you activate the Activate all Software Asset Management Professional plugin including the Software Asset Workspace plugin \(com.sn\_samp\_master\_ws\), you can't access the Software Asset Management Core UI.

    -   **[Basic Software Asset Management \(com.snc.sams\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/t_SAMSetupSAMF.md)**

        To access the foundation capabilities of Software Asset Management, activate the Basic Software Asset Management plugin. After you activate this plugin, activate the Software Asset Workspace store application \(sn\_sam\_workspace\) to complete the setup.


**Parent Topic:**[Asset Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-asset-management-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release introduces streamlined onboarding through the Product Hub and Configuration Console, along with license management for SAP S/4HANA Cloud, Private Edition. It also delivers enhanced publisher integrations for Smartsheet, and Microsoft Entra ID, additional predefined license metrics, enhanced deduplication feature, and automated suite inference.

### What's new

-   **[Install the Software Asset Management application from the Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-product-hub.md)**

    Streamline onboarding by installing Software Asset Management and its dependent applications from the Product Hub. The Product Hub is the central location to view and manage all applications included in your Software Asset Management subscription. Access product documentation, videos, release notes, and community links from the same place.

-   **[Set up the Software Asset Management application using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/config-console-sam.md)**

    Reduce the time it takes to set up Software Asset Management after installing it from the Product Hub by using the Configuration Console, a one-stop shop for setup. Use predefined settings to smoothen the onboarding journey and configure software foundations, properties, AI skills, governance, team management, and data management from a single location. You can also use the AI conversational interface to configure groups, users, and Content Service setup.

-   **[Manage licenses for SAP S/4HANA Cloud, Private Edition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sap-publisher-pack.md)**

    Establish an accurate license position for your SAP S/4HANA Cloud, Private Edition delivered through RISE with SAP, without manually tracking user classifications or engine and database consumption. Collect usage data from your private cloud systems and calculate your Full Usage Equivalent \(FUE\) license position automatically with the Software Asset Management publisher pack for SAP. Reduce audit exposure and avoid unexpected compliance costs by measuring private cloud compliance alongside your existing on-premises SAP systems.

-   **[Manage all reclamation candidates from a consolidated Reclamation tab on the License usage view in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-workspace-workbench.md)**

    Gain insights with a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows. Drill down from the **Reclamation** tab into individual removal candidates for each publisher or integration, without switching between separate reclamation views. This enhancement gives your asset team a complete picture of reclamation opportunities across your software estate.

-   **[Improved license compliance reporting for Smartsheet SaaS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/integrate-with-smartsheet.md)**

    Improve visibility and compliance reporting of Smartsheet user licenses using the assigned seat type in the Smartsheet portal. The integration now retrieves users by seat type and creates subscription records for each category independently.

    **Note:** The updated Smartsheet license reporting is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 18.0.3.

-   **[Use expanded Microsoft Entra ID Single Sign-On \(SSO\) license reclamation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-sso-integration.md)**

    Expand your Microsoft Entra ID SSO integrations to improve identification of inactive users and surface group-assigned users as reclamation candidates. Update SSO subscription reclamation logic to improve stale subscription detection.

    **Note:** The expanded Microsoft Entra ID capability is supported starting from Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) version 18.0.3.

-   **[Automate suite license inference for improved compliance reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-suites-inference.md)**

    Enable automatic suite inference to calculate the optimal suite license for each software installation based on your actual footprint and entitlements. This feature reduces manual configuration required for the suite on the software model and improves compliance reporting.

-   **[Improve reporting of software installation inventory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/deduplication-rule.md)**

    Improve reporting of your software installation inventory by deploying rules that automatically consolidate duplicate product installations across your devices.

-   **[Onboard entitlements faster with additional predefined license metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_SAMLicenseMetrics.md)**

    Reduce entitlement onboarding time by using additional predefined license metrics for supported publishers. These predefined license metrics help you track consumption, verify compliance, and reconcile deployments against entitlements. Review tier ranges and calculation factors on the new **License Metric Tier** tab of the Software entitlement page.

-   **[Analyze software spend transactions with AI in the Software Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-detection-ai-enhancements.md)**

    Reduce manual software spend classification with AI-powered detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.


### What's changed

-   **[Gain clearer visibility into SAP HANA user license types with the renamed License classification column](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/view-sapusers-workspace.md)**

    The **Named user type** column is renamed to **License classification** in the SAP System Users \[samp\_sap\_system\_user\] table for improved visibility into SAP HANA user license types and entitlement reconciliation. The column appears on the SAP System Users related list of software models created for SAP S/4HANA products.

-   **[Manage SAP S/4HANA Cloud, Public Edition entitlements with the renamed User Subscription metric](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/c_SAMLicenseMetrics.md)**

    The **Full Usage Equivalent** license metric for SAP S/4HANA Cloud, Public Edition is renamed to **User Subscription**, aligning with SAP's updated naming for this edition. The Full Usage Equivalent metric continues to apply to SAP S/4HANA Cloud, Private Edition. The calculation logic is unchanged.

-   **[Manage software models with clearer licensing terminology](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-model-fields.md)**

    Understand licensing scope at a glance from the renamed column in the Software Model \[cmdb\_software\_product\_model\] table. The **License all installs accessed by clients** column is renamed to **License all installs**. The new name reflects that all installs meeting the software model's conditions are licensed, not only those tied to client access records.

-   **[Removal candidates tab replaced with the Reclamation tab in the License usage view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/sam-workspace-workbench.md)**

    The **Reclamation** tab in the License usage view on the Software Asset Workspace presents a consolidated view of reclamation candidates across all publishers, SaaS integrations, installed software, and reconciliation flows.

-   **[Software Spend Detection Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/spend-detection-sam-workspace.md)**

    The Software Spend Detection feature is no longer available in the Core UI. Software Spend Detection is now accessible from the Software Asset Workspace under License operations. Existing imports and spend transactions created in the Core UI are now accessible from the Software Asset Workspace.


### Plugin information

-   **New plugins**

    SAM Admin Experience - v1.0 \(sn\_samp\_admin\): Provides access to the Configuration Console for configuring the Software Asset Management application.


