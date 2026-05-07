---
title: Automate repetitive tasks by auto-capturing steps in AI Desktop Actions
description: Create desktop actions by auto-capturing steps to automate repetitive tasks in AI Desktop Actions. You can save the steps that you perform on the application elements as a reusable desktop action of type on-screen task.
locale: en-US
release: australia
topic_type: task
last_updated: "2025-11-10"
reading_time_minutes: 9
breadcrumb: [Design defined-path desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Automate repetitive tasks by auto-capturing steps in AI Desktop Actions

Create desktop actions by auto-capturing steps to automate repetitive tasks in AI Desktop Actions. You can save the steps that you perform on the application elements as a reusable desktop action of type on-screen task.

## Before you begin

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.

Familiarize yourself with the Design workspace and Action recorder. For more information, see [AI Desktop Actions Design workspace](../concept/agentic-desktop-overview.md) and [Action recorder in AI Desktop Actions](../concept/action-recorder-ad.md).

Role required: sn\_aia.admin

## About this task

You can record steps that you want to automate for desktop and web applications and save them as desktop actions of type on-screen task that AI agents can simulate while executing automations.

With Action recorder, you can record every step you perform on desktop applications, including clicks, keystrokes, and data entry, along with visual and contextual information. This detailed recording of steps allows automated tasks to reliably replicate your interactions.

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

7.  In the New desktop action dialog box, select **Auto-capture steps \(recommended\)**.

    ![New desktop action window with auto-capture option selected and fields to enter name and description for the desktop action.](../image/new-desktop-action-window-ad.png)

8.  Enter a name and description for the desktop action.

9.  Select **Start capturing**.

    The AI Desktop Actions window is minimized and the Action recorder panel is launched. You can freely drag and reposition the Action recorder panel anywhere on your desktop screen.

    ![Floating recorder panel that has Discard, Pause, and Start recording UI actions.](../image/recorder-auto-capture-ad.png)

10. Open the applications that you want to record steps for.

11. From the Action recorder panel, select **Start recording**.

    You’ll see a "Recording started" message on the Action recorder panel. You can select any of the following options when needed from the **More options** menu:

    -   **Pause**: Skip recording steps
    -   **Restart**: Restart recording the steps

        You will lose the recorded screens and steps.

    -   **Discard**: Discard the recording if it doesn’t meet your needs
    **Important:**

    Avoid performing steps too quickly while recording because the recorder may miss capturing steps.

    -   When the message in the Action recorder panel appears in red, wait for the recorder to finish processing the current step before continuing.

        ![Message in yellow indicating panel is still capturing step.](../image/recorder-auto-capture-red-ad.png)

    -   Proceed with capturing the next step when the red highlight box appears around the element you interact with and the message in the Action recorder panel changes to blue.

        ![Message in blue indicating panel finished capturing step.](../image/recorder-auto-capture-blue-ad.png)

12. Perform the steps that you want to automate.

    Each step that you perform is captured sequentially and the type of UI action is displayed for each step. For example, Capturing Mouse Left Click event.

13. After you’re done with all the steps, select **End recording** on the Action recorder panel.

    You can capture maximum of 50 steps using the recorder in a recording session. While auto-capturing steps, a counter displays the remaining number of steps you can capture using the recorder \(for example, “35 of 50 max”\). Recording stops automatically after you capture 50 steps. If you need to capture additional steps, start a new recording session. The new recording adds screens and steps to those captured in the previous recording.

    You’ll see the "Drafting recorded action\(s\)" message on the Action recorder panel.

    The recorded steps are displayed as screenshots in the Design workspace with anchors and steps automatically added.

14. Review the sequence of captured screens.

    You can adjust the sequence by dragging the screens in the Screens and steps panel.

15. Review the location of anchors and adjust as necessary.

    **Note:** The auto-anchoring accuracy depends on the application's accessibility, performance, and UI complexity.

16. Review and adjust steps.

    You can modify the sequence by adding, removing, or dragging steps.

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

17. Configure the properties for added screens, anchors, and steps in the Properties panel.

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](../reference/screen-anchor-and-action-properties-ad.md).

18. Modify the auto-generated names for all added screens, anchors, and steps.

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

[Action recorder in AI Desktop Actions](../concept/action-recorder-ad.md)

[Screen, anchor, and step properties in AI Desktop Actions](../reference/screen-anchor-and-action-properties-ad.md)

[Automate repetitive tasks by manually capturing steps in AI Desktop Actions](manual-create-desktop-action-ad.md)

[Add a desktop action to an AI agent](../../../administer/now-assist-ai-agents/task/add-desktop-action-ai-agent.md)

[Examples of creating desktop actions](../concept/examples-of-agentic-desktop-automation.md)

[Examples of executing desktop actions using AI agents](../concept/use-agentic-desktop.md)

