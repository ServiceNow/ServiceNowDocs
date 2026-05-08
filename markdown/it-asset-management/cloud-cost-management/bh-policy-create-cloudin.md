---
title: Define or update a Business hours policy
description: A Business hours job applies policies to identify resources that are running when they should be powered off, reports them, and can start and stop them on a schedule that you specify. Running only during specified business hours can significantly reduce your cloud spend.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Improve resource usage with Business hours, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Define or update a Business hours policy

A Business hours job applies policies to identify resources that are running when they should be powered off, reports them, and can start and stop them on a schedule that you specify. Running only during specified business hours can significantly reduce your cloud spend.

## Before you begin

Required: A cloud account \(parent account\) that has at least one service account or project that has associated datacenters.

A Billing Download job must be defined.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\] or insights\_owner \[sn\_clin\_core.insights\_owner\] for owned service accounts.

## About this task

**Important:** A resource matches the policy if all criteria in the Service Account and Resource Criteria section are met.

-   You must select one of the Cloud Cost Management application scopes to create or update a Business hours policy.
-   You can create as many policies as needed.
-   You can’t change the provider while editing an existing policy.
-   When you deactivate a Business Hours policy, the resources that met the policy criteria might match a different policy \(the matching policy with lowest run order\) and therefore move to another schedule. In this case, the system generates a new change request. If a resource no longer meets any policy, the system attempts to power on the resource using the specified **Power-on flow** setting.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Recommendations** &gt; **Business hours**.

2.  Select **Policies**.

    When a policy is created or updated with changes other than to its name or description, a notification appears on the tab. Select **Apply policies** to apply the updated policy and recalculate the reported data.

3.  Select **New/Edit** to create a policy.

    You can edit an existing policy by selecting a policy name from the **Business Hours Policies** list.

4.  On the form, fill in the fields.

<table id="table_z2z_3cm_tgb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Select business hours policy to edit

</td><td>

The business hour policy that you want to edit.

</td></tr><tr><td>

Active

</td><td>

The option to apply the policy. Selecting the **Active** check box enables Business hours analysis whenever billing data is updated.

</td></tr><tr><td>

Policy name

</td><td>

A unique name that describes the policy for other users.

</td></tr><tr><td>

Description

</td><td>

A brief description of the policy.

</td></tr><tr><td>

Run order

</td><td>

The order in which to apply policies. Each policy must have a unique value. The system applies policies in low-to-high run order and performs the actions for the first policy that matches. After a match, no other policy is applied to the resource.

 **Important:** The system applies two batches of policies in the precedence order that you specify: Policies created by Admins and policies created by Insights Owners. See the **Precedence** setting in [Configure Business hours operations](bh-settings-config-cloudin.md).

 Run order values for Unassigned Resources policies and Business hours policies don’t interfere with each other.

</td></tr><tr><td>

Provider

</td><td>

The cloud provider to apply the policy to.**Note:** You can’t change the provider while editing an existing policy.

</td></tr><tr><td>

Service category

</td><td>

List of all service categories that the policy applies to.

</td></tr><tr><td>

Service accounts

</td><td>

The service accounts to apply the policy to.For Google Cloud only, this field is called Projects.

</td></tr><tr class="sub-head"><td colspan="2">

Tag Values Condition

</td></tr><tr><td>

Tag Name

</td><td>

List of tag names that you can add by selecting **Add**.

</td></tr><tr><td>

Tag Value

</td><td>

List of tag values in a new line.

</td></tr><tr><td>

Approval type

</td><td>

The action to take on each resource that matches the policy. Business Hours operations are directly integrated with the ServiceNow Change Management feature.

 Auto-approval \(Standard Change\):

-   Generate a recommendation to apply the specified business hours and add the resource to the Business hours reports.
-   Generate and then auto-approve a change request for the change group.
-   Add the resource to the Business hours reports.
-   Apply the Business hours schedule to the resource.
 Manual approval \(Normal Change\):

-   Generate a recommendation to apply the specified business hours schedule and add the resource to the Business hours reports.
-   Generate a change request for members of the change group.
-   Add the resource to the Business hours reports.
-   Any member of the group with the sn\_change\_write role can approve the change request.
-   When approved, apply the Business hours schedule to the resource.
 Report-only:

-   Generate a recommendation to apply the specified business hours.
-   Add the resource to the Business hours reports.


</td></tr><tr><td>

Business hour schedule

</td><td>

The schedule that specifies the days of the week and times of day that the resource should be powered on.Select a schedule from the list or define a schedule by navigating to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Business hours schedules**. For more information, see [Create Business hours schedule](create-bh-schedule.md).

</td></tr></tbody>
</table>5.  Select **Submit**.


## Result

-   The created policy appears on the **Business Hours Policies** tab.
-   When the Discovery and Billing Download job executions finish, the system applies active policies to identify matching resources and then performs the policy actions on the resources.

## What to do next

After you create or update a policy, select **Apply policies** to apply the created policy to a resource. This action also notifies you if enough recent billing data for AWS, Azure, or Google doesn't exist to apply the policy.

**Parent Topic:**[Improve resource usage with Business hours](../concept/improve-res-use-business.md)

**Related topics**  


[Business hours](../concept/bh-cloudin.md)

[bundle-itsm.c_ITILChangeManagement]

[bundle-itsm.c_StandardChangeCatalogPlugin]

[bundle-itsm.create-a-change-request-template]

[Exclude a resource from all Cloud Cost Management reports](exclusion-list-add-to-cloudin.md)

