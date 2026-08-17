---
title: Create an agent from automations
description: After reviewing the automations on an automation request, create an AI agent in AI Agent Studio that uses those automations as tools to execute the recorded task on a Windows machine.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/automation-center/create-agent-automations.html
release: australia
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2026-06-17"
reading_time_minutes: 4
keywords: [create agent, decomposed automations, desktop actions, automation center, UI block]
breadcrumb: [Automating tasks from Task Mining, Integration with Task Mining, Automation Center integrations, Use, Automation Center, Workflow Data Fabric]
---

# Create an agent from automations

After reviewing the automations on an automation request, create an AI agent in AI Agent Studio that uses those automations as tools to execute the recorded task on a Windows machine.

## Before you begin

-   Required role: sn\_aia\_admin, sn\_tm\_core.analyst, sn\_ac.automation\_admin, sn\_ac.automation\_technical\_user
-   Automation Center and AI Desktop Actions must be installed on the target instance.
-   The AI Desktop Actions agent application must be downloaded and installed on the Windows machine where the agent will run.
-   You must have completed the steps in [Integration with Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/integration-with-automation-center.md) and reviewed the automations created from the automation request.
-   User task step summarization skill must be activated. For more information, see [Activate skills for ServiceNow Otto for Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/activate-skill.md).
-   The automation request must be in **In progress** state.

## About this task

When you select **Create agent**, Automation Center sends the automation details to AI Agent Studio. AI Agent Studio creates a new agent pre-populated with instructions, a role description, input parameters, and AI Desktop Actions tools. For UI-block automations, a new AI Desktop Actions UI block is created using screenshots from the task recording. For non-UI-block automations, a tool is created for the background application. If a matching background application is already available, instructions are passed to the existing background application.

After the agent is created, you must review the agent instructions and test each AI Desktop Actions tool before activating the agent. AI-generated instructions may require corrections, and UI block anchors may require manual adjustment.

**Important:**

Agent testing and AI Desktop Actions tool execution require a Windows machine with the AI Desktop Actions application installed.

## Procedure

1.  On the **Automations** tab of the automation request, confirm that you have reviewed and are satisfied with the automations.

    For detailed navigation, see step 1 in [Generate automations from a Task Mining request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/generate-automations-tm.md).

2.  Select **Create agent** on the automation request page.

    **Note:** The **Create agent** option is available only if the User task step summarization skill is installed and the automation request is in **In progress** state.

    The **Choose destination instance** dialog box is displayed.

    \[Omitted image "unified-cr-agent.png"\] Alt text: Choose destination instance

3.  Choose an instance to create the agent in, and select **Continue**.

    You can select the current instance or any other instance. Verify that the instance you choose has Automation Center and AI Desktop Actions installed.

    For information on configuring an instance, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connection-alias.md).

    A summary of the agent that is in progress is displayed.

    \[Omitted image "unified-agent-summ.png"\] Alt text: Agent configuration summary

4.  Review the configuration summary, and select **Create agent in AI Studio**.

    Automation Center creates the agent in AI Agent Studio and adds AI Desktop Actions tools based on the automations. The agent opens in AI Agent Studio.

5.  In AI Agent Studio, review the agent instructions.

    The agent is pre-populated with the AI-generated content.

    **Note:** AI-generated instructions may not accurately reflect the task. Review and correct the instructions before activating the agent, particularly the input parameter descriptions and the step sequence.

6.  Test each AI Desktop Actions UI-block tool and correct any anchor issues.

    **Important:** If you notice that no UI-block tool is created for your on-screen automations, then the reason could be that the recording did not have screenshots. Contact the Task Mining user to provide the recording with screenshots.

    To test a UI-block tool, open it in AI Desktop Actions and run a test on the Windows machine where the AI Desktop Actions agent application is installed. For more information, see [Test AI agent or agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/na-ai-wa-test.md).

    Anchors identify the UI elements that AI Desktop Actions interacts with, such as the field to select or the button to activate. Anchors generated from Task Mining recordings may not match the format that AI Desktop Actions expects. Common anchor issues include:

    -   The URL bar is used as an anchor in the Task Mining recording, but AI Desktop Actions can't anchor to the URL bar. Replace URL bar anchors with a specific page element such as a button or field label.
    -   An anchor targets a UI element that is not reliably present or uniquely identifiable. Select a more stable anchor element.
    Repeat testing until each UI-block tool runs without errors on the target application.

7.  Assign roles to the agent and activate it in AI Agent Studio.

    Assign the agent to the roles whose members are authorized to invoke it. After activation, authorized users can invoke the agent from the ServiceNow Otto panel by typing a request that matches the agent's name or description.

    **Note:**

    Authorized users don't need access to Automation Center or AI Agent Studio to run the agent. They invoke it from the ServiceNow Otto panel on any page in ServiceNow.


## Result

The agent is active in AI Agent Studio and available to authorized users. When a user types a request in the ServiceNow Otto panel that matches the agent's name or description, the system invokes the agent. The agent executes the AI Desktop Actions tools on the user's Windows machine to complete the recorded task.

**Parent Topic:**[Automating tasks from Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/automate-tasks-from-task-mining.md)

**Related topics**  


[Automating tasks from Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/automate-tasks-from-task-mining.md)

[Generate automations from a Task Mining request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/generate-automations-tm.md)

