---
title: ServiceNow IDE roles
description: The following roles are installed for use with ServiceNow IDE.Create and develop applications in the ServiceNow IDE.Assign administrator privileges to a MID server user to manage applications in source control from the ServiceNow IDE.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow IDE roles

The following roles are installed for use with ServiceNow IDE.

**Note:** Users with the Creator Studio Restricted User \[sn\_creatorstudio.restricted\_user\] role aren't able to access the ServiceNow IDE regardless of any other roles assigned.

## ServiceNow IDE Administrator \[sn\_glider.admin\]

Create and develop applications in the ServiceNow IDE.

For more information about granular admin roles, see [Granular admin roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/granular-admin-roles.md).

### Contains Roles

List of roles contained within the role.

-   sn\_glider.create\_app\_admin
-   sn\_glider.read\_admin
-   sn\_glider.write\_admin

### Groups

This role is assigned to no groups by default.

### Special considerations

In addition to this role, the following roles are necessary for certain functionality in the ServiceNow IDE:

-   credential\_admin: Required to perform Git operations.
-   sn\_udc.admin: Required to modify application files from the File Categories view.
-   sn\_udc.basic\_read: Used for read-only access to application files in the File Categories view.

## ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]

Assign administrator privileges to a MID server user to manage applications in source control from the ServiceNow IDE.

MID Server users must have the sn\_glider.ide\_git\_user role or admin role to perform Git operations in the ServiceNow IDE. For more information, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SetupMIDServerRole.md) and [Configure a MID Server to use source control with the ServiceNow IDE](../task/configure-mid-server-source-control.md).

### Contains Roles

List of roles contained within the role:

credential\_admin

### Groups

This role is assigned to no groups by default.

### Special considerations

None.

