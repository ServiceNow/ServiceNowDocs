---
title: AI Desktop Actions user interface
description: The AI Desktop Actions application includes a task input field, an execution workspace, and status indicators that show the current state of AI agent task execution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai\_desktop\_actions\_reference\_adaptive.html
release: australia
topic_type: reference
last_updated: "2026-08-18"
reading_time_minutes: 4
keywords: [AI Desktop Actions, execution states, legal disclaimer, privacy, requirements, Mac permissions]
breadcrumb: [Adaptive desktop actions for desktop and web, Explore, AI Desktop Actions, Enable AI experiences]
---

# AI Desktop Actions user interface

The AI Desktop Actions application includes a task input field, an execution workspace, and status indicators that show the current state of AI agent task execution.

## AI Desktop Actions home page

\[Omitted image "ai-da-mac-home-page.png"\] Alt text: AI Desktop Actions home page with a task input field and placeholder example text.

-   **Task input field**

    The input field is where you describe the task to accomplish in natural language. The field accepts text describing the task to perform across browsers, desktop apps, and files. The description must be specific and include complete context. The field includes a placeholder example to guide you on the type of input expected and the **Send Message** \[Omitted image "send-msg-da.png"\] Alt text: button that triggers the action.

-   **Access to profile and documentation**

    A dedicated section enables you to view your profile information, access product documentation, and check the product version.


## AI Desktop Actions execution workspace

\[Omitted image "ai-da-mac-main-page.png"\] Alt text: The main page layout with Chat and screen preview panels. For element descriptions, refer to the list following this image.

-   **1. Execution plan**

    The AI-generated plan that appears before execution begins. AI Desktop Actions restates your request in plain language, breaks it into numbered steps, and asks for approval. This prevents unintended steps and gives you a chance to correct any misunderstandings.

-   **2. AI steps**

    A real-time breakdown of the AI agent's processing steps and observations as it executes your task. AI steps may differ from the execution plan presented. Each step shows what the AI agent observes on screen, identifies potential issues, and explains its decision for the next step. This transparency lets you follow the AI agent's decision-making and understand the reason for each step.

-   **3. Preview window**

    The virtual desktop displaying only the files, folders, or applications that AI agent opens as part of automation execution. This window lets you monitor what the AI agent is doing in real time. The preview updates as steps are performed. You can only interact with this virtual desktop through the preview window.

-   **4. Control buttons**
    -   **Take control**: Pauses execution and gives manual control to you. Use this to intervene if the task is not proceeding as expected or requires human input.
    -   **Return control**: Return control back to AI agent. After you return control, a confirmation dialog appears prompting you to enter handoff notes for the AI agent. These notes help the AI agent interpret the changes you made.
-   **5. Execution status**

    The current state of the task, such as Initiated, Running, Completed, Failed, or Stopped. The status badge updates as the AI progresses through steps. For more information about the statuses, see [Execution status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_reference_adaptive.md).

-   **6. New chat**

    Option to begin a fresh conversation. Clears the current task and resets the chat interface to accept a new request.

    **Note:** The preview window continues to show the applications it opened for the previous task.

-   **7. Back button**

    Option available in the chat interface to return to the home screen.

-   **8. Start/Stop agent**

    Option to start or stop execution immediately. Use the Stop button to cancel an in-progress task.


## Execution status

The execution status indicates the current state of the AI agent's task execution.

<table id="table_sms_mfp_xjc"><thead><tr><th>

Status

</th><th>

Description

</th><th>

What you can do

</th></tr></thead><tbody><tr><td>

Ready

</td><td>

The AI Desktop Actions application is open and waiting for you to describe a task. No execution has started yet. This is the initial state after launching the application or after completing a previous execution.

</td><td>

Enter your task description in the text field and select the **Send Message** \[Omitted image "send-msg-da.png"\] Alt text: button to send your request to AI agent.

</td></tr><tr><td>

Initiated

</td><td>

AI Desktop Actions has initiated your request. The AI agent creates an execution plan and waits for your approval before performing actions on your desktop.

</td><td>

Review the execution plan. Select **Yes, go ahead** to proceed, or **Cancel** to modify your request.

</td></tr><tr><td>

Running

</td><td>

The AI agent is actively performing the planned steps on your desktop.

</td><td>

Monitor progress. Select **Take control** to pause execution and make manual changes.

</td></tr><tr><td>

Input needed

</td><td>

The AI agent has paused execution because it needs additional information or input from you to continue. This might be credentials, a decision, clarification about how to proceed, or confirmation for a background operation. The AI agent may also pause if it needs confirmation on the resource access.

</td><td>

-   Provide the requested information through the chat interface.
-   Select **Take control** to make manual changes in the preview screen.

</td></tr><tr><td>

You have control

</td><td>

Execution is paused and the desktop is under your control. The AI agent has paused performing actions and is waiting for you to take actions.

</td><td>

Make manual changes to your desktop or applications. After you're done, you can return the control, provide handoff notes, and let AI agent resume.

</td></tr><tr><td>

Success

</td><td>

The AI agent has successfully completed all planned steps. The task is finished and the agent displays results or summary information.

</td><td>

Review the completed task results. You can start a new task or close the application.

</td></tr><tr><td>

Failed

</td><td>

The AI Desktop Actions encountered an error or was unable to complete the task. An error message describes the cause of the failure.

</td><td>

Review the error message. You can start a new task with modified request.

</td></tr><tr><td>

Stopped

</td><td>

You stopped the execution before the AI agent could complete the task. The task is halted and no further actions are taken.

</td><td>

You can start a new task.

</td></tr></tbody>
</table>