---
title: Known issues and limitations of adaptive desktop actions
description: Reference known issues, limitations, and resolution steps for AI Desktop Actions on macOS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/adaptive-desktop-actions-troubleshooting.html
release: australia
topic_type: reference
last_updated: "2026-08-27"
reading_time_minutes: 5
breadcrumb: [Example 4: Adaptive desktop action for desktop and web, Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Known issues and limitations of adaptive desktop actions

Reference known issues, limitations, and resolution steps for AI Desktop Actions on macOS.

<table id="table_zsc_csp_jkc"><thead><tr><th>

Issue

</th><th>

Resolution steps

</th></tr></thead><tbody><tr><td>

The app can't interact with lists, window overlays, popovers, pop-ups, or context menus in non-native applications, such as:-   Microsoft Outlook for macOS \(web-based\)
-   Microsoft Teams \(web-based\)
-   Microsoft PowerPoint \(web-based\)
-   Other non-native macOS apps

Reason:

These applications are built as web-based interfaces inside native windows rather than traditional native apps. The interface elements don't respond to automation the same way native controls do.

</td><td>

The AI agent pauses when it encounters these interface elements and asks you to complete the step manually. You can:-   Make the selection or interaction yourself.
-   Tell the AI agent that the action is complete to continue.

 The AI agent then resumes automating the remaining steps.

 **Tip:** When interacting with the app in the virtual desktop, select a text field or select from the list to change the green pointer into the macOS cursor. You can then interact normally and perform actions inside the virtual desktop.

</td></tr><tr><td>

After interacting with an application, the OS cursor may remain inside the virtual desktop instead of returning to your main session.

</td><td>

To bring the cursor back to the main desktop manually, move the cursor diagonally toward the top-left corner inside the virtual desktop. This moves the cursor out of the virtual desktop to your main session.

</td></tr><tr><td>

The green pointer may move outside the preview window when you move an application from the preview window to your main session while the AI agent is still executing.

</td><td>

Avoid moving applications during AI agent execution. If this occurs, the AI agent may pause and ask for manual intervention. Complete the required step manually and allow the AI agent to resume.

</td></tr><tr><td>

Unable to run automation tasks involving Microsoft Excel and Microsoft Word.

</td><td>

To use Microsoft Excel and Microsoft Word connectors, create resource access rules for these applications on your instance.

</td></tr><tr><td>

The AI agent is unable to select values in certain ServiceNow form field types, such as:

 -   List field selections
-   Reference field value selections
-   Date and time picker controls
-   Overlay or pop-up selections

</td><td>

When the AI agent encounters these form field types, it pauses and asks you to take control. Do one of the following:

 -   Select the required value in the list or reference field manually.
-   Pick the date or time from the date and time picker.
-   Confirm the selection is complete.
-   Return control to the AI agent to continue with the remaining steps.

 Alternatively, you can defer the action and provide the value in a subsequent task.

</td></tr><tr><td>

If the AI agent launches one instance of an application \(for example, Outlook or Chrome\), it continues performing actions on that instance even if you open other instances of the same application. The AI agent operates on the window it launched, not on windows you open separately. The AI agent detects and works with the specific application instance it created at the start of the task. It doesn't automatically switch between multiple instances.

If you start a new task using the same application, the AI agent may open a new window or instance. You may see multiple icons of the same app in your dock.

</td><td>

-   Before starting a task, close other instances of the same application to avoid confusion.
-   After completing a task, close unused instances of the application to keep your dock clean.

</td></tr><tr><td>

When the AI agent performs actions on non-UI tools like Microsoft Excel, Microsoft Word, and other document-based applications, you may not see any visual indicator of the actions being performed in the preview window. You can only see the **executing in background** tag in AI steps in the chat interface. Reason:

The AI agent may interact with these applications through automation APIs rather than the graphical user interface. This is more efficient but means you won't see visual feedback of what's happening.

</td><td>

In some cases, the AI agent may open the target file on your main session before performing operations. When this happens, you can see the file open in your main desktop and observe the changes being made.

 Otherwise, monitor the AI agent's progress updates in the chat window, which reports the status of file operations.

</td></tr><tr><td>

Some applications are denied by default for security reasons, including:

 -   Terminal
-   Run Shell Script
-   Automator
-   Script Editor

 The AI agent doesn't interact with these apps without explicit permission.

</td><td>

If you need the AI agent to use one of these apps for a specific task, update the resource access rules to allow these applications.

 **Warning:** These apps have elevated system privileges. Update resource access rules only for trusted tasks.

</td></tr><tr><td>

Sometimes the AI steps shown in the chat window aren't in sync with the actions shown in the preview window. The chat may show one step while the AI agent is still working on a previous step in the preview window. The system is still evaluating the success or failure of its operations. Chat updates are provided as the AI agent progresses, but there can be a slight delay before the chat reflects the actual state in the preview window.

</td><td>

Wait a moment for the chat and preview window to sync. The actions being performed in the preview window are the current state; the chat will update shortly.

</td></tr><tr><td>

The system may use alternate approaches to interact with specific files that differ from the default method. In the process, the alternate approach may generate additional OS dialogs \(such as "Do you want to save?" prompts\).

 Additionally, when the OS alerts you of pending operations, the OS animation may display in the currently active Dock.

 For example, the AI agent may use an alternate app to interact with a file. After some time, if you try to quit that app from your main session, you might see an OS save dialog. You then need to go back into the preview window and select **Don't Save** to complete the quit operation. The Dock icon may keep jumping up and down during this time.

</td><td>

-   Let the AI agent complete its task before manually interacting with applications in your main session.
-   If an unexpected dialog appears, handle it in the preview window where the AI agent is working.
-   After the task is complete, close any alternate applications the AI agent may have opened.

</td></tr></tbody>
</table>**Parent Topic:**[Execute adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use_ai_desktop_actions_adaptive.md)

