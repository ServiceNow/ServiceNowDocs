---
title: Import bulk entitlements in workspace
description: You can import multiple entitlements at one go in the Software Asset Workspace.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Software Asset Workspace, Software Asset Management, IT Asset Management]
---

# Import bulk entitlements in workspace

You can import multiple entitlements at one go in the Software Asset Workspace.

## Before you begin

Role required: sam\_user or sam\_admin

## About this task

The entitlement import records are stored in the Entitlement import \[samp\_bulk\_import\] table. The **Publisher part number**, **Product**, and **Publisher** columns in the Entitlement import \[samp\_bulk\_import\] table offer drop-down lists for value selection.

You can leverage the Activity center in the Software asset overview landing page to view import errors and the import status.

## Procedure

1.  Navigate to **All** &gt; **Software asset** &gt; **Software Asset Workspace**.

2.  Select **Create entitlement**.

    ![Bulk import of entitlements](../image/create-bulkimport.png)

3.  In the Create new entitlement dialog box, select **Import multiple entitlements from an Excel file** and select **Next**.

4.  In the Create New Entitlement Import page, select **Download template** to download a spreadsheet template \(.xlsx\).

    You can add software entitlement fields to the template to include additional fields in your import. Add each field as a new column in the template. The column name must match the field label exactly. Besides the Publisher, Product, Version, Edition, Platform and Language, the Install condition name column is also taken into account to find the correct software model while importing entitlements.

    You can include base system software entitlement fields as well as your custom software entitlement fields. Custom choice columns \(where the type is Choice\) created in the Asset \[alm\_asset\] or Software Entitlement \[alm\_license\] table are also supported.

    **Note:** By default, the **Unit cost** column in the spreadsheet takes into account the currency that your system is set to. However you can manually change the currency and the Software Asset Management application will honor the currency that you specify. To specify a currency, enter the currency code followed by a semicolon and the cost. For example, `EUR;200`. Valid currency codes are the ones listed in the Currency \[fix\_currency\] table and have the **Active** column set to true.

    In the spreadsheet template, if the **Publisher Part Number** column doesn't have a value or the value is invalid and the **Publisher** and **Product** columns have valid values, then during the import process, a software model is automatically created. The source type **entitlement\_import** gets stamped to the automatically created software model. The system property com.snc.samp.smcreation\_on\_entitlement\_import is used to control the software model creation on entitlement import. If you don't want the automatic creation of software models during the import process, you can set this property to false.

5.  Enter the entitlement details in the template and select **Attach File** to upload the spreadsheet.

    Once the file is uploaded, the name of the file appears and the **Description** field is automatically populated. You can change the description to make it more specific.

6.  Select **Import**.

    An import record is created that retains the history of the upload for you to view later.

    A confirmation message appears informing you that the import of entitlements is in progress. Once the import record is processed, the **Status** field displays one of the following values: **Completed**, **Completed with errors**, or **Failed**.

7.  Select the link in the confirmation message to check the status of the record.

    The License operations view appears displaying the entitlement record in the Entitlement Import page

8.  Open the entitlement record to view its details.

9.  Click the **Entitlements** tab to view the list of entitlements that got successfully created.

    **Note:** The **Entitlements** tab only appears if the **Status** field displays the values, **Completed**, or **Completed with errors**.

10. If any errors occur and the status says **Completed with errors**, click **Review import errors**.

    The Review entitlement import errors page opens containing two tabs:

    -   **Import errors**: displays records whose error status is **Needs review**.
    -   **Relate entitlements**: lists entitlements, such as maintenance entitlements, that are in the build state and can be linked to the base entitlements.
11. Select the import error record to view the errors.

    If an import error record doesn't have a software model but the **Publisher** and **Product** fields have valid values, then on selecting **Import**, a software model is automatically created and the status of the record changes to **Manually fixed**.

    For a detailed description of the entitlement import error fields, see [Entitlement import error fields](../reference/entitlement-import-error-fields.md)

12. Correct the errors and select **Import**.

    The entitlement is successfully created. Further processing of the entitlement continues such as validation of downgrade models for the entitlement. For more information on resolving errors, see [Entitlement import error actions](../reference/import-software-rights-form.md).


**Parent Topic:**[Using Software Asset Workspace](../concept/using-sam-workspace.md)

