---
title: User roles and user criteria permissions for mobile apps
description: User roles and user criteria permissions are access control mechanisms that enable you to define roles or segment users into groups within the mobile platform. With these permissions, you can show or hide different components of your mobile app to either individuals or groups.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Considerations before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# User roles and user criteria permissions for mobile apps

User roles and user criteria permissions are access control mechanisms that enable you to define roles or segment users into groups within the mobile platform. With these permissions, you can show or hide different components of your mobile app to either individuals or groups.

## User roles permissions

User roles control access to features and components within mobile apps for defined target audiences. The admin role provides access to all features and capabilities.

After access has been granted to a role, all the groups or users assigned to the role are granted the access. Use role inheritance to group related permissions, making it easier to manage and assign roles. For example, if an employee has been promoted to a sales manager position, you can allocate additional roles to the employee to reflect their new position.

User role records are stored in the Roles \[sys\_user\_role\] table. For more information, see [Managing roles](https://www.servicenow.com/docs/access?context=ua-creating-roles&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

For a list of all the components where you can define user roles and user criteria, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md). Some components apply to both user roles and user criteria, whereas others are mutually exclusive.

## User criteria permissions

User criteria permissions are an access control mechanism that enables you to grant users access to mobile app components, based on categories such as departments, locations, or company.  User criteria records define conditions that are evaluated against user records. When a user criteria is defined, records are only visible to users who pass the defined conditions.

With user criteria permissions, you can change information within a single area of a group to update all users' details associated within that group. For example, a company relocates, and the management requires that users in the new location have access to different mobile content. Admins can update the user criteria permissions, so that this new content is displayed to all users in this group.

User criteria records are stored in the User Criteria \[user\_criteria\] table.

For a list of all the components where you can define user roles and user criteria, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md). Some components apply to both user roles and user criteria, whereas others are mutually exclusive.

## General guidelines for user roles and user criteria in mobile apps

-   When defining user roles and user criteria, careful planning is required to ensure that components are associated with the correct access control mechanism.
-   Some components can be associated with either user roles and user components, whereas other components are associated with one access control mechanism. For a list of how the components are associated, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md). For example, you can apply user roles to screens and functions. Alternatively, you can apply navigation tabs and icon section destinations to user criteria.
-   You can’t select both user roles and user criteria as access control mechanisms for a component in Mobile App Builder. However, in the web-based UI both user roles and user criteria can be defined for a component. In this situation, the operational mechanism is the value defined in the **Access Control Mechanism** field of the record.
-   Both user roles and user criteria are supported in offline.

-   **[Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md)**  
Lists of mobile components that can be applied to user roles, user criteria, or to both these access control mechanisms.
-   **[User role permissions in mobile apps](sg-roles-permissions.md)**  
Control the visibility of different components of mobile apps by applying user role permissions.
-   **[User criteria permissions in mobile apps](user-criteria-permissions.md)**  
Control the visibility of different areas of your mobile apps by defining user criteria permissions. User criteria permissions enable you to segment your users into different groups, such as location, department or company. You can change information within a single area of a group to update all users' details associated within that group.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

