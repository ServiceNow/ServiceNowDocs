---
title: Exploring Agentic Desktop
description: Design, configure, and manage desktop actions with Agentic Desktop to automate repetitive tasks on your desktop using AI agents and agentic workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-11-02"
reading_time_minutes: 7
keywords: [explore]
breadcrumb: [Agentic Desktop, Enable AI experiences]
---

# Exploring Agentic Desktop

Design, configure, and manage desktop actions with Agentic Desktop to automate repetitive tasks on your desktop using AI agents and agentic workflows.

## Agentic Desktop overview

Agentic Desktop is a no-code solution that helps you automate repetitive tasks in legacy desktop applications lacking APIs or backend integrations. Agentic Desktop leverages AI agents created in the ServiceNow AI Platform to interact with desktop applications, perform UI-based tasks, and automate end-to-end workflows.

Agentic Desktop is a client application installed on the Windows operating system. Agentic Desktop provides two workspaces: the Design workspace, where you create and configure desktop automations, and the Execution workspace, where those automations run.

The Design workspace lets you build multi-step desktop actions with intelligence and adaptability. The Execution workspace runs desktop actions in an isolated desktop session and is launched automatically when you test a desktop action or trigger an automation from the Now Assist panel. You do not open the Execution workspace manually. For more information, see [Design workspace](agentic-desktop-overview.md) and [Execution workspace](agentic-desktop-excution-workspace.md).

## How it fits into ServiceNow workflows

Agentic Desktop integrates with AI Agent Studio, enabling you to publish, manage, and incorporate desktop actions into your broader ServiceNow workflows. This integration lets you automate both cloud and desktop applications, giving your AI agents broader capabilities within ServiceNow.

## Agentic Desktop users

<table id="table_zmk_nx3_ygc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Administrators

</td><td>

Set up and deploy the Agentic Desktop application.

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
</table>## Key interfaces related to Agentic Desktop

-   **[Design workspace](agentic-desktop-overview.md)**

    Create and test desktop actions that define how automations interact with desktop applications.

-   **[Execution workspace](agentic-desktop-excution-workspace.md)**

    Automatically runs desktop actions in an isolated desktop session during testing or execution. You do not open this workspace directly.

-   **[AI Agent Studio](../../../administer/now-assist-ai-agents/concept/ai-agent-studio.md)**

    Create and manage AI agents that run desktop actions.

-   **[Now Assist panel](../../../administer/now-assist-platform/concept/now-assist-panel-overview.md)**

    Trigger automations from within ServiceNow.


These components work together to separate design, execution, and monitoring, ensuring secure and reliable desktop automation.

![Agentic Workflow diagram showing four stages: Desktop actions, AI agents, Execution, and Desktop-in-Desktop with related tasks and workspace tools.](../image/agentic-desktop-workflow.png "How Agentic Desktop works end-to-end")

This workflow shows how Agentic Desktop works end to end from designing desktop actions to running them during execution. As you move through the workflow, note which steps you perform manually and which steps are handled automatically by the system.

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

For more information, see [Desktop actions in Agentic Desktop](desktop-actions-designer-workspace-ad.md) and [Creating AI agents for Agentic Desktop](create-ai-agents-ad.md).

## Agentic Desktop capabilities

-   **Design desktop actions**
    -   Create, configure, and manage reusable desktop actions with application metadata.
    -   With the Recorder feature, automatically record and capture user interactions and contextual information while you perform actions on desktop applications.
    -   Additionally, manually capture screens, define UI interactions, and structure steps in a no-code Design workspace.
-   **Run in the background**

    Enable silent and non-intrusive execution of agent tasks, supporting uninterrupted user workflows.

-   **Support for diverse applications on Windows**

    Automate tasks across a wide variety of environments and UI types, including legacy systems, thick client applications, and business applications on Windows operating system.

-   **Core desktop capabilities**

    Support common desktop actions such as form filling, application clicks, and OS file handling.

-   **Performance**

    Supports automations with native integration to AI Agent Studio.

-   **Seamless integration**

    Publish configured desktop actions directly to AI Agent Studio for easy access and deployment.


## Impersonating users

You can trigger AI agents from the Now Assist panel while impersonating another user, provided the impersonated user has the required roles. The sn\_aia.admin role is required to use AI Agent Studio, and the now\_assist\_panel\_user role is required to trigger AI agents that execute desktop actions in the Execution workspace. For more information, see [Impersonating users](https://www.servicenow.com/docs/access?context=c_ImpersonateAUser&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## What to explore next

To learn more about configuring and using Agentic Desktop, see:

-   [Configure Agentic Desktop](../task/configure-agentic-desktop.md)
-   [Desktop actions in Agentic Desktop](desktop-actions-designer-workspace-ad.md)
-   [Creating AI agents for Agentic Desktop](create-ai-agents-ad.md)
-   [Examples of creating desktop actions](examples-of-agentic-desktop-automation.md)
-   [Examples of executing desktop actions using AI agents](use-agentic-desktop.md)
-   [Components installed with Agentic Desktop](../reference/components-installed-with-agentic-desktop.md)
-   [System requirements and limitations in Agentic Desktop](../reference/sys-req-limitations-ad.md)

