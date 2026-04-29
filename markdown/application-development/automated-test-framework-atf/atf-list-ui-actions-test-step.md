---
title: List UI actions test steps
description: Select a UI action from a list to perform different actions on a list or a related list.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# List UI actions test steps

Select a UI action from a list to perform different actions on a list or a related list.

You can create a new UI action of the following types. See [Create a UI action](https://www.servicenow.com/docs/access?context=t_EditingAUIAction&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for more information.

-   **List banner button**: Creates a button on the banner of a list.

    ![Image showing the list banner button](../image/atf-list-banner-button.png "List banner button")

-   **List bottom button**: Creates a button at the bottom of the list.

    ![Image showing list bottom button](../image/atf-bottom-button.png "List bottom button")

-   **List context menu**: Adds an option to the context menu of the list.

    ![Image showing the UI action in the context menu](../image/atf-list-context-menu.png "List context menu")

-   **List choice**: Adds an option to the list choice at the bottom of the list. You need to select one or more tests to enable the recently added list choice.

    ![Image showing the added option in the list](../image/atf-list-choice.png "List choice")

-   **List link**: Adds a link to the **Related Links** list.

    ![Image showing the links added to the Related Links list](../image/atf-list-link.png "List link")


## Design considerations

-   To use the **Click a List UI Action** test step, the test first needs to navigate to the list or the form with the related list containing the UI action.
-   The **Related list** field appears only when you select Related list as the **List type**.
-   **Action type** is mostly auto-filtered depending on the **List action** chosen.
-   The **Record** field appears only when you select **Single record** for the UI action to be applied.
-   Identify the specific record if you have selected **Single record** to apply the UI action.
-   For the **Timeout** field to appear, select **Page reloaded or redirected** as the **Assert** type.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](atf-build-overview.md)

