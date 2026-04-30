---
title: Software Asset Management for Red Hat Enterprise Linux
description: Use the Software Asset Management publisher pack for IBM to track and optimize license positions for the Red Hat Enterprise Linux Server products.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management for Red Hat Enterprise Linux

Use the Software Asset Management publisher pack for IBM to track and optimize license positions for the Red Hat Enterprise Linux Server products.

## Required plugins and applications for Red Hat Enterprise Linux

To manage licenses for your Red Hat Enterprise Linux \(RHEL\) products, request and activate the Software Asset Management Professional for IBM plugin \(com.sn\_samp\_ibm\) from the Now Support service portal. See [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md) for more information on how to request and activate this plugin.

You must also request and install the CMDB CI Class Models application from the ServiceNow Store. This application contains the tables that store RHEL data on your ServiceNow instance and is required for RHEL reconciliation.

The ServiceNow® Discovery application uses the Red Hat Virtualization \(RHV\) discovery pattern to locate RHV components. To enable the discovery of these resources, you must install the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Supported license types

The IBM publisher pack supports licensing for both Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters. The supported license metrics are socket-pair based and core based.

-   **[Red Hat Enterprise Linux socket-pair based licensing](rh-socket-pair-licensing.md)**  
Use the RHEL Server licensing based on the number of socket-pairs or virtual machine \(VM\) pairs on a physical host to manage licenses for your RHEL products.
-   **[Red Hat Enterprise Linux core-based licensing](rh-core-based-license.md)**  
Use the RHEL Per Core license metric to license core-based RHEL products on both physical and virtual environments.
-   **[Red Hat Enterprise Linux entitlements](rhel-entitlements.md#)**  
Software entitlements define the license details for your Red Hat Enterprise Linux \(RHEL\) products. You can create individual entitlements or import a list of entitlements from a spreadsheet.
-   **[Publisher overview for Red Hat in the Software Asset Workspace](../reference/publisher-overview-red-hat.md)**  
View license usage information related to Red Hat Enterprise Linux \(RHEL\) in the publisher overview for Red Hat in the Software Asset Workspace.

**Parent Topic:**[Software Asset Management publisher pack for IBM](ibm-publisher-pack.md)

