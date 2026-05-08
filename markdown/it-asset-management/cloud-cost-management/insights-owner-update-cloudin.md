---
title: Update or reassign insights\_owner privileges
description: Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role. An insights\_owner can define jobs and policies and can view data for owned service accounts.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Assign service accounts to an insights\_owner, Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Update or reassign insights\_owner privileges

Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role. An insights\_owner can define jobs and policies and can view data for owned service accounts.

## Before you begin

Before you assign service accounts, you might want to view the list of current insights\_owner and their owned accounts. See [View the service accounts owned by an insights\_owner](insights-owners-view-list-cloudin.md) for details.

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Account to owner mappings**.

2.  Select **Change the owner for one or more accounts**.

3.  On the form, fill in the fields.

<table id="table_zhb_zsy_jxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Original Insights Owner

</td><td>

Owner to transfer the ownership of service accounts from.

</td></tr><tr><td>

New Insights Owner

</td><td>

User to transfer the ownership of service accounts to.

</td></tr><tr><td>

Service accounts

</td><td>

Service accounts to be assigned to the insights\_owner.

</td></tr><tr><td>

Change template

</td><td>

Change template to use to create the change request for this task.The system uses a Standard Change to alert the insights\_owner of the change for the task to be auto-approved. If no change request template appears in the list, navigate to **Service Catalog** &gt; **Standard Changes** to create a template.

</td></tr></tbody>
</table>4.  Specify how to populate the **Owner** field for CIs in service accounts.

<table id="choicetable_ihs_dpm_rkb"><tbody><tr><td id="d150986e178">

**Assign insights\_owners only to CIs with no owner**

</td><td>

For newly created CIs and for CIs in the service accounts that have no value for the **Owner** property, assign the new insights\_owner.

 **Note:** A daily scheduled job sets the **Owner** field of each newly discovered CI to the Owner setting for the associated service account.

</td></tr><tr><td id="d150986e199">

**Assign insights\_owners to all CIs**

</td><td>

For the **Owner** property of every CI in the specified service accounts, assign the new insights\_owner.**Note:** A daily scheduled job sets the **Owner** field of each newly discovered CI to the Owner setting for the associated service account.

</td></tr><tr><td id="d150986e217">

**Do not update any CIs**

</td><td>

Make no changes to CIs in the specified service accounts.

</td></tr></tbody>
</table>    -   The affected service accounts are removed from policies that were created with the insights\_owner role. The affected service accounts aren’t removed from policies that were created with the insights\_admin role.
    -   The new insights\_owner must create and manage new policies for the affected service accounts.
    -   The new account owner takes ownership of Rightsizing and Unused Machines jobs that include resources from all transferred service accounts.
5.  Specify whether to transfer policies to the new owner.

    This setting applies when the selected service accounts are currently owned by a different insights\_owner. Transferring the policies enables the new insights\_owner to own \(view, update, or delete\) policies that are associated with the specified service accounts.

    **Important:** Policies owned by users with the insights\_admin role aren’t changed in any way.

<table id="choicetable_kzs_1qm_rkb"><tbody><tr><td id="d150986e259">

**Yes**

</td><td>

The following process runs:

1.  The instance clones all affected policies that are owned by Insights Owners.
2.  The instance removes appropriate service accounts from each affected policy and moves the accounts to the new clone policy. Each clone policy contains only the affected service accounts.

    -   If service accounts remain in the original policy, then the original owner retains ownership of the original policy.
    -   If an original policy has no service accounts after all affected accounts are removed, then the clone isn’t used. Instead, the new insights\_owner becomes the owner of the original policy.
3.  The instance assigns ownership of the new policies to the new insights\_owner.
4.  The instance sends email notifications to both the original and new owners.


</td></tr><tr><td id="d150986e315">

**No**

</td><td>

-   The instance removes the affected service accounts from all policies owned by Insights Owners. If no service accounts remain in a policy, then the policy is set to the Invalid state.
-   The new insights\_owner must create and manage the new policies for the affected service accounts.


</td></tr></tbody>
</table>6.  Select **Submit**.


**Parent Topic:**[Assign service accounts to an insights\_owner](insights-owner-new-cloudin.md)

