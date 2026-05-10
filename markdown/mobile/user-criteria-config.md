---
title: Assign mobile user criteria permissions
description: Apply user criteria permissions to segment your users into different groups, such as location, department, or company.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [User criteria permissions, User roles/criteria permissions, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Assign mobile user criteria permissions

Apply user criteria permissions to segment your users into different groups, such as location, department, or company.

## About this task

You can apply user criteria permissions to certain components of your mobile apps. For a complete list, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md). The instructions in this topic demonstrate how to apply user criteria to any one of the supported components. Some components can have either user criteria or user roles associated with them, in such a situation you must select whether this component is to be assigned a user criteria or a user role.

**Note:** If you don't add user criteria to any of the components, all users who have access to the mobile app can see those components. There may be a situation where users may still not see certain components as user role permissions may be implemented.

## Before you begin

Role required: admin

When working with user criteria in the Mobile App Builder, you assign existing user criteria permissions and then map them to a mobile component. To create additional user criteria permissions, you must create a record in the User Criteria \[user\_criteria\] table, by doing the following:

1.  Navigate to **All**.
2.  In the **Filter navigator** field, enter `user_criteria.list`.
3.  Select **New** in the User Criteria Records form.
4.  Complete the form as required and select **Submit**.

    **Note:** Use the following resources when creating a user criteria.

    -   [Create a user criteria record for Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/create-user-criteria-record.md): Describes the various fields in the User Criteria record form.
    -   [Scripts in user criteria](https://www.servicenow.com/community/itsm-blog/scripts-in-user-criteria/ba-p/2294597): Describes how to use scripting logic and apply it to user criteria permissions.

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder opens in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you are working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  Select **All mobile records** from the menu.

4.  Select a record that supports the assignment of user criteria from the **Record type** field.

    For a list of the mobile components that you can assign user criteria, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md).

5.  If your selected record has the option of both user roles and user criteria, then in the **Access control type** field select **User criteria**.

6.  In the **User criteria access** field, select **Choose** to open the Choose an item window.

7.  Assign a predefined user criteria to the current record and select **Apply**.

8.  Repeat step 6 and step 7 to add additional user criteria to a component.

    **Note:** It's suggested to assign no more than two user criteria to each component.

9.  Select **Save**.


## What to do next

By default, when you apply a user criteria to a component the user criteria is in an active state. To change the state from active to inactive, see [Define user criteria status as active or inactive](user-criteria-active-inactive.md).

**Parent Topic:**[User criteria permissions in mobile apps](../concept/user-criteria-permissions.md)

