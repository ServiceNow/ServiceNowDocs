---
title: Import classification codes
description: Import multiple classification codes at one go to your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/import-class-codes-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Asset Management, Asset Management]
---

# Import classification codes

Import multiple classification codes at one go to your ServiceNow instance.

## Before you begin

Role required: sn\_eam.enterprise\_asset\_manager

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **Model classifications** &gt; **Import**.

4.  Select **New**.

5.  On the Create New Enterprise Classification Import page, enter a name for the import in the **Import** field.

6.  Select **Download template** to download a spreadsheet.

7.  Enter the details in the spreadsheet.

    Ensure that you fill out either the Code or the Description column in the spreadsheet. Use commas to specify more than one model category in the Model categories column.

8.  Select **Attach File** to upload the spreadsheet \(.xlsx\).

9.  Select **Import** to perform a validation check on the spreadsheet.

    After you select Import, the Status field changes from **Draft** and moves to **Pending**, **Uploading**, **Transforming**. After the import process is completed, the status changes to either **Completed**, **Completed with errors**, or **Failed**. The details of the import process are displayed in the **Enterprise Classification Import** and **Classification import results** sections.

10. Select the **Classification Import Stagings** related list to view the details of the spreadsheet that you uploaded and also view any errors you received.

11. Open any record for which you got an error.

12. Fix the error, upload the spreadsheet, and import the record again.


