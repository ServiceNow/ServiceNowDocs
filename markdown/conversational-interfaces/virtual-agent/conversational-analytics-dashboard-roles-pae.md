---
title: Conversational Analytics dashboard roles
description: Conversational Analytics dashboard is installed with these roles.Provides read and write access to all dashboard-related tables, for example, sys-conversation.Provides access to view dashboard-related tables, create custom events, create custom formula overrides, reconfigure the dashboard using UI Builder, and set system parameters.Enables you to add, remove, and rearrange dashboard contents. Needs UI Builder, which is a separate ServiceNow product.Provides read access to view the dashboard, Conversations \(sys\_cs\_conversation\), and Conversation Consumers \(sys\_cs\_consumer\) tables.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Conversational Analytics dashboard reference, Conversational Analytics dashboard in Platform Analytics experience, Analyze VA performance, Virtual Agent, Conversational Interfaces]
---

# Conversational Analytics dashboard roles

Conversational Analytics dashboard is installed with these roles.

To learn more about managing subscriptions, see Managing per-user subscriptions in Subscription Management and contact your account representative.

**Parent Topic:**[Conversational Analytics dashboard reference](conversational-analytics-dashboard-reference-pae.md)

## Virtual Agent administrator \[virtual\_agent\_admin\]

Provides read and write access to all dashboard-related tables, for example, sys-conversation.

### Contains Roles

List of roles contained within the role.

-   chat\_analytics\_admin
-   ui\_builder\_admin
-   chat\_analytics\_viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Chat analytics administrator \[chat\_analytics\_admin\]

Provides access to view dashboard-related tables, create custom events, create custom formula overrides, reconfigure the dashboard using UI Builder, and set system parameters.

### Contains Roles

List of roles contained within the role: chat\_analytics\_viewer.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## UI builder administrator \[ui\_builder\_admin\]

Enables you to add, remove, and rearrange dashboard contents. Needs UI Builder, which is a separate ServiceNow product.

### Contains Roles

List of roles contained within the role.

-   workspace\_admin
-   canvas\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Note:** Avoid granting an admin role when more specialized roles are available.

## Chat analytics viewer \[chat\_analytics\_viewer\]

Provides read access to view the dashboard, Conversations \(sys\_cs\_conversation\), and Conversation Consumers \(sys\_cs\_consumer\) tables.

### Contains Roles

List of roles contained within the role: sn\_ace.ace\_user.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

