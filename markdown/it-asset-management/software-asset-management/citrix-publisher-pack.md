---
title: Software Asset Management publisher pack for Citrix
description: Use the Citrix publisher pack for the optimization and reconciliation of your Citrix products. You can track licensing positions for your Citrix users and devices so that you can determine your license compliance.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for Citrix

Use the Citrix publisher pack for the optimization and reconciliation of your Citrix products. You can track licensing positions for your Citrix users and devices so that you can determine your license compliance.

To use the Citrix publisher pack, activate the Software Asset Management Professional for Citrix plugin \(com.sn\_samp\_citrix\). For details, see [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md).

The Citrix publisher pack supports Virtual Applications products \(formerly XenApp\) and Virtual Desktop products \(formerly XenDesktop\). Using this publisher pack, you can manage licenses and determine the license compliance for your Citrix products. You can gain visibility into the third-party applications that are delivered through your virtual applications and desktops. You can also gain visibility into the users that may potentially access those applications.

Use the ServiceNow® Discovery application to collect data from Citrix. The license consumption data for your Citrix products is collected from the Citrix License Server.

Discovery uses OData APIs to identify the third-party applications that are delivered through your Citrix farm from the Citrix Delivery Controller. Use this information to create software installation records and track license usage for these applications. To identify these applications, admins must create a [Discovery schedule](https://www.servicenow.com/docs/access?context=t_CreateADiscoverySchedule&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) to run on the Citrix discovery pattern. See [Citrix License Server and Delivery Controller discovery](https://www.servicenow.com/docs/access?context=citrix-lic-server-deliv-controller&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US) for more details on the Citrix discovery pattern and tables.

## Citrix licensing models

The Citrix publisher pack supports the following Citrix licensing models:

-   **Concurrent licensing model**

    Concurrent licenses are used only during active sessions. When a user begins a session, the application or desktop checks out a license for the device that is running the session. When the session disconnects or ends, the application or desktop checks the license back in to make the license available to other users and devices. Concurrent licenses enable either one connection to a virtual desktop or unlimited applications for any user or device. License consumption is based on the number of licenses being used.

-   **User/Device licensing model**

    User/Device licensing model: User/Device licenses are assigned to either a user or shared device. If the Citrix License Server assigns a license to a user, that user can make unlimited connections from unlimited devices. If the Citrix License Server assigns a license to a device, unlimited users can make unlimited connections from that device. License consumption is based on the user or device using the license.


The architecture for Citrix licenses is shown in the following figure:

![Citrix license architecture.](../image/citrix-architecture.png)

Licensing for third-party applications that are delivered through Citrix virtualization technologies is based on potential access. Any user or device can consume a license as long as they have the potential to access an application or desktop deployed in a virtual Citrix environment. You can control access to these applications and desktops by using Delivery Groups and Application Groups:

-   **Delivery Groups**

    Delivery Groups are collections of devices on which you can use Citrix applications or desktops. Each Delivery Group specifies the users that have access to those devices. In addition, Delivery Groups specify the applications or desktops that are available to those users.

-   **Application Groups**

    Application Groups are collections of applications that are shared across Delivery Groups or subsets of Delivery Group users. Each Application Group specifies the users or Active Directory \(AD\) groups that have access to those applications.


Refer to the [Citrix product documentation](https://docs.citrix.com/) for more information on Citrix deployment guidelines and recommendations. Use this information to determine whether you should map your users at the Delivery Group level or at the Application Group level. If you map users at both levels, Software Asset Management considers mappings at only the Application Group level.

You can view your Citrix license usage data from the [Software Publisher Analytics dashboard for Citrix](../reference/dashboard-citrix.md). Use this data to optimize your license position by reclaiming any unused or unauthorized licenses.

-   **[Create entitlements for Citrix](../task/create-entitlement-citrix.md)**  
Software entitlements enable you to define license details that are matched to software models. You can add an entitlement individually or import a list from a spreadsheet.
-   **[Software Publisher Analytics dashboard for Citrix in Software Asset Management classic](../reference/dashboard-citrix.md)**  
View compliance analysis results for Citrix on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
-   **[Publisher overview for Citrix Systems in the Software Asset Workspace](../reference/publisher-overview-citrix.md)**  
View license usage information related to Citrix in the publisher overview for Citrix Systems in the Software Asset Workspace.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

