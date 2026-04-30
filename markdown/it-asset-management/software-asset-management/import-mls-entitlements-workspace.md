---
title: Import Microsoft entitlements from a Microsoft License Statement \(MLS\) in the Software Asset Workspace
description: Import entitlements from an MLS using the Software Asset Workspace.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Importing Microsoft entitlements from a Microsoft License Statement \(MLS\), Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Import Microsoft entitlements from a Microsoft License Statement \(MLS\) in the Software Asset Workspace

Import entitlements from an MLS using the Software Asset Workspace.

## Before you begin

Before you can import entitlements from an MLS, you must request the MLS from Microsoft. Microsoft provides the MLS as an Excel file.

Role required: sam\_user or sam\_admin

## Procedure

1.  From your ServiceNow instance, navigate to **Software asset** &gt; **Software Asset Workspace**.

    The Software Asset Workspace launches in a new tab, displaying the Software asset overview.

2.  On the Software asset overview, select **Create entitlement**.

    The Create new entitlement dialog box opens.

3.  In the dialog box, select **Import multiple entitlements from an Excel file** and then select **Next**.

    The dialog box closes and then the Create New Entitlement Import form opens in a new tab.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Import type|Type of document that you are importing entitlements from. Set this field to **Microsoft license statement \(MLS\)**.|
    |File|File that you want to import entitlements from. Search for and select the MLS Excel file that you requested from Microsoft.|
    |Description|Description of the entitlement import. This field populates automatically based on the file that you selected in the **File** field.|
    |Automatic creation of contracts|Option to enable automatic creation of both parent and child contracts for the selected MLS. Refer to [Contracts](https://www.servicenow.com/docs/access?context=c_Contracts&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) for more information about contracts.|
    |Import status|Status of the import. This field populates automatically.|

5.  Select **Import**.

    A confirmation message appears, informing you that the import is in progress. You can select the link in the message to open the Entitlement import list, which provides the status of your import and the complete list of entitlement imports.

6.  After the import is complete, open the corresponding entitlement import record to view additional information about the import.

    1.  From the Entitlement import view, select your MLS entitlement import.

        The corresponding entitlement import record opens.

    2.  Use the following options to view additional information about the import:

        -   To view additional information about the import status, refer to the following fields on the **Details** tab:

<table id="table_pqn_f3g_qrb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Import status

</td><td>

Status of the import.

</td></tr><tr><td>

Number of rows processed

</td><td>

Number of Excel rows that were processed during the import.

</td></tr><tr><td>

Number of rows successful

</td><td>

Number of Excel rows that imported successfully.

</td></tr><tr><td>

Number of rows with errors

</td><td>

Number of Excel rows that imported with errors.

</td></tr><tr><td>

Number of entitlements in build state

</td><td>

Number of imported Microsoft Software Assurance \(SA\), Step-up, From SA, or Add-on entitlements that are in the build state and can be linked to a base entitlement.See [step 7](import-mls-entitlements-workspace.md#import-errors) for more information on how to assign a Microsoft SA, Step-up, From SA, or Add-on entitlement to a base entitlement.

</td></tr></tbody>
</table>        -   To view the complete list of imported entitlements, select the **Entitlements** tab.
        -   If you enabled the **Automatic creation of contracts** option in [step 4](import-mls-entitlements-workspace.md#step4), view the complete list of automatically created contracts on the **Contracts** tab.

            **Note:** These contracts are automatically linked to successfully imported entitlements.

7.  If your entitlement import contains any errors, identify and resolve those errors.

    1.  On the entitlement import record, select **Review import errors**.

        The corresponding Review entitlement import errors view opens.

    2.  Use one or both of the following options to resolve your import errors:

        -   Resolve errors related to your imported entitlements.
            1.  Select the **Import errors** tab.
            2.  In the **Error status** field, select **Needs review** for the error that you want to resolve.

                The corresponding entitlement import error record opens in a new tab.

            3.  Update the record as needed to resolve the error.

                For descriptions of the entitlement import error fields, see [Entitlement import error fields](../reference/entitlement-import-error-fields.md). For details about the actions that you can take on entitlement import errors, see [Entitlement import error actions](../reference/import-software-rights-form.md).

            4.  Select **Import**.

                The associated entitlements are re-imported without any errors.

            5.  Close the record to return to the Review entitlement import errors view.
            6.  Repeat steps i-v for each error that you want to resolve.
        -   Resolve errors in which imported Microsoft SA, Step-up, From SA, or Add-on entitlements are not assigned to any base entitlements.

            **Note:** You can assign a From SA or Add-on entitlement to multiple base entitlements.

            1.  Select the **Relate entitlements** tab.
            2.  From the list of available Microsoft SA, Step-up, From SA, or Add-on entitlements, select the entitlement that you want to assign to a base entitlement.
            3.  On the software entitlement record, select **Publish**.
            4.  After the record reloads, select the **Related Entitlements** tab and then select **New**.
            5.  On the form, fill in the fields.

<table id="table_pzq_r54_4rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain

</td><td>

Domain that the base entitlement applies to. The default value is **global**.

</td></tr><tr><td>

Software Entitlement

</td><td>

Microsoft SA, Step-up, From SA, or Add-on entitlement that you want to assign to a base entitlement. This field populates automatically.

</td></tr><tr><td>

Related Entitlement

</td><td>

Base entitlement that you want to assign your Microsoft SA, Step-up, From SA, or Add-on entitlement to.**Important:** The base entitlement for a From SA or Add-on entitlement must use either the Per User or Per Device license metric. In addition, it cannot already be assigned with another entitlement or have any active allocations.

**Note:** If an appropriate base entitlement is not available for the given Microsoft SA, Step-up, From SA, or Add-on entitlement, you can create one.

</td></tr><tr><td>

Active rights

</td><td>

Number of Microsoft SA, Step-up, From SA, or Add-on rights that you want to grant to the base entitlement.**Important:** For From SA rights, you must enter the total number of rights that you purchased for the base entitlement. For example, if you purchased 100 rights for the base entitlement, you must grant 100 From SA rights to that entitlement. For Add-on rights, you can enter any number of rights equal to or less than the total number of rights that you purchased for the given Add-on entitlement.

</td></tr></tbody>
</table>            6.  Select **Save**.
            7.  Close the software entitlement record to return to the Review entitlement import errors view.
            8.  Repeat steps i-vii for each Microsoft SA, Step-up, From SA, or Add-on entitlement that you want to assign to a base entitlement.

**Parent Topic:**[Importing Microsoft entitlements from a Microsoft License Statement \(MLS\)](../concept/importing-mls-entitlements.md)

