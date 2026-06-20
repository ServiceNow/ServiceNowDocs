---
title: Create a scheduled extraction in Zero Copy Connector for ERP
description: Schedule extraction of information for an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record at a regular interval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/erp-integration-framework/erpc-create-a-scheduled-extraction.html
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Extracting and transforming data in Zero Copy Connector for ERP, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Create a scheduled extraction in Zero Copy Connector for ERP

Schedule extraction of information for an ERP \(Enterprise Resource Planning\) extraction table to capture large amounts of data from the system of record at a regular interval.

## Before you begin

You must have a standard or custom ERP extraction table in place to use. For more information, see [Add a new ERP extraction table in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-add-new-extraction-table.md).

Role required: en\_erp\_integration.erp\_user

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the ERP scheduled extractions page by selecting the Scheduled extractions icon \(\[Omitted image "erpc-scheduled-extractions-icon.png"\] Alt text: Scheduled extractions icon\) in the side panel.

3.  Select the **New** button.

4.  On the form, fill in the fields.

    For a description of the field values, see [Zero Copy Connector for ERP scheduled extraction field descriptions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-data-hub-scheduled-extraction-field-descriptions.md).

    \[Omitted image "erpc-schedule-extraction-ys2.png"\] Alt text: New scheduled extraction fields.

5.  Select **Save**.

    The scheduled extraction runs on the date and time specified.

6.  To run the extraction immediately, select **Run now** at any time.

    \[Omitted image "erpc-schedule-extraction-run-now-ys2.png"\] Alt text: Scheduled extraction record with run now button highlighted.


## What to do next

Check the executions. After the scheduled job has run, select the **Executions** tab. For details about an extraction, select any line item in the **Extraction table** column.

\[Omitted image "erpc-view-extraction-executions-ys2.png"\] Alt text: ERP scheduled extraction executions list.

**Parent Topic:**[Extracting and transforming data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/erp-integration-framework/erp-canvas-extraction-tables.md)

