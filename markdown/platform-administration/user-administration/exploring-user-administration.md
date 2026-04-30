---
title: Exploring user administration
description: Learn more about user administration for your instance.
locale: en-US
release: zurich
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [User admin, Configure core features, Administer]
---

# Exploring user administration

Learn more about user administration for your instance.

## User administration overview

Creating users, groups, and roles provide a flexible and scalable way to manage access to features on the ServiceNow AI Platform. By creating user accounts, assigning users to groups, and defining roles and permissions, administrators can ensure that users have the appropriate level of access to applications and data. This enables organizations to control access to sensitive data, maintain conformance with regulatory requirements, and improve overall security. Additionally, users, groups, and roles can be easily managed and modified over time as organizational needs change.

## Work flow

Subscriptions, users, groups, and roles work together to help you define who can access features on your instance.

1.  [Subscription Management](../../subscription-management/reference/subscription-management-landing-page-v2.md)

    Understand your subscriptions. Subscription management enables you to manage your subscriptions proactively and monitor subscription usage on your instances.

    Subscriptions may include per-user subscriptions. For more information, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md).

2.  [Creating users, companies, and departments](using-user-administration.md)

    Create an account record for the individuals who have access to your instance. Each user account has a unique login ID, password, and set of permissions \(roles\) that define what they can do and access within the platform.

3.  [Creating groups](ua-creating-groups.md)

    Define groups that have similar roles or permissions. Groups enable you to apply permissions \(roles\) to multiple users at the same time. When a user is a member of a group, that user has the same permissions that have been defined for the group.

    You can view group members by navigating to **All** &gt; **User Administration** &gt; **Groups**. Select a group name and view the members in the Group Members related list.

4.  [Managing roles](ua-creating-roles.md)

    Roles describe the types of activities that a user can perform on the instance. Each role has a set of permissions that can govern what the users and groups can do, such as read, write, create, or delete records. Roles can be assigned to users and groups. Users can have multiple roles.

    For a complete list of the roles included with the ServiceNow AI Platform, see [Base system roles](../reference/r_BaseSystemRoles.md).

    Role records are stored in the Roles \[sys\_user\_role\] table.

5.  [Monitoring instance usage](../../subscription-management/concept/usage-analytics-module-subscription.md)

    Users with the admin or usage\_admin role can view the **Application usage overview** and ServiceNow Store **usage overview** dashboards to track instance usage.

6.  [Monitoring user activity](user-admin-tools-landing.md)

    Users with the admin role can impersonate users, manage user sessions, and leverage non-interactive sessions.


![Create users and add them to groups. Create and assign roles to both users and groups.](../image/users-groups-roles.png "User administration workflow")

## User preferences

Users can configure many UI features. Some examples include the number of rows per page in a list or whether the response time displays at the bottom of a list or form. Administrators can modify or delete these preferences as needed. For more information, see [User preferences](https://www.servicenow.com/docs/access?context=c_UserPreferences&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

## User groups

A group is a set of users who share a common purpose. Groups may perform tasks such as approving change requests, resolving incidents, receiving email notifications, or performing work order tasks. Any business rules, assignment rules, system roles, or attributes that refer to the group apply to all group members automatically. Users with the user\_admin role can create and edit groups.

When possible, simplify user administration by assigning roles to groups. Create groups that contain all the roles necessary for specific personas, and then assign users to those groups.

**Note:** You can view group members by navigating to **All** &gt; **User Administration** &gt; **Groups**. Select a group name and view the members in the **Group Members** related list.

Group records are stored in the Groups \[sys\_user\_group\] table.

## User roles

Roles control access to features and capabilities in applications and modules. The admin role provides access to all features and capabilities.

After access has been granted to a role, all the groups or users assigned to the role are granted the access. Roles can contain other roles, and any access granted to a role is granted to any role that contains it.

For a complete list of the roles included with the ServiceNow platform, see [Base system roles](../reference/r_BaseSystemRoles.md).

**Note:**

When possible, simplify user administration by assigning roles to groups. Create groups that contain all the roles necessary for specific personas, and then assign users to those groups.

Role records are stored in the Roles \[sys\_user\_role\] table.

