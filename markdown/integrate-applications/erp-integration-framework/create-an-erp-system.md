---
title: Create an ERP system in Zero Copy Connector for ERP
description: Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, create, configure, erp, system]
breadcrumb: [Working with ERP systems, Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Create an ERP system in Zero Copy Connector for ERP

Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

Zero Copy Connector for ERP supports connecting to multiple systems.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP systems list by selecting the systems icon ![](../image/erp-systems-icon-sidebar.png) in the side panel.

3.  Select **New**.

4.  On the form, fill in the fields.

    ![new ERP system form.](../image/erpc-system-new-ys2.png)

    **Note:** To use the HTTP connection option, you must have an SAP system that is enabled to make an OData connection.

    For a description of the field values, see [Zero Copy Connector for ERP new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

5.  Select **Save**.


## Result

After you create a system, you can view heartbeat and retrieval status on the ERP systems list page. For more information, see [View a list of Zero Copy Connector for ERP systems](view-and-monitor-erp-systems-health.md).

**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md)

