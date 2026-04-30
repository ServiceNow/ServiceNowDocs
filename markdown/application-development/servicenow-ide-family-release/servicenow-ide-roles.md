---
title: ServiceNow IDE roles
description: The following roles are installed for use with ServiceNow IDE.Create and develop scoped applications in the ServiceNow IDE.Assign administrator privileges to a MID server user to manage applications in source control from the ServiceNow IDE.
locale: en-US
release: yokohama
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# ServiceNow IDE roles

The following roles are installed for use with ServiceNow IDE.

**Note:** Users with the Creator Studio Restricted User \[sn\_creatorstudio.restricted\_user\] role aren't able to access the ServiceNow IDE regardless of any other roles assigned.

## ServiceNow IDE Administrator \[sn\_glider.admin\]

Create and develop scoped applications in the ServiceNow IDE.

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
-   sn\_udc.admin: Required to modify application files from the Metadata Explorer.
-   sn\_udc.basic\_read: Used for read-only access to application files in the Metadata Explorer.

## ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]

Assign administrator privileges to a MID server user to manage applications in source control from the ServiceNow IDE.

MID Server users must have the sn\_glider.ide\_git\_user role or admin role to perform Git operations in the ServiceNow IDE. For more information, see [Create the MID Server user and grant the role](https://www.servicenow.com/docs/access?context=t_SetupMIDServerRole&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Configure a MID Server to use source control with the ServiceNow IDE](../task/configure-mid-server-source-control.md).

### Contains Roles

List of roles contained within the role:

credential\_admin

### Groups

This role is assigned to no groups by default.

### Special considerations

None.

