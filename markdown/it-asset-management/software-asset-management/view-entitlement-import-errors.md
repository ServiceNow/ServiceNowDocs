---
title: Import bulk entitlements in Software Asset Management classic
description: You can import multiple entitlements together using a Microsoft Excel spreadsheet in Software Asset Management classic.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Software Asset Management classic, Software Asset Management, IT Asset Management]
---

# Import bulk entitlements in Software Asset Management classic

You can import multiple entitlements together using a Microsoft Excel spreadsheet in Software Asset Management classic.

## Before you begin

Role required: sam\_user or sam\_admin

## About this task

The entitlement import records are stored in the Entitlement import \[samp\_bulk\_import\] table.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Entitlement Import**.

2.  In the Entitlement imports page, select **New**.

    A new entitlement import record opens.

3.  In the Entitlement import page, click **Download template** to download a spreadsheet template\(.xlsx\).

    You can add software entitlement fields to the template to include additional fields in your import. Add each field as a new column in the template. The column name must match the field label exactly. You can include base system software entitlement fields as well as your custom software entitlement fields. To learn how to create a custom field, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

    By default, the **Unit cost** column in the spreadsheet takes into account the currency that your system is set to. However you can manually change the currency and the Software Asset Management application will honor the currency that you specify. To specify a currency, enter the currency code followed by a semicolon and the cost. For example, `EUR;200`. Valid currency codes are the ones listed in the Currency \[fx\_currency\] table and have the **Active** column set to true.

4.  Enter the entitlement details in the template and select **Click to add** to select and upload the spreadsheet.

    Once the file is uploaded, the name of the file appears and the **Description** field is automatically populated.

5.  Select **Import**.

    A confirmation message appears informing you that the import of entitlements is in progress. Once the process is completed, the fields on the page show the number of rows that were processed, successful, and with errors. Once you attach and import a spreadsheet, an import record is created that retains the history of the upload for you to view later.

6.  Select the link on the confirmation message to view the status of the import record.

    The Entitlement Imports page appears listing all the entitlement import records.

7.  Select the entitlement import record to display the Entitlement Import page.

    The Entitlement Import page contains two tabs:

    -   **Entitlements**: lists all the entitlements that got successfully created.
    -   **Relate entitlements**: lists entitlements, such as maintenance entitlements, that are in the build state and can be linked to the base entitlements.
8.  If any errors occur, select **Review import errors** to open the Entitlement Import Errors page.

    Only records whose error status is **Needs review** are listed by default. You may need to reload the page to view **Review import errors**.

9.  Select an import error record to view its errors.

    The Entitlement Import Errors page appears. For a detailed description of the entitlement import error fields, see [Entitlement import error fields](../reference/entitlement-import-error-fields.md).

10. Correct the errors and then select **Import**.

    The entitlement is successfully created. For more information on resolving errors, see [Entitlement import error actions](../reference/import-software-rights-form.md).


**Parent Topic:**[Using Software Asset Management classic](../concept/using-sam-classic.md)

