---
title: Software Asset Management publisher pack for IBM
description: Use the Software Asset Management publisher pack for IBM to track and optimize licensing for your IBM software products. You can also use the publisher pack to track and optimize licensing for the Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters products.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for IBM

Use the Software Asset Management publisher pack for IBM to track and optimize licensing for your IBM software products. You can also use the publisher pack to track and optimize licensing for the Red Hat Enterprise Linux Server and Red Hat Enterprise Linux for Virtual Datacenters products.

To use the IBM publisher pack, activate the Software Asset Management Professional for IBM \(com.sn\_samp\_ibm\) [plugin](../task/t_RequSoftwareAssetMgmt.md).

The IBM publisher pack supports the following license metrics:

-   Authorized User
-   Authorized User Value Unit
-   Employee User Value Unit
-   External User Value Unit
-   Per Device
-   Per Named User
-   Per Processor
-   Per User
-   Processor Value Unit \(PVU\)
-   Resource Value Unit \(RVU\)
-   Virtual Processor Core \(VPC\)

**Important:** The PVU, RVU, and VPC license metrics are supported only if you integrate the IBM publisher pack with the IBM License Metric Tool \(ILMT\), BigFix Inventory, or a Software Asset Management provider that is authorized to participate in the IBM Client Value Acceleration \(CVA\) Program. For more information on ILMT and BigFix Inventory integrations, see [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md). For more information on Authorized SAM Provider \(ASP\) integrations, see [Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md).

For more information on the supported IBM license metrics, see [Software license metrics](c_SAMLicenseMetrics.md).

**Important:** The IBM publisher pack is available as part of the Software Asset Management Professional \(com.snc.samp\) plugin. The publisher pack includes all capabilities that are required for tracking and managing both full capacity and sub-capacity PVU and RVU licenses for your IBM products. It does not require the legacy IBM PVU Process Pack to track and manage IBM PVU licenses. See [iBM PVU Process Pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/software-asset-management/c_IBMPVUProcessPack.md) for more information on the legacy process pack.

When you run a discovery using a discovery tool such as the ServiceNow Discovery application, the discovery tool locates the IBM software installations in your environment and then imports the associated data into your ServiceNow instance. The Software Asset Management application compares this data against your IBM software entitlements to automatically reconcile your IBM software products, including products in complex server licensing scenarios.

**Important:** You must use different discovery tools based on the license metric that you are using for reconciliation, and if applicable, the type of IBM integration that you are using with the publisher pack:

-   **PVU and RVU license metrics**

    To reconcile your IBM software products using the PVU or RVU license metrics, you must use one of the following discovery tools:

    -   If you are integrating with the ILMT or BigFix Inventory, you must connect to these discovery tools using either version 1 or version 2 of the integration APIs.
    -   If you are integrating with a Software Asset Management provider that is authorized to participate in the IBM CVA Program, you must use the ServiceNow Discovery application in conjunction with the IBM License Compliance for Software Asset Management application.

-   **VPC license metric**

    To reconcile your IBM software products using the VPC license metric, you must use one of the following discovery tools:

    -   If you are integrating with the ILMT or BigFix Inventory, you must connect to these discovery tools using version 2 of the integration APIs.
    -   If you are integrating with a Software Asset Management provider that is authorized to participate in the IBM CVA Program, you must use the ServiceNow Discovery application in conjunction with the IBM License Compliance for Software Asset Management application.
-   **All other supported license metrics**

    To reconcile your IBM software products using any other supported license metric, including user-based license metrics like Authorized User and External User Value Unit, you can use any other discovery tool.


-   **[Supported IBM license types](supported-ibm-license-types.md)**  
The Software Asset Management publisher pack for IBM adds license metrics for various IBM license types.
-   **[IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md)**  
You can use an IBM License Metric Tool \(ILMT\) or BigFix Inventory integration to create a connection between your IBM servers and the ServiceNow AI Platform. Use this connection to import data into your ServiceNow instance so that you can track and optimize licensing for your IBM software products.
-   **[Authorized SAM Provider \(ASP\) integrations for IBM](ibm-asp-integration.md)**  
You can track and manage IBM licenses in both VMware vSphere environments and IBM LPAR infrastructures by integrating the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program. With these integrations, you can track and manage IBM licensing directly without having to integrate with the IBM License Metric Tool \(ILMT\) or BigFix Inventory.
-   **[Software Publisher Analytics dashboard for IBM in Software Asset Management classic](../reference/dashboard-ibm.md)**  
View compliance analysis results related to IBM on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
-   **[Publisher overview for IBM in the Software Asset Workspace](../reference/publisher-overview-ibm.md)**  
View license usage information related to IBM in the publisher overview for IBM in the Software Asset Workspace.
-   **[Software Asset Management for Red Hat Enterprise Linux](rhel-publisher-pack.md)**  
Use the Software Asset Management publisher pack for IBM to track and optimize licensing for your Red Hat Enterprise Linux \(RHEL\) products.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

