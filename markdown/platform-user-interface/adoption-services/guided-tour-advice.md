---
title: Designing guided tours
description: Use these tips to help you create effective guided tours for your users.
locale: en-US
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Using Guided Tours, Guided tours, Adoption services, Configure user experiences]
---

# Designing guided tours

Use these tips to help you create effective guided tours for your users.

## Planning a guided tour

Before you begin outlining the details of a guided tour, answer the following questions.

-   What is the purpose of the tour? Do you want to use callouts that provide detailed user interface descriptions so your users can better understand the feature? Or do you want the user to learn how to perform a task, such as how to create a new incident? It is important that you consider these questions and perhaps do some research before you begin to plan the tour so that you can properly break down the overall objective into discrete steps.
-   Where should the tour be available? If you intend to guide your users to complete tasks that they might perform daily, such as ordering an item from the Service Catalog or creating an incident, it makes sense to make the tour available on your production instance. If you intend to train users to explore these tasks without creating actual records in the system, consider making the tour available on a non-production instance for training purposes instead. Both scenarios are valid.
-   What should you name your tour? When you create a tour, you are prompted to provide a tour name. The name must be unique and intuitive so your users can understand the purpose of the tour. For example, use “Create a New Incident” or “Review the Incident List” as possible tour names.
-   What assumptions are you making regarding what the user already knows about the page or task? Do all users who can take the tour have the same level of understanding? Use this information to decide how much description to provide at the beginning of the tour so that any user who takes the tour understands the content.
-   If the purpose of the tour is to perform a task, how can you personalize the instructions so that each user who takes the tour creates a different record? For example, if the tour walks users through creating a group called Facilities, you can prevent subsequent users from getting a duplicate name error by instructing them in a callout to assign a unique value to the group Name field.

In planning your tour, you can also address these additional questions.

-   What page should the tour start on?
-   What steps are important to accomplishing the objective?
-   How should a user navigate from one step to the next?

## Guided tour plan

Review the following sample plan for a guided tour whose objective is to explore the Service Portal home page.

Note this key information you will need to provide and the fields values you will use as you create a guided tour.

-   Tour Name: Service Portal Overview
-   Goal: Users should have a good understanding of how to navigate key elements of the Service Portal home page
-   Portal Name: Service Portal
-   Starting Page: Service Portal: ID Index
-   Roles: All

<table id="table_rz5_2fv_zdb"><thead><tr><th>

Step

</th><th>

Callout

</th><th>

Trigger

</th></tr></thead><tbody><tr><td>

Introduction

</td><td>

-   Title: Service Portal Overview
-   Text: Welcome to this guided tour of your new Service Portal home page.

</td><td>

**Next** button

</td></tr><tr><td>

1

</td><td>

-   Points to this element: How can we help?
-   Placement: Below
-   Text: We begin with the **How can we help?** search bar. If you cannot find what you are looking for, enter it here, click the **Search** icon, or press Enter on your keyboard. For now we will take a look at some other areas first.

</td><td>

**Next** button

</td></tr><tr><td>

2

</td><td>

-   Points to this element: Order Something
-   Placement: Top
-   Text: If you would like to order something, such as a new phone, select **Order Something**.

</td><td>

**Next** button

</td></tr><tr><td>

3

</td><td>

-   Points to this element: Knowledge Base
-   Placement: Top
-   Text: If you would like to search the knowledge base, select **Knowledge Base**.

</td><td>

**Next** button

</td></tr><tr><td>

4

</td><td>

-   Points to this element: Get Help
-   Placement: Top
-   Text: If you would like to get help for an issue, select **Get Help**.

</td><td>

**Next** button

</td></tr><tr><td>

5

</td><td>

-   Points to this element: Community
-   Placement: Top
-   Text: If you would like to ask your colleagues a question, select **Community**.

</td><td>

**Next** button

</td></tr><tr><td>

6

</td><td>

-   Points to this element: Knowledge in title bar
-   Placement: Left
-   Text: You can also check the knowledge base, order something, look at requests you have logged, and check other options up here in the title bar.

</td><td>

**Next** button

</td></tr><tr><td>

7

</td><td>

-   Points to this element: Your name
-   Placement: Left
-   Text: View your profile or log out by clicking your name.

</td><td>

**Next** button

</td></tr><tr><td>

8

</td><td>

-   Points to this element: Logo top-left
-   Placement: Below
-   Text: Navigate back to your Service Portal home page by clicking your company logo.

</td><td>

**Next** button

</td></tr><tr><td>

Conclusion

</td><td>

Text: Congratulations! Now you have a general understanding of the Service Portal home page.

</td><td>

Click **Complete** to end the tour.

</td></tr></tbody>
</table>## Selecting triggers

If the purpose of the tour is to introduce your users to the features of a page so that they can become familiar with the product, such as a custom dashboard, use the **Next** button as the trigger. If the purpose is to accomplish a task, such as creating a record, consider the following.

-   To populate a field with a lookup element, such as a reference field or a date field, do not use a trigger that opens the lookup window. The tour ends when the lookup window opens. Use one of the following triggers:
    -   **Next** button: The user types the value or looks it up and selects it, and then clicks **Next**.
    -   **Change Element Value** trigger: After the user selects the value and clicks outside the field, the trigger moves to the next step.
-   For some UI elements, you can use the **Right click the Element** trigger. Typically, the right-click action is used to open a menu, however, you cannot place a callout on a right-click menu option. You can use this trigger in a descriptive guided tour where you want to describe right-click menu options. Put the descriptive information into the callout text, and tell your users to right-click the element to look at the menu. Following is an example of this type of callout.

    ![Example callout instructing the user to right-click to see field options](../image/guided-tour-callout-rightclick-london.png)

    When the user right-clicks the element, in this case a field label, this instruction disappears, and the next one appears.

-   The **Mouse over the Element** trigger is similar to the **Right click the Element** trigger. When the user points to the element, the callout disappears. For example, if you demonstrate that a hint appears when you point to a field label, the callout step disappears before the hint text appears. This type of trigger can seem disruptive to the guided tour flow.

## Using callouts

You must place a callout on top of an element to interact with it. The element is highlighted in blue when it is selected as the target. In the following example, it looks like the callout is pointing to the context menu icon, but notice that the header bar is highlighted blue.

![Wrong placement of the callout](../image/guided-tour-wrong-placement.png "Incorrect callout placement for the context menu")

This example depicts the correct placement of the callout for the context menu. Notice that the context menu icon is highlighted blue.

![Correct placement of the callout](../image/guided-tour-right-placement.png "Correct callout placement for the context menu")

The following tips may also be helpful:

-   When you place a callout on a form that contains tabs, consider that a user may not have the tab open for viewing. Create a new callout that instructs the user to first open the tab before proceeding with the rest of the tour.
-   Minimize callouts on fields that are associated with dynamic content. A delayed page refresh may prematurely end the tour if the user cannot find the associated tour element.
-   When you guide a user through pop-up windows, add your callout to the originating page on or near the pop-up icon. Within the callout instructions, guide your user through the steps intended for the pop-up window, because callouts cannot be added to the pop-up window.
-   While the color of a callout is static in the standard platform UI, you can customize callouts on Service Portal. Consider using this capability to ensure a consistent look-and-feel between your callouts and your Service Portal pages. For more information on guided tours that you create on Service Portal pages, see [Request guided tours](../task/activate-guidedtours-service-portal.md).

## Auto-launching your tour

Auto-launch a tour if you want your users to take the tour on their first page visit.

You may choose to auto-launch multiple tours from a single starting page. In this case, you can apply the auto-launch order to each tour successively so that your users begin the second tour upon their second page visit, their third tour upon their third page visit, and so forth. Use this option if you intend to start your users with an introductory tour and add increasing levels of complexity or different areas of focus with follow-up tours.

