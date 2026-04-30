---
title: Import Microsoft entitlements from a Microsoft License Statement \(MLS\) in Software Asset Management classic
description: Import entitlements from an MLS using the Software Asset Management classic application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Importing Microsoft entitlements from a Microsoft License Statement \(MLS\), Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Import Microsoft entitlements from a Microsoft License Statement \(MLS\) in Software Asset Management classic

Import entitlements from an MLS using the Software Asset Management classic application.

## Before you begin

Before you can import entitlements from an MLS, you must request the MLS from Microsoft. Microsoft provides the MLS as an Excel file.

Role required: sam\_user or sam\_admin

## Procedure

1.  On the page header of your ServiceNow® instance, select **All**.

2.  In the menu navigation filter, enter `samp_bulk_import_list.do`.

    The Entitlement Imports \[samp\_bulk\_import\] table opens.

3.  Select **New**.

4.  On the Entitlement Import form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Import type|Type of document that you are importing software entitlements from. The options are **Standard import document** and **Microsoft license statement \(MLS\)**. Set this field to **Microsoft license statement \(MLS\)**.|
    |File|Spreadsheet of software entitlements that you want to import. Select **Click to add...** to search for and select the MLS Excel file that you requested from Microsoft.|
    |Description|Brief description of the software entitlement import.|
    |Automatic creation of contracts|Option to enable automatic creation of both parent and child contracts for the selected MLS. Refer to [Contracts](https://www.servicenow.com/docs/access?context=c_Contracts&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US) for more information about contracts.|
    |Import status|Status of the import. This field populates automatically.|

5.  Select **Import**.

    A confirmation message appears, informing you that the import is in progress. You can select the link in the message to open the Entitlement import list in the Software Asset Workspace, which provides the status of your import and the complete list of entitlement imports.

6.  After the import is complete, open the corresponding entitlement import record to view additional information about the import.

    1.  From the Entitlement Imports \[samp\_bulk\_import\] table, select your MLS entitlement import.

    2.  Use the following options to view additional information about the import:

        -   To view additional information about the import status, refer to the following fields:

            |Field|Description|
            |-----|-----------|
            |Import status|Status of the import.|
            |Number of rows processed|Number of Excel rows that were processed during the import.|
            |Number of rows successful|Number of Excel rows that imported successfully.|
            |Number of rows with errors|Number of Excel rows that imported with errors.|
            |Number of entitlements in build state|Number of imported Microsoft Software Assurance \(SA\) or Step-up entitlements that are in the build state and can be linked to a base entitlement.|

        -   To view the complete list of imported entitlements, select the **Entitlements** related list.
        -   If you enabled the **Automatic creation of contracts** option in [step 4](import-mls-entitlements-sam-classic.md#step2), view the list of automatically created contracts by selecting the **Contracts** related list.

            **Note:** These contracts are automatically linked to successfully imported entitlements.

        -   To view the list of imported Microsoft SA or Step-up entitlements that are in the build state and can be linked to base entitlements, select the **Entitlements in build state** related list.

            See [step 7](import-mls-entitlements-sam-classic.md#assign-base-entitlement) for more information on how to assign a Microsoft SA or Step-up entitlement to a base entitlement.

7.  If your entitlement import contains any Microsoft SA or Step-up entitlements, assign those entitlements to base entitlements.

    1.  On the Entitlement Import record, select the **Entitlements in build state** related list.

    2.  From the list of available Microsoft SA or Step-up entitlements, select the entitlement that you want to assign to a base entitlement.

    3.  On the corresponding Software Entitlement form, select **Publish**.

    4.  After the form reloads, select the **Related Entitlements** tab.

    5.  In the **Related Entitlement** field, double-click **Insert a new row**.

    6.  When prompted, search for and select the base entitlement that you want to assign the Microsoft SA or Step-up entitlement to, and then select the Save icon \(![Save icon.](../image/save-icon.png)\).

        **Note:** If an appropriate base entitlement is not available for the specified Microsoft SA or Step-up entitlement, you can create one.

    7.  Double-click the corresponding **Active rights** field.

    8.  When prompted, enter the number of rights that you want to grant to the base entitlement and then select the Save icon \(![Save icon.](../image/save-icon.png)\).

    9.  Select **Save** on the Software Entitlement form header.

        The Microsoft SA or Step-up entitlement is assigned to the specified base entitlement.

    10. Return to the Entitlement Import record and repeat steps a to i for each import that you want to resolve.

8.  If your entitlement import contains any errors, identify and resolve those errors.

    1.  On the Entitlement Import record, select **Review import errors**.

        The Entitlement Import Errors list opens.

    2.  In the **Error status** field, select **Needs review** for the error that you want to resolve.

    3.  Update the corresponding Entitlement Import Error form as needed to resolve the error.

        For descriptions of the Entitlement Import Error form fields, see [Entitlement import error fields](../reference/entitlement-import-error-fields.md). For details about the actions that you can take on entitlement import errors, see [Entitlement import error actions](../reference/import-software-rights-form.md).

    4.  Select **Import**.

        The associated entitlements are re-imported without any errors, and you automatically return to the Entitlement Import form.

    5.  Repeat steps a-d for each error that you want to resolve.


**Parent Topic:**[Importing Microsoft entitlements from a Microsoft License Statement \(MLS\)](../concept/importing-mls-entitlements.md)

