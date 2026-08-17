---
title: Building desktop automations from Task Mining data
description: Automatically convert desktop processes into executable AI agents: capture the task \(desktop processes\) in Task Mining, create desktop actions \(automation blocks\) and AI agent in Automation Center, and test and deploy the AI agent in AI Agent Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/better-together/creating-desktop-actions-tm-ac.html
release: australia
topic_type: concept
last_updated: "2026-07-07"
reading_time_minutes: 4
keywords: [create agent, decomposed automations, automations blocks, desktop actions, automation center, UI block, non UI block, deterministic desktop actions]
breadcrumb: [Solutions]
---

# Building desktop automations from Task Mining data

Automatically convert desktop processes into executable AI agents: capture the task \(desktop processes\) in Task Mining, create desktop actions \(automation blocks\) and AI agent in Automation Center, and test and deploy the AI agent in AI Agent Studio.

This feature currently supports only Excel-to-browser interactions, where data is copied from a Microsoft Excel file and it is entered into a form in a browser.

**Note:** This feature uses generative AI to produce automation. AI-generated content, including automation blocks and agent instructions, may be inaccurate or incomplete. Review and validate AI-generated output before activating an agent.

## Automation workflow stages

\[Omitted image "automation-tm-ad-workflow.png"\] Alt text: Business analyst in Task Mining submits an automation request that flows through Automation Center, AI Agent Studio, and AI Desktop Actions, with technical users creating and deploying AI agents and desktop actions at each stage.

-   **[Stage 1: Capture and refine \(Task Mining\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining.md)**
    -   Workstation users use the Task Mining agent to capture their desktop processes end-to-end, including interactions across multiple applications for the selected project. Agent captures screenshots and UI interaction metadata of steps users perform.
    -   Business analyst runs a mining job on the project to generate an analysis of the collected data \(desktop activities\).
    -   Captured desktop activities are stored as tasks in Task Mining.
-   **[Stage 2: Automate \(Task Mining + Automation Center\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/create-automation-request-tm.md)**
    -   Business analysts review the task timeline to define specific optimization opportunities and automation candidates, and submit an automation request for the task in Task Mining.
    -   Automation Center captures the structured data in an automation request for AI-powered step generation and automation block creation.
    -   Technical users generate automation blocks \(on-screen and background tasks\) from the automation request in Automation Center.
    -   Based on the automation request, an AI agent and desktop actions are created in Automation Center.
-   **[Stage 3: Deploy \(AI Agent Studio\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md)**
    -   Technical users with the sn\_aia.admin role verify auto-generated agent name and description, agent steps, and desktop action tools in AI Agent Studio.
    -   Technical users test and deploy the AI agent in AI Agent Studio.
-   **[Stage 4: Execute \(AI Desktop Actions\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)**
    -   Authorized users invoke deployed AI agents from the ServiceNow Otto panel, where the agent automatically executes the complete desktop automation process.
    -   The agent runs both background tasks \(such as fetching data from source files\) and on-screen tasks \(such as navigating web applications and entering form data\) desktop actions in AI Desktop Actions on the Windows machine, completing the entire workflow without user intervention.

## Progressive refinement

The workflow supports progressive refinement at each stage:

1.  Validate Task Mining captured the right interactions.
2.  Verify Automation Center extracted meaningful workflow components.
3.  Validate on-screen task desktop actions on the AI Desktop Actions design workspace.
4.  Verify the description and instructions of the AI agent and test it in AI Agent Studio.
5.  Execute the complete workflow end-to-end in AI Desktop Actions execution workspace.

This staged approach reduces risk and enables early detection of issues before deploying full automations.

## Persona and roles

The automation creation journey involves four key personas:

<table id="table_xzn_lwc_vjc"><thead><tr><th>

Persona

</th><th>

Responsibilities

</th><th>

Key skill

</th></tr></thead><tbody><tr><td>

Business analyst

</td><td>

Reviews tasks, edits captured steps, and creates Automation Request records in Task Mining.

</td><td>

Process documentation, data validation

</td></tr><tr><td>

Technical user

</td><td>

Creates production-ready desktop actions and AI agents from the automation request in Task Mining.Reviews and approves desktop actions. Deploys agents to target instances and performs end-to-end testing in AI Agent Studio.

**Note:** The sn\_aia.admin role is required for editing and testing the AI agent.

</td><td>

Automation development, testing, deployment

</td></tr><tr><td>

Authorized user

</td><td>

Business users, process owners, or operations team members with no automation development experience execute desktop actions in the Windows environment.**Note:** The now\_assist\_panel\_user role is required for executing the desktop actions in AI Desktop Actions.

</td><td>

Executing desktop actions

</td></tr></tbody>
</table>## Key benefits

-   **Automated process documentation**

    By building automation skeletons directly from Task Mining data, ServiceNow eliminates the need to manually construct baseline automation logic.

-   **Reduced clarification cycles**

    Automation artifacts include desktop actions, task steps, input/output mappings, and guardrails.

    Developers receive a pre-configured structure that already contains:

    -   Identified steps in the correct sequence
    -   Relevant data mappings
    -   UI element references
    -   Initial tool connections
-   **Self-service desktop action review**

    Developers can open and validate desktop actions on their own Windows machine, ensuring captured intent matches actual process steps.

-   **AI agent pre-population**

    AI Agent Studio is automatically populated with agent name, specialty description, tools, and tool descriptions sourced directly from the task breakdown.

-   **Reduction in authoring time**

    This approach saves development time compared to building agents from scratch without predefined tool connections and configurations.


## What to explore next

-   [Requirements and limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/tm-ac-req-limitations.md)
-   [Create an automation request in Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/create-automation-request-tm.md)
-   [Create automation blocks from the automation request in Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/generate-automations-tm.md)
-   [Create an AI agent and desktop actions from Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/create-agent-automations.md)

**Related topics**  


[Create Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-task-mining-project.md)

[Create a Task Mining project](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/create-task-mining-projects.md)

[Install the Task Mining agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/install-agent.md)

[Categorize workstation activities to simplify analysis](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/define-default-categorization-rules.md)

[Task Mining agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/task-mining-agent-features-and-workarounds.md)

[Defined path desktop actions in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/desktop-actions-designer-workspace-ad.md)

[Test and activate a desktop action in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-activate-desktop-action-ad.md)

[Create an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-next-best-action-agent.md)

[Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/use-agentic-desktop.md)

