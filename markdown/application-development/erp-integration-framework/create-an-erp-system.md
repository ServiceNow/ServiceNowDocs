---
title: Create an ERP system in ERP Data Hub
description: Configure an ERP \(Enterprise Resource Planning\) system in ERP Data Hub to organize your connections to the system of record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/erp-integration-framework/create-an-erp-system.html
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

Alternatively, you can run Guided Setup. For more information, see [Run Guided Setup for ERP Data Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-guided-setup.md).

## Procedure

1.  Navigate to **All** &gt; **ERP Data Hub**.

2.  Open the ERP systems list by selecting the systems icon \(\[Omitted image "erp-systems-icon-sidebar.png"\] Alt text: ERP systems icon\) in the side panel.

3.  Select **New**.

4.  On the form, fill in the fields.

    \[Omitted image "erpc-system-new2.png"\] Alt text: ERP Data Hub new ERP system form.

    **Note:** The HTTP connection option is available starting in Xanadu Store Release 2. You must have an SAP system that is enabled to make an OData connection.

    For a description of the field values, see [ERP Data Hub new system field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-create-new-system-descriptions.md).

5.  Select **Save**.


## Result

After you create a system, you can view heartbeat and retrieval status on the ERP systems list page. For more information, see [View a list of ERP Data Hub systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/view-and-monitor-erp-systems-health.md).

**Parent Topic:**[Working with ERP systems in ERP Data Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/erp-integration-framework/erp-canvas-work-with-systems.md)

