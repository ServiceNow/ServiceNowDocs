---
title: Reporting roles
description: Reporting is installed with roles that limit report creation. Access control lists \(ACLs\) can also limit report viewing and creation.Create and view reports that have been shared with them. Cannot share, edit, or delete reports that have been shared with them. Users with the itil role also have these limitations.Schedule emailing of all reports that they can see, including reports they cannot manage. Users with this role must also have another role that grants permission to create, edit, and share reports.Can manage and share reports that are shared with the groups they are members of \(listed in Group\).Can share a report that is shared with everyone. This role can share with everyone. Cannot share a report that is shared with the user or a group.Manage, share, publish, and schedule all reports. Access Reports Administration and manage all report-related objects.Read and update table and field descriptions for reports. Included in the plugin Table and field description configuration for report \[com.glideapp.report.description\_config\].
locale: en-US
release: australia
product: Reporting
classification: reporting
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reporting reference, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Reporting roles

Reporting is installed with roles that limit report creation. Access control lists \(ACLs\) can also limit report viewing and creation.

**Note:**

-   Users must have the report\_user role to see the **Reports** module on the application navigator \(left navigation pane\).
-   Users with any reporting role or the itil role can access the following report options for all reports that are visible to them: **Insert**, **Insert and Stay**, **Add to Dashboard**, and **Export to PDF**.

To learn more about managing per-user subscriptions, see Managing per-user subscriptions in Subscription Management and contact your account representative.

In the following table, the term manage indicates access to the following report options: **Update**, **Delete**, and **Export settings**.

## Access with no roles

Can view reports that are shared with them.

## Reporting access with ACL

The report\_view access controls on tables and fields limits the ability to read, edit and create reports. Administrators can create other ACL rules. You need a role that gives you access to the data that is the subject of the report. For more information, see [Restrict report creation with an ACL rule](../task/t_RestrictRepCreationWAnACLRule.md) and [Report\_view access control](../concept/report-view-access-control.md).

**Note:** The Report Publisher \[report\_publisher\] and Report Alias Administrator \[report\_alias\_admin\] roles also exist, but support deactivated functions.

**Parent Topic:**[Reporting reference](../concept/reporting-reference.md)

## Report user \[report\_user\]

Create and view reports that have been shared with them. Cannot share, edit, or delete reports that have been shared with them. Users with the itil role also have these limitations.

### Contains Roles

The Report user \[report\_user\] role contains the Visualization Creator \[viz\_creator\] role. The viz\_creator role also enables a user to create reports.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Report scheduler \[report\_scheduler\]

Schedule emailing of all reports that they can see, including reports they cannot manage. Users with this role must also have another role that grants permission to create, edit, and share reports.

### Contains Roles

The Report scheduler \[report\_scheduler\] role contains the Report user \[report\_user\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Group report user \[report\_group\]

Can manage and share reports that are shared with the groups they are members of \(listed in Group\).

### Contains Roles

The report\_group role contains the Report user \[report\_user\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Global report user \[report\_global\]

Can share a report that is shared with everyone. This role can share with everyone. Cannot share a report that is shared with the user or a group.

### Contains Roles

The report\_global role contains the Report user \[report\_user\] role.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## Report administrator \[report\_admin\]

Manage, share, publish, and schedule all reports. Access **Reports** &gt; **Administration** and manage all report-related objects.

### Contains Roles

List of roles contained within the role.

-   report\_scheduler
-   analytics\_filter\_admin
-   report\_global
-   report\_group
-   gauge\_maker
-   viz\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Report description administrator \[report\_description\_admin\]

Read and update table and field descriptions for reports. Included in the plugin Table and field description configuration for report \[com.glideapp.report.description\_config\].

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

For more information, see [Administer table and field descriptions](../task/admin-table-field-descriptions.md#).

