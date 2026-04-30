---
title: Roles installed with Notify
description: Notify adds the following roles.Administrator with privileges for Notify 2 functionality.Assign to users who need to view notify content.
locale: en-US
release: xanadu
product: Notify
classification: notify
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Components installed with Notify, Reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Roles installed with Notify

Notify adds the following roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Components installed with Notify](installed-with-notify2.md)

## Notify administrator \[notify\_admin\]

Administrator with privileges for Notify 2 functionality.

### Contains Roles

List of roles contained within the role.

-   workflow\_admin
-   workflow\_creator
-   workflow\_publisher

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## Notify viewer \[notify\_view\]

Assign to users who need to view notify content.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

This role has read-only access to the Notify Conference Calls table \[notify\_conference\_call\] and the Notify Conference Call Participants table \[notify\_participant\].

The itil role inherits the notify\_view role when the Incident Communications Management and the Notify plugins are activated.

