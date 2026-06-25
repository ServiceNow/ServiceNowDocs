---
title: Action recorder in AI Desktop Actions
description: With Action recorder, you can capture steps to automate repetitive tasks in AI Desktop Actions. You can save the steps that you perform on application elements as a reusable desktop action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/action-recorder-ad.html
release: australia
topic_type: concept
last_updated: "2026-02-11"
reading_time_minutes: 5
breadcrumb: [Defined desktop actions for desktop, Explore, AI Desktop Actions, Enable AI experiences]
---

# Action recorder in AI Desktop Actions

With Action recorder, you can capture steps to automate repetitive tasks in AI Desktop Actions. You can save the steps that you perform on application elements as a reusable desktop action.

Action recorder helps you record your interactions with desktop applications to create automated workflows. By recording steps, you can automate tasks that replicate your interactions. The recorded actions are displayed as screenshots in the Design workspace with anchors and steps automatically added.

The recorder captures the following items:

-   Visual snapshots of your screen at key interaction points.
-   Steps in the form of the buttons, fields, and other interface components you interact with.

## Record with AI

Record with AI is the recommended way to create desktop actions. Record with AI generates more accurate anchor positions automatically, reducing the time you spend on manual anchor adjustments.

When you record with AI, after you finish recording, AI analyzes the recording, validates anchor positions, and corrects inaccuracies before you save or activate the action. AI also generates a screen context for each captured screen and description for the desktop action. Screen context is a description of what the screen does and what it contains, which helps reviewers and AI agents understand the screen's intent.

After AI processing completes, a confirmation banner appears: `AI analysis complete. Verify AI generated anchors and screen contexts before continuing.` Review and refine the AI-generated anchors and screen contexts before activating the action.

**Important:** Record with AI feature requires the ServiceNow AI Lens skill to be active on your instance and you must have the sn\_desktop\_core.desktop\_action\_user role. If these conditions aren't met, the **Record with AI** option is unavailable. Contact your ServiceNow administrator for help.

## Capture modes

You can select a capture mode from the **Capture options** menu in the **Screens and Steps** panel.

\[Omitted image "recorder-screens-menu-ad.png"\] Alt text: Record screens menu showing three options: Record with AI \(recommended\), Auto capture with recorder, and Manual capture.

-   **Record with AI \(recommended\)**

    Records your interactions by capturing screens and adding steps and uses AI to automatically validate anchor positions and generate screen contexts at design time, reducing the risk of automation failures at runtime.

-   **Auto capture with recorder**

    Records your interactions automatically and adds anchors and steps without AI processing.

-   **Manual capture**

    Captures screens without automated recording, giving you full control over what is captured.


## Recorder controls

You can select any of the following options from the **More options** menu on the Action recorder panel:

\[Omitted image "recorder-auto-capture-ad.png"\] Alt text: Floating recorder panel that has Discard, Pause, and Start recording UI actions.

-   **Start recording**: Start recording the steps
-   **Pause**: Skip recording steps
-   **Restart**: Restart recording the steps
-   **Discard**: Discard the recording if it doesn't meet your needs
-   **Stop recording**: Stop recording steps

Each step that you perform is captured sequentially and the type of UI action is displayed for each step. For example, Capturing Mouse Left Click event.

## Limitations

Scrolls performed using a laptop touchpad aren't captured.

## Tips for accurate recording

Follow these tips to improve the accuracy of your recordings.

-   Before performing any action, ensure the highlighter is visible on the target control. Recording too quickly may prevent the recorder from capturing the action sequence correctly.
-   Avoid performing steps too quickly. When the message in the Action recorder panel appears in red, wait for the recorder to finish processing the current step before continuing.

    \[Omitted image "recorder-auto-capture-red-ad.png"\] Alt text: Message in red indicating panel is still capturing step.

    Proceed with the next step when the red highlight box appears around the element you interact with and the message in the Action recorder panel changes to blue.

    \[Omitted image "recorder-auto-capture-blue-ad.png"\] Alt text: Message in blue indicating panel finished capturing step.

-   Temporarily hovering components, such as drop-downs, multi-select fields, reference fields, and date pickers may not always be captured during recording, or may generate inaccurate anchors. Review the recording after completion and recapture any affected steps as needed.
-   When selecting check boxes or radio buttons, click as close to the center of the control as possible to avoid activating areas outside the intended element.
-   Scrolling the page or hovering over a field may result in inaccurate anchors. Avoid both while recording.
-   Perform scrolls in small increments, one scroll at a time, so the recorder captures each scroll action accurately.
-   On the desktop home screen, the system may select the Windows icon instead of the Chrome icon as the anchor due to differences in the desktop layout between the main and inset user sessions. Verify that the correct icon is selected after recording.
-   In rare instances, latency between capturing a screenshot and retrieving control details may cause an anchor to reflect an element from a subsequent screen rather than the intended one. If this occurs, recapture the affected screen.

## How screens are captured

During recording, the steps that you perform are captured as screens. Related steps are captured in the same screen, for example, the steps related to filling in the text fields in the same window. A new screen is captured in the following conditions:

1.  Window is changed
2.  Button is clicked or option is selected that might change the layout
3.  Page is scrolled
4.  Special keyboard keys are used, such as Enter or Tab

This helps maintain the correct screen context and reliable automation replay.

You can capture a maximum of 50 steps using the recorder in a recording session. While auto-capturing steps, a counter displays the remaining number of steps you can capture \(for example, "35 of 50 max"\). Recording stops automatically after you capture 50 steps. If you need to capture additional steps, start a new recording session. The new recording adds screens and steps to those captured in the previous recording.

**Related topics**  


[AI Desktop Actions Design workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/agentic-desktop-overview.md)

[Automate repetitive tasks by recording steps with AI in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/record-with-ai-ad.md)

[Automate repetitive tasks by auto-capturing steps in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/auto-create-desktop-action-ad.md)

[Create badge desktop action in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/example-badging-magmt-concept-ad.md)

