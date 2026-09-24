---
title: Recovery teams, loss scenarios, and recovery tasks
description: Business continuity planning workspace guides you to complete your business continuity plan. You can create a recovery team, define roles for the users, and direct the team to execute the plan. When you create a continuity plan for a department or a business unit, it is necessary to identify the loss scenarios to the business continuity plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/recovery-teams.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Business continuity planning, Explore, Business Continuity Management, Governance, Risk, and Compliance]
---

# Recovery teams, loss scenarios, and recovery tasks

Business continuity planning workspace guides you to complete your business continuity plan. You can create a recovery team, define roles for the users, and direct the team to execute the plan. When you create a continuity plan for a department or a business unit, it is necessary to identify the loss scenarios to the business continuity plan.

## Recovery teams

Starting with release 12.x.x, you create and manage the recovery team itself at a global level; the steps below describe adding users, groups, and a description to it. For the current end-to-end procedure, see [Create and manage a recovery team](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-recovery-team.md).

You can create a recovery team by entering the name and description for a recovery team or update an existing recovery team. You can select one or more users and groups from the respective lists.

The description for the recovery team also indicates the responsibilities of the users and groups who are assigned to the recovery team. You can also create a recovery team and add the user and group assignment later as shown in the example.

\[Omitted image "recovery-teams.png"\] Alt text: Recovery team.

Starting with BCM release 12.x.x, recovery teams are created and managed at a global level instead of separately for each plan. The same recovery team can be added to more than one plan. A **Locations** field is also added to the recovery team, letting you associate one or more locations with the recovery team.

The **Recovery teams** related list on a plan record now uses this global recovery team model, as shown in the example.\[Omitted image "cm-plan-record-reco-team-table-global.png"\] Alt text: Plan record with the Recovery teams related list. Previously, this related list was backed by a plan-specific recovery team table. It's now backed by the `sn_bcp_m2m_plan_recovery_team` table, a many-to-many junction table between the plan and the global recovery team, as shown in the example.\[Omitted image "cm-reco-team-table-moved-to-bcm.png"\] Alt text: Plan record with the Recovery teams related list showing the underlying table name.

Starting with BCM Core version 12.x.x and later, you can build a hierarchy of recovery teams. Set a parent recovery team or add one or more child recovery teams. For example, you can add a site-level team that reports to a regional team. You cannot set a team as its own ancestor or descendant, as the application prevents cyclic dependencies.

You can also use the **Active** option to control whether a recovery team is available for selection. Inactive recovery teams do not appear in the recovery-team picker on a plan or in the recovery-team typeahead on a collaboration thread. Add team members and groups to the recovery team in separate related lists, with each list including a **Department** column.

If you try to add a team as a parent and child of the same recovery team, or otherwise create a cyclic relationship, an inline error appears. The picker dialog blocks the add operation.

## Recovery groups and assignment groups

While drafting the plan details, the business continuity plan owners can assign one or more recovery groups and individual users to the recovery teams. While creating recovery tasks, the owner can assign them to one or more assignment groups and to the appropriate recovery teams. Additional assignees can also be added to the recovery task assignments.

## Loss scenarios

Identifying a loss scenario helps your business to be prepared for future disruptive events and continue with your business functions as usual.

If you have the BCM administrator role, you create a business continuity plan by using the plan template. The loss scenarios that are identified in the plan template automatically get associated to the plan that you have created.

Your plan has a basic set of loss scenarios attached to it. You can then add additional loss scenarios to the plan as per your requirement in the BCM UIB Workspace as shown in the example.

\[Omitted image "loss-scenarios.png"\] Alt text: Loss scenario.

## Recovery tasks

You can assign the recovery task to a group by identifying an owner to execute the processes and procedures of a recovery. The recovery task contains the details of the item to be recovered and the time by which it should be accomplished as shown in the example.

\[Omitted image "new-recovery-task.png"\] Alt text: Recovery task.

