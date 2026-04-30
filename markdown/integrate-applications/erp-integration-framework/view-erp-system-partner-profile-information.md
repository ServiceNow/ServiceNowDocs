---
title: View Zero Copy Connector for ERP partner profile information
description: In Zero Copy Connector for ERP, view partner profile information including number and type.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, partner, profile, information, detail]
breadcrumb: [Working with ERP systems, Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# View Zero Copy Connector for ERP partner profile information

In Zero Copy Connector for ERP, view partner profile information including number and type.

## Before you begin

This feature is available starting with the Zurich Patch 4 release.

Role required: sn\_erp\_integration.erp\_user

## About this task

Partner profiles are fetched from SAP during initial load. If any new profiles are added on the remote SAP system, select the **Restart data retrieval** button on the system record in Zero Copy Connector for ERP to reload.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP systems list by selecting the systems icon ![](../image/erp-systems-icon-sidebar.png) in the side panel.

3.  Open a system record.

4.  Check the **IDoc retrieval status** on the record.

    ![Zero Copy Connector for ERP system record with IDOC retrieval status area highlighted.](../image/erp-system-partner-profile-tab2.png)

5.  Select the **Partner profile** tab to view available profiles.

    ![Zero Copy Connector for ERP system record with partner profile tab displayed.](../image/erp-system-partner-profile-tab.png)

    For column descriptions, see [Zero Copy Connector for ERP partner profile tab column descriptions](../reference/erp-partner-profile-tab-fields.md).

6.  Select a **Partner number** to view information about a specific profile.

    ![Zero Copy Connector for ERP profile record for one individual profile.](../image/erp-system-partner-profile-tab3.png)

    For field descriptions, see [Zero Copy Connector for ERP partner profile field descriptions](../reference/erp-partner-profile-fields.md).


**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](../concept/erp-canvas-work-with-systems.md)

