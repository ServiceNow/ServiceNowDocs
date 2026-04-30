---
title: View Zero Copy Connector for ERP system heartbeat information
description: In Zero Copy Connector for ERP, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system, heartbeat, connection, error, status]
breadcrumb: [Working with ERP systems, Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# View Zero Copy Connector for ERP system heartbeat information

In Zero Copy Connector for ERP, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin or sn\_erp\_integration.erp\_user

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP systems list by selecting the systems icon ![](../image/erp-systems-icon-sidebar.png) in the side panel.

3.  Open a system.

4.  Select the **RFC heartbeats** or **HTTP heartbeats** tab.

    ![Zero Copy Connector for ERP system record with HTTP heartbeats tab displayed.](../image/erpc-system-rfc-heartbeat-ys2.png)

    View information about the heartbeats, including updated date and time, and status. If there's an error, the error text is displayed and a link to a knowledge base article \(if available\) is provided. For more information, see [Zero Copy Connector for ERP new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

    By default, all heartbeat information is kept for one week, but users with the admin role can change that setting.

    1.  Navigate to **All** &gt; **System Data Management** &gt; **Data Management Policies**.
    2.  Open the **ERP heartbeat log policy** \(sn\_erp\_integration\_log\_heartbeat\).
    3.  Select the **Table Cleanup Rules** tab.
    4.  In the list, select **sn\_erp\_integration\_log\_heartbeat**.
    5.  Edit the **Age in seconds**.

**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md)

