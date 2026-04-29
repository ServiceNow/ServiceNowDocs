---
title: Components installed with Software Asset Management Professional
description: Roles, plugins, and scheduled jobs are installed with the activation of the Software Asset Management Professional application. Demo data is available with this application.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management]
---

# Components installed with Software Asset Management Professional

Roles, plugins, and scheduled jobs are installed with the activation of the Software Asset Management Professional application. Demo data is available with this application.

## Scheduled jobs installed

To view the list of scheduled jobs installed with the Software Asset Management Professional application, navigate to your ServiceNow instance, select **All**, and enter `Scheduled jobs` in the application navigator. On the Scheduled jobs page, select the Show/hide filter and in the condition builder, enter the filter condition, `Name starts with SAM`.

## Roles installed

The following roles are installed with the Software Asset Management Professional application.

<table id="table_iwq_3xg_l1c"><thead><tr><th>

Role name

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Software Asset Management administrator \[sam\_admin\]

</td><td>

Granular admin role that has full access to the Software Asset Management application. This role is required to import entitlements, manage reclamation rules, run reconciliation, create custom products and pattern normalization rules, set up Content Service, and other administrative features.

</td><td>

-   sam\_user
-   sam\_spend\_import
-   asset
-   model\_manager
-   contract\_manager

 **Note:** The sam\_spend\_import role is installed with Software Spend Detection. The it\_demand\_user role is no longer automatically installed with [PPM Standard](https://www.servicenow.com/docs/access?context=c_ProjectPortfolioSuiteWithFinancials&version=australia&pubname=australia-it-business-management&ft:locale=en-US).

</td></tr><tr><td>

Software Asset Management user \[sam\_user\]

</td><td>

This role has access to all Software Asset Management features except administrative. If Software Spend Detection is installed, this role has access to all Software Spend Detection features except financial transaction data import and Content Service setup.

</td><td>

-   pa\_viewer
-   cmdb\_read
-   report\_user
-   sn\_remote\_dir\_sync.reader

</td></tr><tr><td>

Software Asset Management developer \[sam\_developer\]

</td><td>

Writes scripts on the platform, comparable to the script-writing privileges granted to a sys\_admin. Users with this role must be trained ServiceNow administrators.

</td><td>

sam\_admin

</td></tr><tr><td>

SaaS License Management integration administrator\[sam\_integrator\]

</td><td>

Granular admin role required to create and manage SaaS integration profiles.

</td><td>

-   sam\_user
-   connection\_admin
-   flow\_operator

</td></tr><tr><td>

Software Spend Detection import user \[sam\_spend\_import\]

</td><td>

Role required to import financial transaction data into Software Spend Detection. Users with this role have access to all Software Spend Detection features except Content Service setup. Users with this role cannot view Software Asset Management without being granted additional roles.

</td><td>

pa\_viewer

</td></tr></tbody>
</table>## Plugins installed

The following plugins are installed with the Software Asset Management Professional application.

<table id="table_jdd_jj1_x2b"><thead><tr><th>

Plugin

</th><th>

Location

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activate all Software Asset Management Professional plugins including Software Asset Workspace com.sn\_samp\_master\_ws

</td><td>

Now Support Service Portal

</td><td>

Requires subscription. Provides the capability to normalize software discovery information, reconcile entitlements with installs, and reclaiming unused software. Provides additional capabilities to reconcile publisher products. Loads the following plugin and store application in one step:-   Software Asset Management Professional \(com.sn\_samp\_master\) plugin
-   Software Asset Workspace \(sn\_sam\_workspace\) store application.

</td></tr><tr><td>

Activate all Software Asset Management Professional plugins\(com.sn\_samp\_master\)

</td><td>

Now Support Service Portal

</td><td>

This plugin is for releases prior to Australia. Loads the following Software Asset Management Professional plugins in one step:

 -   Software Asset Management Professional \(com.snc.samp\) plugin
-   All publisher pack add-on plugins
-   Software Asset Management UI Components \(com.sn\_samp\_workbench\)

 **Note:** To enable SaaS License Management, you must request the Software Asset Management — SaaS License Management \(sn\_sam\_saas\_int\) plugin separately from the ServiceNow Store. See [Request SaaS License Management](../task/request-saas-license-management.md) for information on how to request and activate this plugin.

</td></tr><tr><td>

Integration — Microsoft SCCM 2012 v2 Software Usage\(com.snc.samp\_usage\_sccm\)

</td><td>

Now Support Service Portal

</td><td>

Required to gather software usage data from Microsoft SCCM \(System Center Configuration Manager\) 2012 v2.Automatically activates the Integration — Microsoft SCCM 2012 v2 \(com.snc.integration.sccm2012v2\) plugin if not already active.

 **Important:** This plugin will be deprecated in the Tokyo release. If you are integrating with SCCM for the first time, request and install the Service Graph connector for Microsoft SCCM application from the [ServiceNow Store](https://store.servicenow.com/) instead. If you have already activated this plugin on your ServiceNow instance, use the Migration Readiness Tool for Service Graph Connector for SCCM store application to prepare your instance for migration to the Service Graph connector. See [Service Graph connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information on the Service Graph connector.

</td></tr><tr><td>

Integration — Microsoft SCCM 2016 Software Usage\(com.snc.samp.usage\_sccm\_2016\)

</td><td>

Now Support Service Portal

</td><td>

Required to gather software usage data from Microsoft SCCM \(System Center Configuration Manager\) 2016.Automatically activates the Integration — Microsoft SCCM 2016 \(com.snc.integration.sccm2016\) plugin if not already active.

 **Important:** This plugin will be deprecated in the Tokyo release. If you are integrating with SCCM for the first time, request and install the Service Graph connector for Microsoft SCCM application from the [ServiceNow Store](https://store.servicenow.com/) instead. If you have already activated this plugin on your ServiceNow instance, use the Migration Readiness Tool for Service Graph Connector for SCCM store application to prepare your instance for migration to the Service Graph connector. See [Service Graph connector for Microsoft SCCM](https://www.servicenow.com/docs/access?context=cmdb-integration-sccm&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for more information on the Service Graph connector.

</td></tr><tr><td>

Orchestration — Client Software Distribution\(com.snc.orchestration.client\_sf\_distribution\)

</td><td>

Now Support Service Portal

</td><td>

Required to activate ServiceNow® Orchestration application, which enables install and uninstall functionality of software on devices.**Note:** Users who purchase the Software Asset Management Professional \(com.snc.samp\) plugin are licensed for software uninstall functionality only, also called software reclamation. Additional licensing is required for software install functionality.

</td></tr><tr><td>

Software Asset Management — SaaS License Management\(sn\_sam\_saas\_int\)

</td><td>

ServiceNow Store

 See [Request SaaS License Management](../task/request-saas-license-management.md) for information on how to request and activate this plugin from the ServiceNow Store.

</td><td>

Requires the Software Asset Management Professional \(com.snc.samp\) plugin. Provides integrations to manage licenses for SaaS products.

</td></tr><tr><td>

Software Asset Management — Spend Detection \(com.sn\_sam\_spend\)

</td><td>

Now Support Service Portal

</td><td>

Requires the Software Asset Management Professional \(com.snc.samp\) plugin. Provides core capabilities to detect software spend from financial transaction data.

</td></tr><tr><td>

File Signature Normalization \(com.snc.file\_signature\_normalization\)

</td><td>

Now Support Service Portal

</td><td>

Required to normalize discovered file signatures while creating installed software records. This plugin also gets activated with File-based Discovery.

</td></tr><tr><td>

Mobile Employee Experience My Asset \(com.glide.mobile-employee.myassets\)

</td><td>

Now Support Service Portal

</td><td>

Provides the capabilities needed for end users to view assigned assets on a mobile device and to create incidents to request service for these assets.

</td></tr><tr><td>

IT Asset Management Mobile\(com.sn\_itam\_mobile\)

</td><td>

Now Support Service Portal

</td><td>

Provides the capabilities for receiving personnel to receive purchased assets on a mobile device.

</td></tr><tr><td class="sub-head" id="pub-pack" colspan="3">

Publisher pack add-on plugins

</td></tr><tr><td>

Software Asset Management Professional for Adobe \(com.sn\_samp\_adobe\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile Adobe subscription software.

</td></tr><tr><td>

Software Asset Management Professional for Citrix \(com.sn\_samp\_citrix\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile Citrix software, such as Virtual Applications and Virtual Desktop.

</td></tr><tr><td>

Software Asset Management Professional for IBM \(com.sn\_samp\_ibm\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile IBM products using PVU and RVU license metrics.

 This plugin also provides additional capabilities to reconcile Red Hat Enterprise Linux software, such as Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters.

</td></tr><tr><td>

Software Asset Management Professional for Microsoft \(com.snc.samp.microsoft\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile Microsoft software such as Microsoft SQL Server.

</td></tr><tr><td>

Software Asset Management Professional for Oracle \(com.snc.samp.oracle\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile Oracle software, such as Oracle DB Server.

</td></tr><tr><td>

Software Asset Management Professional for SAP \(com.sn\_samp\_sap\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile SAP named user compliance and optimization.

</td></tr><tr><td>

Software Asset Management Professional for VMware \(com.sn\_samp\_vmware\)

</td><td>

Now Support Service Portal

</td><td>

Provides additional capabilities to reconcile VMware software, such as vCenter and vSphere.

</td></tr><tr><td>

Software Asset Management Professional for Engineering Applications \(com.sn\_samp\_eng\_app\)

</td><td>

Now Support Service Portal

</td><td>

Requires the Software Asset Management Professional \(com.snc.samp\) plugin. Provides additional capabilities to reconcile engineering applications such as AutoCAD.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](references.md)

