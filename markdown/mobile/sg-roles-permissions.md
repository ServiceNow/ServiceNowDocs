---
title: User role permissions in mobile apps
description: Control the visibility of different components of mobile apps by applying user role permissions.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [User roles and user criteria permissions for mobile apps, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# User role permissions in mobile apps

Control the visibility of different components of mobile apps by applying user role permissions.

Apply user roles to determine which components are accessible within mobile apps for specific groups of users. The admin role, for instance, enables access to all components. Once a role is assigned, this access extends to all users or groups linked to that role. Additionally, roles can be nested within other roles, so that any permission assigned to one role automatically applies to any inclusive roles.

For example, if an employee moves from the sales department to the finance department, you can assign them roles that relate to their new position, and remove roles that relate to their former position. This means that the user no longer has access to the UI sections showing sales data visualizations, and instead has access to the UI sections showing financial data visualizations.

**Note:** If you don't select user roles for any of these components, any user who has access to the mobile app can see that component. However, users still may not see certain components, as user criteria permissions may be defined.

For a full list of components where you can apply user roles and user criteria, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md).

User roles are supported in the following components: Native Client, screens, launcher screen, UI sections, and functions.

-   **Native Client and applications**

    Limit a user's ability to access certain applications in the mobile app. For example, prevent IT Service Management \(ITSM\) users from accessing Field Service Management \(FSM\) applications. Native Client relates to app level functionality and includes components like mobile themes, empty state, navigation bar, geolocation, and offline. You can also define that users don't have permission to view an app. For example, you want to prevent agents having access to the Now Mobile app.

-   **Screens**

    Allow only users with specified roles to access screens within your mobile applications. For example, enabling only managers to view user records for all their employees. For more information, see  [Mobile screen types](sg-mobile-applet.md).

-   **Launcher screens**

    Allow only users with specified roles to access launcher screens within your mobile apps. For example, create a launcher screen that only employees with a manager role can see. Additionally, create a launcher screen with an employee role that everyone can view. For more information on launcher screens, see [Launcher screens](sg-mobile-applet-launcher.md).

-   **UI sections**

    Limit a user’s ability to access certain UI sections within a launcher screen in the mobile app. For example, assign a development role to certain UI sections, and permit only users with specified development roles to view these UI sections. For more information on launcher screen UI sections, see [Launcher screen UI sections](alp-ui-sections.md).

-   **Functions**

    Only allow users with certain roles to perform specified actions in the app. For example, limit an IT Infrastructure Library \(ITIL\) user's ability to reassign an incident from a swipe action. For more information on limiting user access by role to a specific function, see the steps for creating each function type listed in [Mobile functions](sg-studio-mobile-button-types.md).


## General guidelines for using user roles

-   Use user roles if the segmentation is based on the user’s skill and role definition. Use user criteria, if the segmentation is based on things like, location, companies, departments, and groups.
-   Some components can be associated with both user roles and user components, whereas other components are associated with one access control mechanism. For a list of how the components are associated, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md).
-   For components where you can assign both user roles and user criteria, prioritize assigning user roles unless there's a specific need otherwise, as this approach streamlines operations and improves system responsiveness.
-   User roles are supported in offline.

-   **[Assign mobile user roles permissions](../task/user-roles-config.md)**  
Apply user roles to determine which components are accessible within mobile apps for specific groups of users.

**Parent Topic:**[User roles and user criteria permissions for mobile apps](roles-user-criteria.md)

