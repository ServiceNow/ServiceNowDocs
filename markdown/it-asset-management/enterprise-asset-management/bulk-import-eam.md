---
title: Manually import enterprise models and assets in the Enterprise Asset Workspace
description: Manually import multiple enterprise models and assets in one go in the Enterprise Asset Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/bulk-import-eam.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Bulk import of your enterprise models and assets, Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Manually import enterprise models and assets in the Enterprise Asset Workspace

Manually import multiple enterprise models and assets in one go in the Enterprise Asset Workspace.

## Before you begin

Download and update the appropriate template for your import. This template, which is a spreadsheet in the .xlsx or .xls format, must contain all external enterprise model and asset data that you want to import. For detailed instructions, see [Download seeded templates for manual bulk imports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/download-seeded-template-manual-bulk-imports.md).

Role required: sn\_eam.enterprise\_admin

## About this task

You can import enterprise models and assets of different types such as simple, pre-assembled, user-assembled assets, and consumables. You can also view the import errors and status.

The enterprise models and asset import records are stored in the Enterprise Bulk Import \[sn\_eam\_bulk\_import\] table.

The Flow Designer application is used to initiate the EAM Bulk Import subflow to assist you in importing enterprise models and assets. As the flow takes you through the various stages, the import details are automatically updated. You can open the EAM Bulk Import flow to view the status of the stages in the flow.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  In the navigation panel of the Admin center view, select **Bulk import** &gt; **Manual import**.

4.  Depending on the type of import that you want to perform, select one of the following manual import options:

    -   **Create models and assets**: Manually import new enterprise models and assets.
    -   **Create models**: Manually import new enterprise models.
    -   **Create assets**: Manually import new enterprise assets.
    -   **Update models and assets**: Manually import existing enterprise models and assets that have been updated.
    -   **Update models**: Manually import existing enterprise models that have been updated.
    -   **Update assets**: Manually import existing enterprise assets that have been updated.
5.  On the corresponding import page, select **New**.

    The Create New Enterprise Bulk Import page opens.

    **Note:** At any point during the bulk import process, you can view detailed import guidelines by selecting the Bulk import job instructions icon \[Omitted image "bulk-imp-instructions-icon.png"\] Alt text: on the contextual side bar of the Create New Enterprise Bulk Import page.

6.  Enter a unique name for the import process in the **Name** field.

7.  Select a mode for the import in the **Mode** field.

8.  Select **Attach File** to upload the spreadsheet \(.xlsx or .xls\) that contains your enterprise model or asset data.

9.  Select **Import** to perform a validation check on the spreadsheet.

    After you select Import, the Status field changes from **Draft** and moves to **Pending**, **Uploading**, **Transforming**. After the import process is completed, the status changes to either **Completed**, **Completed with errors**, or **Failed**. You can view details regarding the result of the import process for models and assets in the **Model import result** and **Asset import result** sections.

10. Select **Model Import staging**, **Model component Import staging**, or **Asset Import Staging** related lists to view the details of the spreadsheet that you uploaded and also view any errors you received.

11. Open any record for which you got an error.

12. Fix the error, upload the spreadsheet, and import the record again.


