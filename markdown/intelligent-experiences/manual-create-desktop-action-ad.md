---
title: Automate repetitive tasks by manually capturing steps in AI Desktop Actions
description: Create desktop actions by manually capturing steps to automate repetitive tasks in AI Desktop Actions. The steps that you define on one or more application screens are saved as a reusable desktop action of type on-screen task.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 9
breadcrumb: [Design defined-path desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Automate repetitive tasks by manually capturing steps in AI Desktop Actions

Create desktop actions by manually capturing steps to automate repetitive tasks in AI Desktop Actions. The steps that you define on one or more application screens are saved as a reusable desktop action of type on-screen task.

## Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.
-   Remote Desktop must be enabled on your machine and your account must be granted Remote Desktop access permissions before you start using the AI Desktop Actions Execution workspace.

Familiarize yourself with the Design workspace and Action recorder. For more information, see [AI Desktop Actions Design workspace](../concept/agentic-desktop-overview.md) and [Action recorder in AI Desktop Actions](../concept/action-recorder-ad.md).

Role required: sn\_aia.admin

## About this task

You can simulate a user interaction in an automation by manually capturing screens and defining steps.

Using the controls in the window, you can capture an area of an application window. You can then set one or more anchors, and define steps that represent the user interactions in that window.

-   **Anchor**: Anchors help specify the target area for the interaction by defining a static area from which steps can be defined at a relative distance.
-   **Step**: Steps are your sequential interactions of type click, select, type, scroll, and more.

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

## Procedure

1.  From your Windows system, launch the AI Desktop Actions application.

2.  On the login page, in the **Add ServiceNow URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

    ![AI Desktop Actions login screen for entering ServiceNow instance URL.](../image/ad-login-screen.png)

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your user name and password.

    Your must have the sn\_aia.admin role.

    ![Login window for entering your ServiceNow account username and password.](../image/ad-login-screen-cred.png)

5.  On the onboarding journey wizard, complete the onboarding and select **Get started**.

    ![Onboarding journey widget with five pages to show you the highlights of the application.](../image/onboarding-widget-ad.png)

    If you launch the AI Desktop Actions for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch AI Desktop Actions or **Skip intro** to skip the onboarding.

6.  On the AI Desktop Actions home page, select **Create desktop action**.

    ![AI Desktop Actions home page displaying the Create desktop action UI action, search and select options, and cards of existing desktop actions.](../image/home-page-actions-ad.png)

7.  In the New desktop action dialog box, select **Manual capture steps**.

    ![New desktop action window with manual capture option selected and fields to enter name and description for the desktop action.](../image/create-desktop-action-manual-ad.png)

8.  Enter a name and description for the desktop action.

9.  Select **Start capturing**.

    The Design workspace is displayed.

    ![Design workspace in a state when no screenshot is captured.](../image/design-workspace-ad.png)

10. Capture screens.

    1.  In the Design tab, select the **Capture Options** icon ![](../image/capture-options-icon.png).

    2.  Select **Manual capture**.

        ![Design workspace displaying two options: Auto-capture with recorder and Manual capture screens.](../image/design-tab-manual-ad.png)

        The AI Desktop Actions window is minimized and the Capture panel is launched.

        ![Manual capture floating panel with Select and Cancel UI actions.](../image/manual-select-screen-ad.png)

    3.  Open the applications that you want to automate steps for.

    4.  Capture the area of the external application’s window by selecting the **Select** icon ![](../image/ad-select-icon.png) on the Capture panel or pressing the `Ctrl + Shift + C` on the keyboard.

        **Note:** If the `Ctrl + Shift + C` shortcut conflicts with another application on the your machine, such as Zoom, then you must use the **Select** button to initiate manual screen capture.

        For example, you can capture the area surrounding a button or a text field in a web browser. The cursor icon changes to the ![](../../../reuse/icons/product-icons/plus-outline-24.svg) icon.

    5.  Drag the ![](../../../reuse/icons/product-icons/plus-outline-24.svg) icon and select the required screen area.

        When you leave the ![](../../../reuse/icons/product-icons/plus-outline-24.svg) icon, the selected area is captured as a screenshot in the Design workspace.

        If you are not satisfied with the captured screen, you can recapture the screen area by selecting the **Capture image** icon ![](../image/ad-capture-image-icon.png).

11. Insert anchors.

    1.  Insert an anchor on the captured screen by selecting the **Add anchor** icon ![](../image/ad-add-anchor-icon.png).

        ![Screen capture of the Shipping Management app with anchor added on the Window title](../image/ex-ship-app-anchor-ad.png)

        An anchor is a reference point on the screen that helps the automation identify and interact with a nearby UI elements. During execution, the system uses computer vision to locate the anchor and then identifies the UI elements at a related distance from the anchor. Anchors improve the stability and accuracy of steps when the target element’s location may shift or when the UI layout varies across sessions.

        **Note:** Do not use dynamically changing UI elements as anchors. If an element changes its color, text, or state after an action \(for example, after a click\), select a different anchor that remains static on the screen.

    2.  Move the anchor to a part of the captured image that won’t change.

        For example, move the anchor to a title or field label.

        If the area under the anchor doesn’t exactly match the corresponding area of the captured image, the anchor isn't recognized, and the steps are not performed as intended. Choose a static area of the image for setting your anchor.

        You can add multiple anchors on each screen. Multiple anchors let you define the geographical relationship between anchor and target with greater accuracy when targeting different locations in the image.

12. Configure the steps.

    1.  From the Anchor control menu, select the **Add step** icon ![](../../../reuse/icons/product-icons/circle-plus-outline-24.svg).

    2.  Select the type of step to perform for this step from the contextual menu.

        ![Screen capture of an app with anchor added, displaying various type of input and output steps.](../image/add-action-context-menu-ad.png)

<table id="table_vtf_jds_ghc"><thead><tr><th>

Goal

</th><th>

Step

</th><th>

Type

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Enter text in a field

</td><td>

Set Text

</td><td>

Input

</td><td>

Enter any text data such as a user name, an address, a survey response, or in any situation where text entry is accepted.**Note:** If you set a static value for this field, the automation uses it during execution and doesn’t prompt you for input from the Now Assist panel.

</td></tr><tr><td>

Simulate a mouse click

</td><td>

Click

</td><td>

Input

</td><td>

Click a button, open a menu, or perform any step typically performed by a mouse click.

</td></tr><tr><td>

Simulate an alternative mouse action \(for example, right-click, drag, scroll, or paste\)

</td><td>

Mouse Click

</td><td>

Input

</td><td>

Perform various mouse device actions, such as right-click and select an object or scroll on a web page.

</td></tr><tr><td>

Simulate a key press or a key function

</td><td>

Send Keys

</td><td>

Input

</td><td>

Perform keyboard shortcuts, such as copying text by entering `Ctrl + C` on fields and elements.**Note:** If you set a static value for this field, the automation uses it during execution and doesn’t prompt you for input from the Now Assist panel.

</td></tr><tr><td>

Capture text from a window or web page

</td><td>

Get Text

</td><td>

Output

</td><td>

Receive text from the source area.

</td></tr><tr><td>

Capture a table

</td><td>

Get Table

</td><td>

Output

</td><td>

Receive table from the source area when the text is in the table format.**Note:** For the step to capture table data successfully, the data must already be in the table form. The step can’t convert ordinary text to table data.

</td></tr><tr><td>

Read text from an image

</td><td>

OCR Read Text

</td><td>

Output

</td><td>

Recognize text from images and return it in the standard text format.

</td></tr></tbody>
</table>        You can add multiple steps representing your automation steps.

13. Configure the properties for added screens, anchors, and steps in the Properties panel.

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](../reference/screen-anchor-and-action-properties-ad.md).

14. Modify the auto-generated names for all added screens, anchors, and steps.

    You can modify the auto-generated names following these naming guidelines.

    -   Name fields must not be empty.
    -   Name fields must contain only alphanumeric characters. Spaces and special characters are not permitted.
    -   Each name must be unique at its respective parent level.
        -   Each screen must have a unique name at the desktop-action level.
        -   Each anchor must have a unique name at the screen level.
        -   Each step must have a unique name at the anchor level.

## What to do next

1.  Configure the details of your desktop action. For more information, see [Add details to desktop actions in AI Desktop Actions](add-details-desktop-action-ad.md).
2.  Test and activate the desktop action so that it can be added as a tool to AI agents. For more information, see [Test and activate a desktop action in AI Desktop Actions](test-activate-desktop-action-ad.md).
3.  Add the desktop action as a tool to AI agents in AI Agent Studio. For more information, see [Add a desktop action to an AI agent](../../../administer/now-assist-ai-agents/task/add-desktop-action-ai-agent.md).

**Related topics**  


[AI Desktop Actions Design workspace](../concept/agentic-desktop-overview.md)

[Screen, anchor, and step properties in AI Desktop Actions](../reference/screen-anchor-and-action-properties-ad.md)

[Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](auto-create-desktop-action-ad.md)

[Add a desktop action to an AI agent](../../../administer/now-assist-ai-agents/task/add-desktop-action-ai-agent.md)

[Examples of creating desktop actions](../concept/examples-of-agentic-desktop-automation.md)

[Examples of executing desktop actions using AI agents](../concept/use-agentic-desktop.md)

