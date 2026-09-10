---
title: Execute adaptive desktop actions for desktop and web
description: Use AI Desktop Actions to automate desktop or web-based tasks. Describe your task to the AI agent, review and approve the execution plan, and monitor real-time progress.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/use\_ai\_desktop\_actions\_adaptive.html
release: australia
topic_type: task
last_updated: "2026-07-14"
reading_time_minutes: 6
keywords: [use AI Desktop Actions, automate desktop task, execute agent action, request automation, adaptive desktop actions, probabilistic desktop actions]
breadcrumb: [Execute desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Execute adaptive desktop actions for desktop and web

Use AI Desktop Actions to automate desktop or web-based tasks. Describe your task to the AI agent, review and approve the execution plan, and monitor real-time progress.

## Before you begin

-   Confirm that AI Desktop Actions is enabled on your ServiceNow instance. For more information, see [Configure AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-agentic-desktop.md).
-   Confirm that the AI Desktop Actions installer is installed to automate repetitive tasks across applications and desktop. For more information, see [Download AI Desktop Actions installer for adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/download-agentic-desktop-installer-adaptive.md).
-   Confirm that the following system requirements are met:

    -   macOS machine is used.
    -   The ServiceNow AI Lens skill must be active on your instance. Contact your ServiceNow administrator if you're unsure whether this condition is met.

Role required: sn\_aia.admin and lens\_user, now\_assist\_panel\_user and lens\_user, or desktop\_action\_user

## About this task

Use this procedure when you have a repetitive or complex desktop task that involves multiple applications or steps. Examples include copying data between systems, filling out forms, organizing files, or extracting information from documents. Instead of doing these tasks manually, you can describe what you want done and let AI handle the execution while you review and control the process.

AI Desktop Actions maintains context of the task until it is completed or failed. Each task starts without context from the previous task.

**Warning:** Don't lock the desktop during automation execution. If the desktop locks, the AI agent loses access and can't continue the automation.

## Procedure

1.  From your macOS machine, launch the AI Desktop Actions application.

2.  Verify that you granted the following system permissions on your macOS system.

    When you first launch the application, you will be prompted to grant two permissions:

    -   **Screen Recording**: Enables the AI agent to see your screen
    -   **Accessibility**: Enables the AI agent to control your keyboard and cursor
    You can grant system permissions by selecting **Open system settings**. After granting permissions, restart the application.

    \[Omitted image "ai-da-system-settings.png"\] Alt text:

    If you have already granted the permissions, the application displays the login page.

3.  On the login page, in the **Add ServiceNow URL** field, enter the ServiceNow instance URL.

    For example, `https://<instance name>.service-now.com`.

    \[Omitted image "ad-login-screen.png"\] Alt text: AI Desktop Actions login screen for entering ServiceNow instance URL.

4.  Select **Proceed**.

5.  Log in to your ServiceNow account by entering your user name and password.

    \[Omitted image "ad-login-screen-cred.png"\] Alt text: Login window for entering your ServiceNow account username and password.

6.  In the text field, describe the task you want the AI agent to perform in natural language.

    Include specific details such as:

    -   Which application to start with
    -   What data or documents to use
    -   Where the data is located
    -   What the result should be
    -   Any specific values or settings to use
    Example: Open /users/sales\_data.xlsx. Navigate to sheets "Q1", "Q2", "Q3". In each sheet, identify column C \(Revenue\) and sum all values. Create a new sheet named "Annual\_Summary". In this new sheet, create a table with: Row headers \(Q1, Q2, Q3\), Column A with quarterly totals calculated from each sheet, Column B with monthly averages. Add a row for Annual Total. Format cells with currency format. Save the file.

    **Note:** Some actions, such as background processing or non-UI operations, displays an "Executing in background" tag in AI steps to indicate that the AI agent is working on a task that is not visible on your screen.

7.  Select the **Send Message** \[Omitted image "send-msg-da.png"\] Alt text: button to send your request.

    You're taken to the execution workspace. The AI agent begins analyzing your request and creates an execution plan.

8.  In the execution workspace, review the execution plan that the AI agent created.

    The AI agent displays a numbered list of steps it will perform and applications it will access.

9.  Select one of the following options based on the plan proposed.

    -   **Yes, go ahead**: Select this option if the plan is correct. The agent displays legal disclaimer and proceeds with execution.

        Before executing the task on your desktop, the system checks for applicable security policies and resource access rules based on user criteria.

    -   **Cancel**: Select this option if you want to modify the plan and resubmit with more specific instructions.
10. Depending on the security policy evaluation result, do one of the following.

<table id="choicetable_tlm_zjb_jkc"><thead><tr><th align="left" id="d198589e358">

Resource access

</th><th align="left" id="d198589e361">

Description and action

</th></tr></thead><tbody><tr><td id="d198589e367">

**Denied**

</td><td>

-   File, folder, website: The AI agent can't access the denied resource and stops execution.
-   Application: The AI agent tries an alternative approach to open the application.


</td></tr><tr><td id="d198589e385">

**Allowed**

</td><td>

The AI agent continues with the task automatically.

</td></tr><tr><td id="d198589e394">

**Neither allowed nor denied**

</td><td>

No policy rule exists for this resource, so the AI agent prompts you to allow access. Choose:-   **Allow once**: The AI agent accesses this resource for this task only
-   **Deny**: The AI agent stops and halts execution


</td></tr></tbody>
</table>11. Observe the execution progress in the preview window.

    The AI agent opens applications, navigates windows, and performs the requested actions.

12. Monitor the execution status to track the AI agent's progress.

    For more information about execution statuses, see [Execution status](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_reference_adaptive.md).

13. If the AI agent paused execution and needs your inputs or encounters an issue, do one of the following.

    -   Provide the requested information or clarify your instructions in the chat. The AI agent resumes automatically.
    -   Take control of execution, manually complete the blocked step yourself, and then return control to the AI agent. For more information, see [Take control of AI Desktop Actions execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/control_ai_desktop_actions_execution_adaptive.md).
14. If the AI agent is not executing steps according to your expectations, select **Take control** and manually perform the step.

    For more information, see [Take control of AI Desktop Actions execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/control_ai_desktop_actions_execution_adaptive.md).


## Result

After the AI agent completes all planned steps, verify that the results match your expectations.

-   If the results are correct, the task is complete. Any data collected, files created, or changes made are available for your review.
-   If adjustments are needed, you can start a new task or manually edit any changes the AI agent made.

-   **[Take control of AI Desktop Actions execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/control_ai_desktop_actions_execution_adaptive.md)**  
Take control and pause the execution that AI agent is running. Make manual changes to your desktop, and then resume execution by providing handoff notes to the AI agent.
-   **[Known issues and limitations of adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/adaptive-desktop-actions-troubleshooting.md)**  
Reference known issues, limitations, and resolution steps for AI Desktop Actions on macOS.

**Parent Topic:**[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)

**Related topics**  


[Adaptive desktop actions for desktop and web-based tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai_desktop_actions_adaptive.md)

[Take control of AI Desktop Actions execution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/control_ai_desktop_actions_execution_adaptive.md)

[Known issues and limitations of adaptive desktop actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/adaptive-desktop-actions-troubleshooting.md)

