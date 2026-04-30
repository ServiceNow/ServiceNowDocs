---
title: Red Hat Enterprise Linux entitlements
description: Software entitlements define the license details for your Red Hat Enterprise Linux \(RHEL\) products. You can create individual entitlements or import a list of entitlements from a spreadsheet.Create individual software entitlements for your Red Hat Enterprise Linux \(RHEL\) products.Import a list of Red Hat Enterprise Linux \(RHEL\) software entitlements from a spreadsheet.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Software Asset Management for Red Hat Enterprise Linux, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Red Hat Enterprise Linux entitlements

Software entitlements define the license details for your Red Hat Enterprise Linux \(RHEL\) products. You can create individual entitlements or import a list of entitlements from a spreadsheet.

**Important:** You can create and import entitlements in both the Software Asset Management classic application and the Software Asset Workspace. The following sections provide details on how to create and import entitlements in the Software Asset Management classic application. For details on how to create entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md). For details on how to import entitlements in the Software Asset Workspace, see [Import bulk entitlements in workspace](../task/import-entitlements-workspace.md).

**Parent Topic:**[Software Asset Management for Red Hat Enterprise Linux](rhel-publisher-pack.md)

## Create entitlements for Red Hat Enterprise Linux

Create individual software entitlements for your Red Hat Enterprise Linux \(RHEL\) products.

### Before you begin

Role required: sam\_user or sam\_admin

**Important:** You can create entitlements in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on how to create entitlements in the Software Asset Management classic application. For details on how to create entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).

### Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **Portfolios** &gt; **Software Entitlement**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_cjg_xfn_mnb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the software entitlement. This field is automatically set based on the **Asset tag** and **Software model** fields.

</td></tr><tr><td>

Asset tag

</td><td>

Serial number and bar code that are used to identify and track the asset.

</td></tr><tr><td>

Publisher part number

</td><td>

Publisher part number \(PPN\) for the entitlement.

</td></tr><tr><td>

Software model

</td><td>

Software model that has the entitlement.

</td></tr><tr><td>

Agreement type

</td><td>

Type of license agreement. Possible values include the following:-   Generic
-   Enterprise License Agreement \(ELA\)


</td></tr><tr><td>

License type

</td><td>

Type of license. Set this field to **Subscription**.

</td></tr><tr><td>

Subscription period

</td><td>

Length of time for which the subscription is valid. This field appears only when **Subscription** is selected from the **License type** field.

</td></tr><tr><td>

Start date

</td><td>

Date when the subscription begins. This field appears only when **Subscription** is selected from the **License type** field.

</td></tr><tr><td>

End date

</td><td>

Date when the subscription expires. Do not select a date if the subscription does not expire. This field appears only when **Subscription** is selected from the **License type** field.

</td></tr><tr><td>

Metric group

</td><td>

Software publisher or software bundle that predefined software calculations are assigned to. Select **Red Hat**.

</td></tr><tr><td>

License metric

</td><td>

Group of predefined software calculations that are assigned to a metric group. Software Asset Management uses license metrics to calculate the rights for a specific set of software products during reconciliation. License metric options are based on the software publisher or software bundle that you select from the Metric group list. Possible values include the following:

 -   Per Socket-pair
-   Per Core


</td></tr><tr><td>

Rights per license pack

</td><td>

Total number of rights associated with each pack that you purchased for Red Hat. This field appears only when **Per Core** is selected from the **License metric** field.

</td></tr><tr><td>

Purchased rights

</td><td>

Total number of rights that you purchased.

</td></tr><tr><td>

Active rights

</td><td>

Total number of rights that you can allocate to your users or devices. This field is set automatically.

</td></tr><tr><td>

Allocations available

</td><td>

Number of active rights that you have not yet allocated to any user or device. This field is set automatically.

</td></tr><tr><td>

Unit cost

</td><td>

Cost of each software right.

</td></tr><tr><td>

Total cost

</td><td>

Total cost of your purchased rights. This field is automatically set based on the **Purchased rights** and **Unit cost** fields.

</td></tr></tbody>
</table>4.  Select **Submit**.


## Import entitlements for Red Hat Enterprise Linux

Import a list of Red Hat Enterprise Linux \(RHEL\) software entitlements from a spreadsheet.

### Before you begin

Role required: sam\_admin

**Important:** You can import software entitlements in both the Software Asset Management classic application and the Software Asset Workspace. The following steps provide details on how to import software entitlements in the Software Asset Management classic application. For details on how to import software entitlements in the Software Asset Workspace, see [Import bulk entitlements in workspace](../task/import-entitlements-workspace.md).

### Procedure

1.  Download the spreadsheet template for the software entitlement import.

    1.  On the page header of your ServiceNow® instance, select **All**.

    2.  In the menu navigation filter, enter `samp_bulk_import_list.do`.

        The Entitlement Imports \[samp\_bulk\_import\] table opens.

    3.  Select **New**.

    4.  On the Entitlement Import form, select **Download template**.

2.  Fill in the spreadsheet with all software entitlements that you want to import.

3.  Import your software entitlements into your ServiceNow instance.

    1.  On the page header of your ServiceNow® instance, select **All**.

    2.  In the menu navigation filter, enter `samp_bulk_import_list.do`.

        The Entitlement Imports \[samp\_bulk\_import\] table opens.

    3.  Select **New**.

    4.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Import type|Type of document that you are importing software entitlements from. The options are **Standard import document** and **Microsoft license statement \(MLS\)**. Set this field to **Standard import document**.|
        |File|Spreadsheet of software entitlements that you want to import. Select **Click to add...** to search for and select the same spreadsheet that you filled out in [step 2](rhel-entitlements.md#spreadsheet).|
        |Description|Brief description of the software entitlement import.|

    5.  Select **Import**.


### Result

All software entitlements are imported into your ServiceNow instance.

