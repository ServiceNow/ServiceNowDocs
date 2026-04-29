---
title: Upload, validate, and import the OT device inventory spreadsheet
description: Chat with an AI agent in the Now Assist panel to begin the process for uploading, validating, and importing your Operational Technology \(OT\) device data into the OT CMDB.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Import your device spreadsheet into OT CMDB, Use agentic AI in the OTM application, OT Manager Foundation, Operational Technology]
---

# Upload, validate, and import the OT device inventory spreadsheet

Chat with an AI agent in the Now Assist panel to begin the process for uploading, validating, and importing your Operational Technology \(OT\) device data into the OT CMDB.

## Before you begin

The Now Assist panel must be activated. For more information, see [Activate the Now Assist panel standard chat](https://www.servicenow.com/docs/access?context=activate-now-assist-panel&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: ot\_excel\_import\_user and now\_assist\_panel\_user

## Procedure

1.  Select the **Now Assist** ![](../image/now-assist-icon.png) icon.

    The Now Assist panel is displayed.

2.  To initiate the Import OT device spreadsheet into OT CMDB agentic workflow, enter a prompt such as `I want to import an OT device`.

    The OT Excel import task AI agent begins the workflow process and creates an OT Excel SGC Import Task record. For more information about import tasks, see [Using the Service Graph Connector for Microsoft Excel through import tasks](../../mftg-manufacturing-oper-tech-mgr/concept/use-excel-sgc-through-import-tasks.md).

3.  Select **Open OT Excel SGC Import Task**.

4.  In Attachment panel of the import task record, download and save the Microsoft Excel spreadsheet template to your local drive.

    ![Downloading the Microsoft Excel spreadsheet from the OT import task with the Now Assist panel open.](../image/download-spreadsheet-now-assist-otm.png)

5.  Once you have filled out the spreadsheet with your OT device inventory, upload it in the Attachment panel.

    For more information about how to fill out the spreadsheet, see [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](../../mftg-manufacturing-oper-tech-mgr/task/preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md).

6.  In the Now Assist panel, enter a prompt such as `Done` to alert the agent that you have uploaded the spreadsheet.

    The agent uploads the spreadsheet to the SG OT Excel Stagings table. Wait for the **State** field of the import task record to update to **Staging import succeeded** and for the staging records to be created. You can view the staging records in the import task record's **Staging Records** tab.

7.  Once the import is complete, enter a prompt in the Now Assist panel to alert the agent that the import was successful and can proceed to the next step, such as `Yes, proceed`.

    The agent validates the staging records and replies with the number of valid records, partially valid records, and invalid records. For invalid records, the agent asks if you want to create a remediation task.

8.  If you want to create a remediation task for the invalid records, enter `Yes`.

    The agent creates a remediation task for all invalid records so you can resolve them as needed. For more information about possible validation errors, see [Managing Validations](../../mftg-manufacturing-oper-tech-mgr/concept/managing-validations.md).

    The agent then asks if you want to proceed importing the valid or partially invalid staging records.

9.  To import the valid or partially valid staging records, enter `Yes`.

    The agent triggers the CMDB import process. The **State** field of the import task record changes to **Pending CMDB import**. Once the import process is complete, the **State** field changes to **CMDB import complete**.

    The AI agent asks if you require any further assistance.

10. If no further assistance is needed, enter `No` to conclude the AI agent session.


## What to do next

To verify the CMDB import, navigate to the Industrial Workspace list view and open the **All OT Devices** list. The recently imported OT device records should appear in the list.

**Parent Topic:**[Import the OT device spreadsheet into OT CMDB agentic workflow](../concept/now-assist-otm-aiagents-import-ot-device-workflow.md)

