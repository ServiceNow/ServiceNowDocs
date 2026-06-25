---
title: Extend a desktop action by manually capturing steps in AI Desktop Actions
description: Extend the automation logic in a desktop action by manually capturing steps in AI Desktop Actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/manual-create-desktop-action-ad.html
release: australia
topic_type: task
last_updated: "2026-05-27"
reading_time_minutes: 10
breadcrumb: [Design defined-path desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Extend a desktop action by manually capturing steps in AI Desktop Actions

Extend the automation logic in a desktop action by manually capturing steps in AI Desktop Actions.

## Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.
-   Remote Desktop must be enabled on your machine and your account must be granted Remote Desktop access permissions before you start using the AI Desktop Actions Execution workspace.

Familiarize yourself with the Design workspace and Action recorder. For more information, see [AI Desktop Actions Design workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-overview.md) and [Action recorder in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/action-recorder-ad.md).

Role required: sn\_aia.admin

## About this task

**Note:** To create desktop actions with AI-assisted anchor validation and automatic screen context generation, use [Record with AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/record-with-ai-ad.md) instead.

You can simulate a user interaction in an automation by manually capturing screens and defining steps.

Using the controls in the window, you can capture an area of an application window. You can then set one or more anchors, and define steps that represent the user interactions in that window.

-   **Anchor**: Anchors help specify the target area for the interaction by defining a static area from which steps can be defined at a relative distance.
-   **Step**: Steps are your sequential interactions of type click, select, type, scroll, and more.

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

## Procedure

1.  From your Windows system, launch the AI Desktop Actions application.

2.  On the login page, in the **Add ServiceNow URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

    \[Omitted image "ad-login-screen.png"\] Alt text: AI Desktop Actions login screen for entering ServiceNow instance URL.

3.  Select **Proceed**.

4.  Log in to your ServiceNow account by entering your user name and password.

    Your must have the sn\_aia.admin role.

    \[Omitted image "ad-login-screen-cred.png"\] Alt text: Login window for entering your ServiceNow account username and password.

5.  On the onboarding journey modal, complete the onboarding and select **Get started**.

    \[Omitted image "onboarding-widget-ad.png"\] Alt text: Onboarding journey widget with five pages to show you the highlights of the application.

    If you launch the AI Desktop Actions for the first time, the onboarding journey widget appears. You can select **Don't show me again** to hide the widget the next time you launch AI Desktop Actions or **Skip intro** to skip the onboarding.

6.  On the AI Desktop Actions home page, select an existing desktop action.

    \[Omitted image "home-page-actions-ad.png"\] Alt text: AI Desktop Actions home page displaying the Create desktop action UI action, search and select options, and cards of existing desktop actions.

    The Design workspace is displayed.

    \[Omitted image "design-workspace-ad.png"\] Alt text: Design workspace in a state when no screenshot is captured.

7.  Capture screens.

    1.  In the Design tab, select the **Capture Options** icon \[Omitted image "capture-options-icon.png"\] Alt text:.

    2.  Select **Manual capture**.

        \[Omitted image "design-tab-manual-ad.png"\] Alt text: Design workspace displaying two options: Auto-capture with recorder and Manual capture screens.

        You can also extend the desktop action logic using the **Record with AI \(Recommended\)** or **Auto capture with recorder** options. For more information, see [Automate repetitive tasks by recording steps with AI in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/record-with-ai-ad.md) and [Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/auto-create-desktop-action-ad.md).

        The AI Desktop Actions window is minimized and the Capture panel is launched.

        \[Omitted image "manual-select-screen-ad.png"\] Alt text: Manual capture floating panel with Select and Cancel UI actions.

    3.  Open the applications that you want to automate steps for.

    4.  Capture the area of the external application’s window by selecting the **Select** icon \[Omitted image "ad-select-icon.png"\] Alt text: on the Capture panel or pressing the `Ctrl + Shift + C` on the keyboard.

        **Note:** If the `Ctrl + Shift + C` shortcut conflicts with another application on the your machine, such as Zoom, then you must use the **Select** button to initiate manual screen capture.

        For example, you can capture the area surrounding a button or a text field in a web browser. The cursor icon changes to the \[Omitted image "plus-outline-24.svg"\] Alt text: icon.

    5.  Drag the \[Omitted image "plus-outline-24.svg"\] Alt text: icon and select the required screen area.

        When you leave the \[Omitted image "plus-outline-24.svg"\] Alt text: icon, the selected area is captured as a screenshot in the Design workspace.

        If you aren't satisfied with the captured screen, you can recapture the screen area by selecting the **Capture image** icon \[Omitted image "ad-capture-image-icon.png"\] Alt text:.

8.  Insert anchors.

    1.  Insert an anchor on the captured screen by selecting the **Add anchor** icon \[Omitted image "ad-add-anchor-icon.png"\] Alt text:.

        \[Omitted image "ex-ship-app-anchor-ad.png"\] Alt text: Screen capture of the Shipping Management app with anchor added on the Window title

        **Note:** If two applications in the frame have similar logos or visual elements, verify that the anchor position is unique to the target application to avoid incorrect element identification during automation.

        An anchor is a reference point on the screen that helps the automation identify and interact with a nearby UI elements. During execution, the system uses computer vision to locate the anchor and then identifies the UI elements at a related distance from the anchor. Anchors improve the stability and accuracy of steps when the target element’s location may shift or when the UI layout varies across sessions.

        **Note:** Don't use dynamically changing UI elements as anchors. If an element changes its color, text, or state after an action \(for example, after a click\), select a different anchor that remains static on the screen.

    2.  Move the anchor to a part of the captured image that won’t change.

        For example, move the anchor to a title or field label.

        If the area under the anchor doesn’t exactly match the corresponding area of the captured image, the anchor isn't recognized, and the steps aren't performed as intended. Choose a static area of the image for setting your anchor.

        You can add multiple anchors on each screen. Multiple anchors let you define the geographical relationship between anchor and target with greater accuracy when targeting different locations in the image.

9.  Configure the steps.

    1.  From the Anchor control menu, select the **Add step** icon \[Omitted image "circle-plus-outline-24.svg"\].

    2.  Select the type of step to perform for this step from the contextual menu.

        \[Omitted image "add-action-context-menu-ad.png"\] Alt text: Screen capture of an app with anchor added, displaying various type of input and output steps.

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

10. Configure the properties for added screens, anchors, and steps in the Properties panel.

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/screen-anchor-and-action-properties-ad.md).

11. Modify the auto-generated names for all added screens, anchors, and steps.

    You can modify the auto-generated names following these naming guidelines.

    -   Name fields must not be empty.
    -   Name fields must contain only alphanumeric characters. Spaces and special characters are not permitted.
    -   Each name must be unique at its respective parent level.
        -   Each screen must have a unique name at the desktop-action level.
        -   Each anchor must have a unique name at the screen level.
        -   Each step must have a unique name at the anchor level.

## What to do next

1.  Configure the details of your desktop action. For more information, see [Add details to desktop actions in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-details-desktop-action-ad.md).
2.  Test and activate the desktop action so that it can be added as a tool to AI agents. For more information, see [Test and activate a desktop action in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-activate-desktop-action-ad.md).
3.  Add the desktop action as a tool to AI agents in AI Agent Studio. For more information, see [Add a defined desktop action tool to an AI agent for desktop and web-based task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-desktop-action-ai-agent.md).

**Related topics**  


[AI Desktop Actions Design workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-overview.md)

[Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/screen-anchor-and-action-properties-ad.md)

[Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/auto-create-desktop-action-ad.md)

[Add a defined desktop action tool to an AI agent for desktop and web-based task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-desktop-action-ai-agent.md)

[Examples of creating desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/examples-of-agentic-desktop-automation.md)

[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)

