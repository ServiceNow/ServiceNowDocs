---
title: Roles installed with Notify
description: Notify adds the following roles.Administrator with privileges for Notify 2 functionality.Assign to users who need to view notify content.
locale: en-US
release: australia
product: Notify
classification: notify
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Components installed with Notify, Notify reference, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Roles installed with Notify

Notify adds the following roles.

If you have created a new role, then you must add the new role to the corresponding deny ACL list to not allow user to access the Notify tables.

**Note:** Only the user with the Notify administrator \[notify\_admin\], and Notify viewer \[notify\_view\] roles can have access to Notify tables. The deny unless authenticated ACLs restrict access to the Notify tables for any unauthenticated role such as public role user.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[Components installed with Notify](installed-with-notify2.md)

## Notify administrator \[notify\_setup\_admin\]

Administrator with privileges for Notify 2 functionality.

### Contains Roles

List of roles contained within the role.

-   notify\_admin
-   sn\_twilio\_direct.admin
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

