---
title: Agentic Desktop Design workspace
description: The Design workspace is an interactive environment within Agentic Desktop that enables you to create desktop actions by recording and configuring user interactions with desktop applications. The workspace provides a visual canvas where you can design multi-screen automation workflows that capture business processes across different applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-09"
reading_time_minutes: 5
breadcrumb: [Explore, Agentic Desktop, Enable AI experiences]
---

# Agentic Desktop Design workspace

The Design workspace is an interactive environment within Agentic Desktop that enables you to create desktop actions by recording and configuring user interactions with desktop applications. The workspace provides a visual canvas where you can design multi-screen automation workflows that capture business processes across different applications.

**Important:** Access to the Design workspace and Execution workspace depends on the user’s role.

-   When users with the AI Agent Admin \(sn\_aia.admin\) role sign in from their desktop, they can access the Home page and Design workspace to create desktop actions. When they test a desktop action, the Execution workspace launches automatically.
-   When users with the Now Assist panel user \(now\_assist\_panel\_user\) role trigger an automation from the Now Assist panel, the Execution workspace launches automatically to run the desktop action.

You don’t open the Execution workspace directly. It launches automatically when you test or run a desktop action.

## Agentic Desktop home page

The home page provides an intuitive interface to help you quickly create, track, and manage your desktop actions. You can easily find and manage your existing desktop actions and monitor their status.

![Agentic Desktop home page with Create desktop action UI action, search and filter options, and cards of existing desktop actions.](../image/home-page-actions-ad.png "Agentic Desktop home page")

When you log in to Agentic Desktop, the home page is the first screen you see. The home page lets you interact with various functionalities.

-   **Create desktop action**

    You can create desktop actions by manually capturing steps or auto-capture steps through recording.

-   **Search and manage actions**

    You can search for specific actions and manage them directly from the home page.

-   **My Actions and All Actions**

    **My Actions** tab shows only the actions published by the logged in user. **All Actions** tab shows list of all actions available on the instance the logged in user is connected to.

-   **Desktop action cards**

    Configured desktop actions with details, such as created date, user who created, applications added, and activation status.

-   **Edit desktop actions**

    You can modify a desktop action by selecting the **Edit** option for each card. Any changes you make are saved and reflected on the home page.

-   **Access to profile and documentation**

    A dedicated section enables you to view your profile information, access product documentation, and check the product version.


## Agentic Desktop Design tab

The Design workspace provides a no-code environment for creating, managing, and testing your desktop actions. You can either auto-capture or manually record a series of steps you perform on your computer, such as clicking buttons, entering text, selecting from drop-down, or interacting with different applications. You can then save this sequence as a reusable desktop action.

![Agentic Desktop Design tab that shows interface elements like Design, Details tabs, Screens and steps panel, and a captured currency converter screen with numbered annotations.](../image/design-tab-overview-ad.png "Design tab")

<table id="table_dqh_1bz_ghc"><thead><tr><th>

No.

</th><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1

</td><td>

**Design** tab

</td><td>

Enables you to design your desktop actions by adding screens, anchors, and steps.

</td></tr><tr><td>

2

</td><td>

**Details** tab

</td><td>

Enables you to add details to your desktop actions, such as name, description, and applications that this desktop action interacts with. You can also review the inputs and outputs of this desktop action.

</td></tr><tr><td>

3

</td><td>

**Screens and Steps** panel

</td><td>

Shows all the captured screens and added anchors and steps in a sequence the desktop action must perform them. You can drag and move these items to change the order. You can also run a screen-level test by selecting the Run screen test icon ![](../image/icon-video-play-ad.png).

</td></tr><tr><td>

4

</td><td>

**Properties** panel

</td><td>

Enables you to configure the properties for screens, anchors, and steps.

</td></tr><tr><td>

5

</td><td>

**Capture options**

</td><td>

Provides two options for capturing interactions with applications that you want to automate.-   **Auto-capture steps**: Automatically records the steps that you perform for the task that you want to automate.
-   **Manual capture screens**: Enables you to capture the screens manually, insert anchors, and add steps that you want to automate.

</td></tr><tr><td>

6

</td><td>

Captured screen

</td><td>

The application screen that you captured.You can delete any screen by selecting the **Delete** icon ![](../image/ad-delete-icon.png) from the Screens and steps panel.

</td></tr><tr><td>

7

</td><td>

**Anchor**

</td><td>

An anchor is a reference point on the screen that helps the automation identify and interact with a nearby UI elements. During execution, the system uses computer vision to locate the anchor and then identifies the UI elements at a related distance from the anchor. Anchors improve the stability and accuracy of steps when the target element’s location may shift or when the UI layout varies across sessions.You can delete any anchor by selecting the **Delete** icon ![](../image/ad-delete-icon.png).

</td></tr><tr><td>

8

</td><td>

**Step**

</td><td>

A step in your automation. The following types of steps are supported:**Inputs**

-   Set Text
-   Click
-   Mouse Click
-   Send Keys

**Outputs**

-   Get Text
-   Get Table
-   OCR Read Text

You can add a step by selecting the **Add step** icon ![](../../../reuse/icons/product-icons/circle-plus-outline-24.svg) from the Step control menu. You can delete any step by selecting the **Delete** icon ![](../image/ad-delete-icon.png).

</td></tr><tr><td>

9

</td><td>

**Test**

</td><td>

Enables you to test the desktop action in Execution workspace before you activate it. You can also test individual screens to quickly identify and troubleshoot issues. Run the test by entering the required inputs manually.

</td></tr><tr><td>

10

</td><td>

**Save**

</td><td>

Enables you to save the desktop action after you have configured the required fields.

</td></tr><tr><td>

11

</td><td>

**Activate**

</td><td>

Option to activate the desktop action so that it can be published to AI Agent Studio. You can add the activated desktop action as a tool to AI agents.**Note:** After activation, save the desktop action to make it available as a tool in AI Agent Studio.

</td></tr><tr><td>

12

</td><td>

Screen capture options

</td><td>

-   Re-capture screen - Re-capture new screen to replace the existing screen.
-   Add anchor - Add anchor on the captured screen.
-   Delete screen - Delete the captured screen. All the associated anchor and steps are deleted.

</td></tr></tbody>
</table>**Related topics**  


[Desktop actions in Agentic Desktop](desktop-actions-designer-workspace-ad.md)

[Automate repetitive tasks by auto-capturing steps in Agentic Desktop](../task/auto-create-desktop-action-ad.md)

[Automate repetitive tasks by manually capturing steps in Agentic Desktop](../task/manual-create-desktop-action-ad.md)

[Example: Automate badge request management using Agentic Desktop](example-badging-magmt-concept-ad.md#)

[Example: Automate shipping management tasks using Agentic Desktop](example-shipping-magmt-concept-ad.md#)

[Screen, anchor, and step properties in Agentic Desktop](../reference/screen-anchor-and-action-properties-ad.md)

