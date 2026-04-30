---
title: User sets and groups in Subscription Management
description: Subscription Management uses groups \(previously user sets\) to provide entitlement to sets of users.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reference, Subscription Management, Get started, Administer the ServiceNow AI Platform]
---

# User sets and groups in Subscription Management

Subscription Management uses groups \(previously user sets\) to provide entitlement to sets of users.

## User set and groups overview

Prior to Quebec, Subscription Management used user sets to group users together. Usage\_admins grouped users by conditions, such as what city or department they are in. User sets could then be assigned to subscriptions to give every user in the user set a license to the subscription.

In Quebec and later releases, all user sets are converted to groups. A group is a set of users who share a common purpose. Similar to user sets, groups can be added to subscriptions. Adding a group to a subscription gives every user in the group entitlement.

## User set conversion

On upgrade to Quebec or later releases, all current user sets convert to groups. The new groups contain the same users and properties as your user sets. The conversion is a one-time occurrence, and users are not automatically added or removed from the new group after the conversion.

## Group management

Admins and user\_admins create groups and add users in the **User Administration** application.

To learn more about creating and editing groups, see [Creating groups](../../roles/concept/ua-creating-groups.md).

**Parent Topic:**[Subscription Management reference](../reference/subscription-management-reference-v2.md)

