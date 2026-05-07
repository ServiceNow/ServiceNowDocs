---
title: Defined desktop actions for desktop and web-based tasks
description: Automate desktop and web-based tasks that involve fixed steps using AI Desktop Actions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-13"
reading_time_minutes: 5
breadcrumb: [Explore, AI Desktop Actions, Enable AI experiences]
---

# Defined desktop actions for desktop and web-based tasks

Automate desktop and web-based tasks that involve fixed steps using AI Desktop Actions.

AI Desktop Actions is a client application that is installed on the Windows operating system. The app offers two workspaces, the Design workspace, where you create and configure desktop automations, and the Execution workspace, where those automations run. Design workspace enables you to automate multi-step processes by recording or manually capturing steps. Execution workspace enables AI agents to execute desktop actions in an isolated desktop session.

Defined desktop actions are categorized into two categories.

-   **On screen task**: These desktop actions help you simulate humans interacting with UI elements on your thick client applications, legacy systems, or SaaS applications without APIs. These actions include clicking buttons, typing into text boxes, selecting from dropdown menus, and more.
-   **Background task**: These desktop actions include prebuilt connectors that enable your AI agents to interact with various applications and system components in the background.

## Key interfaces related to AI Desktop Actions

-   **[Design workspace](agentic-desktop-overview.md)**

    Create and test desktop actions that define how automations interact with desktop applications.

-   **[Execution workspace](agentic-desktop-excution-workspace.md)**

    Automatically runs desktop actions in an isolated desktop session during testing or execution. You do not open this workspace directly.

-   **[AI Agent Studio](../../../administer/now-assist-ai-agents/concept/ai-agent-studio.md)**

    Create and manage AI agents that run desktop actions.

-   **[Now Assist panel](../../../administer/now-assist-platform/concept/now-assist-panel-overview.md)**

    Trigger automations from within ServiceNow.


These components work together to separate design, execution, and monitoring, ensuring secure and reliable desktop automation.

## AI Desktop Actions users

<table id="table_zmk_nx3_ygc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrators

</td><td>

Set up and deploy the AI Desktop Actions application.

</td></tr><tr><td>

Developers

</td><td>

Design, manage, and deploy automation solutions within their organization.

</td></tr><tr><td>

Business users

</td><td>

Automate repetitive desktop tasks without extensive technical knowledge.

</td></tr><tr><td>

Process owners

</td><td>

Optimize business processes by automating manual desktop interactions.

</td></tr></tbody>
</table>## How AI Desktop Actions works end-to-end

![Agentic Workflow diagram showing four stages: Desktop actions, AI agents, Execution, and Desktop-in-Desktop with related tasks and workspace tools.](../image/agentic-desktop-workflow.png "Workflow for automating fixed steps using desktop actions")

This workflow shows how AI Desktop Actions works end to end from designing desktop actions to running them during execution. As you move through the workflow, note which steps you perform manually and which steps are handled automatically by the system.

**Important:** Access to the Design workspace and Execution workspace depends on the user’s role.

-   When users with the AI Agent Admin \(sn\_aia.admin\) role sign in from their desktop, they can access the Home page and Design workspace to create desktop actions. When they test a desktop action, the Execution workspace launches automatically.
-   When users with the Now Assist panel user \(now\_assist\_panel\_user\) role trigger an automation from the Now Assist panel, the Execution workspace launches automatically to run the desktop action.

You don’t open the Execution workspace directly. It launches automatically when you test or run a desktop action.

-   With the AI Agent Admin role, use the no-code Design workspace to create reusable desktop actions that AI agents can execute. You can visually create and simulate application interactions, such as clicks, text entry, and extraction that mimic human behavior using screen and UI element recognition.
-   When you test a desktop action, the system automatically launches the Execution workspace in an isolated desktop session. You do not open or manage the Execution workspace directly.
-   Activate your desktop actions from the Design workspace so that AI agents can use them as tools in AI Agent Studio.
-   Create AI agents by providing simple text instructions in AI Agent Studio.
-   Add your designed desktop actions as tools to your AI agents.
-   Verify your AI agents function correctly with their integrated tools.
-   With the Now Assist panel user role, provide instructions for the task you want to complete on your desktop in the Now Assist panel.
    -   An AI agent is triggered from the Now Assist panel to execute the desktop actions.
    -   The AI agent selects the appropriate desktop action to complete the task.
    -   The system automatically launches the Execution workspace in an isolated desktop session to run the desktop actions. You do not open or manage the Execution workspace directly.
-   Observe and manage automations as they run in real time in the Execution workspace, which provides a dedicated execution environment.
-   Step in and out of the automation where your inputs are required.
-   Check the outcome of the execution in the Now Assist panel.

For more information, see [Defined path desktop actions in AI Desktop Actions](desktop-actions-designer-workspace-ad.md) and [Creating AI agents for AI Desktop Actions](create-ai-agents-ad.md).

## AI Desktop Actions capabilities

-   **Design desktop actions**
    -   Create, configure, and manage reusable desktop actions with application metadata.
    -   With the Recorder feature, automatically record and capture user interactions and contextual information while you perform actions on desktop applications.
    -   Additionally, manually capture screens, define UI interactions, and structure steps in a no-code Design workspace.
-   **Run in the background**

    Enable silent and non-intrusive execution of agent tasks, supporting uninterrupted user workflows.

-   **Support for diverse applications on Windows**

    Automate tasks across a wide variety of environments and UI types, including legacy systems, thick client applications, and web applications on Windows operating system.

-   **Core desktop capabilities**

    Support common desktop actions such as form filling, application clicks, and OS file handling.

-   **Performance**

    Supports automations with native integration to AI Agent Studio.

-   **Seamless integration**

    Publish configured desktop actions directly to AI Agent Studio for easy access and deployment.


**Related topics**  


[Configure AI Desktop Actions](../task/configure-agentic-desktop.md)

[Examples of creating desktop actions](examples-of-agentic-desktop-automation.md)

[Examples of executing desktop actions using AI agents](use-agentic-desktop.md)

[AI Desktop Actions reference](../reference/agentic-desktop-reference.md)

