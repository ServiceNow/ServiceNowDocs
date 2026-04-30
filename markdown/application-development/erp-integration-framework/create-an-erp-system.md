---
title: Create an ERP system in ERP Data Hub
description: Configure an ERP \(Enterprise Resource Planning\) system in ERP Data Hub to organize your connections to the system of record.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with ERP systems in ERP Data Hub, Configuring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Create an ERP system in ERP Data Hub

Configure an ERP \(Enterprise Resource Planning\) system in ERP Data Hub to organize your connections to the system of record.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## About this task

The ERP system is set on the extraction table or remote table. ERP Data Hub supports connecting to multiple systems.

Alternatively, you can run Guided Setup. For more information, see [Run Guided Setup for ERP Data Hub](erp-canvas-guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub**.

2.  Open the ERP systems list by selecting the systems icon \(![ERP systems icon](../image/erp-systems-icon-sidebar.png)\) in the side panel.

3.  Select **New**.

4.  On the form, fill in the fields.

    ![ERP Data Hub new ERP system form.](../image/erpc-system-new2.png)

    **Note:** The HTTP connection option is available starting in Xanadu Store Release 2. You must have an SAP system that is enabled to make an OData connection.

    For a description of the field values, see [ERP Data Hub new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

5.  Select **Save**.


## Result

After you create a system, you can view heartbeat and retrieval status on the ERP systems list page. For more information, see [View a list of ERP Data Hub systems](view-and-monitor-erp-systems-health.md).

**Parent Topic:**[Working with ERP systems in ERP Data Hub](../concept/erp-canvas-work-with-systems.md)

