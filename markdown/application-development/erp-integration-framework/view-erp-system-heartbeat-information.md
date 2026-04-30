---
title: View Zero Copy Connector for ERP system heartbeat information
description: In Zero Copy Connector for ERP, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Working with ERP systems in Zero Copy Connector for ERP, Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# View Zero Copy Connector for ERP system heartbeat information

In Zero Copy Connector for ERP, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin and sn\_erp\_integration.erp\_user

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP**.

2.  Open the ERP systems list by selecting the systems icon \(![ERP systems icon](../image/erp-systems-icon-sidebar.png)\) in the side panel.

3.  Open a system.

4.  Select the **RFC heartbeats** or **HTTP heartbeats** tab.

    ![Zero Copy Connector for ERP system record with RFC heartbeats tab displayed.](../image/erpc-system-rfc-heartbeat-ys2.png)

    View information about the heartbeats, including updated date and time, and status. If there's an error, the error text is displayed and a link to a knowledge base article \(if available\) is provided. For more information, see [Zero Copy Connector for ERP new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

    By default, all heartbeat information is kept for one week. To change that setting, go to **All** &gt; **Data Management Policies**, open the sn\_erp\_integration\_log\_heartbeat policy, select the **Table Cleanup Rules** tab, select the **Tablename**, and edit the **Age in seconds**.


**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md)

