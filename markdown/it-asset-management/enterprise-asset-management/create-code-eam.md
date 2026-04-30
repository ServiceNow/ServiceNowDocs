---
title: Create a failure or resolution code
description: Create a failure or resolution code to help enterprise asset technicians identify either the asset failure or the solution to the asset problem.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage failure and resolution codes, Configure, Enterprise Asset Management, IT Asset Management]
---

# Create a failure or resolution code

Create a failure or resolution code to help enterprise asset technicians identify either the asset failure or the solution to the asset problem.

## Before you begin

The source for the code that you want to create should already be available. For more details, see [Create a source for failure and resolution codes](create-source-failure-res-code.md).

Role required: sn\_eam.enterprise\_admin or inventory\_admin

## About this task

Failure and resolution codes are stored in the Asset service source \[Asset service code\] table.

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Failure and resolution**.

2.  In the Failure and resolution list, select **Codes**.

    Any existing codes are shown in the Codes list.

3.  Select **New**.

4.  On the form, fill in the fields.

<table id="table_tz1_v1s_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the code that's automatically generated based on the values in the **Code** and the **Description** fields when the code is created. For example, if the **Code** field has a value F1001 and the **Description** field is Power failure, then the Display name is F1001-Power failure.

</td></tr><tr><td>

Code

</td><td>

Unique identifier used to identify an asset failure or the solution to it. For example, `F1001` or `R1001`.

</td></tr><tr><td>

Description

</td><td>

Brief description that explains what the code signifies. For example, `Power failure`.

</td></tr><tr><td>

Type

</td><td>

Type of code. The following values are available:-   **Failure**
-   **Resolution**


</td></tr><tr><td>

Parent

</td><td>

Code of the parent.**Note:** The parent code is of the same type as the child code. For example, the parent of a failure code is another failure code, and the same applies to resolution codes.

</td></tr><tr><td>

Model categories

</td><td>

Model categories to which the code can be applied.**Note:** When you select a parent on the code, the model category is inherited from the parent code. However, you can still update the this field.

If you don't select any model category, the code applies to all model categories.

</td></tr><tr><td>

Source

</td><td>

Source of the code. This field is required.

</td></tr></tbody>
</table>5.  Select **Save**.


## Result

The code that you created is shown in the Codes list.

