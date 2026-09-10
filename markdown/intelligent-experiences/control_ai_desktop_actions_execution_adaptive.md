---
title: Take control of AI Desktop Actions execution
description: Take control and pause the execution that AI agent is running. Make manual changes to your desktop, and then resume execution by providing handoff notes to the AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/control\_ai\_desktop\_actions\_execution\_adaptive.html
release: australia
topic_type: task
last_updated: "2026-07-14"
reading_time_minutes: 3
keywords: [control execution, pause agent, handoff notes, give back control]
breadcrumb: [Example 4: Adaptive desktop action for desktop and web, Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Take control of AI Desktop Actions execution

Take control and pause the execution that AI agent is running. Make manual changes to your desktop, and then resume execution by providing handoff notes to the AI agent.

## Before you begin

-   AI Desktop Actions must be in the Running state. For more information, see [Execute adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use_ai_desktop_actions_adaptive.md).

Role required: sn\_aia.admin and lens\_user, now\_assist\_panel\_user and lens\_user, or desktop\_action\_user

## About this task

When the AI agent is running, you can take control to pause it, make your changes, and then return control to the AI agent. Use this to correct a data entry error, adjust a workflow, or provide manual input that the agent can't detect. Taking control lets you address issues without restarting the task.

Some actions may run in the background, particularly non-UI operations or processing tasks that don't require screen interaction. When you take control during background execution, AI Desktop Actions pauses all processing and waits for your input. After you provide handoff notes, the AI agent resumes with the updated context.

## Procedure

1.  Select **Take control** from the execution interface.

    The AI agent pauses immediately and the execution status changes to **You have control**.

2.  Review the current state of your desktop and applications.

    The applications the AI agent was working will remain open and in their current state. The AI agent has paused executing any actions.

3.  Make any manual changes or corrections you require to your desktop or applications.

    Examples of manual changes:

    -   Dismiss a pop-up or browser security dialog
    -   Complete a CAPTCHA or security challenge
    -   Correct data that the agent entered incorrectly
    -   Navigate to a different location or window
    -   Make adjustments to form fields or settings
    -   Organize or reorganize files
    -   Cancel an action the agent started and redirect it
4.  When you're ready to resume execution, select **Return control**.

    A text input area opens for you to leave notes for the AI agent.

    \[Omitted image "handoff-note-agent-da.png"\] Alt text: Add a note for the AI agent dialog box with text area to enter notes and action button to submit.

5.  In the Add a note for the AI agent dialog, describe the manual changes you made and any additional context the AI agent needs to resume correctly.

    Example handoff note: "Changed category to Subscriptions and corrected the amount to $250. The new total should be $2,100."

    Example handoff note: "Navigated to the Reports tab. Password field now contains the updated credentials."

    Be specific about what you changed and why, so the AI agent can continue with the correct context and avoid repeating unnecessary steps.

6.  Select **Return control to AI agent** to resume execution.

    The AI agent reads your handoff notes, updates its context, and continues executing the remaining steps of your original request.

7.  Monitor the execution status as the AI agent continues working.

    The execution status returns to Running. The AI Desktop Actions continues from where it paused, incorporating the changes you made and the context you provided in your handoff notes.


## What to do next

After the AI agent resumes:

-   Monitor the progress to verify the AI agent is executing correctly with your manual changes.
-   If additional corrections are needed, you can pause execution again by selecting **Take control**.
-   When execution completes, review the final results to verify that all steps were performed correctly.

**Parent Topic:**[Execute adaptive desktop actions for desktop and web](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use_ai_desktop_actions_adaptive.md)

**Related topics**  


[Adaptive desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md)

[Known issues and limitations of adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/adaptive-desktop-actions-troubleshooting.md)

