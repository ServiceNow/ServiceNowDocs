---
title: Import classification codes
description: Import multiple classification codes at one go to your ServiceNow instance.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create and manage enterprise models, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Import classification codes

Import multiple classification codes at one go to your ServiceNow instance.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Model classifications** &gt; **Import**.

2.  Select **New**.

3.  On the Create New Enterprise Classification Import page, enter a name for the import in the **Import** field.

4.  Select **Download template** to download a spreadsheet.

5.  Enter the details in the spreadsheet.

    Ensure that you fill out either the Code or the Description column in the spreadsheet. Use commas to specify more than one model category in the Model categories column.

6.  Select **Attach File** to upload the spreadsheet \(.xlsx\).

7.  Select **Import** to perform a validation check on the spreadsheet.

    After you select Import, the Status field changes from **Draft** and moves to **Pending**, **Uploading**, **Transforming**. After the import process is completed, the status changes to either **Completed**, **Completed with errors**, or **Failed**. The details of the import process are displayed in the **Enterprise Classification Import** and **Classification import results** sections.

8.  Select the **Classification Import Stagings** related list to view the details of the spreadsheet that you uploaded and also view any errors you received.

9.  Open any record for which you got an error.

10. Fix the error, upload the spreadsheet, and import the record again.


**Parent Topic:**[Create and manage enterprise models](../concept/create-manage-enterprise-models.md)

