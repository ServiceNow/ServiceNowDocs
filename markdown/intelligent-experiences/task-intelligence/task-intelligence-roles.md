---
title: Task Intelligence roles
description: Task Intelligence is installed with these roles.Admin user with rights to all actions in the application. Creates, edits, and monitors all Task Intelligence models.Views and monitors Task Intelligence models. Requires additional accesses to see training.Monitors Task Intelligence models through the Analytics dashboard.
locale: en-US
release: australia
product: Task Intelligence
classification: task-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Task Intelligence references, Task Intelligence, Enable AI experiences]
---

# Task Intelligence roles

Task Intelligence is installed with these roles.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/managing-user-subscriptions-v2.md) and contact your account representative.

## Task Intelligence Admin \[tia\_admin\]

Admin user with rights to all actions in the application. Creates, edits, and monitors all Task Intelligence models.

### Contains Roles

List of roles contained within the role.

-   ml\_admin
-   platform\_ml\_read

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## Task Intelligence User \[tia\_user\]

Views and monitors Task Intelligence models. Requires additional accesses to see training.

### Contains Roles

List of roles contained within the role: ml\_report\_user.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

## Task Intelligence Analyst \[tia\_analyst\]

Monitors Task Intelligence models through the Analytics dashboard.

### Contains Roles

List of roles contained within the role: ml\_admin.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

