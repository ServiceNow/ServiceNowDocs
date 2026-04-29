---
title: Assign service accounts to an insights\_owner
description: Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role. An insights\_owner can define jobs and policies and can view data for owned service accounts.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Assign service accounts to an insights\_owner

Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role. An insights\_owner can define jobs and policies and can view data for owned service accounts.

## Before you begin

Before you assign service accounts, you might want to view the list of current insights\_owner and their owned accounts. For more information, see [View the service accounts owned by an insights\_owner](insights-owners-view-list-cloudin.md).

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

## About this task

The insights\_owner role spreads responsibility for Cloud Cost Management activities to persons who have good knowledge of operations in the service accounts. For more information about the insights\_owner role, see [Cloud Cost Management roles](../reference/cloud-insights-roles.md).

A service account is a secure record on your instance that holds the credential and access information for your provider account. Discovery uses the information to access your provider account to get data on each resource in each specified datacenter.

**Tip:** When you assign service accounts to a user, the user is auto-granted the insights\_owner role.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Administration** &gt; **Account to owner mappings**.

2.  Select **Assign accounts that currently have no owner**.

3.  On the form, fill in the fields.

<table id="table_opt_lqy_jxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Insights Owner

</td><td>

User to whom the service account has to be assigned.

</td></tr><tr><td>

Service accounts

</td><td>

Service accounts to be assigned to the insight\_owner.

</td></tr><tr><td>

Change template

</td><td>

Change template to use to create the change request for this task.The system uses a Standard Change to alert the insights\_owner of the change for the task to be auto-approved. If no change request template appears in the list, navigate to **Service Catalog** &gt; **Standard Changes** to create a template.

</td></tr></tbody>
</table>4.  Specify how to populate the **Owner** field for CIs in service accounts.

<table id="choicetable_ihs_dpm_rkb"><tbody><tr><td id="d323354e202">

**Assign insights\_owners only to CIs with no owner**

</td><td>

For newly created CIs and for CIs in the service accounts that have no value for the **Owner** property, assign the new insights\_owner.

 **Note:** A daily scheduled job sets the **Owner** field of each newly discovered CI to the Owner setting for the associated service account.

</td></tr><tr><td id="d323354e223">

**Assign insights\_owners to all CIs**

</td><td>

For the **Owner** property of every CI in the specified service accounts, assign the new insights\_owner.**Note:** A daily scheduled job sets the **Owner** field of each newly discovered CI to the Owner setting for the associated service account.

</td></tr><tr><td id="d323354e241">

**Do not update any CIs**

</td><td>

Make no changes to CIs in the specified service accounts.

</td></tr></tbody>
</table>    -   The affected service accounts are removed from policies that were created with the insights\_owner role. The affected service accounts aren’t removed from policies that were created with the insights\_admin role.
    -   The new insights\_owner must create and manage new policies for the affected service accounts.
    -   The new account owner takes ownership of Rightsizing and Unused Machines jobs that include resources from all transferred service accounts.
5.  Add any additional details to your request such as delivery address and special instructions.

6.  Select **Submit**.


-   **[Update or reassign insights\_owner privileges](insights-owner-update-cloudin.md)**  
Assign ownership of one or more service accounts and, optionally, the related CIs to users that have the insights\_owner role. An insights\_owner can define jobs and policies and can view data for owned service accounts.
-   **[View the service accounts owned by an insights\_owner](insights-owners-view-list-cloudin.md)**  
View the list of users that have the insights\_owner role and the service accounts that each owner owns.

**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

