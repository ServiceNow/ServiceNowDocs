---
title: Upload, validate, and import the OT device inventory spreadsheet
description: Chat with an AI agent in the ServiceNowOtto panel to begin the process for uploading, validating, and importing your Operational Technology \(OT\) device data into the OT CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/upload-import-validate-ot-device-inventory-spreadsheet.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 3
breadcrumb: [Import your device spreadsheet into OT CMDB, Agentic AI for the Operational Technology Manager, Use, Operational Technology Manager, Operational Technology]
---

# Upload, validate, and import the OT device inventory spreadsheet

Chat with an AI agent in the ServiceNowOtto panel to begin the process for uploading, validating, and importing your Operational Technology \(OT\) device data into the OT CMDB.

## Before you begin

The ServiceNowOtto panel must be activated. For more information, see [Activate the panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).

Role required: ot\_excel\_import\_user and now\_assist\_panel\_user

## Procedure

1.  Select the ServiceNowOtto \[Omitted image "now-assist-icon.png"\] Alt text: icon.

    The ServiceNowOtto panel is displayed.

2.  Enter a prompt such as `I want to import an OT device` to initiate the Import OT device spreadsheet into OT CMDB agentic workflow.

    The OT Excel import task AI agent begins the workflow process and creates an OT Excel SGC Import Task record. For more information about import tasks, see [Using the Service Graph Connector for Microsoft Excel through import tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/use-excel-sgc-through-import-tasks.md).

3.  Select **Open OT Excel SGC Import Task**.

4.  In the Attachment panel of the import task record, download and save the Microsoft Excel spreadsheet template to your local drive.

    \[Omitted image "download-spreadsheet-now-assist-otm.png"\] Alt text: Downloading the Microsoft Excel spreadsheet from the OT import task with the ServiceNowOtto panel open.

5.  After you fill out the spreadsheet with your OT device inventory, upload it in the Attachment panel.

    For more information about how to fill out the spreadsheet, see [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md).

6.  In the ServiceNowOtto panel, enter a prompt such as `Done` to alert the agent that you have uploaded the spreadsheet.

    The agent uploads the spreadsheet to the SG OT Excel Stagings table. Wait for the **State** field of the import task record to update to **Staging import succeeded** and for the staging records to be created. You can view the staging records in the import task record's **Staging Records** tab.

7.  After the import is complete, enter a prompt in the ServiceNowOtto panel, such as `Yes, proceed`.

    The prompt alerts the agent that the import was successful and can proceed to the next step. The agent validates the staging records and replies with the number of valid records, partially valid records, and invalid records. For invalid records, the agent asks whether to create a remediation task.

8.  If you want to create a remediation task for the invalid records, enter `Yes`.

    The agent creates a remediation task for all invalid records so you can resolve them as needed. For more information about possible validation errors, see [Managing Validations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/managing-validations.md).

    The agent then asks whether to proceed importing the valid or partially invalid staging records.

9.  To import the valid or partially valid staging records, enter `Yes`.

    The agent triggers the CMDB import process. The **State** field of the import task record changes to **Pending CMDB import**. After the import process is complete, the **State** field changes to **CMDB import complete**.

    The AI agent asks if you require any further assistance.

10. If no further assistance is needed, enter `No` to conclude the AI agent session.


## What to do next

To verify the CMDB import, navigate to the Industrial Workspace list view and open the **All OT Devices** list. The recently imported OT device records appear in the list.

**Parent Topic:**[Import the OT device spreadsheet into OT CMDB agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/now-assist-otm-aiagents-import-ot-device-workflow.md)

