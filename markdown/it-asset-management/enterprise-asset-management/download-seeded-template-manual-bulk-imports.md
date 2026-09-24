---
title: Download seeded templates for manual bulk imports
description: Download seeded templates that you can use for your manual enterprise model and asset imports. You can use the templates as is or modify them based on your organization's needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/download-seeded-template-manual-bulk-imports.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Import enterprise models and assets manually, Bulk import of your enterprise models and assets, Managing enterprise models and assets, Enterprise Asset Management, Asset Management]
---

# Download seeded templates for manual bulk imports

Download seeded templates that you can use for your manual enterprise model and asset imports. You can use the templates as is or modify them based on your organization's needs.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## About this task

Seeded templates are pre-configured for specific import scenarios. They also include a detailed implementation aid that provides comprehensive guidance on the fields and formatting that are required for each import. You can use these templates to import enterprise models only, enterprise assets only, or a combination of both enterprise models and assets.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  In the navigation panel of the Admin center view, select **Bulk import** &gt; **Manual import** &gt; **Seeded template**.

4.  From the list of available templates, select the seeded template that you want to download.

    -   **Seeded Template - Asset Import only**: Template for importing enterprise assets only. Select this option if you want to create or update enterprise assets.
    -   **Seeded Template - Model and Asset Import**: Template for importing both enterprise models and assets. Select this option if you want to create or update both enterprise models and assets.
    -   **Seeded Template - Model Import only**: Template for importing enterprise models only. Select this option if you want to create or update enterprise models.
5.  On the contextual side panel of the template record, select the Attachment icon \[Omitted image "attachments-icon.png"\] Alt text:.

6.  In the Attachments window, select the Actions icon \[Omitted image "configure-options-icon.png"\] Alt text:next to the template name.

7.  From the list of available actions, select **Download**.

    The template downloads as a spreadsheet in the .xlsx format.

8.  Modify the downloaded template based on your organization's needs.

    If your organization has specific import requirements, you can modify the template and upload it for later use. Users across your organization can then download and use the modified template for future imports.

    1.  Open the downloaded template in Microsoft Excel.

    2.  Make any of the following modifications to the template:

        -   Remove the columns for any optional fields that aren't necessary for your imports.

            **Important:** Do not remove the columns for any mandatory fields.

        -   Rearrange the column order to match the structure of your source data.

            **Important:** Do not change the names of any column headers.

    3.  Save the modified template.

    4.  Return to your ServiceNow instance and then reopen the template record.

    5.  In the Attachments window of the template record, select the Add file icon \[Omitted image "add\_content\_icon.png"\] Alt text: to search for and select the modified template that you want to upload.

        The modified template is uploaded to your ServiceNow instance. It is then available to download and use for future imports.


## What to do next

Enter all enterprise model or asset details in the spreadsheet.

**Note:** You must enter values in all mandatory fields of the spreadsheet. If you leave any mandatory fields empty, the import fails. An error message then appears, asking you to check the template format. For the complete list of mandatory fields, see [Mandatory fields in the bulk import spreadsheets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/mandatory-bulk-fields.md).

**Note:** The following optional fields accept only user ID values:

-   **Assigned to**
-   **Managed by**
-   **Reserved for**
-   **Owned by**
-   **Supported by**

**Note:** The optional **Location full name** field helps verify that assets are linked to the correct location. If you provide values for both the **Location full name** and **Location** fields, and the two values don't match, an error message appears and the import for that specific asset is not processed. Similarly, if the specified location can't be found or if multiple locations are found with the same name, an error message appears and the import for that specific asset is also not processed.

