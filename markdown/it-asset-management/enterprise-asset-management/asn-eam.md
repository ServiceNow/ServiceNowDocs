---
title: Use Advanced Shipment Notification in Enterprise Asset Management
description: Use Advanced Shipment Notification \(ASN\) to automate and create enterprise asset records for when your assets are in transit.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Enterprise Asset Management by enterprise administrators, Configuring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Use Advanced Shipment Notification in Enterprise Asset Management

Use Advanced Shipment Notification \(ASN\) to automate and create enterprise asset records for when your assets are in transit.

## Before you begin

Download your ASN template and have your asset vendor update it. Upload the updated template to your ServiceNow instance. Before using the ASN template to import asset records, ensure that your ServiceNow instance has the model ID defined and that the same model ID is mentioned in the template.

Role required: sn\_eam.enterprise\_admin

## About this task

Creating enterprise asset records manually is time consuming and can lead to errors. Use ASN to reduce the risk of shipment going missing or misplaced and increase inventory accuracy.

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Asset operations** &gt; **Shipment Notifications**.

2.  Select **New**.

    The Create New Shipment Notification Upload page appears.

3.  Enter a unique name for the ASN in the **Name** field.

4.  Select **Attach File** to upload a spreadsheet \(.xlxs\).

    The spreadsheet should be in the format of the download template. If you do not have a sample spreadsheet, select **Download template** to download a sample spreadsheet, fill in the details in the spreadsheet, and then select **Attach File**to upload the spreadsheet. Ensure that in the spreadsheet the format for **Ship date**, **Order date**, and **Warranty end date** fields is `month/date/year`.

    The upload may take some time. Once the file is uploaded, the name of the spreadsheet appears in the **File** field.

5.  Select **Import** to perform a validation check on the spreadsheet.

    After you select **Import**, the **Status** field changes from **Draft** and moves to **Pending**, **Extracting Rows** and **Importing**. Once the import process is completed, the status changes to either **Completed**, **Completed with errors**, or **Failed**.

    The **Shipment Upload Result** section appears that gives information on the import process. Information such as how many records were inserted, ignored or skipped.

6.  Select **Shipment Notification Upload Stagings** related link to view any errors you received as well as to view the details of the spreadsheet that you uploaded.

7.  If you got an error, select the record in **Shipment Notification Upload Stagings** related link.

8.  Scroll down to the **Errors** section and view the error in the **Comment** field.

9.  Fix the error, upload the spreadsheet, and import the record again.

    Serialized assets do not have duplicate enterprise import records created, but consumables do have duplicate entries.


**Parent Topic:**[Configuring Enterprise Asset Management by enterprise administrators](../concept/config-eam-enterrpriseadmins.md)

