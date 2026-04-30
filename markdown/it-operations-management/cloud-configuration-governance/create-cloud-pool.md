---
title: Create a resource pool
description: Based on blueprint settings, resource pools control the values that a user sees in a catalog item when they request a resource. Only values that pass the pool filter or script appear as options on the catalog item request form.
locale: en-US
release: zurich
product: Cloud Configuration Governance
classification: cloud-configuration-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Pools and Filters for Cloud Provisioning, Cloud Admin Portal, Cloud Provisioning and Governance administration guide, Cloud Provisioning and Governance, ITOM Cloud Accelerate, IT Operations Management]
---

# Create a resource pool

Based on blueprint settings, resource pools control the values that a user sees in a catalog item when they request a resource. Only values that pass the pool filter or script appear as options on the catalog item request form.

## Before you begin

Role required: sn\_cmp.cloud\_governor

## Procedure

1.  In the Cloud Admin Portal, navigate to **Manage** &gt; **Resource Pools**.

2.  Click **New**, enter a unique and descriptive **Resource Pool Name**, and then fill in the form.

<table id="table_u54_tcn_2z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Select the type that determines whether the total count of available values for the option the user is selecting will remain the same \(Static\) or decrease by one \(Diminishing\).

</td></tr><tr><td>

Lookup Table

</td><td>

Select the table that contains the records that should appear as options in the catalog item for the resource.

</td></tr><tr><td>

Lookup Field\[Not necessary if using a script. This field is ignored if you configure a script filter.\]

</td><td>

Select the table field that contains the values to display to the user. The display value for the lookup field is not used on the Cloud User Portal. Instead, use the **Lookup label field\(s\)**.

</td></tr><tr><td>

Lookup label fields\[Not necessary if using a script. This field is ignored if you configure a script filter.\]

</td><td>

Enter the lookup field label that should appear to the user.

</td></tr></tbody>
</table>3.  Right-click in the header and select **Save**.

4.  On the Resource Pool Filters related list, click **New**, enter a unique and descriptive **Filter Name**, and then fill in the form.

    ![Resource Pool for security group filter](../image/reource-pool-filter-form.png)

<table id="table_ftb_bfn_2z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource Pool

</td><td>

Select the resource pool that the filter belongs to.

</td></tr><tr><td>

Type

</td><td>

Select the type of filter:-   **Query**: Perform a query on records in the table that you specified for the **Lookup Table** based on the **Lookup Field** that you specified.
-   **Script**: Run a script to filter the records. Enter the code in the **Script** text box.


</td></tr></tbody>
</table>    The resource pool filter is created.

5.  Right-click the form header and select **Save**.

    If you must return a filter value to the pool and that value is mapped to another table, create a record in the Resource Pool Filter Values related list.

6.  On the Resource Pool Filter Values related list, click **New**, fill in the form, and then click **Update**.

<table id="table_jxv_xfn_2z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource Pool Filter

</td><td>

Enter the name of the filter that the filter value belongs to.

</td></tr><tr><td>

Type

</td><td>

Enter the type of filter value:-   **Query**:
-   **Metadata Rule**:


</td></tr><tr><td>

Metadata Rule Name\[Appears if you select the Metadata Rule type\]

</td><td>

Enter the metadata rule name.This field appears only when **Metadata Rule** is selected from the **Type** field.

</td></tr><tr><td>

Operator

</td><td>

Select either:-   **AND**
-   **OR**


</td></tr><tr><td>

Field

</td><td>

Enter the field that is in the **Lookup Table**. For example, **CloudAccount**.

</td></tr><tr><td>

Value

</td><td>

Enter the value that you are passing back to the resource pool in the format `${field}`, where `field` is the value in the **Field** field. For example, **$\{CloudAccount\}**.

</td></tr><tr><td>

Order

</td><td>

Enter an order number that determines when the value applies, relative to other resource pool filter values. Lower values are applied first.

</td></tr></tbody>
</table>    ![Resource Pool for security group filter value](../image/resource-pool-filter-value.png)

    The resource pool filter is created.


