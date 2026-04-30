---
title: Assign mobile user roles permissions
description: Apply user roles to determine which components are accessible within mobile apps for specific groups of users.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [User role permissions in mobile apps, User roles and user criteria permissions for mobile apps, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Assign mobile user roles permissions

Apply user roles to determine which components are accessible within mobile apps for specific groups of users.

## About this task

You can apply user roles to certain components of your mobile apps. For a complete list, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md). The instructions in this topic demonstrate how to apply roles to supported mobile components. Some components can have either user roles or user criteria components associated with them, in such a situation you must select whether this component is assigned a user role or a user criteria.

**Note:** If you do not add roles to any of the components, all users who have access to the mobile app can see those components. There may be a situation where users may still not see certain components as user criteria permissions may be implemented.

## Before you begin

Role required: admin

When working with user roles in the Mobile App Builder, you assign existing user roles permissions and map them to a mobile component. To create additional user roles, you must access the Roles \[sys\_user\_role\] table. For more information, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  Select a record that supports the assignment of user roles from the **Record type** field.

    For a list of the mobile components that you can assign user roles, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md).

5.  If your selected record has the option of both user roles and user criteria, then in the **Access control type** field, select **User roles**.

6.  In the **Role access** field, select **Choose** to open the Choose an item window.

7.  Select all the roles that you want to assign to the current record.

8.  Select **Apply**.

9.  Select **Save**.


**Parent Topic:**[User role permissions in mobile apps](../concept/sg-roles-permissions.md)

