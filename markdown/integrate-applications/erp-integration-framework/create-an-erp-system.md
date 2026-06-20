---
title: Create an ERP system in Zero Copy Connector for ERP
description: Configure an ERP \(Enterprise Resource Planning\) system in Zero Copy Connector for ERP to organize your connections to the system of record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/erp-integration-framework/create-an-erp-system.html
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

2.  Open the ERP systems list by selecting the systems icon \[Omitted image "erp-systems-icon-sidebar.png"\] Alt text: in the side panel.

3.  Select **New**.

4.  On the form, fill in the fields.

    \[Omitted image "erpc-system-new-ys2.png"\] Alt text: new ERP system form.

    **Note:** To use the HTTP connection option, you must have an SAP system that is enabled to make an OData connection.

    For a description of the field values, see [Zero Copy Connector for ERP new system field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-create-new-system-descriptions.md).

5.  Select **Save**.


## Result

After you create a system, you can view heartbeat and retrieval status on the ERP systems list page. For more information, see [View a list of Zero Copy Connector for ERP systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/view-and-monitor-erp-systems-health.md).

**Parent Topic:**[Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md)

