---
title: Create a CMDB Data Manager policy
description: Create a CMDB Data Manager policy in CMDB Workspace or Service Graph Workspace to automatically process CIs life-cycle events such as deletion. Applying consistent and standard life-cycle policies to CIs helps maintain the health of the CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 16
breadcrumb: [Administer CMDB Data Manager, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB Data Manager policy

Create a CMDB Data Manager policy in CMDB Workspaceor Service Graph Workspace to automatically process CIs life-cycle events such as deletion. Applying consistent and standard life-cycle policies to CIs helps maintain the health of the CMDB.

## Before you begin

-   The life-cycle policies Retire, Archive, and Delete, require that an active retirement definition exists for each targeted class in the policy. If you attempt to create a policy of a policy type for which this requirement applies but isn't met, an error message appears and the operation fails.

    For more information about retirement definitions, see [Retirement definitions](../concept/life-cycle-rules.md).

-   Verify that any custom subflow that you want to associate with a policy, exists:
    1.  Open either workspace:
        -   Navigate to **Workspaces** &gt; **CMDB Workspace** and select **Management** in the CMDB Workspace menu bar. Then, select the **Data Manager** link in Management tools, in the Manage section.
        -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel, select the Governance icon. Then, in the Governance navigation pane, select **Data Manager overview**.
    2.  Select **Subflows** in the navigation bar on the left.
    3.  Review the subflows on the Data Manager subflows page, and drill down to a subflow to open it in Workflow Studio.
    4.  Select **Create new subflow** to [create a new subflow in Workflow Studio](https://www.servicenow.com/docs/access?context=subflows&version=australia&pubname=australia-build-workflows&ft:locale=en-US).
-   To require a review and an approval for a policy task: Ensure that the **Managed By Group** attribute is populated in target CIs and that the assigned users have the privilege to approve the policy tasks.
-   When [Asset Management](https://www.servicenow.com/docs/access?context=c_AssetManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US) is activated, check if there's an asset record associated with that CI before retiring the CI. Check the associated asset record, if there's one, and verify that its asset state \(install\_status\) is **Retired**.

Role required: sn\_cmdb\_admin

## About this task

Specify for each policy a policy type, a subflow for life-cycle policies, a set of CIs to operate on as target CIs, and any other options specific to the selected policy type. Target CIs must typically be from classes extending the Configuration Item \[cmdb\_ci\] table, and with the Delete CMDB Related Entry policy type, also tables in the Related Entries \[cmdb\_related\_entry\] table. However, the Certification policy type for example, also supports non-CMDB tables. Many fields dynamically appear on the form based on how you set previous fields and some fields are specific to the policy type that you set.

Set condition filters to specify the initial set of CIs that the policy applies to. You can then further narrow down the initial set of CIs by using a CI exclusion list for the policy type. During the final preview of the policy, or from a policy task, you can select individual CIs to also exclude for the policy type. In addition, for operations that require that CIs are in a retired state, retirement definitions are enforced. The policy eventually applies to the resulting set of CIs, after applying all those filters.

**Note:** CMDB Data Manager limits the number of target CIs per task to 10,000. Therefore, when a task exceeds that number, Data Manager automatically creates as many additional tasks as needed to include all the CIs for the task. For example, if you target 30,000 CIs in an attestation task, Data Manager breaks down that task into three tasks, each targeting 10,000 CIs.

For more information about life-cycle state definitions and other concepts for working with the CMDB Data Manager, see [Working with CMDB Data Manager](../concept/cmdb-data-management.md).

## Procedure

1.  Open either workspace:

    -   Navigate to **Workspaces** &gt; **CMDB Workspace** and select **Management** in the CMDB Workspace menu bar. Then, select the **Data Manager** link in Management tools, in the Manage section.
    -   Navigate to **Workspaces** &gt; **Service Graph Workspace** and in the navigation panel, select the Governance icon. Then, in the Governance navigation pane, select **Data Manager overview**.
2.  Select **Policies** in the left-side bar.

    For information about the Policies page, see [View CMDB Data Manager policies](data-manager-view-policies-wrkspc.md).

3.  Select **Create new policy**.

4.  Fill out the General information form and then select **Continue**.

<table id="table_fsv_fpx_z4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the policy.

</td></tr><tr><td>

Description

</td><td>

Description for the policy.

</td></tr><tr><td>

Policy type

</td><td>

Life-cycle event or data management action, such as Delete or Attestation, that this policy manages, indicating the type of actions to perform on target CIs.

 Your **Policy Type** setting determines which fields appear in the forms that follow.

</td></tr><tr><td>

Work notes

</td><td>

Notes that are internal and visible only to administrators.

</td></tr></tbody>
</table>5.  Fill out the Data Filter form.

    1.  Fill out filter conditions for the target CIs and records for the policy.

<table id="table_nfz_flr_dzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Table from which to select target CIs or records for the policy. Only classes that you have read access to, are available for selection.

</td></tr><tr><td>

Filter conditions

</td><td>

Use the condition builder to specify the criteria that CIs from the specified **Table** must meet to be included as target CIs for the policy.

 Select **New condition set** to add a condition to the filter.

</td></tr><tr><td>

Related List Condition

</td><td>

Add a condition that is based on related lists that are associated with the target records for the policy.

</td></tr></tbody>
</table>    2.  Select **Apply filters** and then review the results of the impact analysis.

        This analysis estimates the number of CIs that the policy applies to based on the policy filters, any CI exclusion lists, and the life cycle stage of CIs. For example:

        -   If the policy type is retired, CIs that meet the policy filters but are already in a retired state according to the class retirement definitions, aren't targeted for the policy.
        -   If the policy type is archive or delete, CIs that meet the policy filters but aren't retired according to the class retirement definitions, aren’t targeted for the policy. A filter on the **Life Cycle Stage** or the **Life Cycle Stage Status** attributes has no effect if the respective class retirement definition is based on those attributes.
        Review the lists in the following tabs:

        -   **Included records**: You can select records to be excluded from the policy, and select **Exclude records**.
        -   **Excluded records**: Select records to be included in the policy, and select **Include records**.

            **Note:** The Excluded records tab doesn't appear when the policy type is Certification.

    3.  Select **Continue**.

6.  Fill out the Assignment form and then select **Continue**.

    1.  Set the **Assignment type** and then the **Task assignment** field that appears, to specify the type of assignment and the table columns to use for assigning the policy tasks. The drop-down list in **Task assignment** is dynamically populated with columns in the table that the policy is created for, and that reference **Assignment type** tables, as follows:

        -   **User Field**: Assigns policy tasks to a user in the user field specified in **Task assignment**. The drop-down list in **Task assignment** contains fields in the table set by the data filter, that reference the User \[sys\_user\] table \(such as **Attested by** and **Assigned to**\).

            During assignment, records will be grouped based on the selected column, allocated to tasks, and then the tasks will be assigned to the resulting users.

        -   **User Group Field**: Assigns policy tasks to the user group in the user group field specified in **Task assignment**. The drop-down list in **Task assignment** contains fields from the table set in the data filter, that reference the Groups \[sys\_user\_group\] table \(such as **Change Group** and **Support Group**\).

            During assignment, records will be grouped based on the selected column, allocated to tasks, and then the tasks will be assigned to the resulting user group.

        -   **Specific User**: Assigns policy tasks to the user specified in **Task assignment**. The drop-down list in **Task assignment** contains users with the **data\_manager\_user** role.
        -   **Specific User Group**: Assigns policy tasks to the user group specified in **Task assignment**. The drop-down list in **Task assignment** contains user groups that are either directly associated with the **data\_manager\_user** role, or contain at least one user with the **data\_manager\_user** role.
        In the **User Group Field** and **User Field** you can use dot-walking by selecting the search icon for the field. In the selection dialog box, drill down lists by expanding or selecting list items that are links \(usually appear in a unique text color\).

    2.  For certification and attestation tasks, set the **If task assignment field is empty** field to create assigned or unassigned tasks in cases where the specified task assignment field is empty. If you select to create an assigned task, then depending on the **Assignment type** setting, select the user or user group to assign a task to in that situation. Unassigned tasks are later reviewed by an administrator for assignment.
7.  Fill out the Options form and then select **Continue**.

    The options that appear depends on whether they are relevant to the selected policy type. Therefore, some of the following options don't appear on your form. For example, not all policy types are associated with a subflow.

<table id="table_all_j3s_dzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Days to complete

</td><td>

Maximum number of days that policy tasks must be completed by.

 If notifications are enabled for certification or attestation tasks, then this number is used to calculate the milestones for sending notifications. The full time \(100%\) interval starts when a task is created and ends when the number of days to complete the task arrives. Notifications are sent if a task isn't closed when 50%, 70%, and 90% of that interval passes. For more information about setting those notifications, see [Components related to CMDB Data Manager](../reference/components-cmdb-data-manager.md).

</td></tr><tr><td>

Subflow

</td><td>

A subflow with the actions that will run on the target CIs for the policy.

 The subflow typically matches the policy type. For example, if **Policy type** is set to **Delete CMDB Related Entry**, then set **Subflow** to **Delete Related Entry Configuration Item**.

</td></tr><tr><td>

Needs review

</td><td>

Option to require a review and an approval of the policy tasks, by the group assignment in CIs' **Managed by Group** attribute or by an administrator.

 Otherwise, all policy tasks are approved automatically.

</td></tr><tr><td>

Retention time

</td><td>

The length of time for retaining archived CIs in the archive table before they're deleted.

 During the specified retention period, you can use the ServiceNow AI Platform® data archiving feature to [restore archived CIs](https://www.servicenow.com/docs/access?context=managing-archived-data&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

**Note:** You can't use the CMDB Data Manager to re-archive a CI that was previously archived and restored.

</td></tr><tr><td>

Display fields

</td><td>

One or more fields that appear in list views in Data Certification tasks, that uniquely identify the records that require certification.

 The selected fields can't overlap fields in **Certification fields**.

</td></tr><tr><td>

Certification fields

</td><td>

One or more fields whose value requires verification and certification.

 The selected fields can't overlap fields in **Display fields**.

</td></tr><tr><td>

Allow field updates

</td><td>

Option to allow certification task reviewers to update field values while reviewing CIs.-   When selected, certification task reviewers can update field values in order to certify a CI.
-   When clear, certification task reviewer can't update field values, and therefore reject CIs that aren't compliant.


</td></tr><tr><td>

Allow empty field values

</td><td>

Option to allow users to certify CIs with empty attributes:

-   When selected, certification task reviewers can certify or fail certification of a CI with an empty attribute.
-   When clear, certification task reviewers can fail certification of a CI with an empty attribute but aren't able to certify that CI.


</td></tr><tr><td>

Instructions

</td><td>

Any instructions to assigned users, to help them complete the tasks.

</td></tr></tbody>
</table>8.  Fill out the Schedule form and then select **Continue**.

<table id="table_yxp_gsr_dzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Schedule

</td><td>

Recurring schedule for how often and when to run the task. The **On demand** option doesn't set any recurring schedule for running the policy.

 To learn how to run a task configured with **On demand**, see 'What to do next' below.

 Your setting determines which other fields appear on the form.

</td></tr><tr><td>

Start time

</td><td>

Time in the day to start running the policy.

</td></tr><tr><td>

Day of the week

</td><td>

Day of the week to run the policy.

</td></tr><tr><td>

On

</td><td>

Day of the month to run the policy.

</td></tr><tr><td>

Start day and time

</td><td>

Date and time of first run of the policy.

</td></tr><tr><td>

Run after every

</td><td>

Interval \(by days\) between subsequent runs after running the policy for the first time.

</td></tr><tr><td>

Run policy scheduled job as

</td><td>

User to set the **Run as** field with, in scheduled jobs for attestation and certification tasks.

 By default, the drop-down list is populated with users in the Data Manager Scheduled Job Users user group and the field is set to the user specified by the **Scheduled job default user** property \(DataManager Job Runner\). For more information about this property and the **Scheduled job default user** user role, see [Components related to CMDB Data Manager](../reference/components-cmdb-data-manager.md).

</td></tr></tbody>
</table>9.  Review the policy details on the Review form, and then select **Publish policy** to activate the policy or **Save &amp; Exit** to save the policy as a draft.

    You can later continue to configure a draft policy, and then publish it when it's ready.


## Result

After you publish a policy:

-   A daily scheduled job processes the published policy and policy tasks are assigned according to the policy settings. If the policy is associated with a subflow, then policy tasks trigger the policy subflow. Policy execution issues are recorded in an error log with notifications sent to the CMDB Data Manager administrator.

    If the policy is configured to require an approval for its tasks, then email notifications are sent to members of the assignment group in the **Managed by Group** attribute of the CI. If the policy is associated with a subflow, then a policy task triggers the policy subflow only after the task is approved.

-   If the policy is associated with a subflow, then after a policy task is complete, the policy subflow closes the task. For an Attestation policy \(which isn't associated with a subflow\), a user must process all CIs in the task and submit the task to close it.
-   For Attestation policies, attestation tasks are assigned to users as specified, and those tasks appear in the [CMDB Workspace](../concept/cmdb-workspace.md)and [Service Graph Workspace](../concept/sg-workspace.md) when those users log in.
-   For some policy types, such as **Delete**, the list of the target CIs is rolled up in a CSV file that is then attached to the task for tracking purposes.
-   Stale tasks are set to **Closed Canceled** by a daily scheduled job. A task becomes stale when it's still open and not approved after at least 90 days. The number of days after which a task is considered stale is determined by the **cmdb.data.manager.stale.task.life.in.days** system property.

## What to do next

-   [Publish a draft CMDB Data Manager policy](data-manager-publish-draft-policy.md).
-   On the Policies page, in the Published policies list view, select a policy to see policy details on a policy form. Select **View Policy** to see the settings in all of the policy form pages.
-   On the Policies page, in the Published policies list view, select a policy that you want to deactivate. On a policy form select **Deactivate Policy** to temporarily prevent the policy from running.
-   Select **View Open Tasks** in the Open Policy Tasks tile to track the processing of policy tasks in the CMDB Data Management Task Control list view. The Success Percent column shows the percentage of CIs in the task for which the task is completed. A CI is counted as complete in an archival task only after the archival process has been fully completed for the CI \(and isn't counted as complete while the CI is initially staged for archival for example\).
-   Run a policy on-demand. In general, the system generates a scheduled job for on-demand policies, prefixed with the policy name.

    -   Run the scheduled job:
        1.  Navigate to **System Definition** &gt; **Scheduled Jobs**.
        2.  Select the scheduled job for the task policy that you want to run.
        3.  On the scheduled job form, select **Execute Now**.
-   Users log in to [CMDB Workspace](../concept/cmdb-workspace.md)or to [Service Graph Workspace](../concept/sg-workspace.md) to [review and process attestation tasks](review-data-manager-attes-task.md) assigned to them.
-   Users log in to [CMDB Workspace](../concept/cmdb-workspace.md)or to [Service Graph Workspace](../concept/sg-workspace.md) to [review and process non-attestation tasks](data-manager-review-task-wrkspc.md) assigned to them.
-   You can use update sets to transfer a policy between instances, in which case that policy is imported as a draft policy at the destination instance. You can later continue to configure the draft policy at the destination instance and then [publish it when it's ready](data-manager-publish-draft-policy.md).

