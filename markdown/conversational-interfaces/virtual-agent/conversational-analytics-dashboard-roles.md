---
title: Legacy - Conversational Analytics dashboard roles
description: Conversational Analytics dashboard is installed with these roles.Provides read and write access to all dashboard-related tables, for example, sys-conversation.Provides access to view dashboard-related tables, create custom events, create custom formula overrides, reconfigure the dashboard using UI Builder, and set system parameters.Enables you to add, remove, and rearrange dashboard contents. Needs UI Builder, which is a separate ServiceNow product.Provides read access to view the dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy - Conversational Analytics dashboard reference, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Conversational Analytics dashboard roles

Conversational Analytics dashboard is installed with these roles.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Legacy - Conversational Analytics dashboard reference](conversational-analytics-dashboard-reference.md)

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

Provides read access to view the dashboard.

### Contains Roles

List of roles contained within the role: sn\_ace.ace\_user.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

