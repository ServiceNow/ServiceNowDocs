---
title: Automate repetitive tasks by recording steps with AI in AI Desktop Actions
description: Create desktop actions by recording steps with AI to automate repetitive tasks in AI Desktop Actions. AI validates anchor positions and generates screen contexts automatically after recording, reducing the risk of automation failures at runtime.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/record-with-ai-ad.html
release: australia
topic_type: task
last_updated: "2026-05-22"
reading_time_minutes: 11
breadcrumb: [Design defined-path desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Automate repetitive tasks by recording steps with AI in AI Desktop Actions

Create desktop actions by recording steps with AI to automate repetitive tasks in AI Desktop Actions. AI validates anchor positions and generates screen contexts automatically after recording, reducing the risk of automation failures at runtime.

## Before you begin

Familiarize yourself with the Design workspace and Action recorder. For more information, see [AI Desktop Actions Design workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-overview.md) and [Action recorder in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/action-recorder-ad.md).

To access the AI Desktop Actions functionality, perform the following steps:

-   Enable AI Desktop Actions on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-agentic-desktop.md).
-   Download the AI Desktop Actions installer to automate repetitive tasks across applications and systems. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

Confirm that the following system requirements are met:

-   Windows 11 operating system is used.
-   A .NET 9.0 runtime v9.0.10 and .NET 9 Desktop Runtime v9.0.10 is installed.
-   No extended monitors are connected.
-   Theme must match between the systems used for recording and execution.
-   The ServiceNow AI Lens skill must be active on your instance. Contact your ServiceNow administrator if you're unsure whether this condition is met.

Role required: sn\_desktop\_core.desktop\_action\_user

## About this task

Record with AI generates more accurate anchor positions automatically, reducing the time you spend on manual anchor adjustments.

When you record with AI, after you finish recording, AI analyzes the recording, validates anchor positions, and corrects inaccuracies before you save or activate the desktop action. AI also generates a screen context for each captured screen and description for the desktop action. Screen context is a description of what the screen does and what it contains, which helps reviewers and AI agents understand the screen's intent.

**Note:** If your automation requires manual inputs, such as entering an OTP or CAPTCHA, you must provide instructions to the AI Agent to wait for the user input during execution. Otherwise, the automation can't proceed.

The **sn\_desktop\_core.record\_with\_ai** property is enabled by default, making **Record with AI** the default recording option. Turn off this property to set the manual recorder as the default recording option.

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

6.  On the AI Desktop Actions home page, select **Create desktop action**.

    \[Omitted image "home-page-actions-ad.png"\] Alt text: AI Desktop Actions home page displaying the Create desktop action UI action, search and select options, and cards of existing desktop actions.

7.  In the Create Desktop Action dialog, keep the **Record with AI \(recommended\)** check box selected.

    \[Omitted image "create-desktop-action-with-ai.png"\] Alt text: Create desktop action modal with Record with AI option selected and a field to enter name for the desktop action.

    **Important:** If the **Record with AI \(recommended\)** check box is unavailable, the ServiceNow AI Lens is inactive on your instance. Contact your ServiceNow administrator to enable it. You can still create desktop actions using [auto-capture](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/auto-create-desktop-action-ad.md) mode.

    \[Omitted image "ad-lens-skill-disabled.png"\] Alt text: Create desktop action modal with Record with AI option inactive and a fields to enter name and description for the desktop action.

8.  Enter a name for the desktop action.

9.  Select **Continue**.

10. In the modal, review the tips and select **Open recorder** to begin.

    \[Omitted image "open-recorder-ad.png"\] Alt text: Guided slow model for providing tips for effective recording.

    The AI Desktop Actions window is minimized and the Action recorder panel is launched. You can freely drag and reposition the Action recorder panel anywhere on your desktop screen.

    \[Omitted image "recorder-auto-capture-ad.png"\] Alt text: Floating recorder panel that has Discard, Pause, and Start recording UI actions.

11. Open the applications that you want to record steps for.

12. From the Action recorder panel, select **Start recording**.

    **Important:** Before you start recording, review the tips for accurate capturing of anchors and steps. For more information, see [Tips for accurate recording](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/action-recorder-ad.md).

    You will see a "Recording started" message on the Action recorder panel. You can select any of the following options when needed from the **More options** menu:

    -   **Pause**: Skip recording steps
    -   **Restart**: Restart recording the steps

        You will lose the recorded screens and steps.

    -   **Discard**: Discard the recording if it doesn't meet your needs
13. Perform the steps that you want to automate.

    Each step that you perform is captured sequentially and the type of UI action is displayed for each step. For example, Capturing Mouse Left Click event.

    You can capture maximum of 50 steps using the recorder in a recording session. While auto-capturing steps, a counter displays the remaining number of steps you can capture using the recorder \(for example, "35 of 50 max"\). Recording stops automatically after you capture 50 steps. If you must capture additional steps, start a new recording session. The new recording adds screens and steps to those captured in the previous recording.

14. After you're done with all the steps, select **End recording** on the Action recorder panel.

    You will see the "Draft workflow saved" message on the Action recorder panel.

    AI processes the recording in three stages:

    1.  Analyzing your recording with AI
    2.  Inserting anchors
    3.  Generating screen contexts
    You must not close the application during processing.

    The recorded steps are displayed as screenshots in the Design workspace with anchors and steps automatically added.

15. When the `AI analysis complete` banner appears, review the AI-generated anchors and screen contexts.

    **Note:** If two applications in the frame have similar logos or visual elements, verify that the anchor position is unique to the target application to avoid incorrect element identification during automation.

    Anchors and screen context generated by AI are marked with an AI badge in the properties panel. For each screen, review the screen context and edit it if needed.

    \[Omitted image "ad-screen-ai-tag.png"\] Alt text: AI badge, retry option, and screen context for screens in the properties panel.

    \[Omitted image "ad-anchor-ai-tag.png"\] Alt text: AI badge for anchors in the properties panel.

    **Note:** The accuracy of AI-generated anchors depends on the application's accessibility, performance, and UI complexity. Always review before activating.

16. To regenerate the screen context and anchor position for a specific screen, select **Retry** \[Omitted image "icon-retry.png"\] Alt text: in the screen properties panel.

17. Review the sequence of captured screens and adjust if necessary.

    You can adjust the sequence by dragging the screens in the Screens and steps panel.

18. Review and adjust steps.

    You can modify the sequence by adding, removing, or dragging steps.

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

19. Configure the properties for added screens, anchors, and steps in the Properties panel.

    For more information, see [Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/screen-anchor-and-action-properties-ad.md).

20. Modify the auto-generated names for all added screens, anchors, and steps.

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

[Action recorder in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/action-recorder-ad.md)

[Screen, anchor, and step properties in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/screen-anchor-and-action-properties-ad.md)

[Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/auto-create-desktop-action-ad.md)

[Extend a desktop action by manually capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/manual-create-desktop-action-ad.md)

[Add a defined desktop action tool to an AI agent for desktop and web-based task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/add-desktop-action-ai-agent.md)

[Examples of creating desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/examples-of-agentic-desktop-automation.md)

[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)

