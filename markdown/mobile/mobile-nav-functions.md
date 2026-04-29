---
title: Navigation functions
description: Navigation functions transition users from their current screen to another screen or launcher screen.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile functions, Mobile app components, Building mobile apps, Mobile Platform]
---

# Navigation functions

Navigation functions transition users from their current screen to another screen or launcher screen.

<table id="table_utd_nbc_xlb"><tbody><tr><td>

Use navigation functions to transition from your current screen to another screen or launcher screen. For example, opening a record from a list, or moving from an employee user profile screen to a manager user profile screen. Navigation functions use the **Global** or **Record** context.

</td><td>

![A navigation function configured to navigate from a form field to a user record.](../image/navigation-example.png)

</td></tr></tbody>
</table>## Navigation function contexts

-   **Global Context**

    Use global context navigation functions in situation where the navigation does not depend on information from a record. For example, to navigate to a specific screen or launcher screen, you can use a global context navigation function. For examples of global context navigation configuration, see:

    -   [Configure a navigation to a screen](../task/sg-config-navigation-function.md)
    -   [Configure navigation to a launcher screen](sg-launcher-nav-example.md)
-   **Record Context**

    Use record context navigation functions in situations where the navigation depends on information from a record. For example, you want to navigate from the **Assigned to** field in an incident record to the assignee's user record. In this case, you would use a record context navigation.


