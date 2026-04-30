---
title: Create entity criteria
description: Create an entity criteria record to define customer-based conditions, either for selected accounts \(B2B\) or consumers \(B2C\). These criteria can be applied to filter which customers are eligible for specific services.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure customer criteria for a service definition, Configuring service definitions, Service definitions, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create entity criteria

Create an entity criteria record to define customer-based conditions, either for selected accounts \(B2B\) or consumers \(B2C\). These criteria can be applied to filter which customers are eligible for specific services.

## Before you begin

Role required:sn\_csm\_case\_types.service\_definition\_manager, sn\_csm\_case\_types.service\_definition\_admin, or admin

## About this task

You can select entity criteria records when you configure customer criteria for a service definition. The system uses this configuration to determine which customers are eligible for that particular service.

**Note:** Entity criteria records are available for all CSM applications.

## Procedure

1.  Navigate to **All** &gt; **Service request operations** &gt; **Entity criteria**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_e2n_dcf_bgc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the entity criteria.

</td></tr><tr><td>

Condition for

</td><td>

The type of customer for which the condition applies. There are two types of customers:-   Select **Account** for B2B customers.
-   Select **Consumer** for B2C customers.


</td></tr><tr><td>

Condition on

</td><td>

The table on which the conditions in the condition builder apply. For example, Customer Account \[customer\_account\]. The selected table determines the visibility of the **Customer field** and the available elements in that field.

</td></tr><tr><td>

Condition

</td><td>

Use the condition builder to select the conditions that apply to this entity criteria record, such as location or account type.

</td></tr><tr><td>

Customer field

</td><td>

Field that references the account, consumer, or other selection in the **Condition for** field from the table selected in the **Condition on** field.For example:

-   If **Condition for** is set to **Account** and if **Condition on** is set to Account Address \[account\_address\_relationship\], then you can select a field like **Account**.
-   If **Condition for** is set to **Consumer** and if **Condition on** is set to Interaction \[interaction\], select a field like **Consumer**.


</td></tr></tbody>
</table>4.  Select **Submit**.


