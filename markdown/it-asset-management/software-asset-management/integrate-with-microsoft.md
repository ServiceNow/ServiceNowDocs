---
title: Integrating with Microsoft 365
description: Integrating the Software Asset Management application with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrating with Microsoft 365

Integrating the Software Asset Management application with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required?

</th><th>

Required user role in the Microsoft 365 application

</th><th>

Authentication scopes

</th><th>

Purpose

</th><th>

Least privilege?

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Mandatory

</td><td>

Application developer

</td><td>

-   User.Read.All
-   LicenseAssignment.Read.All

</td><td>

Permits the ServiceNow instance to read tenant, user, and license information to synchronize Microsoft 365 subscription data.

</td><td>

The user role and scope are read-only and limited to metadata access. It doesn't allow modifying users, groups, or licenses.

</td></tr><tr><td>

Pull user activity

</td><td>

Optional

</td><td>

-   Application developer
-   Power platform administrator

</td><td>

Reports.Read.All

</td><td>

-   Pulls usage of Microsoft 365 apps for Enterprise \(Microsoft Word, Excel, PowerPoint\), and other products such as Exchange Online, Teams, OneDrive, Power BI, SharePoint Online, Viva Engage \(previously Yammer\). Required for the Software Asset Management Professional application to generate optimization recommendations for low usage. For example, low usage for Microsoft 365 E1, Microsoft 365 E3-&gt; E1.
-   Pulls Power BI usage and activity metrics for license optimization. Required for the Software Asset Management Professional application to generate optimization recommendation for low usage. For example, Microsoft 365 E5-&gt; E3.

</td><td>

-   The role and scope are read-only and limited to metadata access. It doesn't allow modifying users, groups, or licenses.
-   For getting Power BI usage, this is the least privilege role. You should consider limiting membership to specific security groups and enabling read-only Power BI admin settings for the service principal.

</td></tr><tr><td>

Reclaim subscriptions

</td><td>

Optional

</td><td>

Application developer

</td><td>

-   GroupMember.ReadWrite.All
-   LicenseAssignment.ReadWrite.All

</td><td>

Permits the Software Asset Management Professional application to reclaim inactive licenses by removing Microsoft 365 subscriptions assigned to inactive users.

</td><td>

These permissions only enable modifying license assignments and don't provide tenant-wide admin capabilities.

</td></tr><tr><td>

Assign licenses

</td><td>

Optional

</td><td>

Application developer

</td><td>

-   GroupMember.ReadWrite.All
-   LicenseAssignment.Read.All
-   LicenseAssignment.ReadWrite.All
-   User.Read.All

</td><td>

Allows license assignment to users in the Microsoft 365 portal.

</td><td>

These permissions only enable Microsoft 365 license assignment.

</td></tr></tbody>
</table>## Setting up Microsoft 365 integration

Manage Microsoft 365 license compliance and optimization by performing the following steps:

-   **Prerequisites**

    Before you begin with Microsoft 365 integration, confirm that all prerequisites are met.

    1.  [Install Software Asset Management Professional for Microsoft](microsoft-publisher-pack.md)

        Install the Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\) plugin to access the Microsoft Publisher pack features in the Software Asset Management application.

    2.  [Install ITAM Health Check application](health-check-dboard.md)

        Install the ITAM Health Check application to get an overview of your Software Asset Management configurations and receive recommendations for correcting errors.

    3.  [Install Software Asset Management - SaaS License Management plugin](../task/request-saas-license-management.md)

        Install the Software Asset Management - SaaS License Management plugin \(com.sn\_sam\_saas\_int\) to create and manage integrations with your SaaS and Single Sign-On \(SSO\) applications. These integrations enable you to track license usage and reclaim unused licenses effectively.

    4.  Install Microsoft Entra ID Spoke

        Install the Microsoft Entra ID spoke \(formerly Azure AD spoke\) to enable automated integration with the Microsoft 365 Admin Center for license removal and other scenarios. An Integration Hub subscription is required for this spoke. For more information about Integration Hub, see Integration Hub.

    5.  [Receive latest updates from Software Asset Management Content Service](c_SAMContentService.md)

        Update your instance with new content twice every week on a scheduled basis through Software Asset Management Content Service. The Software Asset Management application provides automated content to simplify the normalization of software installations and subscriptions, offering enriched data such as lifecycle information, downgrade rights, and suite definitions. This data is essential for maintaining accurate license compliance and optimization.

    6.  [Create a success goal](../task/create-success-goals.md)

        Create a success goal to track the success of Microsoft 365 configuration setup on the Software Asset Management application.

-   **Software Asset Management configurations**

    Configure your Software Asset Management \(SAM\) application, which includes setting up user accounts, managing licenses, and confirming compliance with Microsoft's software usage policies.

    1.  [Register application on Microsoft Entra ID](../task/register-microsoft-app.md)

        Register an application on Microsoft Entra ID \(formerly Azure Active Directory\) that enables the retrieval of all subscriptions provisioned in the Microsoft 365 admin center.

    2.  [Configure Power BI usage to get usage information](../task/enable-service-principal-authentication-microsoft.md)

        Enable service principal authentication for Power BI read-only APIs to enable your application access to Power BI service content and APIs. This access helps optimize your Microsoft 365 subscriptions, such as downgrading subscriptions from Office 365 E5 to Office 365 E3 or removing Power BI low-usage subscriptions​.

    3.  [Prevent anonymous user information](../task/conf-update-micro-admin.md)

        By default, Microsoft hides the user names of subscribers in the Microsoft 365 Admin Center, preventing ServiceNow from accurately tracking Microsoft 365 license usage. To resolve this issue, disable this anonymization feature in the Microsoft 365 Admin Center.

    4.  [Set up a Microsoft 365 integration profile](../task/set-up-microsoft-office-365.md)

        Create a Microsoft 365 integration profile in the Software Asset Management application to import user subscription data, determine license compliance, and identify optimization opportunities. If you manage multiple tenants, create a separate integration profile for each.

    5.  [Configure the integration profile to get data for government customers](../task/update-o365-gov-plans.md)

        The ServiceNow AI Platform supports Microsoft 365 Government plans, offering all the features of Microsoft 365 services within a government-exclusive cloud. This setup helps organizations comply with the U.S. security and compliance standards.

    6.  [Configure the integration profile to get usage for Microsoft 365 Copilot, Visio Online, and Project Online](../task/upload-usage-reports-copilot-visio-project.md)

        Microsoft doesn't provide APIs to get usage directly for Microsoft 365 subscription products, such as Microsoft Visio, Microsoft Project, and Microsoft Copilot. However, you can download activity reports for these products from the Microsoft 365 admin center. Microsoft 365 administrators can download these reports and SAM Admin can attach them unmodified to the integration profile in the Software Asset Management application. The scheduled jobs within ServiceNow will then process these reports and identify reclamation candidates if the usage is low.

    7.  [Configure reclamation rules](../task/add-reclamation-rule-sub.md)

        The Software Asset Management application automatically provides base system reclamation rules when you create an integration profile for Microsoft 365. For more information, see [Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md).

    8.  [Configure user resolution rules](../task/map-user-data.md)

        Resolve or match the Microsoft 365 admin center user to the ServiceNow user \(sys\_user\) to determine the right license compliance and provide correct optimization recommendations.

        **Important:** Remember that sometimes licenses are assigned to non-human users such as email accounts. In these instances, you can skip the user resolution process as it isn’t required.

    9.  [Run scheduled jobs](../reference/m365-scheduled-jobs.md)

        The Microsoft 365 integration profile you created automatically gets subscription and usage information from the Microsoft 365 admin center on a scheduled basis. You can now run these jobs on demand and verify they’re completed successfully.

    10. [Set up software models and entitlements](../task/view-user-subscription-workspace.md)

        The Software Asset Management application integrates with the Microsoft 365 admin center to generate software models automatically based on assigned subscriptions. These models include suite components, downgrades, and lifecycle details to confirm compliance and optimize licensing. For these automatically created software models, remember to add your entitlements. If you have previously set up entitlements using Publisher Part Number, the software models from that setup are used in this integration, avoiding the creation of duplicate models.

        **Note:** Verify that no software models are created without Discovery Maps \(DMAPs\) and no entitlements are created without a Publisher Part Number \(PPN\) for a smoother implementation.

    11. [Set up Add on, From SA, and Step Up entitlements](creating-m365-from-sa-add-on-entitlements.md)

        Associate an Add-on license with a perpetual office legacy license with active Software Assurance. Microsoft 365 offers various subscription types such as Full USL, Add On USL, From SA USL, Step-up license, and reserved licenses. To learn more about these licenses, see [Supported Microsoft 365 license types](supported-microsoft-365-license-types.md).

    12. [Set up license reservations](creating-0365-reserve-entitlements.md)

        Create reserve entitlements for Microsoft online services to add licenses to your existing Microsoft 365 subscriptions.

-   **Software Asset Management configurations verification**

    Review and validate the Software Asset Management configurations to track and manage Microsoft 365 licenses and usage accurately.

    1.  [Verify the complete pull of all subscriptions](../task/ver-o365-info.md)

        Verify with the Microsoft 365 administrator that all subscription records have been successfully pulled.

    2.  [Run health check](../task/run-healthcheck.md)

        Run a health check on the Health check dashboard by selecting **Microsoft 365**, **SaaS**, and **General** to verify the Microsoft 365 configurations and review the findings for each suite.

    3.  [Verify the pull of all required software usage](o365-usage-activity.md)

        Verify if the Software Asset Management application has pulled the usage details for your Microsoft 365 subscribed users, which is required to identify the last activity and determine optimization opportunities.

    4.  [Create a success goal](../task/create-success-goals.md)

        Create a success goal to manage your Microsoft 365 licenses.

    5.  [Add Microsoft 365 and associated products to the published product list](../task/add-published-products.md)

        Add Microsoft 365 and associated products to the published product list to improve readability and declutter the Software Asset Workspace. Scale your SAM efforts strategically by evaluating progress based on resource needs, work quality, and configuration management.

    6.  [Run reconciliation](../task/run-recon-workspace.md)

        Run reconciliation on the Software asset overview page to verify that the licenses are consumed according to the Software Asset Management configurations. You must run reconciliation only for Microsoft as the publisher to verify Microsoft 365 license consumption.

    7.  [Check license position report](sam-license-position-report.md)

        Check your overall compliance positions for Microsoft 365 and associated products in the License Position Report.

    8.  [Act on unlicensed subscriptions](../reference/publisher-overview-microsoft.md)

        Identify and address the unlicensed Microsoft 365 subscriptions.

    9.  [Act on optimization recommendations](../reference/pub-opt-microsoft.md)

        Software Asset Management supports various optimization use cases, which you can view on the Software asset analytics page.

        ​


**Related topics**  


[Microsoft 365 integration](microsoft-o365.md)

[Automated license removal for Microsoft 365](m365-license-auto-removal.md)

[Software Asset Management software suites](software-suites.md)

[Evaluating software usage activity for Microsoft 365 subscriptions](o365-usage-activity.md)

