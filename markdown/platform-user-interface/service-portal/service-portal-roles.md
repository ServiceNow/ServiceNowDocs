---
title: Service Portal roles
description: Service Portal installs these roles.Manages the configuration of portals created by Service Portal.Manages posting announcements to portals.Can create Usage Insights settings for Service Portal.Users with this role can view the Analytics Dashboard link and settings within in the application navigator, and have viewer role permissions for portal metrics in the Service Portal Analytics Dashboard.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Service Portal reference, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Service Portal roles

Service Portal installs these roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=australia&pubname=australia-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Service Portal reference](../concept/reference-service-portal.md)

## Service Portal administrator \[sp\_admin\]

Manages the configuration of portals created by Service Portal.

### Contains Roles

List of roles contained within the role.

-   evam\_admin
-   taxonomy\_admin
-   search\_application\_admin
-   announcement\_admin

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Announcements administrator \[announcement\_admin\]

Manages posting announcements to portals.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Portal analytics administrator \[portal\_analytics\_admin\]

Can create Usage Insights settings for Service Portal.

### Contains Roles

List of roles contained within the role: portal\_analytics\_viewer.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Portal analytics viewer \[portal\_analytics\_viewer\]

Users with this role can view the **Analytics Dashboard** link and settings within in the application navigator, and have viewer role permissions for portal metrics in the **Service Portal** &gt; **Analytics** Dashboard.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Read-only access to analytics. Use the Portal analytics administrator \[portal\_analytics\_admin\] role to manage analytics.

