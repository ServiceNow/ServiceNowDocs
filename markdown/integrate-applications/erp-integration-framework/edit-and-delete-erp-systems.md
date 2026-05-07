---
title: Edit and delete ERP systems
description: After creating an ERP \(Enterprise Resource Planning\) system, you can edit system details or delete the system at any time.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system, edit, delete, remove]
breadcrumb: [Working with ERP systems, Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Edit and delete ERP systems

After creating an ERP \(Enterprise Resource Planning\) system, you can edit system details or delete the system at any time.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP systems list by selecting the systems icon ![](../image/erp-systems-icon-sidebar.png) in the side panel.

3.  Open a system.

4.  Edit system information, such as name, description, connection, or ERP software.

    For detailed information about the system record fields, see [Zero Copy Connector for ERP new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

5.  On the status bar, confirm that the heartbeats are successful and the retrieval status is complete.

    **Note:** If any failed, select **Restart data retrieval**. Any data retrieval that failed \(BAPI, OData, or tables\) is fetched again.

6.  Delete an ERP system record from the ERP system table.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

    2.  In the **Name** column, search for and open sn\_erp\_integration\_system.

    3.  In **Related Links**, select **Show List**.

    4.  Select the ERP system to delete.

    5.  Select **Delete**.


**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md)

