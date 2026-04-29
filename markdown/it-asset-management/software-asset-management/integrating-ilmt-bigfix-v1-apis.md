---
title: Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v1 APIs
description: You can use version 1 of the IBM License Metric Tool \(ILMT\) and BigFix Inventory integration APIs to create a connection between your IBM servers and the ServiceNow AI Platform.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [ILMT and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v1 APIs

You can use version 1 of the IBM License Metric Tool \(ILMT\) and BigFix Inventory integration APIs to create a connection between your IBM servers and the ServiceNow AI Platform.

This connection enables you to import software installation data into your ServiceNow instance so that you can track and optimize full capacity and sub-capacity processor value unit \(PVU\) and resource value unit \(RVU\) licensing for your IBM software products.

**Important:** Version 1 of the ILMT and BigFix Inventory integration APIs have been deprecated by IBM. However, the Software Asset Management application continues to support integrations that are using this version of the APIs. If you are setting up an ILMT or BigFix Inventory integration for the first time, use version 2 of the APIs instead. For more information on setting up the integration using version 2 of the APIs, see [Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v2 APIs](integrating-ilmt-bigfix-v2-apis.md). For more information on the deprecation of these APIs, see [Deprecated REST APIs](https://www.ibm.com/docs/en/license-metric-tool?topic=api-deprecated-rest-apis).

![Integration between ILMT and ServiceNow.](../image/ibm-pvu-rvu-licensing.png)

The ILMT and BigFix Inventory integration enables you to create connections between one or more IBM servers and the ServiceNow AI Platform using HTTP or HTTPS. Upon activating the Software Asset Management Professional for IBM \(com.sn\_samp\_ibm\) plugin, you receive an IBM Server connection alias that you can then use to set up your IBM server connections. If a connection is successful, the Software Asset Management application retrieves historical software installation data within the aggregated period that you defined in ILMT or BigFix Inventory. This data includes products, components, editions, hosts, virtual machines, and license usage.

**Note:** License usage is based on product use and not component use.

## Prerequisites

To track your IBM full capacity and sub-capacity PVU and RVU licenses using this integration, you must complete the following prerequisites:

-   Install, set up, and run ILMT or BigFix Inventory on a physical host or virtual machine \(VM\).

    **Important:** When you are setting up ILMT, ensure that all required configuration item \(CI\) data, including serial numbers, names, and IP addresses, is configured correctly so that your ServiceNow instance can accurately create corresponding CI records in the Configuration Management Database \(CMDB\). Refer to [KB0691430](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0691430) for more details.

-   Install ILMT version 9.2.7 or later.
-   Configure your IBM ILMT agents to scan your physical hosts or VMs in compliance with IBM usage measurement guidelines.

    **Note:** Refer to [Measuring License Use](https://www.ibm.com/about/software-licensing/measurement/measuring_license_use) for more information on IBM usage measurement guidelines.

-   Enable ILMT or BigFix Inventory to discover the configurations of both physical hosts and VMs as well as the relationships between them.
-   Classify and bundle IBM components into IBM products through ILMT or BigFix Inventory.
-   Set the **Connect to ILMT using** \(**sn\_samp\_ibm\_lic.ilmt\_api\_version**\) Software Asset Management property to **v1 API's**. For more details on this property, see [Software Asset Management properties](../reference/sam-properties.md).

-   **[Transform maps for IBM License Metric Tool \(ILMT\) and BigFix Inventory integration v1 APIs](ibm-transform-maps.md)**  
When you import data from the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 1 of the ILMT and BigFix Inventory integration APIs, your ServiceNow instance uses transform maps to process this data into ServiceNow tables.

**Parent Topic:**[IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md)

