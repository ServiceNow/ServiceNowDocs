---
title: Workflow Data Fabric Hub roles
description: Workflow Data Fabric Hub is installed with these roles.Role for creating and managing connections in Workflow Data Fabric Hub.Role for creating and managing data fabric tables in Workflow Data Fabric Hub.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: reference
last_updated: "2023-11-20"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric Hub reference, Workflow Data Fabric Hub, Data and Automation]
---

# Workflow Data Fabric Hub roles

Workflow Data Fabric Hub is installed with these roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Workflow Data Fabric Hub reference](wdf-reference.md)

## Connection administrator \[df\_connection\_admin\]

Role for creating and managing connections in Workflow Data Fabric Hub.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

A user with the df\_connection\_admin role can create and manage connections in Workflow Data Fabric Hub, and can also create and manage data fabric tables just like a user with the a role that contains the df\_data\_steward role.

## Data steward \[df\_data\_steward\]

Role for creating and managing data fabric tables in Workflow Data Fabric Hub.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

When a user contains a role that inherits the df\_data\_steward role, the user is considered a data steward in Workflow Data Fabric Hub, and can create and manage data fabric tables. When the df\_data\_steward role is granted directly to a user, that user can access Workflow Data Fabric Hub, but can't create or manage any data fabric tables.

