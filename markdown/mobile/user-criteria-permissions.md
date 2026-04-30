---
title: User criteria permissions in mobile apps
description: Control the visibility of different areas of your mobile apps by defining user criteria permissions. User criteria permissions enable you to segment your users into different groups, such as location, department or company. You can change information within a single area of a group to update all users' details associated within that group.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [User roles and user criteria permissions for mobile apps, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# User criteria permissions in mobile apps

Control the visibility of different areas of your mobile apps by defining user criteria permissions. User criteria permissions enable you to segment your users into different groups, such as location, department or company. You can change information within a single area of a group to update all users' details associated within that group.

Use user criteria permissions to control access to mobile app components based on factors like departments, groups, locations, roles, or company, or any logic that can be defined via a script. These criteria set specific conditions that are matched against user profiles. When these criteria are established, only users who meet these conditions can see the relevant records.

## User criteria use cases

-   With user criteria permissions, you can change information within a single area of a group to update all users' details associated within that group. For instance, if a company moves to a new location and needs users there to access different mobile content, administrators can modify the user criteria permissions to ensure that new content is shown to all users in that group.
-   User criteria can also be used for mobile theming. For example, a large corporation with many subsidiary companies can maintain the look-and-feel specific to each company. This can include the overall appearance, the empty state images, and the different tabs that display on the navigation bar.
-   You can assign management employees the ability to view certain navigation tabs and data visualizations.

**Note:** If you don't select user criteria for any of these components, any user who has access to the mobile app can see that component. However, users still may not see certain components, as user role permissions may be defined. For a full list of the components where you can apply user roles and user criteria, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md).

User criteria permissions are supported for the following components: Native Client, launcher screen, UI sections, navigation tabs and icon section destination.

-   **Native Client and applications**

    Limit a user's ability to access certain applications in the mobile app. For example, prevent IT Service Management \(ITSM\) users from accessing Field Service Management \(FSM\) applications. Native Client relates to app level functionality and includes components like mobile themes, empty state, navigation bar, geolocation, and offline. You can also define that users don't have permission to view an app. For example, you prefer that agents don’t have access to the Now Mobile app.

-   **Launcher screens**

    Allow only users with specified user criteria to access launcher screens within your mobile applications. For example, create launcher screens specifically for certain roles, and permit only users with specified roles to view these launchers. For more information on launcher screens, see [Launcher screens](sg-mobile-applet-launcher.md).

-   **UI sections**

    Allow only users with specified roles to access launcher screens within your mobile apps. For example, create a launcher screen that only employees with a manager role can see. Additionally, create a launcher screen with an employee role that everyone can view. For more information on launcher screens, see [Launcher screen UI sections](alp-ui-sections.md).

-   **Navigation tabs**

    Limit a user’s ability to access certain tabs displayed in the navigation bar. For more information, [Navigation bar](sg-mobile-tab-bar.md).

    **Note:** You shouldn't remove the Settings and Notifications tabs from the navigation bar.

-   **Icon section destination**

    Limit a user's ability to view either the whole icon section or the icon destination component within an icon section. Icon destination components are icons and images that represent a launcher screen, a function, or a navigation point to a screen.

    -   For icons, use the reference lookup icon to select an existing icon to display in the icon section. For more information, see [Configure an icon UI section](../task/sg-ui-section-config-navig.md).
    -   For images, use the reference lookup icon to select the image to display in the icon section. For more information, see [Adding images to an icon section](../task/add-image-icon-section.md).

## General guidelines for using user criteria

-   Use user criteria if the segmentation is based on things such as location, companies, departments, and groups. Use user roles if the segmentation is based on the user’s skill and role definition.
-   Consider how you're managing different brands, subsidiaries, and locations. Consider if user criteria or user roles is a more appropriate solution for you.
-   Some components can be associated with both user roles and user components, whereas other components are associated with one access control mechanism. For a list of how the components are associated, see [Mobile components where user roles and user criteria permissions apply](../reference/components-roles-criteria.md).
-   For components where you can assign both user roles and user criteria, prioritize assigning user roles unless there's a specific need otherwise, as this approach streamlines operations and improves system responsiveness.
-   Don't associate more than two user criteria to a single mobile component. Exceeding this number may complicate the conditions set and could result in the component not displaying as intended.
-   When assigning user criteria, note that broader user criteria takes precedence over more specific user criteria. For example, if you choose to hide the entire icon section, it overrides any other user criteria that specify hiding individual icons within that section.
-   Minimize the use of scripted user criteria, as they can adversely affect performance.
-   User roles are supported in offline.

-   **[Assign mobile user criteria permissions](../task/user-criteria-config.md)**  
Apply user criteria permissions to segment your users into different groups, such as location, department, or company.
-   **[Define user criteria status as active or inactive](../task/user-criteria-active-inactive.md)**  
Learn how to define a user criteria component's status as active or inactive.

**Parent Topic:**[User roles and user criteria permissions for mobile apps](roles-user-criteria.md)

