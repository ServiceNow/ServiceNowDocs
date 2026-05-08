---
title: Plan Guided Tours
description: Planning is essential before entering a guided tour into the system. Create an outline and include any assumptions to assist you during the tour creation.
locale: en-US
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Plan Guided Tours

Planning is essential before entering a guided tour into the system. Create an outline and include any assumptions to assist you during the tour creation.

## Planning a guided tour

Before outlining a guided tour, consider these factors:

-   **Purpose of the tour**

    Decide whether to create a tour that describes a user interface or one that helps users complete a task. Conduct research and break down the main goal into clear, manageable steps.

-   **Accessibility of the tour**

    Enable the tour on your production system to help users perform routine tasks like ordering from the Service Catalog or creating incidents. If your aim is to train users to explore these tasks without creating real records, provide the tour on your non-production system.

-   **Name of the tour**

    Choose a unique, intuitive tour name that clearly indicates its purpose, like “Create a New Incident” or “Review the Incident List”.

    Customize the instructions so that each user creates a unique record. For instance, if the tour instructs users on how to create a group called "Facilities," you can avoid duplicate name errors for subsequent users by prompting them in a callout to assign a unique value to the group name field.

-   **User's knowledge about the task**

    Not all users who take the tour have the same knowledge level. Evaluate the information needed to make sure that participants comprehend the content from the start.


When planning your tour, consider addressing the following additional questions:

-   What page should the tour start on?
-   What steps are important to accomplish the objective?
-   How should a user navigate from one step to the next?

## Selecting triggers

Triggers are actions that you take to move the tour to the next step. Each callout in a guided tour step has a specific trigger that activates the subsequent step. You define the trigger for each callout, and only relevant triggers appear based on the UI element referenced by the callout.

For more information, see [GTD triggers](../reference/guided-tour-triggers.md).

## Using callouts

You must place a callout on top of an element to interact with it. The element is highlighted in blue when it’s selected as the target.

In the following example, it looks like the callout is pointing to the context menu icon, but notice that the header bar is highlighted blue.

![Wrong placement of the callout](../image/guided-tour-wrong-placement.png "Incorrect callout placement for the context menu")

This example depicts the correct placement of the callout for the context menu. Notice that the context menu icon is highlighted blue.

![Correct placement of the callout](../image/guided-tour-right-placement.png "Correct callout placement for the context menu")

The following tips may also be helpful:

-   When you place a callout on a form that contains tabs, consider that a user may not have the tab open for viewing. Create a new callout that instructs the user to first open the tab before proceeding with the rest of the tour.
-   When adding callouts to fields with dynamic content, keep them minimal. If users can’t locate the associated tour element due to a delayed page refresh, the tour may end unexpectedly.
-   When you guide a user through pop-up windows, add your callout to the originating page on or near the pop-up icon. Within the callout instructions, guide your user through the steps intended for the pop-up window, because callouts can’t be added to the pop-up window.
-   While the color of a callout is static in the Standard platform UI, you can customize callouts on Service Portal. Consider using this capability to make sure that a consistent look-and-feel between your callouts and your Service Portal pages.

## Auto-launching your tour

Automatically start a tour if you want users to take the tour on their first visit to the page.

You can choose to launch multiple tours automatically from a single starting page. You can set the auto-launch order so that users start the second tour on their second page visit, the third tour on their third page visit, and so on. Use this option if you want to begin with an introductory tour and then add more complex or focused follow-up tours.

**Parent Topic:**[Configuring Guided Tours](../task/configure-guided-tours.md)

