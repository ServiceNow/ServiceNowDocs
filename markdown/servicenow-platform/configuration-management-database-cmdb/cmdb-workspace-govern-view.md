---
title: My Work view in CMDB Workspace
description: Use the My Work view in CMDB Workspace to manage your tasks. Tasks in this view are related to data compliance such as attestation, certification, and other life-cycle tasks.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# My Work view in CMDB Workspace

Use the My Work view in CMDB Workspace to manage your tasks. Tasks in this view are related to data compliance such as attestation, certification, and other life-cycle tasks.

For CMDB administrators, lists of tasks can also contain unassigned tasks, for reassignment.For managers, tasks of direct reports are included, and if you are a manager of a user group, then tasks of members in that group are also included.

## Access

Role requirements: sn\_cmdb\_admin \(CMDB Admin\), sn\_cmdb\_editor \(CMDB Editor\), or sn\_cmdb\_user \(CMDB User\).

To access the My Work view, navigate to **Workspaces** &gt; **CMDB Workspace** and then select **My Work** in the CMDB Workspace menu bar.

## Task status

The Task status section provides overall counts of tasks by their status. Counts in each status card are for attestation, certification, and life-cycle tasks as applicable. Total tasks for example, is a count of all open tasks from [CMDB Data Manager](cmdb-data-management.md) that are assigned to you, or to an assigned group in the **Managed by Group** attribute which you are a member of. For CMDB Admins, also tasks that aren't assigned to anyone are included.The Closed card counts all tasks that are in a closed state \('Closed Complete', 'Closed Canceled', 'Closed Incomplete', and 'Rejected'\).

Select a status card to show the associated tasks in the various lists such as **Attestation tasks** and **Certification** tabs in the My tasks section. For example, when you select the In progress status card in the Task status section, the **Attestation tasks** list shows attestation tasks that are in progress and the **All other tasks** list shows all non-attestation and non-certification tasks that are in progress.

## Certification tasks

The **Certification tasks** tab in the My tasks section lists any Data Certification tasks assigned to you or to an assignment group that you belong to in accordance with [CMDB Data Manager](cmdb-data-management.md) policies. For managers, tasks of direct reports are included, and for user group managers, tasks of members in the group are also included.Review and process these tasks by checking audit results for the associated CIs and attribute values. For more information about reviewing Data Certification tasks, see [Review certification tasks](../task/data-certific-review-tasks.md).

## Attestation tasks

The **Attestation tasks** tab in the My tasks section lists any attestation tasks assigned to you or to an assignment group that you belong to in accordance with CMDB Data Manager Attestation policies.For managers, tasks of direct reports are included, and for user group managers, tasks of members in the group are also included. Review and process these attestation tasks by checking the physical existence of IT infrastructure or applications associated with the CIs in the tasks. For information about reviewing and processing attestation tasks, see [Review CMDB Data Manager attestation tasks in CMDB Workspace or in Service Graph Workspace](../task/review-data-manager-attes-task.md).

The **Overdue tasks** tab lists those tasks that are overdue so you can review those tasks at a higher priority.

## Life-cycle tasks

The **All other tasks** tab in the My tasks section lists any tasks, aside from attestation and certification tasks, assigned to you or to an assignment group that you belong to in accordance with [CMDB Data Manager](cmdb-data-management.md) policies. The list includes tasks that are in a closed state \('Closed Complete', 'Closed Canceled', 'Closed Incomplete', and 'Rejected'\).For managers, tasks of direct reports are included, and for user group managers, tasks of members in the group are also included. For information about reviewing and processing life-cycle tasks, see [Review CMDB Data Manager tasks](../task/data-manager-review-task-wrkspc.md).

**Parent Topic:**[Exploring CMDB Workspace](exploring-cmdb-workspace.md)

