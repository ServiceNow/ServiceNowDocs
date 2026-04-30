---
title: Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v2 APIs
description: You can use version 2 of the IBM License Metric Tool \(ILMT\) and BigFix Inventory integration APIs to create a connection between your IBM servers and the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using v2 APIs

You can use version 2 of the IBM License Metric Tool \(ILMT\) and BigFix Inventory integration APIs to create a connection between your IBM servers and the ServiceNow AI Platform.

This connection enables you to import usage data into your ServiceNow instance so that you can track and optimize full capacity and sub-capacity processor value unit \(PVU\) and resource value unit \(RVU\) licensing as well as sub-capacity virtual processor core \(VPC\) licensing for your IBM software products.

See [REST API resources and HTTP methods](https://www.ibm.com/docs/en/license-metric-tool?topic=api-rest-resources-http-methods) for more information on the ILMT and BigFix Inventory integration APIs.

![Integration between ILMT and ServiceNow.](../image/ilmt-bigfix-inventory-integration-v2-apis.png)

The ILMT and BigFix Inventory integration enables you to create connections between one or more IBM servers and the ServiceNow AI Platform using HTTP or HTTPS. When you initiate the integration, you receive an IBM Server connection alias that you can use to set up your IBM server connections. If a connection is successful, the Software Asset Management application retrieves peak usage data within the aggregated period that you defined in ILMT or BigFix Inventory.

## Prerequisites

To track your IBM full capacity and sub-capacity PVU, RVU, and VPC licenses using this integration, you must complete the following prerequisites:

-   Install, set up, and run ILMT or BigFix Inventory on a physical host or virtual machine \(VM\).

    **Important:** When you are setting up ILMT, ensure that all required configuration item \(CI\) data, including serial numbers, names, and IP addresses, is configured correctly so that your ServiceNow instance can accurately create corresponding CI records in the Configuration Management Database \(CMDB\). Refer to [KB0691430](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB0691430) for more details.

-   Install ILMT version 9.2.24 or later.

    **Note:** If you are using ILMT version 9.2.23 or earlier, you can import usage data only against your discovered IBM software products and not against the hosts that are running those products.

-   Configure your IBM ILMT agents to scan your physical hosts or VMs in compliance with IBM usage measurement guidelines.

    **Note:** Refer to [Measuring License Use](https://www.ibm.com/about/software-licensing/measurement/measuring_license_use) for more information on IBM usage measurement guidelines.

-   Enable ILMT or BigFix Inventory to discover the configurations of both physical hosts and VMs as well as the relationships between them.
-   Classify and bundle IBM components into IBM products through ILMT or BigFix Inventory.
-   Request and install the IBM License Compliance for Software Asset Management application from the ServiceNow® Store. See [Request the IBM License Compliance for Software Asset Management application for IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](../task/request-ibm-license-compliance-sam-application-ilmt-bigfix.md) for detailed instructions.
-   Set the **Connect to ILMT using** \(**sn\_samp\_ibm\_lic.ilmt\_api\_version**\) Software Asset Management property to **v2 API's**. For more details on this property, see [Software Asset Management properties](../reference/sam-properties.md).

-   **[Request the IBM License Compliance for Software Asset Management application for IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](../task/request-ibm-license-compliance-sam-application-ilmt-bigfix.md)**  
If you are using version 2 of the IBM License Metric Tool \(ILMT\) and BigFix Inventory integration APIs to integrate with ILMT or BigFix Inventory, request the IBM License Compliance for Software Asset Management application from the ServiceNow® Store. Use the integration to track and manage your IBM licenses.
-   **[IBM License Metric Tool \(ILMT\) and BigFix Inventory transform map for v2 APIs](ibm-transform-maps-v2.md)**  
When you import data from the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the ILMT and BigFix Inventory integration APIs, your ServiceNow instance uses a default transform map to process this data into ServiceNow tables.
-   **[View the peak usage of your IBM software products](../task/view-ibm-ilmt-v2-peak-usage-product.md)**  
If you are integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the ILMT and BigFix Inventory integration APIs, view the highest full capacity and sub-capacity Processor Value Unit \(PVU\), Resource Value Unit \(RVU\), and Virtual Processor Core \(VPC\) usage for your IBM software products within an aggregated time period of up to 90 days.
-   **[View the peak usage of your IBM software products by device](../task/view-ibm-ilmt-v2-peak-usage-device.md)**  
If you are integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the ILMT and BigFix Inventory integration APIs, view the highest full capacity and sub-capacity Processor Value Unit \(PVU\), Resource Value Unit \(RVU\), and Virtual Processor Core \(VPC\) usage for your IBM software products by physical host or virtual machine \(VM\).
-   **[View the devices that are running your IBM software products](../task/view-ibm-ilmt-v2-discovered-computer.md)**  
If you are integrating with the IBM License Metric Tool \(ILMT\) or BigFix Inventory using version 2 of the ILMT and BigFix Inventory integration APIs, view the complete list of physical hosts and virtual machines \(VMs\) that are running your IBM software products.

**Parent Topic:**[IBM License Metric Tool \(ILMT\) and BigFix Inventory integrations](ibm-ilmt-bigfix-inventory-integration.md)

