---
title: Create a scheduled extraction in Zero Copy Connector for ERP
description: Schedule extraction of information for an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record at a regular interval.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, schedule, extract, interval, data]
breadcrumb: [Extracting and transforming data, Retrieving data, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Create a scheduled extraction in Zero Copy Connector for ERP

Schedule extraction of information for an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record at a regular interval.

## Before you begin

**Important:**

If you have existing scheduled extractions and have upgraded to Zurich or Australia, run the **Scheduled Extraction V2 Move** fix script to place scheduled extractions in a new table where scheduling is done by the scheduled scripts engine. For detailed steps, see [Run fix scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/t_RunFixScripts.md).

You must have a standard or custom ERP extraction table in place to use. For more information, see [Add a new ERP extraction table in Zero Copy Connector for ERP](erp-canvas-add-new-extraction-table.md).

Role required: en\_erp\_integration.erp\_user

This video was recorded in the Zurich release.

Video that shows how to create a scheduled extraction. 

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP scheduled extractions page by selecting the scheduled extractions icon ![](../image/erpc-scheduled-extractions-icon.png) in the side panel.

3.  Select the **New** button.

4.  On the form, fill in the fields.

    For a description of the field values, see [Zero Copy Connector for ERP scheduled extraction field descriptions](../reference/erp-data-hub-scheduled-extraction-field-descriptions.md).

    ![New scheduled extraction fields.](../image/erpc-schedule-extraction-ys2.png)

5.  Select **Save**.

    The scheduled extraction runs on the date and time specified.

6.  To run the extraction immediately, select **Run now** at any time.

    ![Scheduled extraction record with run now button highlighted.](../image/erpc-schedule-extraction-run-now-ys2.png)


## What to do next

Check the executions. After the scheduled job has run, select the **Executions** tab. For details about an extraction, select any line item in the **Extraction table** column.

![ERP scheduled extraction executions list.](../image/erpc-view-extraction-executions-ys2.png)

**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](../concept/erp-canvas-extraction-tables.md)

