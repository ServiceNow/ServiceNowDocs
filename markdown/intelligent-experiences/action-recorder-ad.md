---
title: Action recorder in Agentic Desktop
description: With Action recorder, you can auto-capture steps to automate repetitive tasks in Agentic Desktop. You can save the steps that you perform on the application elements as a reusable desktop action of type UI block.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-02-11"
reading_time_minutes: 2
breadcrumb: [Explore, Agentic Desktop, Enable AI experiences]
---

# Action recorder in Agentic Desktop

With Action recorder, you can auto-capture steps to automate repetitive tasks in Agentic Desktop. You can save the steps that you perform on the application elements as a reusable desktop action of type UI block.

Action recorder helps you record your interactions with desktop applications to create automated workflows. By recording steps, you can automate tasks that replicate your interactions. The recorded actions are displayed as screenshots in the Design workspace with anchors and steps automatically added.

The recorder captures the following items:

-   Visual snapshots of your screen at key interaction points.
-   Steps in the form of the buttons, fields, and other interface components you interact with.

You can select any of the following options when needed from the **More options** menu on the Action recorder panel:

![Floating recorder panel that has Discard, Pause, and Start recording UI actions.](../image/recorder-auto-capture-ad.png)

-   **Start recording**: Start recording the steps
-   **Pause**: Skip recording steps
-   **Restart**: Restart recording the steps
-   **Discard**: Discard the recording if it doesn’t meet your needs
-   **Stop recording**: Stop recording steps

Each step that you perform is captured sequentially and the type of UI action is displayed for each step. For example, Capturing Mouse Left Click event.

![Message in red indicating panel is still capturing step.](../image/recorder-auto-capture-red-ad.png)

During recording, the steps that you perform are captured as screens. Related steps are captured in the same screen, for example, the steps related to filling in the text fields in the same window. A new screen is captured in the following conditions:

1.  Window is changed
2.  Button is clicked or option is selected that might change the layout
3.  Page is scrolled
4.  Special keyboard keys are used, such as Enter or Tab

This helps maintain the correct screen context and reliable automation replay.

You can capture maximum of 50 steps using the recorder in a recording session. While auto-capturing steps, a counter displays the remaining number of steps you can capture using the recorder \(for example, “35 of 50 max”\). Recording stops automatically after you capture 50 steps. If you need to capture additional steps, start a new recording session. The new recording adds screens and steps to those captured in the previous recording.

**Related topics**  


[Agentic Desktop Design workspace](agentic-desktop-overview.md)

[Automate repetitive tasks by auto-capturing steps in Agentic Desktop](../task/auto-create-desktop-action-ad.md)

[Create badge desktop action in Agentic Desktop](example-badging-magmt-concept-ad.md#)

