---
title: SaaS License Management
description: SaaS License Management helps organizations track and control cloud-based applications and service subscriptions as part of Software Asset Management \(SAM\). It promotes ownership, visibility, agility, and accountability, enabling better cost control and efficient use of resources.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-12-04"
reading_time_minutes: 5
breadcrumb: [Software Asset Management, IT Asset Management]
---

# SaaS License Management

SaaS License Management helps organizations track and control cloud-based applications and service subscriptions as part of Software Asset Management \(SAM\). It promotes ownership, visibility, agility, and accountability, enabling better cost control and efficient use of resources.

## SaaS subscription models

SaaS applications and services are typically subscribed to on a per-user basis. They generally fall into two categories:

-   **Hybrid SaaS**

    Hybrid SaaS combines on-premise installations with cloud-based subscriptions. It’s commonly used by organizations that require offline access to certain applications while also using cloud features for collaboration. This model is also suitable for businesses with compliance requirements that mandate local installations. For example, a Microsoft 365 subscription enables you to access cloud services and install applications like Microsoft Excel on their devices. SAM supports the following Hybrid SaaS integrations:

    -   [Adobe Cloud integration](adobe-cloud-integration.md)
    -   [Microsoft 365 integration](microsoft-o365.md)
-   **Direct SaaS**

    Direct SaaS refers to applications where all data and functionality are hosted in the cloud and accessed through the internet. You typically log in via a web browser or a dedicated app without installing software locally. For example, a Miro subscriber accesses the application entirely online. This model is common for organizations that prioritize ease of deployment and minimal maintenance, and for teams that work remotely or across multiple locations.

    **Important:** This topic focuses on the Direct SaaS category. It explains how to get started, identifies areas where Direct SaaS can be applied, and outlines ways to use available solutions and workflows effectively.


## Managing Direct SaaS with the SaaS License Management application

Managing Direct SaaS applications can vary based on organizational needs. The best approach depends on factors such as the level of integration required, available APIs, and whether Single Sign-On \(SSO\) is in place.

-   Use [Direct Integration](create-integration-profile.md) when you need deep usage insights and automated license management for supported vendors.
-   Use [SaaS License Connections](saas-license-connections.md) when you want flexibility to connect any SaaS app with a public API and prefer a low-code setup.
-   Use [SSO Integration](saas-sso-integration.md) when you need visibility into apps connected through an SSO provider and want to address SaaS sprawl.

For more information about installing SaaS License Management, see [Request SaaS License Management](../task/request-saas-license-management.md).

![Flowchart to guide through SaaS license management](../image/saas-license-management.png)

<table id="table_mz1_csf_jhc"><thead><tr><th>

Option

</th><th>

Key features

</th><th>

Benefits

</th></tr></thead><tbody><tr><td>

[Direct Integration](create-integration-profile.md)

</td><td>

-   Base system or default direct integrations
-   Automated license reclamation

</td><td>

-   Provides detailed usage insights
-   Automates license management
-   Reduces manual effort

</td></tr><tr><td>

[SaaS License Connections](saas-license-connections.md)

</td><td>

-   Connect to any SaaS application with a public API
-   Low-code framework using ServiceNow® via [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) and Workflow Studio

</td><td>

-   Flexible for any SaaS application
-   Customizable workflows

</td></tr><tr><td>

[SSO Integration](saas-sso-integration.md)

</td><td>

-   Connect via SSO providers such as Okta and Microsoft Entra ID.
-   Download the list of applications or users
-   Identify overlapping software and rationalize applications

</td><td>

-   Helps tackle SaaS sprawl
-   Improves cost control
-   Simplifies user access management

</td></tr></tbody>
</table>-   **[Request SaaS License Management](../task/request-saas-license-management.md)**  
Request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) so that you can create and manage integrations with your SaaS and Single Sign-on \(SSO\) applications. You can use these integrations to track license usage and to reclaim unused licenses.
-   **[SaaS Overview dashboard](saas-overview-dashboard.md)**  
Optimize how much your organization spends on SaaS and SSO licensing by analyzing the subscription usage, cost, and compliance of your SaaS applications and SSO providers using the SaaS Overview dashboard.
-   **[Playbook for SaaS integrations](playbook-saas-integrations.md)**  
The SaaS playbook provides step-by-step guidance for integrating an SaaS application. It takes you in a phased way through each stage of the integration process, from initiation to completion.
-   **[Integrate with SaaS applications](create-integration-profile.md)**  
Create an integration profile to view software usage information and optimize stale licenses.
-   **[Integrate with SSO providers](saas-sso-integration.md)**  
Integrate with a Single Sign-On \(SSO\) provider to view software usage for all connected SSO applications.
-   **[Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md)**  
Create a child alias to set up multiple integration profiles with unique connections and manage different configurations for each integration profile.
-   **[Viewing your SaaS and SSO subscriptions](usage-summary-saas.md)**  
View a list of all subscriptions for your SaaS and Single Sign-On \(SSO\) applications.
-   **[SaaS License Connections](saas-license-connections.md)**  
Creating a custom integration helps you connect the Software Asset Management application with a SaaS application that doesn't have an existing integration in SaaS License Management.
-   **[Review a software reclamation rule](../task/add-reclamation-rule-sub.md)**  
Use reclamation rules to cancel user subscriptions that have limited to no activity.
-   **[Reclaiming user subscriptions](reclaiming-user-subscriptions-saas.md)**  
You can reclaim unused SaaS and SSO subscriptions to reduce your total software costs.
-   **[Disconnect SSO apps](../task/disconnect-azure-ad-apps.md)**  
Disconnect an SSO application to stop viewing subscription information for the app, or before creating a direct integration for the app.
-   **[Delete an integration profile](delete-saas-integration.md)**  
If your company stops using a SaaS application or SSO provider, you can delete the integration profile.
-   **[Subscription identifiers for SaaS and SSO applications](subscription-identifiers.md#)**  
Use the SaaS License Management application to view, manage, and resolve subscription identifiers for your SaaS and SSO applications.

**Parent Topic:**[Software Asset Management](c_SoftwareAssetMgmt.md)

