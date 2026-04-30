---
title: Add a software reclamation rule
description: Add a reclamation rule to aggregate usage records and to identify unused software.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 6
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Add a software reclamation rule

Add a reclamation rule to aggregate usage records and to identify unused software.

## Before you begin

Role required: sam\_admin

## About this task

If you select the **Notify user** option in the reclamation rule, then the user has a chance to respond with approval during the process of reclamation. If no response is received during a specified period, the software rights are automatically reclaimed. If the user still wants to keep the software installation, it becomes the responsibility of the manager to approve or decline the removal.

For information on creating a reclamation rule for SCCM products, see [Create a reclamation rule to import Microsoft SCCM usage data](create-reclamation-rule-sccm.md).

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Reclamation Rules**.

2.  Select **New**.

3.  On the form, fill in the fields.

    **Note:** You can edit the software members of the Software Products list after the reclamation rule is created.

<table id="table_rkk_t4d_c1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_tql_x2h_nfb"><td>

Name

</td><td>

Name for the reclamation rule.

</td></tr><tr id="row_ftt_x2h_nfb"><td>

Applies to

</td><td>

Item type that the reclamation rule applies to.

</td></tr><tr id="row_w5c_y2h_nfb"><td>

Reclamation type

</td><td>

Type of reclamation rule. The possible values are the following:-   Total Usage Time \(default\)
-   Last Used Date
-   Peak Concurrent Usage \(appears only when you select **Engineering App License** from the Applies to list\)
-   Active Transaction Codes \(appears only when you select **SAP Named User** from the Applies to list\)


</td></tr><tr><td>

Named user type

</td><td>

SAP named user type. This field appears only when you select **SAP Named User** from the Applies to list. **Note:** This field is applicable to only to the SAP publisher.

</td></tr><tr><td>

Create reclamation candidate

</td><td>

When selected, a removal candidate is created for this reclamation rule, in addition to pulling in usage for all the software products associated with this rule.

 By default, this check box is selected. If you unselect this check box, a removal candidate is not created for this rule, although usage of the software products is still pulled in.

</td></tr><tr><td>

Include no activity

</td><td>

When selected, software products that have installations on devices but don’t have usage records in the usage table are also reclaimed based on the following rules:

-   Usage is available for the selected product \(at least one usage record\) within the time period of the reclamation rule.
-   For the **Last Used Date** reclamation type, the install must be created greater than the **Last used before** value.
-   For the **Total Usage Time** reclamation type, the install date must be greater than the **Aggregate usage by** value.


</td></tr><tr><td>

Assignment group

</td><td>

The assignment group to manage the removal candidates created by the specific reclamation rule. Whenever a removal candidate is created based on this rule, the assignment group mentioned in the reclamation rule is copied over to the removal candidate.By default, the value **Software managers** is selected. You can select any other group or create a group from the Group \[sys\_user\_group\] table.

</td></tr><tr id="row_x2j_y2h_nfb"><td>

Notify user

</td><td>

Option to notify the relevant user that you’re requesting permission to remove the software.

</td></tr><tr><td>

Days before auto-reclamation

</td><td>

This field appears if you select **Notify user**. Once the removal candidate goes for approval and no response is received from the user, after the number of days mentioned in this field, the software product is revoked.

</td></tr><tr><td>

Software install condition/Subscription condition

</td><td>

The software install condition field appears if you select **Installed Software** in the **Applies to** field.

 The Subscription condition field appears when the **Applies to** field is set to **Subscription software** in preconfigured rules.

</td></tr><tr><td class="sub-head" colspan="2">

Usage Metering Data

</td></tr><tr><td colspan="2">

This section appears only when you select **Total Usage Time**, **Peak Concurrent Usage**, or **Active Transaction Codes** from the **Reclamation type** field.

</td></tr><tr id="row_p11_z2h_nfb"><td>

Aggregate usage by

</td><td>

Time period over which usage information is aggregated. Possible values are the following:-   Last Month
-   Last Two Months
-   Last Three Months
-   Last Six Months \(available only if you select **Installed Software** from the **Applies to** list\)


</td></tr><tr id="row_ppk_z2h_nfb"><td>

Total hours used

</td><td>

Amount of time that the software must be used to avoid reclamation.

</td></tr><tr><td>

Percent utilized

</td><td>

License utilization percentage. For example, If you specify 60% and you utilized less than 60%, then a reclamation candidate is automatically created for the remaining 40% rights. This field is available only when you select **Engineering App License** from the Applies to list.

</td></tr><tr><td>

Minimum transaction codes required

</td><td>

Minimum number of SAP transaction codes that must be active so that a named user can avoid reclamation. You can specify the applicable transaction codes in the SAP Transaction Codes related list. The list appears after you submit the reclamation rule.This field is applicable to only to the SAP publisher. This field is available only when **SAP Named User** is selected from the Applies to list.

</td></tr><tr><td class="sub-head" colspan="2">

Last Used Data

</td></tr><tr><td colspan="2">

This section appears only when you select **Last Used Date** from the **Reclamation type** field.

</td></tr><tr id="row_fjt_z2h_nfb"><td>

Last used before

</td><td>

Amount of time to keep unused software before it’s reclaimed.-   One Month Ago
-   Two Months Ago
-   Three Months Ago
-   Six Months Ago
-   Nine Months Ago
-   One Year Ago


</td></tr></tbody>
</table>4.  Select **Submit**.

    After the reclamation rule is created, add software products to the reclamation rule. You can also add a custom software product.

    Additionally, you can specify filter conditions on software products that are suite parents. For details on adding a custom software product, see [Add a custom software product in Software Asset Management classic](t_AddACustomProduct.md). For details on filter conditions, refer to [Software reclamation rules](../concept/sw-reclamation-rules.md).

5.  Select **Edit** in the Software Products related list to add software products.

    When you add a product that is also a suite parent, all the suite components automatically get added and appear in the Software Product related list. The **Parent** field is automatically populated for all the suite components but it's empty for the suite parent.

    Additionally, when a product is added to the related list, the product process related list appears as well as any product processes \(if already present in the system\) for the parent and suite products.

6.  If a product process doesn’t exist for the software product, you can add a custom product process.

    1.  Select **New** in the Product Process related list.

    2.  On the form, fill in the fields.

        **Note:** The Product Process related list appears only when you select a software product with a product process.

        |Field|Description|
        |-----|-----------|
        |Product|Software product.|
        |File name|File name of the software product. The file name is required for the SCCM Usage to pull data.|
        |Platform|Platform of the software product.|

    3.  Select **Save**.

    **Note:** The Product Process related list is displayed only when a software product with a product process is selected.

7.  If you selected **SAP Named User** from the Applies to list, specify the SAP transaction codes that must be active to help prevent reclamation.

    **Note:** This step is applicable to only the SAP publisher.

    Not all specified transaction codes must be active to help prevent reclamation. The minimum number of transaction codes that must be active is based on the value of the **Minimum transaction codes required** field.

    1.  From the SAP Transaction Codes related list, select **Edit...**.

    2.  On the Edit Members form, select a transaction code from the Collection list or from the SAP Transaction Codes List.

        The Collection list displays all available transaction codes. The SAP Transaction Codes List displays only the transaction codes that must be active to help prevent reclamation.

    3.  Select the right and left arrow icons to move the transaction code between the lists.

    4.  Select **Save**.


