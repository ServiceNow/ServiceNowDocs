---
title: Integrating with Adobe Cloud
description: Integrate your Software Asset Management application with Adobe Cloud services to track your software subscriptions and to determine your license compliance.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrating with Adobe Cloud

Integrate your Software Asset Management application with Adobe Cloud services to track your software subscriptions and to determine your license compliance.

The Adobe Cloud integration supports the following Adobe Cloud services:

-   Adobe Creative Cloud
-   Adobe Experience Cloud
-   Adobe Document Cloud

**Note:** You can create an Adobe Cloud integration only if you’re using the Adobe Creative Cloud for Enterprise subscription plan. If you’re using any other subscription plan, such as Adobe Creative Cloud for Teams, Education, or Individuals, you can’t create an integration.

Integrate your Adobe subscriptions with Software Asset Management for compliance reporting using Adobe authentication. For more information about Adobe authentication integrations and certificates, see the [Adobe Authentication Guide](https://developer.adobe.com/developer-console/docs/guides/authentication/).

You can integrate your ServiceNow® instance with Adobe Cloud services using the [OAuth Server to Server credential](integrate-adobe-cloud-oauth.md) authentication method.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Adobe Cloud application|Authentication scopes|
|-------|-------------------------------------------------|---------------------|
|Download subscriptions|Administrator|None|

## Setting up Adobe Cloud integration

Manage Adobe Cloud license compliance and optimization by performing the following steps:

-   **Prerequisites**

    Before you begin with Adobe Cloud integration, confirm that all prerequisites are met.

    1.  [Install Software Asset Management Professional for Adobe](adobe-publisher-pack.md)

        Install the Software Asset Management Professional for Adobe \(com.sn\_samp\_adobe\) plugin to access the Adobe Publisher Pack features in the Software Asset Management application.

    2.  [Install Software Asset Management - SaaS License Management plugin](../task/request-saas-license-management.md)

        Install the Software Asset Management - SaaS License Management \(com.sn\_sam\_saas\_int\) plugin to create and manage integrations with your SaaS and Single Sign-On \(SSO\) applications. These integrations enable you to track license usage and reclaim unused licenses effectively.

    3.  [Verify content updates for Software Asset Management](c_SAMContentService.md)

        The content library on your instance is updated regularly through the Software Asset Management Content Service. The Software Asset Management application provides automated content to simplify software normalization, offering data such as life cycle information, downgrade rights, and suite definitions. This data is essential for accurate license compliance and optimization.

    4.  [Create a success goal](../task/create-success-goals.md)

        Create a success goal to track the success of Adobe Cloud configuration setup on the Software Asset Management application.

    5.  [​ Set up OAuth on Adobe Cloud](../task/create-adobe-cloud-oauth.md)

        Set up OAuth Server-to-Server credentials on the Adobe Cloud services portal before creating an Adobe Cloud integration profile on the Software Asset Management application.

-   **Software Asset Management configurations**

    Configure your Software Asset Management application, which includes setting up user accounts, managing licenses, and confirming compliance with Adobe's software usage policies.

    1.  [​ Set up Adobe Cloud integration profile](../task/create-adobe-cloud-integration-oauth.md)

        Create an Adobe Cloud integration profile in the Software Asset Management application to import user subscription data, determine license compliance, and identify optimization opportunities. If you manage multiple tenants, create a separate integration profile for each.

    2.  [Configure user resolution rules](../task/map-user-data.md)

        Resolve or match the Adobe Cloud user to the ServiceNow user \(sys\_user\) to determine the suitable license compliance and provide correct optimization recommendations.

        **Note:** If the licenses are assigned to non-human users, such as email accounts, the user resolution process is optional for you.​​

    3.  [Review and configure reclamation rules](../reference/reclamation-rules-adobe.md)

        The Software Asset Management application automatically provides base system reclamation rules when you create an integration profile for Adobe Cloud. You can customize these rules based on your specific activity thresholds, such as 15, 30, 90, or 180 days. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    4.  [Pull subscription data](../reference/adobe-scheduled-jobs.md)

        After the Adobe Cloud integration is complete, the subscription data is pulled into the Software Asset Management application when the SAM - Import Adobe User Subscriptions scheduled job runs. If you want to run this job on demand for pulling the latest subscription data, contact the ServiceNow administrator.

    5.  [Set up software models](customppn-swap.md)

        The Software Asset Management application integrates with Adobe Cloud to automatically generate software models based on assigned subscriptions. These models include suite components, downgrades, and life cycle details to confirm compliance and optimize licensing.

        **Important:** You must verify that no software models are created without a Discovery Map \(DMAP\) to confirm inclusion of all required details.

        Alternatively, you can create software models manually for any unknown identifiers. For more information, see [Create a software model in the Software Asset Workspace](../task/create-swmodels-workspace.md).

    6.  [Set up entitlements](../task/create-entitlements-workspace.md)

        Add your entitlements for the software models created automatically or manually in the previous step. If you have already set up entitlements using a Publisher Part Number \(PPN\), those software models are used in this integration to avoid duplicates.

        **Important:** To achieve a cleaner implementation, you must verify that no software entitlements are created without a PPN.

        ​

-   **Software Asset Management configurations verification**

    Review and validate the Software Asset Management configurations to track and manage Adobe Cloud licenses and usage accurately.

    1.  [Verify the complete pull of all subscriptions](../task/verify-adobe-info.md)

        Verify with the Adobe Cloud administrator that all subscription records have been pulled successfully. You must verify that the subscription records are complete and the subscription account details are accurate.

    2.  [Run health check](../task/run-healthcheck.md)

        Run a health check on the Health check dashboard by selecting **SaaS** and **General** to verify the Adobe configurations and review the findings for each suite.

    3.  [Verify the pull of all required software usage](../task/view-sw-usage-workspace.md)

        Verify if the Software Asset Management application has pulled the usage details from discovery sources such as SCCM. Usage details, such as last activity, is required to identify user subscriptions with low usage and determine optimization opportunities. When the subscription data is pulled, the SAM - Optimize Adobe Subscriptions scheduled job runs monthly to optimize the Adobe Creative Cloud subscriptions.

    4.  [Create a success goal](../task/create-success-goals.md)

        Create a success goal to manage your Adobe Cloud subscription and compliance.

    5.  [Run reconciliation](../task/run-recon-workspace.md)

        Run reconciliation on the Software asset overview page to verify that the licenses are consumed according to the Software Asset Management configurations. Reconciliation runs automatically each week, but you can also trigger it manually as needed. For quicker results, run reconciliation with Adobe as the publisher to verify the Adobe Cloud license consumption.

    6.  [Check license position report](sam-license-position-report.md)

        Check your overall compliance positions for Adobe Cloud and associated products in the License Position Report. For Adobe-specific license position, select Adobe Systems as the publisher.​

    7.  [Act on unlicensed subscriptions](../reference/publisher-overview-adobe.md)

        Identify and address the unlicensed Adobe Cloud subscriptions.

    8.  [Act on optimization recommendations](../reference/pub-opt-adobe.md)

        Software Asset Management supports various optimization use cases, which you can view on the Software asset analytics page. For Adobe-specific optimization, select Adobe as the publisher.

        ​


