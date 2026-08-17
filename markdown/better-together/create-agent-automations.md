---
title: Create an AI agent and desktop actions from Automation Center
description: After reviewing the automation blocks generated from an automation request, create an AI agent that executes desktop actions on a Windows machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/better-together/create-agent-automations.html
release: zurich
topic_type: task
last_updated: "2026-06-17"
reading_time_minutes: 4
keywords: [create agent, decomposed automations, automations blocks, desktop actions, automation center, UI block, non UI block, deterministic desktop actions]
breadcrumb: [Building desktop automations from Task Mining data, Solutions]
---

# Create an AI agent and desktop actions from Automation Center

After reviewing the automation blocks generated from an automation request, create an AI agent that executes desktop actions on a Windows machine.

## Before you begin

-   Verify that Automation Center and AI Desktop Actions are installed.
-   Verify that the AI Desktop Actions client application is downloaded and installed on the Windows machine where the AI agent runs.
-   Verify that ServiceNow Otto for Automation Center plugin is installed and the User task step summarization skill is activated.
-   Confirm that you have created automation blocks from an automation request Automation Center. For more information, see [Create automation blocks from the automation request in Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/better-together/generate-automations-tm.md).
-   The automation request must be in the **In progress** state.

Role required: sn\_aia.admin, sn\_tm\_core.analyst, sn\_ac.automation\_admin, sn\_ac.automation\_technical\_user

## About this task

When you select **Create agent**, Automation Center converts the generated automation blocks into desktop actions. It also creates a new AI agent pre-populated with instructions, a role description, input parameters, and desktop actions tools. For on-screen tasks, a new desktop action is created using screenshots from the task recording and added as a tool. For background tasks, a tool is created for the background application. If a matching background application is already available, instructions are passed to the existing background application.

After the agent is created, you must review the agent instructions and test each desktop action tool before activating the agent in AI Agent Studio. You must verify and manually adjust the anchors of on-screen desktop actions in AI Desktop Actions.

**Important:**

Agent testing and AI Desktop Actions tool execution require a Windows machine with the AI Desktop Actions application installed. For more information, see [Download AI Desktop Actions installer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/download-agentic-desktop-installer.md).

## Procedure

1.  From the Automation Center workspace, open the automation request.

2.  Select the Automations tab on the automation request page.

    The Automations tab displays the generated automation blocks. Confirm that you have reviewed and are satisfied with the generated automation blocks before proceeding.

3.  Select **Create agent** on the automation request page.

    **Note:** The **Create agent** option is available only if the ServiceNow AI Agents skill is installed and the automation request is in **In progress** state.

    The **Choose destination instance** dialog box is displayed.

    \[Omitted image "image.unified-cr-agent"\] Alt text: Choose destination instance

4.  Select an instance to create the agent in, and select **Continue**.

    You can select the current instance or any other instance. Verify that the instance you choose has Automation Center and AI Desktop Actions installed.

    For information on configuring an instance, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/connection-alias.md).

    A summary of the agent being created is displayed.

    \[Omitted image "image.unified-agent-summ"\] Alt text: Agent configuration summary

5.  Review the agent configuration summary, and select **Create agent in AI Studio**.

    An AI agent and desktop actions are created and activated in AI Agent Studio. The desktop actions are automatically added as tools to the AI agent

6.  In AI Agent Studio, review the agent instructions.

    The agent is pre-populated with the AI-generated content.

    **Note:** AI-generated instructions may not accurately reflect the task. Review and correct the instructions, particularly the input parameter descriptions and the step sequence.

7.  In the Define user access step, assign required roles and the now\_assist\_panel\_user role to the AI agent so the users with these roles can invoke the AI agent.

    Authorized users can invoke the agent from the ServiceNow Otto panel by typing a request that matches the agent's name or description.

    **Note:**

    Authorized users don't need access to Automation Center or AI Agent Studio to run the agent. They can invoke it from the ServiceNow Otto panel.

    The now\_assist\_panel\_user role is required for executing the desktop actions in AI Desktop Actions.

8.  In AI Desktop Actions, fix any anchor issues for each on-screen task desktop action.

    **Important:** If there are no on-screen task desktop actions created, then the reason could be that the recording didn't have screenshots. Contact the Task Mining analyst to provide the recording with screenshots.

    1.  Open an on-screen task desktop action in the AI Desktop Actions client application.

    2.  Test the on-screen task desktop action.

        For more information, see [Test and activate a desktop action in AI Desktop Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/test-activate-desktop-action-ad.md).

    3.  Verify the position of failed anchors and adjust for each screen in the desktop action.

        Anchors help identify the UI elements that AI Desktop Actions interacts with, such as the field to select or the button to activate. Anchors generated from Task Mining recordings may not match the format that AI Desktop Actions expects. Common anchor issues include:

        -   The URL bar is used as an anchor in the Task Mining recording, but AI Desktop Actions can't anchor to the URL bar. Replace URL bar anchors with a specific page element such as a button or field label.
        -   An anchor targets a UI element that is not reliably present or uniquely identifiable. Select a more stable anchor element.
    4.  Repeat testing until each on-screen task desktop action runs without errors on the target application.


## Result

AI agent and desktop actions are ready for execution.

## What to do next

When an authorized user types a request in the ServiceNow Otto panel that matches the agent's name or description, the system invokes the AI agent. The AI agent executes the desktop action in the AI Desktop Actions execution workspace on user's Windows machine.

For more information about executing desktop actions, see [Examples of executing desktop actions using AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/use-agentic-desktop.md).

