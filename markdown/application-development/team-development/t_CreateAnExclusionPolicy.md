---
title: Create an exclusion policy
description: Application developers can create an exclusion policy to avoid pushes or pulls to specific instances in the team development hierarchy.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Defining Exclusion policies, Configure, Team Development, Planning your application, Building applications]
---

# Create an exclusion policy

Application developers can create an exclusion policy to avoid pushes or pulls to specific instances in the team development hierarchy.

## Before you begin

Role required: user

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Exclusion Policy**.

2.  Select **New**.

3.  Fill in the form.

<table id="table_s5f_fmb_bq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique description of the policy.

</td></tr><tr><td>

Policy

</td><td>

Select when the policy applies. Options include:-   Push only
-   Push and Pull
-   Pull only


</td></tr><tr><td>

Remote Instance

</td><td>

Leaving this field empty ignores changes from all remote instances.Select a specific remote instance to ignore changes from during pull operations.

</td></tr><tr><td>

Table

</td><td>

Select which table to ignore changes for.

</td></tr><tr><td>

Conditions

</td><td>

Select any additional criteria to be ignored, other than the table name. This field is only visible when the Policy is Push only.

</td></tr></tbody>
</table>4.  Select **Submit**.


**Parent Topic:**[Exclusion policies](../concept/c_ExclusionPolicies.md)

