---
title: Create Microsoft 365 From SA and Add-on entitlements in the Software Asset Workspace
description: Create a Microsoft 365 From SA or Add-on entitlement in the Software Asset Workspace so that you can track and manage the From SA or Add-on licensing terms for your Microsoft 365 subscription software products and services.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Creating Microsoft 365 From SA and Add-on entitlements, Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Create Microsoft 365 From SA and Add-on entitlements in the Software Asset Workspace

Create a Microsoft 365 From SA or Add-on entitlement in the Software Asset Workspace so that you can track and manage the From SA or Add-on licensing terms for your Microsoft 365 subscription software products and services.

## Before you begin

Role required: sam\_user or sam\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Create a software entitlement.

    -   From the Software asset overview, select **Create entitlement**.
    -   From the License operations view, navigate to **Licensing** &gt; **Software entitlements** and then select **Create entitlement**.
3.  In the Create new entitlement dialog box, select the option to **Fill out the details in a standard form** and then select **Next**.

    The dialog box closes and you’re automatically redirected to the Create New Software Entitlement form.

4.  On the form, fill in the fields.

    For a detailed description of each field, see [Software entitlement fields](../reference/software-entitlement-fields.md).

    **Important:** To create a Microsoft 365 From SA or Add-on entitlement, set the **Software model** field to a Microsoft 365 software model and then set the **License type** field to either **From SA** or **Add-on**.

    **Tip:** If you’re using both Full and Add-on USLs for the same Microsoft 365 subscription software product or service, associate the corresponding entitlements with different software models to avoid licensing conflicts.

5.  Select **Save**.

    The form closes and you’re automatically redirected to the new software entitlement record.

6.  On the software entitlement record, select **Publish**.

    The State of the entitlement changes from Build to In use, and the entitlement is ready to be used in the reconciliation process.

7.  Assign the From SA or Add-on entitlement to the entitlement for the corresponding Microsoft software product or service that you want to transition from or add on to.

    **Note:** You can assign a From SA or Add-on entitlement to multiple corresponding Microsoft entitlements.

    **Note:** By default, the software model for your From SA or Add-on entitlement includes the corresponding Microsoft software product or service as a suite component. If the product or service isn’t already included as a suite component, you can include it manually. See [Create a software model in the Software Asset Workspace](create-swmodels-workspace.md) for detailed instructions.

    1.  On the **Related Entitlements** tab of the software entitlement record, select **New**.

    2.  On the form, fill in the fields.

<table id="table_i3c_t13_ldc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Domain

</td><td>

Domain that the corresponding Microsoft entitlement applies to. The default value is **global**.

</td></tr><tr><td>

Software entitlement

</td><td>

From SA or Add-on entitlement that you want to assign to the corresponding Microsoft entitlement. This field populates automatically.

</td></tr><tr><td>

Related Entitlement

</td><td>

Corresponding Microsoft entitlement that you want to assign the From SA or Add-on entitlement to.**Important:** This entitlement must use either the Per User or Per Device license metric. In addition, it can’t already be assigned with another entitlement or have any active allocations.

**Note:** If a corresponding Microsoft entitlement isn’t available for the given From SA or Add-on entitlement, you can create one. See [Create entitlements in workspace](create-entitlements-workspace.md) for detailed instructions.

</td></tr><tr><td>

Active rights

</td><td>

Number of From SA or Add-on rights that you want to grant to the corresponding Microsoft entitlement.**Important:**

-   For From SA rights, you must enter the total number of rights that you purchased for the corresponding Microsoft entitlement. For example, if you purchased 100 rights for the corresponding Microsoft entitlement, you must grant 100 From SA rights to that entitlement.
-   For Add-on rights, you can enter any number of rights equal to or less than the total number of rights that you purchased for the given Add-on entitlement.


</td></tr></tbody>
</table>    3.  Select **Save**.

    The From SA or Add-on entitlement is assigned to the specified Microsoft entitlement.


**Parent Topic:**[Creating Microsoft 365 From SA and Add-on entitlements](../concept/creating-m365-from-sa-add-on-entitlements.md)

**Related topics**  


[Software entitlement fields](../reference/software-entitlement-fields.md)

