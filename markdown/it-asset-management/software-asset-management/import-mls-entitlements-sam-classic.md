---
title: Import Microsoft entitlements from a Microsoft License Statement \(MLS\) in Software Asset Management classic
description: Import entitlements from an MLS using the Software Asset Management classic application.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Importing entitlements from an MLS, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
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
    |Import type|Type of document that you’re importing software entitlements from. The options are **Standard import document** and **Microsoft license statement \(MLS\)**. Set this field to **Microsoft license statement \(MLS\)**.|
    |File|Spreadsheet of software entitlements that you want to import. Select **Click to add...** to search for and select the MLS Excel file that you requested from Microsoft.|
    |Description|Brief description of the software entitlement import.|
    |Automatic creation of contracts|Option to enable automatic creation of both parent and child contracts for the selected MLS. Refer to [Contracts](https://www.servicenow.com/docs/access?context=c_Contracts&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US) for more information about contracts.|
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
            |Number of entitlements in build state|Number of imported Microsoft Software Assurance \(SA\), Step-up, From SA, or Add-on entitlements that are in the build state and can be linked to a base entitlement.|

        -   To view the complete list of imported entitlements, select the **Entitlements** related list.
        -   If you enabled the **Automatic creation of contracts** option in [step 4](import-mls-entitlements-sam-classic.md#step2), view the list of automatically created contracts by selecting the **Contracts** related list.

            **Note:** These contracts are automatically linked to successfully imported entitlements.

        -   To view the list of imported Microsoft SA, Step-up, From SA, or Add-on entitlements that are in the build state and can be linked to base entitlements, select the **Entitlements in build state** related list.

            See [step 7](import-mls-entitlements-sam-classic.md#assign-base-entitlement) for more information on how to assign a Microsoft SA, Step-up, From SA, or Add-on entitlement to a base entitlement.

7.  If your entitlement import contains any Microsoft SA, Step-up, From SA, or Add-on entitlements, assign those entitlements to base entitlements.

    **Note:** You can assign a From SA or Add-on entitlement to multiple base entitlements.

    1.  On the Entitlement Import record, select the **Entitlements in build state** related list.

    2.  From the list of available Microsoft SA, Step-up, From SA, or Add-on entitlements, select the entitlement that you want to assign to a base entitlement.

    3.  On the corresponding Software Entitlement form, select **Publish**.

    4.  After the form reloads, select the **Related Entitlements** tab.

    5.  In the **Related Entitlement** column of the Related Entitlements list, double-click **Insert a new row**.

    6.  When prompted, search for and select the base entitlement that you want to assign the Microsoft SA, Step-up, From SA, or Add-on entitlement to.

        **Important:** The base entitlement for a From SA or Add-on entitlement must use either the Per User or Per Device license metric. In addition, it cannot already be assigned with another entitlement or have any active allocations.

        **Note:** If an appropriate base entitlement isn’t available for the given Microsoft SA, Step-up, From SA, or Add-on entitlement, you can create one.

    7.  Select the Save \(Enter\) icon ![](../image/save-icon.png).

    8.  Double-click the corresponding field in the **Active rights** column of the Related Entitlements list.

    9.  When prompted, enter the number of Microsoft SA, Step-up, From SA, or Add-on rights that you want to grant to the base entitlement.

        **Important:** For From SA rights, you must enter the total number of rights that you purchased for the base entitlement. For example, if you purchased 100 rights for the base entitlement, you must grant 100 From SA rights to that entitlement. For Add-on rights, you can enter any number of rights equal to or less than the total number of rights that you purchased for the given Add-on entitlement.

    10. Select the Save \(Enter\) icon ![](../image/save-icon.png).

    11. Select **Save** on the Software Entitlement form header.

        The Microsoft SA, Step-up, From SA, or Add-on entitlement is assigned to the specified base entitlement.

    12. Return to the Entitlement Import record and repeat steps a to k for each import that you want to resolve.

8.  If your entitlement import contains any errors, identify and resolve those errors.

    1.  On the Entitlement Import record, select **Review import errors**.

        The Entitlement Import Errors list opens.

    2.  In the **Error status** field, select **Needs review** for the error that you want to resolve.

    3.  Update the corresponding Entitlement Import Error form as needed to resolve the error.

        For descriptions of the Entitlement Import Error form fields, see [Entitlement import error fields](../reference/entitlement-import-error-fields.md). For details about the actions that you can take on entitlement import errors, see [Entitlement import error actions](../reference/import-software-rights-form.md).

    4.  Select **Import**.

        The associated entitlements are reimported without any errors, and you automatically return to the Entitlement Import form.

    5.  Repeat steps a-d for each error that you want to resolve.


**Parent Topic:**[Importing Microsoft entitlements from a Microsoft License Statement \(MLS\)](../concept/importing-mls-entitlements.md)

