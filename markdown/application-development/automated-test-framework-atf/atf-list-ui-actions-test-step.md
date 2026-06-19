---
title: List UI actions test steps
description: Select a UI action from a list to perform different actions on a list or a related list.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/atf-list-ui-actions-test-step.html
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

You can create a new UI action of the following types. See Create a UI action for more information.

-   **List banner button**: Creates a button on the banner of a list.

    \[Omitted image "atf-list-banner-button.png"\] Alt text: Image showing the list banner button

-   **List bottom button**: Creates a button at the bottom of the list.

    \[Omitted image "atf-bottom-button.png"\] Alt text: Image showing list bottom button

-   **List context menu**: Adds an option to the context menu of the list.

    \[Omitted image "atf-list-context-menu.png"\] Alt text: Image showing the UI action in the context menu

-   **List choice**: Adds an option to the list choice at the bottom of the list. You need to select one or more tests to enable the recently added list choice.

    \[Omitted image "atf-list-choice.png"\] Alt text: Image showing the added option in the list

-   **List link**: Adds a link to the **Related Links** list.

    \[Omitted image "atf-list-link.png"\] Alt text: Image showing the links added to the Related Links list


## Design considerations

-   To use the **Click a List UI Action** test step, the test first needs to navigate to the list or the form with the related list containing the UI action.
-   The **Related list** field appears only when you select Related list as the **List type**.
-   **Action type** is mostly auto-filtered depending on the **List action** chosen.
-   The **Record** field appears only when you select **Single record** for the UI action to be applied.
-   Identify the specific record if you have selected **Single record** to apply the UI action.
-   For the **Timeout** field to appear, select **Page reloaded or redirected** as the **Assert** type.

**Parent Topic:**[Building and running automated tests with the Automated Test Framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/atf-build-overview.md)

