---
title: Microsoft 365 integration
description: Create an integration with Microsoft 365 to download subscription information that is compared with software installations for compliance.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Microsoft 365 integration

Create an integration with Microsoft 365 to download subscription information that is compared with software installations for compliance.

Microsoft 365 is a suite of software products that includes a range of subscription software and services such as Microsoft Office 365, Windows, and Enterprise Mobility and Security \(EMS\). Microsoft 365 and EMS include many other products and services within them​.

Microsoft 365 admin center includes many other products that you can purchase and activate. However, some of these products don't come with the Microsoft 365 subscription, such as Dynamics 365 and Visio Online.

The following are some of the products and services that are available with the Microsoft 365 subscription:

-   Microsoft 365
-   Microsoft Exchange Online
-   Enterprise Mobility Suite
-   Microsoft Office 365
-   Microsoft SharePoint Online
-   Microsoft Entra ID
-   Microsoft Power BI
-   Microsoft OneDrive
-   Microsoft Teams
-   Windows
-   Microsoft Intune

SAM managers can use the Microsoft 365 integration to do the following:

-   Get user subscription information for all the Microsoft 365 plans purchased on the Microsoft 365 admin center, such as Microsoft Office 365, Microsoft 365, and so on.
-   Determine license compliance of Microsoft 365 subscriptions by reconciling user subscription, entitlement, and software installations.
-   View active, inactive, and unassigned subscriptions by their last activity date.
-   Get user activity for individual Microsoft Office 365 software products within Microsoft 365 subscriptions. For more information, see [Evaluating software usage activity for Microsoft 365 subscriptions](integrate-with-microsoft.md#).
-   Get user activity with device-specific activation count details from the Microsoft 365 admin portal that helps in identifying users who have activated their Microsoft subscriptions on at least one device. The activation count also helps SAM managers accurately determine the total number of activations across both desktops and devices.
-   Get automated optimization recommendations and workflows for Microsoft 365 subscriptions.
-   Determine potential savings while acting on the recommendation.
-   Find your available licenses from the subscription details for the Microsoft 365 portal in the Optimization and savings dashboard in the Software Asset Workspace. For more information, see [Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md).

Access the content related to software subscriptions by navigating to **SaaS License** &gt; **Overview**.

-   **Office 365 &amp; Adobe Cloud** in the Software asset analytics view of [SaaS overview dashboard in workspace](../reference/saas-dashboard-workspace.md).
-   **Software Models** lists software model records for subscription products.
-   **All User Subscriptions** lists all subscription records for subscription products \(also accessible through the **Software Asset** &gt; **Discovery** &gt; **Software Subscriptions** navigation menu\).
-   **Create New Profile** creates a Microsoft 365 subscription profile.
-   **All Integration Profiles** lists Microsoft 365 subscription profile records.

Software Asset Management uses the subscription information to determine license compliance and perform optimization. View license compliance on the [License usage view](sam-workspace-workbench.md) and optimization on the [Optimization and Savings dashboard](../reference/optimization-dashboard-workspace.md).

The **SAM - Import M365 User Subscriptions** scheduled job runs once every week to obtain subscription information from Software Asset Management.

For setting up Microsoft 365 integration to determine license compliance and optimization, follow the steps in [Integrating with Microsoft 365](integrate-with-microsoft.md#).

**Note:** You must activate the add-on Microsoft content pack \(com.snc.samp.microsoft\) [plugin](../task/t_RequSoftwareAssetMgmt.md) to view Microsoft 365 compliance reporting on the [Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic](sam-saas-subscription-dash.md) and [SaaS overview dashboard in workspace](../reference/saas-dashboard-workspace.md).

-   **[Integrating with Microsoft 365](integrate-with-microsoft.md#)**  
Integrating your ServiceNow instance with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.
-   **[Creating reserve entitlements for Microsoft online services](creating-0365-reserve-entitlements.md)**  
You can create reserve entitlements for Microsoft online services to add licenses to your existing Microsoft 365 subscriptions. You can pay for the new licenses during your true-up process.

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md)

