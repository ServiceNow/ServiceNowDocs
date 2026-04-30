---
title: Types of subscriptions in Subscription Management
description: Subscriptions to ServiceNow applications come in different types. The type of subscription determines the allocation of users, access to applications, and custom application and table entitlements.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# Types of subscriptions in Subscription Management

Subscriptions to ServiceNow applications come in different types. The type of subscription determines the allocation of users, access to applications, and custom application and table entitlements.

Each type of product subscription is measured according to a meter. For details on the different types of meters and what they measure see [KB0727967](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0727967).

<table id="table_jls_2y3_yq"><thead><tr><th>

Subscription type

</th><th>

Associated meter types

</th><th>

Usage allocation method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Capacity

</td><td>

-   Devices
-   Subscription Units
-   Transactions
-   Assists

</td><td>

No manual steps are required. Usage is automatically calculated and shown in your instance.

</td><td>

Automatically tracks measured units, and counts of transactions, records created, or resources managed such as devices, software, or nodes.

</td></tr><tr><td>

Display Only

</td><td>

None

</td><td>

Allocation isn't measured

</td><td>

Displays information. This type of subscription doesn't support allocation.

</td></tr><tr><td>

Per-User

</td><td>

-   Rights-based user: measure of Fulfiller Users and Business Stakeholder Users
-   Application user: measure of users with any level of access to a product; includes Creator Users

</td><td>

Manually allocated

</td><td>

Provides entitlements to users according to their assigned roles and associated access rights. You allocate per-user subscriptions manually by adding groups with measured roles or access rights to a product subscription. Subscription Management helps you with the allocation process by recommending groups based on their role assignments.

</td></tr><tr><td>

Unlimited

</td><td>

Unlimited: No measurement limit

</td><td>

Automatically allocated by your instance

</td><td>

Provides entitlements to users, with no limit to the number of users that can be allocated.

</td></tr><tr><td>

Unrestricted User

</td><td>

Unrestricted user: Instance-wide measure of all active users

</td><td>

Automatically allocated by your instance

</td><td>

Provides entitlements for an organization's number of active users regardless of their role assignments. An active user is any user whose record in the Users \[sys\_user\] table has a value in the **User ID** field and has the **Active** field set to true.

</td></tr></tbody>
</table>**Parent Topic:**[Subscription Management reference](subscription-management-reference-v2.md)

