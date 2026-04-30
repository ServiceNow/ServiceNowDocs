---
title: Mobile functions
description: Configure functions in Mobile App Builder to determine which actions users can perform in the mobile app.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Mobile app components, Building mobile apps, Mobile Platform]
---

# Mobile functions

Configure functions in Mobile App Builder to determine which actions users can perform in the mobile app.

## Function types

<table id="table_k21_ktm_rlb"><tbody><tr><td>

Actions

 Use action functions to change data, such as assigning a task to yourself or adding a comment to a record. Action functions require a write-back action item to operate. Configure your actions with input parameters to include user input in the changes you make. For more detail on this function type, see [Action functions](mobile-actions.md).

</td><td>

![Action function.](../image/action-functions.png)

</td></tr><tr><td>

Navigations

 Use navigation functions to transition from your current screen to another screen or launcher screen. For example, opening a record from a list, or moving from an employee user profile screen to a manager user profile screen. For more detail on this function type, see [Navigation functions](mobile-nav-functions.md).

</td><td>

![Action function.](../image/navigation-function.png)

</td></tr><tr><td>

Smart buttons

 Use smart button functions enable your users to take an action using the native capabilities of their mobile device. These buttons give your users quick access to phone, email, locations or navigate to a specific URL. For more detail on this function type, see [Smart button functions](sg-mobile-smart-button.md).

</td><td>

![Smart button functions.](../image/smart-button-function.png)

</td></tr><tr><td>

Predefined buttons

 Predefined button functions allow you to use prebuilt functions that don’t require any additional configuration. Choose from Cancel, Continue, and Log Out actions. For more detail on this function type, see  [Predefined button functions](predefined-button-functions.md).

</td><td>

![predefined button functions](../image/predefined-button-functions.png)

</td></tr></tbody>
</table>## Function context

When you create an action, you must choose whether the function context is **record** or **global**. Choose a context based on what you want to function to do.

-   **Record context**

    Use record context for functions that use the current record. For example, a function on a form used to update or edit the record would use record context.

-   **Global context**

    Use global context when the function is not required to act on an existing record. For example, a function to create a new record on a table, or global actions that appear in a launcher screen.


## Function locations

For each function you create for an application, you must associate it with a specific location. You can associate most functions with a top menu, a swipe, or a specific field. For details on this configuration, see [Associate a function with a location in the app](../reference/sg-studio-button-instances.md)

## Carried parameters

Parameters are a way of creating a variable or a placeholder that is waiting for input from either the user or the database. The variable then queries the database or the user for more information.

