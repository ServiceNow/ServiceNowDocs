---
title: Create an import task
description: Create an import task for the Service Graph Connector for Microsoft Excel to handle the import of Operational Technology \(OT\) device data from your Microsoft Excel spreadsheet.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-10-15"
reading_time_minutes: 2
breadcrumb: [Using the Service Graph Connector for Microsoft Excel through import tasks, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Create an import task

Create an import task for the Service Graph Connector for Microsoft Excel to handle the import of Operational Technology \(OT\) device data from your Microsoft Excel spreadsheet.

## Before you begin

Role required: ot\_excel\_import\_user

## About this task

Watch this short video to learn how to create an import task in the Industrial Workspace.

Create an import task in the Industrial Workspace 

## Procedure

1.  In the Industrial Workspace, select the **List** \(![List icon](../../../common/image/icon-list.png)\) icon.

2.  Under the OT Excel SGC - Import Task module, select one of the available lists.

3.  Select **New**.

4.  On the form, fill in fields.

5.  Select **Save**.

6.  Refresh the form to access the Microsoft Excel template.

7.  From the **Attachments** panel, download the Microsoft Excel template by selecting the **Actions** ![](../../mftg-manufacturing-ot-knowledge/image/more-actions-vertical.png) icon next to the **sg\_ot\_excel\_staging.xlsx** template and clicking **Download**.

8.  Save the template locally on your computer.

9.  Fill in the template as needed with your OT device data.

    For more information about how to fill out the spreadsheet, see [Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md).

10. From the **Attachments** panel, delete the original template by selecting the **Actions** ![](../../mftg-manufacturing-ot-knowledge/image/more-actions-vertical.png) icon next to the **sg\_ot\_excel\_staging.xlsx** and clicking **Delete**.

11. Upload your completed Microsoft Excel spreadsheet.

    1.  Ensure that you are assigned to the import task so that you can see the **Import Attachment** UI action.

        If you are not in the **Assigned to** field of the import task, click the **Assign to me** UI action before proceeding with the next step.

    2.  Click **Select file**.

    3.  From your local drive, upload the completed Microsoft Excel spreadsheet.

    4.  Once the spreadsheet is updated, select the **Import Attachment** UI action.

    5.  Wait for your system to complete the import process.

        Once complete, the **State** field changes from **Pending staging import** to **Staging import succeeded**.


## Result

After the import process is complete and the Microsoft Excel spreadsheet has been successfully imported, you can view the staging records for your Operational Technology \(OT\) device data by selecting the **Staging Records** tab.

## What to do next

After the import process is complete, you can validate the imported staging records. For more information, see [Validate imported staging records](run-validations.md).

-   **[Prepare your Pre-import OT Worksheet Entry Review tool for Service Graph Connector import](preparing-your-pre-import-ot-worksheet-entry-review-tool-for-sgc-import.md)**  
Prepare your spreadsheet by positioning your existing data in the correct columns is crucial to the success of your upload.

**Parent Topic:**[Using the Service Graph Connector for Microsoft Excel through import tasks](../concept/use-excel-sgc-through-import-tasks.md)

