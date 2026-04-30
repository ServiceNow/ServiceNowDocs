---
title: Software Asset Management for Red Hat Enterprise Linux
description: Use the Software Asset Management publisher pack for IBM to track and optimize licensing for your Red Hat Enterprise Linux \(RHEL\) products.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management for Red Hat Enterprise Linux

Use the Software Asset Management publisher pack for IBM to track and optimize licensing for your Red Hat Enterprise Linux \(RHEL\) products.

## Required plugins and applications for Red Hat Enterprise Linux

To manage licenses for your RHEL products, request and activate the Software Asset Management Professional for IBM plugin \(com.sn\_samp\_ibm\) from the Now Support service portal. See [Request Software Asset Management](../task/t_RequSoftwareAssetMgmt.md) for more information on how to request and activate this plugin.

You must also request and install the CMDB CI Class Models application from the ServiceNow Store. This application contains the tables that store RHEL data on your ServiceNow instance and is required for RHEL reconciliation.

The ServiceNow® Discovery application uses the Red Hat Virtualization \(RHV\) discovery pattern to locate RHV components. To enable the discovery of these resources, you must install the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Supported license types

The IBM publisher pack supports licensing for both Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters. The supported license metrics are socket-pair based and core-based.

-   **[Red Hat Enterprise Linux socket-pair based licensing](rh-socket-pair-licensing.md)**  
The Software Asset Management publisher pack for IBM supports socket-pair based licensing rules for Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters.
-   **[Red Hat Enterprise Linux core-based licensing](rh-core-based-license.md)**  
The Software Asset Management publisher pack for IBM supports core-based licensing rules for RHEL products in both physical and virtual environments.
-   **[Red Hat Enterprise Linux entitlements](rhel-entitlements.md#)**  
Software entitlements define the license details for your Red Hat Enterprise Linux \(RHEL\) products. You can create individual entitlements or import a list of entitlements from a spreadsheet.
-   **[Publisher overview for Red Hat in the Software Asset Workspace](../reference/publisher-overview-red-hat.md)**  
View license usage information related to Red Hat Enterprise Linux \(RHEL\) in the publisher overview for Red Hat in the Software Asset Workspace.

**Parent Topic:**[Software Asset Management publisher pack for IBM](ibm-publisher-pack.md)

