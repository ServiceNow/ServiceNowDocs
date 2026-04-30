---
title: Create an ERP system in Zero Copy Connector for ERP
description: Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with ERP systems in Zero Copy Connector for ERP, Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Create an ERP system in Zero Copy Connector for ERP

Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

The ERP system is set on the extraction table or remote table. Zero Copy Connector for ERP supports connecting to multiple systems.

Alternatively, you can run Guided Setup. For more information, see [Run Guided Setup for Zero Copy Connector for ERP](erp-canvas-guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP**.

2.  Open the ERP systems list by selecting the systems icon \(![ERP systems icon](../image/erp-systems-icon-sidebar.png)\) in the side panel.

3.  Select **New**.

4.  On the form, fill in the fields.

    ![new ERP system form.](../image/erpc-system-new-ys2.png)

    **Note:** To use the HTTP connection option, you must have an SAP system that is enabled to make an OData connection.

    For a description of the field values, see [Zero Copy Connector for ERP new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

5.  Select **Save**.


## Result

After you create a system, you can view heartbeat and retrieval status on the ERP systems list page. For more information, see [View a list of Zero Copy Connector for ERP systems](view-and-monitor-erp-systems-health.md).

**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md)

