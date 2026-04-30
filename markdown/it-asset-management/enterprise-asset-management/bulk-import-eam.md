---
title: Import enterprise models and assets in workspace
description: Import multiple enterprise models and assets at one go in the Enterprise Asset Workspace.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring Enterprise Asset Management by enterprise administrators, Configuring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# Import enterprise models and assets in workspace

Import multiple enterprise models and assets at one go in the Enterprise Asset Workspace.

## Before you begin

You can import enterprise models and assets of different types such as simple, pre-assembled, user-assembled assets, and consumables. You can also view the import errors and status.

The enterprise models and asset import records are stored in Enterprise Bulk Import \[sn\_eam\_bulk\_import\] table.

The Flow Designer application is used to initiate the EAM Bulk Import sub flow to assist you in importing enterprise models and assets. As the flow takes you through the various stages, the import details are automatically updated. You can open the EAM Bulk Import flow to view the status of the stages in the flow.

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Asset operations**.

2.  Select any of the import actions under **Bulk Import**.

3.  Select **New**.

    The Create New Enterprise Bulk Import page opens.

4.  Enter a unique name for the import process in the **Name** field.

5.  Select a mode for the import in the **Mode** field.

6.  Select **Download template** to download a spreadsheet.

    Based on the mode you select, a spreadsheet is available. Templates are available for models, for assets, and a combined template for models and assets.

7.  Enter the details in all the mandatory fields in the spreadsheet.

    If you don’t enter values in all the mandatory columns in the template, the import fails, and an error message appears asking you to check the template format. For details on mandatory fields, see [Mandatory fields in the bulk import spreadsheets](../reference/mandatory-bulk-fields.md).

8.  Select **Attach File** to upload the spreadsheet \(.xlsx\).

9.  Select **Import** to perform a validation check on the spreadsheet.

    After you select Import, the Status field changes from **Draft** and moves to **Pending**, **Uploading**, **Transforming**. After the import process is completed, the status changes to either **Completed**, **Completed with errors**, or **Failed**. You can view details regarding the result of the import process for models and assets in the **Model import result** and **Asset import result** sections.

10. Select **Model Import staging**, **Model component Import staging**, or **Asset Import Staging** related lists to view the details of the spreadsheet that you uploaded and also view any errors you received.

11. Open any record for which you got an error.

12. Fix the error, upload the spreadsheet, and import the record again.


**Parent Topic:**[Configuring Enterprise Asset Management by enterprise administrators](../concept/config-eam-enterrpriseadmins.md)

