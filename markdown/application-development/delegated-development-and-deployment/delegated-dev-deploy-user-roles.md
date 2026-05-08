---
title: System-managed developer and deployment roles
description: Although system admins can still manually assign and remove the user roles, they are encouraged to let the system manage the following delegated developer roles.
locale: en-US
release: australia
product: Delegated Development and Deployment
classification: delegated-development-and-deployment
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [User roles, Configure, Delegated Development, Planning your application, Building applications]
---

# System-managed developer and deployment roles

Although system admins can still manually assign and remove the user roles, they are encouraged to let the system manage the following delegated developer roles.

To learn more about managing per-user subscriptions, see Managing per-user subscriptions in Subscription Management and contact your account representative.

<table id="table_wp4_wjx_hv"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

delegated\_developer

</td><td>

User has one or more developer permissions.

</td></tr><tr><td>

Roles that start with an sn\_dd prefix \(for example, sn\_dd\_&lt;app\_name&gt;\_upgrade\_app\)

</td><td>

User has an application-specific developer permission. The role name indicates the application scope to which it applies.For example, after a user with a sn\_appclient.app\_client\_company\_installer role installs a company application, the system automatically grants a sn\_dd\_&lt;app\_name&gt;\_upgrade\_app delegated deployment role. This role allows the user to upgrade the application when future updates are published to the Application Client page.

</td></tr><tr><td>

glide.security.add\_admin\_contained\_roles\_to\_system

</td><td>

Default Value: true if the property is true, then all the roles, directly or indirectly contained by the admin role, are added to the system user, including the scoped-admin roles.

 **Note:** Setting the property to false results in the old behavior, where the system user has the admin role, but not any of the scoped-admin roles contained by the admin role.

 Example: The admin role contains the **sn\_templated\_snip.template\_snippet\_admin** role

 Old behavior: The system user does not have the **sn\_templated\_snip.template\_snippet\_admin** role.

 New behavior: The system user has the **sn\_templated\_snip.template\_snippet\_admin** role and other scoped roles that it contains.

</td></tr></tbody>
</table>**Note:** Users with delegated developer roles cannot add or remove the system admin role.

