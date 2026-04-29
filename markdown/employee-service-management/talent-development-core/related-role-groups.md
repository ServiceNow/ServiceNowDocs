---
title: Create related role groups
description: Create a connection between two different role groups in the Skills Workspace to enable a transition path for the employees to move across different role groups.
locale: en-US
release: australia
product: Talent Development Core
classification: talent-development-core
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Working with job architecture, Skills Workspace, Exploring Skills Foundation, Skills Foundation, Growth Experiences, HR Service Delivery, Employee Service Management]
---

# Create related role groups

Create a connection between two different role groups in the Skills Workspace to enable a transition path for the employees to move across different role groups.

## Before you begin

Creating a related role group record creates a configuration for the progression from one job level to another job level across the role groups. This configuration is used by Talent Development to help employees choose their career progression. For example, Front-end engineering and Back-end engineering are two different role groups. By creating a bilateral relation between these two role groups, an Associate front-end Engineer \(IC1\) can move to an Associate back-end Engineer \(IC1\) role and vice-versa.

Role required: sn\_skills\_int.job\_arch\_admin

## Procedure

1.  Navigate to **All** &gt; **Skills Workspace**.

2.  Select the Lists icon \(![Lists icon](../../../common/image/icon-list.png)\).

3.  Go to **Job architecture** &gt; **Role groups**.

4.  Select a role group to open it.

5.  Select the **Related Role Groups** tab.

6.  Either create your related role group manually or by selecting from the recommendations.

<table id="choicetable_at3_cbk_s1c"><thead><tr><th align="left" id="d208724e118">

Method

</th><th align="left" id="d208724e121">

Actions

</th></tr></thead><tbody><tr><td id="d208724e127">

**Add from recommendations**

</td><td>

1.  Select the Recommendations icon \(![Recommendations icon](../image/skills-recommendations-icon.png)\) on the sidebar.
2.  Select **Link** on the role group.

The linked role group and the value in the **From role group** field will create a related role group.

After linking, the role groups are not displayed in the recommendations list.

**Note:** The recommendation panel is only displayed if data is available in the sn\_skills\_int\_role\_level\_m2m\_ind\_title table.

</td></tr><tr><td id="d208724e163">

**Manually**

</td><td>

1.  Select **New**.
2.  Select the role group to associate with the parent role group in the **To role group** field.

The default value of the **From role group** field is the selected role group.

</td></tr></tbody>
</table>7.  If you want to associate job levels to the selected role groups, select them in the **From Job Level** and **To Job Level** fields.

    The field values are populated from the job levels defined in the Job levels \[sn\_skills\_int\_job\_level\] table.

    **Note:** If you don't select a value in the **From job level** and **To job level** fields, the initial job levels of the role group \(as defined in Job levels under Job architecture\) are  considered automatically.

8.  Select **Save**.


## Result

A new relation between two role groups is created.

**Parent Topic:**[Working with job architecture](../concept/job-architecture-working.md)

**Related topics**  


[Creating a new role group through the Skills Workspace](create-new-role-group.md)

[Add more skills to a role group](adding-skills-with-skills-matrix.md)

[Edit skills and proficiencies in the Skills Matrix](edit-skills-with-skills-matrix.md)

