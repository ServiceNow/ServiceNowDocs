---
title: View Zero Copy Connector for ERP partner profile information
description: In Zero Copy Connector for ERP, view partner profile information including number and type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/view-erp-system-partner-profile-information.html
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

2.  Open the ERP systems list by selecting the systems icon \[Omitted image "erp-systems-icon-sidebar.png"\] Alt text: in the side panel.

3.  Open a system record.

4.  Check the **IDoc retrieval status** on the record.

    \[Omitted image "erp-system-partner-profile-tab2.png"\] Alt text: Zero Copy Connector for ERP system record with IDOC retrieval status area highlighted.

5.  Select the **Partner profile** tab to view available profiles.

    \[Omitted image "erp-system-partner-profile-tab.png"\] Alt text: Zero Copy Connector for ERP system record with partner profile tab displayed.

    For column descriptions, see [Zero Copy Connector for ERP partner profile tab column descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-partner-profile-tab-fields.md).

6.  Select a **Partner number** to view information about a specific profile.

    \[Omitted image "erp-system-partner-profile-tab3.png"\] Alt text: Zero Copy Connector for ERP profile record for one individual profile.

    For field descriptions, see [Zero Copy Connector for ERP partner profile field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-partner-profile-fields.md).


**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md)

