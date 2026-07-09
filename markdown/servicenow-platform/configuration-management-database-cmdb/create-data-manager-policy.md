---
title: Create a CMDB Data Manager policy \(in Core UI\)
description: Create a policy in the CMDB Data Manager legacy build on Core UI to automatically process CIs life-cycle event such as deletion. Applying consistent and standard life-cycle policies to CIs helps maintain the health of the CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/create-data-manager-policy.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [CMDB Data Manager \(Core UI\), CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a CMDB Data Manager policy \(in Core UI\)

Create a policy in the CMDB Data Managerlegacy build on Core UI to automatically process CIs life-cycle event such as deletion. Applying consistent and standard life-cycle policies to CIs helps maintain the health of the CMDB.

## Before you begin

-   The life-cycle policies Retire, Archive, and Delete, require that an active [retirement definition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/life-cycle-rules.md) exists for each targeted class in the policy. If you attempt to create a policy of a policy type for which this requirement applies but isn't met, an error message appears and the operation fails.
-   Ensure that any custom subflow that you want to associate with a policy, exists.
-   To require a review and an approval for a policy task: Ensure that the **Managed By Group** attribute is populated in target CIs and that the assigned users have the privilege to approve the policy tasks.
-   When [Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/it-service-management/c_AssetManagement.md) is activated, check if there is an asset record associated with that CI before retiring the CI. Check the associated asset record, if there is one, to ensure that the asset state \(install\_status\) is **Retired**.

Role required:

-   data\_manager\_admin: Full access to policies
-   data\_manager\_user: Can read and preview policies

## About this task

Specify for each policy a policy type, a life-cycle subflow, and a set of CIs to operate on as target CIs. Target CIs must be from classes extending the Configuration Item \[cmdb\_ci\] table, and with the Delete CMDB Related Entry policy type, also tables in the Related Entries \[cmdb\_related\_entry\] table.

Set condition filters to specify the initial set of CIs that the policy applies to. You can then further narrow down the initial set of CIs by using a CI exclusion list for the policy type. During the final preview of the policy, or from a policy task, you can select individual CIs to also exclude for the policy type. In addition, for operations that require that CIs are in a retired state, [retirement definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/life-cycle-rules.md) are enforced. In these cases:

-   CIs that meet the policy filters but aren't retired according to the class retirement definitions, aren’t targeted for the policy.
-   A filter on the **Life Cycle Stage** or the **Life Cycle Stage Status** attributes has no effect if the respective class retirement definition is based on those attributes.

The policy eventually applies to the resulting set of CIs, after applying all those filters.

**Note:** CMDB Data Manager limits the number of target CIs per task to 10,000. Therefore, when a task exceeds that number, Data Manager automatically creates as many additional tasks as needed to include all the CIs for the task. For example, if you target 30,000 CIs in an attestation task, Data Manager breaks down that task into three tasks, each targeting 10,000 CIs.

More information:

-   About life cycle state definitions, see [Working with CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.md).
-   About creating a policy in the CMDB Data Manager in CMDB Workspace, see [Create a CMDB Data Manager policy in CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/data-manager-create-policy-wrkspc.md).

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Data Manager**.

2.  On the CMDB Data Manager landing page, in the Policies tile, click **View Policies**.

3.  In the CMDB Data Manager Policy and Attributes list view, click **New**.

4.  Fill out the fields in the different sections on the **Define Policy** tab.

    **Note:** Some fields are applicable only to specific policy types. Therefore some of the following fields, might not appear for the policy type that you choose.

<table id="table_fsv_fpx_z4b"><thead><tr><th>

Field \(General\)

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the policy.

</td></tr><tr><td>

Task Assignment Group

</td><td>

Group to assign the task to.

</td></tr><tr><td>

Task Due In Days

</td><td>

Due date for completing the policy tasks such as attestation tasks.

</td></tr><tr><td>

Needs Review

</td><td>

Check to require a review and an approval of the policy tasks, by the group assignment in CIs' **Managed by Group** attribute or by an administrator.

 Otherwise, all policy tasks are approved automatically.

</td></tr><tr><td>

Policy Type

</td><td>

Life-cycle event or data management action, such as Deleteor Attestation, that this policy manages, indicating the type of actions to perform on target CIs.

</td></tr><tr><td>

User Group

</td><td>

Group to use as the task assignment group for the Delete CMDB Related Entry policy type. The list is a subset of user groups from the Group \[sys\_user\_group\] table, where at least one member has a data\_manager\_user role.

</td></tr><tr><td>

Apply Retention Time

</td><td>

The length of time for retaining archived CIs in the archive table before they are deleted.

 During the specified retention period, you can use the ServiceNow AI Platform® data archiving feature to restore archived CIs. .

</td></tr></tbody>
</table><table id="table_ej1_zqq_wsb"><thead><tr><th>

Field \(Condition Filter\)

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Related Entry Table

</td><td>

The related table to apply a Delete CMDB Related Entry policy. The list contains related tables from the Related Entry \[cmdb\_related\_entry\] table.

</td></tr><tr><td>

Condition Filter

</td><td>

Criteria that CIs must meet to be included for the policy as target CIs.

 Additional filtering such as a CI exclusion list, can further narrow down the set of target CIs.

</td></tr></tbody>
</table><table id="table_mdd_zqq_wsb"><thead><tr><th>

Field \(Action\)

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Subflow

</td><td>

A subflow with the actions that will run on the target CIs for the policy.

 The subflow typically matches the policy type. For example, if **Policy type** is set to **Delete CMDB Related Entry**, then set **Subflow** to **Delete Related Entry Configuration Item**.

**Note:** The Attestation policy type is not associated with a subflow.

</td></tr></tbody>
</table>    |Field \(Schedule\)|Description|
    |------------------|-----------|
    |Frequency|How often to run the task.|
    |Start Time|Time to start running the task when it is due to run.|

5.  Click **Run filter** in the Condition Filter section, to see the resulting list of CIs that match the condition filters.

6.  Click **Save**.

7.  Click **Preview** and wait for an impact analysis for the policy on the **Preview Policy Impact** page to complete.

    This analysis estimates the number of CIs that the policy applies to based on the policy filters, any CI exclusion lists, and the life cycle stage of CIs. For example:

    -   If the policy type is retired, CIs that meet the policy filters but are already in a retired state, are not targeted for the policy.
    -   If the policy type is archive or delete, CIs that meet the policy filters but are not retired, are not targeted for the policy.
8.  Select CIs in the target CIs list that you want to also exclude for the policy type. Click **Exclude CI** and then click **Recalculate Preview** to recalculate the data on the preview page.

9.  Click **Publish** to activate the policy.

    Unpublished tasks are saved as draft policies.


## Result

After you publish a policy:

-   A daily scheduled job processes the published policy and policy tasks are assigned as set in the policy. If the policy is associated with a subflow, then policy tasks trigger the policy subflow. Policy execution issues are recorded in an error log with notifications sent to the CMDB Data Manager Administrator.

    If the policy is configured to require an approval for its tasks, then email notifications are sent to members of the assignment group in the **Managed by Group** attribute of the CI. If the policy is associated with a subflow, then a policy task triggers the policy subflow only after the task is approved.

-   If the policy is associated with a subflow, then after a policy task is complete, the policy subflow closes the task. For an Attestation policy \(which is not associated with a subflow\), a user must process all CIs in the task and submit the task to close it.
-   For Attestation policies, attestation tasks are assigned to users as specified, and those tasks appear in the [CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md) when those users log in.
-   For some policy types, such as Delete, the list of the target CIs is rolled up in a CSV file that is then attached to the task for tracking purposes.
-   Stale tasks are set to **Closed Cancelled** by a daily scheduled job. A task becomes stale when it is still open and not approved after at least 90 days. The number of days after which a task is considered stale is determined by the **cmdb.data.manager.stale.task.life.in.days** system property.

## What to do next

-   Click **View Open Tasks** in the Open Policy Tasks tile to track the processing of policy tasks in the CMDB Data Management Task Control list view. The Success Percent column shows the percentage of CIs in the task, for which the task is completed. A CI is counted as complete in an archival task only after the archival process has been fully completed for the CI \(and isn't counted as complete while the CI is just staged for archival for example\).
-   Users log in to the [CMDB Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-workspace.md) to [review and process attestation tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/review-data-manager-attes-task.md) assigned to them.
-   You can open a policy in CMDB Data Manager and click **Deactivate** to temporarily prevent the policy from running.
-   [Manage exclusion lists of CMDB Data Manager \(in Core UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/manage-data-mgr-ci-exclusion-list.md).

**Related topics**  


[Working with CMDB Data Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/cmdb-data-management.md)

