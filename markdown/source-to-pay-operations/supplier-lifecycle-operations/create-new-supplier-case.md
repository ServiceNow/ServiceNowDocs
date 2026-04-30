---
title: Create a case on behalf of a supplier from the Source-to-Pay Workspace
description: Create a supplier case to track the progress of supplier tasks, resolve issues related to supplier products or services, and request additional information from a supplier.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Managing supplier cases from the Source-to-Pay Workspace, Using Source-to-Pay Workspace, Using Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create a case on behalf of a supplier from the Source-to-Pay Workspace

Create a supplier case to track the progress of supplier tasks, resolve issues related to supplier products or services, and request additional information from a supplier.

Describes the procedure for creating a case on behalf of a supplier from the Source to Pay workspace. 

## Before you begin

Role required: sn\_slm.manager, sn\_slm.owner, or sn\_slm.admin

**Note:** The sn\_slm.owner role can create cases only for the suppliers they own.

## Procedure

1.  Navigate to **All** &gt; **Supplier Lifecycle Operations** &gt; **Source-to-Pay Workspace**.

2.  Do one of the following.

<table id="choicetable_qn2_ksn_wtb"><thead><tr><th align="left" id="d35253e81">

To

</th><th align="left" id="d35253e84">

Do this

</th></tr></thead><tbody><tr><td id="d35253e90">

**To create a case from Quick actions**

</td><td>

On the home page, do one of the following:-   Under Quick actions, select **Create case**.
-   Under Quick actions, select **Manage my suppliers** and do the following:
    1.  Select the link to the supplier name under the Legal name column.
    2.  From the **Create** drop-down list, select **Supplier case**.


</td></tr><tr><td id="d35253e127">

**To create a case from the List page**

</td><td>

1.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\) and do one of the following:
    -   Navigate to **Lists** &gt; **My work** &gt; **Open cases**
    -   Navigate to **Lists** &gt; **All work** &gt; **Cases**
2.  Select **New**.
3.  On the Create new case dialog box, select a case type from the **Case type** field, and then select **Submit**.


</td></tr></tbody>
</table>3.  On the Create New Supplier Case form, fill in the fields.

    For more information about the form fields and descriptions, see [Create New Supplier Case form](../reference/new-supplier-case.md).

4.  Select **Save**.

    The case is created in Draft state.

5.  Do the following steps only if you selected these case types:

    1.  Select **Add more details**.
    2.  On the Add more details form, fill in the fields.

        In the **Case type** field, if you selected **Banking information change request**, see [Update banking details form](../reference/update-supp-banking-form.md) for more information about the form fields and descriptions.

        In the **Case type** field, if you selected **Supplier information change request**, see [Update profile details form](../reference/update-supp-profile-form.md) for more information about the form fields and descriptions.

        In the **Case type** field, if you selected **Supplier location change request**, see [Add New Location form](../reference/supplier-location-form.md) for more information about the form fields and descriptions.

    3.  Select **Submit**.
6.  Select **Submit case**

    The case moves to the Open state.


## What to do next

After you submit the case, depending on the case type, the specific playbook for the supplier case opens.

For more information, see [Case playbook for specific supplier case types](../concept/gen-playbook-cases.md) and [Playbook for updating the supplier primary data](../concept/primary-playbook-cases.md).

**Parent Topic:**[Managing supplier cases from the Source-to-Pay Workspace](../concept/managing-cases.md)

