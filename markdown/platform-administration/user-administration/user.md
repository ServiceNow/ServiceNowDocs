---
title: The User record
description: Learn about user records and their use within the ServiceNow AI Platform.
locale: en-US
release: australia
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring user admin, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# The User record

Learn about user records and their use within the ServiceNow AI Platform.

## User account records

User records establish a relationship between an individual and your ServiceNow instance. User records consist of a user name, a password, and information relating to the individual, such as contact information, location, and job title.

![A sample user record.](../image/user-record.png "User record")

User records are stored in the Users \[sys\_user\] table.

## Related records

User records are associated with records on several other tables to control permissions, preferences, and other features.

-   **Roles**

    Roles control access to features and capabilities in applications and modules. For more information on roles, see [Managing roles](ua-creating-roles.md).

    **Note:**

    When possible, simplify user administration by assigning roles to groups. Create groups that contain all the roles necessary for specific personas, and then assign users to those groups.

-   **Groups**

    A group is a set of users who share a common purpose. Users assigned to groups are automatically assigned to all roles associated with that group. For more details, see [Creating groups](ua-creating-groups.md) and [Managing roles](ua-creating-roles.md).

-   **Delegates**

    In addition to role and group assignments, users can be assigned as delegates, giving them permission to act with the same permissions as a delegator user. See [Delegating roles](c_DelegateRoles.md) for more information on delegation.

-   **Skills**

    Use skill management to associate users with their areas of training and expertise. For more information on skill management, see Skill Management.

-   **Subscriptions**

    Administrators use subscriptions to control which users have access to purchased subscriptions on their instances. Details on subscription management can be found at [Subscription Management](../../subscription-management/reference/subscription-management-landing-page-v2.md).

-   **User preferences**

    User accounts are also connected with user preferences. Users can save personalized preferences to configure many UI features, as well as preferences regarding the notifications they receive. Details on administering user preferences are found at User preferences.


## Date and time formatting

You can set your preferred date and time formatting through the User record. If you don't specify a preference in these fields, the system applies default formatting.

The Date format field appears in the User record by default and can be modified without specific permissions. However, the Time format field must be added to the User record by revealing additional form fields. For instructions on showing or hiding form fields, see [Configuring the form layout](../../form-administration/concept/configure-form-layout.md#). If you can't modify form fields, contact your organization's user administrator to update your time format preferences.

The Date and time format field in **User Menu** &gt; **Preferences** &gt; **Language &amp; Region** extends the options you select in the Date format and Time format fields of your User record. For more information, see User preferences. Timezone settings automatically sync between the User record and your preferences.

## System and guest users

Some automated processes use the system or guest user to apply and track changes to records. As a result, some records may show that they were last updated by system or guest.

For example, when a user logs in for the first time in a day, some fields on that user's record are updated by the system user, such as **Last login** and **Last login time**. If a user has a failed login attempt or is locked out, some fields on that user's record are updated by the guest user, such as **Failed Login Attempts** or **Locked Out**.

If a record was last updated by the system or by guest users, identify the fields that were updated by enabling auditing for the table and viewing the audit history set. For more information, see Configuring auditing for a table and Knowing about History sets.

