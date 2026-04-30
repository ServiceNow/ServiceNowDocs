---
title: Components related to CMDB Data Manager
description: The following scheduled jobs, tables, roles, and properties, are related to CMDB Data Manager. Some of those, are installed with CMDB Workspace and Service Graph Workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Components related to CMDB Data Manager

The following scheduled jobs, tables, roles, and properties, are related to CMDB Data Manager. Some of those, are installed with CMDB Workspaceand Service Graph Workspace.

## System properties

As a Data Manager Administrator \(data\_manager\_admin\) you can view CMDB Data Manager properties in [CMDB Workspace](../concept/data-mgr-exp-cmdb-workspace.md).

1.  Open either workspace:
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **Management** and then select the **Data Manager** quick link in Management tools, in the Manage section.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel, select the Governance icon. Then, in the Governance navigation pane, select **Data Manager overview**.
2.  Select **Settings** in the left navigation bar.

<table id="table_w2w_tdx_npb"><thead><tr><th>

Property/Setting/Label

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.cmdb.data.manager.delete.batch.size

</td><td>

Size of each batch of CIs that is deleted or archived \(affects performance optimization\).-   Type: Integer
-   Default value: 1000

</td></tr><tr><td>

Retirement definitions

</td><td>

List of retirement definitions used in CMDB Data Manager life-cycle policies. For more information about the concept and usage of retirement definitions, see:-   [Retirement definitions](../concept/life-cycle-rules.md)
-   [Manage retirement definitions for CMDB Data Manager](../task/data-manager-manage-ret-def-wrkspc.md#)

</td></tr><tr><td>

Scheduled job users

</td><td>

User group from which to select the user that scheduled jobs run as, when creating certification and attestation policies. The default value for the **Scheduled job default user** field is DataManager Job Runner which is a member of the default **User group** Data Manager Scheduled Job Users.

 The setting of this property determines the list of users available in the **Run policy scheduled job as** field on the Schedule form of a new policy.

</td></tr><tr><td>

sn\_cmdb\_ws.cmdb.dm.policy\_types.due\_date\_notification

 Notifications

</td><td>

Notifications about certification and attestation incomplete tasks. When either is checked, the system notifies task owners as the due date for incomplete tasks is approaching. Notifications are sent when 50%, 70%, and 90% of the time to due date has passed. On the task due date, a past due notification is sent to the task owner and to the task owner's manager.

 Upon closing a task, sending notifications stops.

 For information about how the **Days to complete** setting is used to calculate when notifications are sent, see [Create a CMDB Data Manager policy](../task/data-manager-create-policy-wrkspc.md).

</td></tr><tr><td>

sn\_cmdb\_ws.glide.cmdb.data.manager.aging.policy.task.timeframe

 Aging policy task timeframe

</td><td>

Number of days before a Data Manager task is marked as aged.-   Type: Integer
-   Default value: 30

</td></tr><tr><td>

glide.cmdb.data.manager.subflow.timeout

 Threshold for subflow run time

</td><td>

Threshold \(in milliseconds\) for subflow running time. A subflow that passes this threshold while running, is cancelled.-   Type: Integer
-   Default value: 600,000 \(10 minutes\)

</td></tr><tr><td>

glide.cmdb.data\_manager.default\_archive\_time

 Number of days CIs are archived before they get deleted permanently

</td><td>

Number of days that it is still possible to restore archived CIs from archive tables. After the specified number of days pass, archived CIs are permanently deleted from the archive tables. -   Type: Integer
-   Default value: 120

</td></tr><tr><td>

cmdb.data.manager.stale.task.life.in.days

 Number of days after which task is considered stale

</td><td>

Number of days after which a task is considered stale and is set to **Closed Cancelled** by the **CMDB Data Manager - Stale Task Cleaner** daily scheduled job.

 Details:

-   Type: Integer
-   Default value: 90

</td></tr><tr><td>

sn\_cmdb\_ws.glide.cmdb.data\_manager.rejected.task.notifications.group

 Group to receive notifications for a rejected task

</td><td>

System identifier of a user group to notify about tasks that are being rejected.

 By default, this property has no value, in which case, all data manager administrators are notified about rejected tasks.

 For information about how this property is used when reviewing and rejecting life-cycle tasks, see [Review CMDB Data Manager tasks](../task/data-manager-review-task-wrkspc.md).

</td></tr><tr><td>

cmdb.data.manager.stale.tasks.notifications.frequency

</td><td>

Number of days between notification reminders for stale tasks.-   Type: Integer
-   Default value: 7

</td></tr></tbody>
</table>## Scheduled jobs

<table id="table_ebl_y5n_mpb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Data Manager Archive/Delete Policy Processor

</td><td>

Processes all published polices of type Archive and Delete:

-   Applies policies only to CIs that are already retired.
-   Processes all Archive policies first, and if no errors encountered, continues to process any Delete policies.

</td></tr><tr><td>

CMDB Data Manager Retire Policy Processor

</td><td>

Processes all published polices of type Retire: Applies policies only to CIs that are not retired.

</td></tr><tr><td>

CMDB Data Manager - Stale Task Cleaner

</td><td>

Cleans up stale CMDB Data Manager tasks by setting the task to **Closed Cancelled**.

 The **cmdb.data.manager.stale.task.life.in.days** system property determines the number of days after which a task is considered stale \(90 by default\).A task becomes stale if:

-   The task was created at least 90 days \(by default\) ago and it is still open.
-   The approval requests are older than 90 days \(by default\) and the task is not yet approved.

</td></tr><tr><td>

CMDB Data Manager Delete Related Entry Policy Processor

</td><td>

Processes the Delete CMDB Related Entry policy by deleting the specified related tables from the Related Entry \[cmdb\_related\_entry\] table.

</td></tr></tbody>
</table>## Tables

<table id="table_ety_2hs_npb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CMDB Data Management Policy\[cmdb\_data\_management\_policy\]

</td><td>

Details about CMDB Data Manager policies.

</td></tr><tr><td>

CMDB Data Management Policy Executions\[cmdb\_data\_management\_policy\_execution\]

</td><td>

Execution records that correspond to each policy run. As policies run according to their recurring schedule, for each run the system generates a record with a unique policy execution number for that run. A policy execution number has a prefix of 'PLCEXEC'.

 Execution records associated with certification policy runs, are used for populating the Data Certification Dashboard.

</td></tr><tr><td>

CMDB Data Management Policy Runtime Attributes\[cmdb\_data\_management\_policy\_runtime\_attributes\]

</td><td>

Current policy metadata including status and summary.

</td></tr><tr><td>

CMDB Data Management Task Control\[cmdb\_data\_management\_task\]

</td><td>

Open policy tasks generated by published policies.

</td></tr><tr><td>

CMDB Data Management Tasks to CIs\[cmdb\_data\_management\_task\_to\_ci\]

</td><td>

Associations of tasks to CIs.

</td></tr><tr><td>

CMDB Data Manager Task to Documents\[cmdb\_data\_management\_task\_to\_document\]

</td><td>

Associations of task and to related items.

</td></tr><tr><td>

CMDB Data Management Attestation Tasks to CIs\[sn\_cmdb\_ws\_attestation\_task\_to\_ci\]

</td><td>

Associations of task and attestation CIs.

</td></tr><tr><td>

CMDB Data Management Tasks to CIs\[cmdb\_ci\_state\_management\_task\_to\_ci\]

</td><td>

Associations of task and CIs for 'Dependent CI Deletion' policy type.

</td></tr><tr><td>

Excluded CIs\[cmdb\_policy\_ci\_exclusion\_list\]

</td><td>

Tracks the CIs that are set to be excluded during policy evaluation.

</td></tr><tr><td>

CMDB Policy Type\[cmdb\_policy\_type\]

</td><td>

Policy types supported by the CMDB Data Manager.

</td></tr><tr><td>

CMDB Policy Type Categories\[cmdb\_policy\_type\_categories\]

</td><td>

Associations of policy types to Workflow Studio Categories.

</td></tr><tr><td>

CMDB Retirement Custom Definitions\[cmdb\_retirement\_custom\_definitions\]

</td><td>

Custom retirement definitions used in life-cycle policies \(Retire/Archive/Delete\).

</td></tr><tr><td>

CMDB Policy Scheduled Jobs\[cmdb\_policy\_scheduled\_job\]

</td><td>

Policy scheduled Job details.

</td></tr><tr><td>

Dependent CI Relations Evaluation Config\[cmdb\_dependent\_ci\_extra\_rels\_config\]

</td><td>

Information about CIs' extraneous relationships which is used for the delete and archive operations. Extraneous relationships are those relationships that are not in the CI’s chain of dependency.

 For more information, see [Dependent CIs management](../concept/manage-dependent-ci.md).

</td></tr><tr><td>

CMDB Dependent CI Class Exclusions\[cmdb\_dependent\_ci\_class\_exclusion\]

</td><td>

Excluded classes for dependent CI, which is used with the Archive/Retire/Delete policy types to determine which CIs are orphan dependent CIs.

 For more information, see [Dependent CIs management](../concept/manage-dependent-ci.md).

</td></tr><tr><td>

CMDB Dependent CI Ledger\[cmdb\_dependent\_ci\_ledger\]

</td><td>

Staging table for orphaned dependent CI related to the deletion or archival of the main CI that they depend on. Also used in a cascade-retire dependent CIs operation.For more information, see [Dependent CIs management](../concept/manage-dependent-ci.md).

</td></tr><tr><td>

CMDB CI End Of Life Ledger\[cmdb\_ci\_end\_of\_life\_ledger\]

</td><td>

CIs that are being set as retired that belong to a class that has any downstream dependencies.

 Used in the Dependent CI Retire policy.

</td></tr></tbody>
</table>## Roles

<table id="table_ilg_tks_npb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

CMDB Data Manager administrator\[data\_manager\_admin\]

</td><td>

Can access all features in the CMDB Data Manager, including:

-   Full access to assigned tasks.
-   Full access to policies.
-   Ability to associate subflow categories to policy type.

 Can create, edit, and delete policies, calculate previews, approve tasks, and manage exclusion lists.

</td><td>

-   task\_editor
-   data\_manager\_user
-   cmdb\_query\_builder\_read

</td></tr><tr><td>

CMDB Data Manager user\[data\_manager\_user\]

</td><td>

Can view CMDB Data Manager policies in read-only mode and calculate previews.

Can perform the following tasks:-   View assigned tasks.
-   Update, approve, or reject an assigned task.
-   Add a CI to an exclusion list from their task.

</td><td>

cmdb\_read

</td></tr><tr><td>

DataManager Job Runner\[dataManager.jobRunner\]

</td><td>

Default user for the **Scheduled job default user** CMDB Data Manager property.

 The **Run policy scheduled job as** field on the Schedule form in a policy, is set to this user if no other option is chosen.

</td><td>

 

</td></tr></tbody>
</table>