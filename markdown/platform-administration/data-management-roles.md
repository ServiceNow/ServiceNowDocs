---
title: Data Management roles
description: Data Management includes the following roles.The data\_mgmt\_tools\_admin role is a granular admin role designed to provide more targeted permissions for data management tasks, reducing the need to grant full admin access.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Data Management roles

Data Management includes the following roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Data Management reference](data-management-reference.md)

## Data Management tools admin \[data\_mgt\_tools\_admin\]

The data\_mgmt\_tools\_admin role is a granular admin role designed to provide more targeted permissions for data management tasks, reducing the need to grant full admin access.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Granting data\_mgmt\_tools\_admin alone is not sufficient for most data management operations. To enable full functionality for the data\_mgmt\_tools\_admin role, you must also assign the following roles:

-   delegated\_developer: Required for access to tables, columns, and application scopes
-   events\_admin: Required to write trigger data for scheduling jobs
-   context\_rollback\_executor: Required to roll back records that have been updated or deleted

These roles are not embedded within data\_mgmt\_tools\_admin by default. You must assign these additional roles to the user explicitly.

After assigning these roles, also add roles that provide CRUD \(Create, Read, Update, Delete\) access to data tables \(for example, itil and itil\_admin\). For example, adding the itil\_admin enables an ITIL administrator to archive or update records in the associated ITIL tables \(incident, problem, change, and so on\) depending on configuration. If these roles aren’t assigned, some or all data management functionality will be limited or unavailable.

