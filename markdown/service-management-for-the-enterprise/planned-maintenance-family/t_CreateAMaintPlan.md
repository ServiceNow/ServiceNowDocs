---
title: Create a maintenance plan
description: When creating a maintenance plan, options on the form help to determine how and when maintenance should be performed.
locale: en-US
release: australia
product: Planned Maintenance \(Family\)
classification: planned-maintenance-family
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing maintenance plans, Planned Maintenance, Service Management]
---

# Create a maintenance plan

When creating a maintenance plan, options on the form help to determine how and when maintenance should be performed.

## Before you begin

Role required: SM admin

## Procedure

1.  Navigate to **All** &gt; **Planned Maintenance** &gt; **Maintenance Plans**.

2.  Click **New**, specify a meaningful **Name** and **Short description**, fill in the form, and then click **Submit**.

<table id="table_wcf_kbw_mr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

Auto-generated identification number for the maintenance plan.

</td></tr><tr><td class="sub-head" colspan="2">

Conditions

</td></tr><tr><td>

Type

</td><td>

Type of trigger that determines when maintenance should be performed.

-   **Model based**: Base the maintenance plan on a specified model of a CI, such as a product model.
-   **General**: Base the maintenance plan on a table and filter.
 **Note:** Model-based plans apply only to hardware models, specifically ones that have at least one model category defined.

</td></tr><tr><td>

Model

</td><td>

Select one or more [Product catalog items](https://www.servicenow.com/docs/access?context=c_ManagingProductCatalogItems&version=australia&pubname=australia-it-service-management&ft:locale=en-US) to identify the CIs that require preventive maintenance. When you select a model, the associated table appears in the **Table** field. For example, if you select a specific model of PC, the **Table** field displays Computer \[cmdb\_ci\_computer\]. This field appears if you selected the **Model based** type.

 If you select more than one model in the same category, the table does not change. But if you select a CI from a different category, the **Table** field displays the lowest level table that contains all the selected CIs. For example, if you select two PCs and one laser printer, the **Table** field changes to Hardware \[cmdb\_ci\_hardware\], because that table includes computers and printers. If you then add a computer rack, the **Table** field changes to Configuration Item \[cmdb\_ci\], which contains all CIs.

</td></tr><tr><td>

Table

</td><td>

If you selected the **General** type, select the table you want to associate with the maintenance plan. If you selected the **Model based** type, this field displays the lowest level table that contains all the selected CIs.

</td></tr><tr><td>

Filter condition

</td><td>

Filter conditions to locate the specific assets you want to maintain. Only records in the selected table that match the filtering criteria require maintenance.

</td></tr><tr><td>

Apply to new matching records

</td><td>

Select the check box to ensure that the schedules defined for this maintenance plan are applied to all records that have been added to the specified table since the last time the plan was executed, and that meet the conditions entered in the **Filter condition**. For more information, see [Associate a maintenance plan to filtered records](t_AssocMaintPlanToFilterRec.md).

</td></tr><tr><td>

Task creation policy

</td><td>

Specify what to do when a maintenance plan runs on a record that is already under maintenance.-   **Leave alone**: Do not allow the creation of new tasks or the deletion of existing ones.
-   **Cancel existing**: Allow tasks currently associated with the plan to be deleted.
-   **Add to existing**: Allow new tasks, along with existing active tasks, to be added to maintenance plans.


</td></tr></tbody>
</table>    The maintenance plan is now ready for you to [Configure a maintenance schedule](t_DefineAMaintSched.md).

    **Note:** You can [configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) to add **Asset**, **CI**, and **User** reference fields. These fields are appropriately pre-filled in the associated table and can be useful for generating reports. When a configuration item is selected for the maintenance plan and it is associated with an asset, the **Asset** field is pre-populated with that CI.

    **Note:** After you define a maintenance plan and create maintenance schedules for the plan, you cannot change the **Type**, **Model**, and **Table** fields, or the **Filter conditions**. Changes could potentially cause conflicts. If you need to make changes to those fields, first delete the maintenance schedules, then recreate the schedules with the desired settings.


**Parent Topic:**[Managing maintenance plans](../concept/c_MaintPlanMgmt.md)

