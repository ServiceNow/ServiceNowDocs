---
title: Create an exclusion policy
description: Application developers can create an exclusion policy to prevent pushes or pulls to particular instances in the team development hierarchy.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Team Development setup, Team Development, Planning your application, Building applications]
---

# Create an exclusion policy

Application developers can create an exclusion policy to prevent pushes or pulls to particular instances in the team development hierarchy.

## Procedure

1.  Navigate to **All** &gt; **Team Development** &gt; **Exclusion Policy**.

2.  Click **New**.

3.  Complete the Exclusion Policy form \(see table\).

4.  Click **Submit**.

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

\[Optional\] Select a specific remote instance to ignore changes from during pull operations. Leaving this field blank ignores changes from all remote instances.

</td></tr><tr><td>

Table

</td><td>

Select which table to ignore changes for.

</td></tr><tr><td>

Conditions

</td><td>

Select any additional criteria a change must meet to be ignored other than the table name. This field is only visible when the Policy is Push only.

</td></tr></tbody>
</table>
**Parent Topic:**[Team Development setup](../concept/c_SettingUpTeamDevelopment.md)

**Related topics**  


[Access rights for developers](../reference/r_GrantingAccessRightsToDevelopers.md)

[Define a remote instance](t_DefineARemoteInstance.md)

[Enable a code review](t_EnableCodeReview.md)

[Select the parent instance](t_SelectTheParentInstance.md)

[Set up an instance hierarchy](t_SetUpAnInstanceHierarchy.md)

