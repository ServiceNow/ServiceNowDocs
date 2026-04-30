---
title: View ERP Data Hub system heartbeat information
description: In ERP Data Hub, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2024-10-27"
reading_time_minutes: 1
breadcrumb: [Working with ERP systems in ERP Data Hub, Configuring ERP Data Hub, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# View ERP Data Hub system heartbeat information

In ERP Data Hub, the heartbeat shows the status, date, and time of connections to the ERP system, along with error information.

## Before you begin

Role required: admin and sn\_erp\_integration.erp\_user

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub**.

2.  Open the ERP systems list by selecting the systems icon \(![ERP systems icon](../image/erp-systems-icon-sidebar.png)\) in the side panel.

3.  Open a system.

4.  Select the **RFC heartbeats** or **HTTP heartbeats** tab.

    ![ERP Data Hub system record with RFC heartbeats tab displayed.](../image/erpc-system-rfc-heartbeat.png)

    View information about the heartbeats, including updated date and time, and status. If there's an error, the error text is displayed and a link to a knowledge base article \(if available\) is provided. For more information, see [ERP Data Hub new system field descriptions](../reference/erp-canvas-create-new-system-descriptions.md).

    By default, all heartbeat information is kept for one week. To change that setting, go to **All** &gt; **Data Management Policies**, open the sn\_erp\_integration\_log\_heartbeat policy, select the **Table Cleanup Rules** tab, select the **Tablename**, and edit the **Age in seconds**.


**Parent Topic:**[Working with ERP systems in ERP Data Hub](../concept/erp-canvas-work-with-systems.md)

