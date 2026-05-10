---
title: Zero Copy Connectors roles
description: Zero Copy Connectors is installed with these roles.Role for creating and managing connections in Zero Copy Connector Hub.Role for creating and managing data fabric tables in Zero Copy Connector Hub.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Zero Copy Connectors, Workflow Data Fabric]
---

# Zero Copy Connectors roles

Zero Copy Connectors is installed with these roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Zero Copy Connectors reference](reference-zcc.md)

## Connection administrator \[df\_connection\_admin\]

Role for creating and managing connections in Zero Copy Connector Hub.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

A user with the df\_connection\_admin role can create and manage connections in Zero Copy Connector Hub, and can also create and manage data fabric tables just like a user with the a role that contains the df\_data\_steward role.

## Data steward \[df\_data\_steward\]

Role for creating and managing data fabric tables in Zero Copy Connector Hub.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

When a user contains a role that inherits the df\_data\_steward role, the user is considered a data steward in Zero Copy Connector Hub, and can create and manage data fabric tables. When the df\_data\_steward role is granted directly to a user, that user can access Zero Copy Connector Hub, but can't create or manage any data fabric tables.

