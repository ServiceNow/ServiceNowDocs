---
title: Proactive Triggers roles
description: Proactive Triggers adds the Proactive Triggers admin role.Users who create proactive rules and have access to related tables and related records.
locale: en-US
release: australia
product: Product Support for Technology
classification: product-support-for-technology
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with the Proactive Triggers feature, Proactive Triggers reference, Proactive Triggers, Manage people and work, Conversational Interfaces]
---

# Proactive Triggers roles

Proactive Triggers adds the Proactive Triggers admin role.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

## Installed roles

<table id="table_mlr_2xn_cyb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains Roles

</th><th>

Groups

</th><th>

Elevated

</th><th>

Considerations

</th></tr></thead><tbody><tr><td>

Proactive Triggers admin

 \[sn-pt.proactive\_admin\]

</td><td>

Users who create proactive rules and have access to related tables and related records.

</td><td>

-   User Criteria Administrator \[user\_critera\_admin\]
-   Service Portal administrator \[sp\_admin\]

</td><td>

None.

</td><td>

No

</td><td>

Users assigned this role can access any related tables and records including potentially protected information, as well as proactive rules.

</td></tr></tbody>
</table>**Note:**

Simplify user administration by creating groups that contain all the roles necessary for specific personas rather than to individual users. You can then assign individual users to those groups. When users transition to new roles, you can then re-assign their group memberships, and avoid scenarios where users retain unexpected roles.

For details on the administration of users, groups, and roles, see [User Administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/c_UserAdministration.md).

**Parent Topic:**[Components installed with the Proactive Triggers feature](../concept/components-installed-with-proactive-triggers.md)

## Proactive Triggers admin \[sn-pt.proactive\_admin\]

Users who create proactive rules and have access to related tables and related records.

### Contains Roles

List of roles contained within the role.

-   User Criteria Administrator \[user\_critera\_admin\]
-   Service Portal administrator \[sp\_admin\]

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

