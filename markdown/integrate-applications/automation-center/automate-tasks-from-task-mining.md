---
title: Automating tasks from Task Mining
description: Automation Center can receive task recordings from Task Mining, breaks them into discrete automations, and generates an AI agent in AI Agent Studio that executes those automations using AI Desktop Actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/automation-center/automate-tasks-from-task-mining.html
release: australia
product: Automation Center
classification: automation-center
topic_type: concept
last_updated: "2026-06-17"
reading_time_minutes: 5
keywords: [automate tasks, task mining, automation center, desktop actions, AI agent, generate automations]
breadcrumb: [Integration with Task Mining, Automation Center integrations, Use, Automation Center, Workflow Data Fabric]
---

# Automating tasks from Task Mining

Automation Center can receive task recordings from Task Mining, breaks them into discrete automations, and generates an AI agent in AI Agent Studio that executes those automations using AI Desktop Actions.

## About task automation

Automation Center reads the task recording summary, breaks it into modular automations, and generates an AI agent — without requiring the user to manually author agent instructions or AI Desktop Actions tools from scratch.

This feature currently supports only Excel-to-browser interactions, where data is copied from a Microsoft Excel file and it is entered into a form in a browser.

This section provides information about the tasks that must be performed in Automation Center. For the complete flow starting from Task Mining, see [Building desktop automations from Task Mining data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/better-together/creating-desktop-actions-tm-ac.md).

**Important:**

This feature uses generative AI to produce its output. AI-generated content, including automations and agent instructions, may be inaccurate or incomplete. Review and validate AI-generated output before activating an agent.

## Key benefits

Automating tasks from Task Mining provides the following benefits:

-   Reduces the effort required to automate repetitive desktop work by generating agent instructions from recorded task data.
-   Automatically identifies and categorizes steps as UI-based or background interactions, reducing manual analysis by the technical user.
-   Technical users can refine AI-generated automations before creating an agent so the output reflects the actual task requirements.
-   Creates a reusable AI agent that any authorized user can invoke from the ServiceNow Otto panel without accessing Automation Center or AI Agent Studio directly. The agent can also automatically run if a trigger is set and it meets the trigger criteria.

## Task automation workflow

The following graphic describes the end-to-end workflow for automating tasks from Task Mining:

\[Omitted image "task-mining-auto-gen.png"\] Alt text: Workflow diagram showing the end-to-end process from Task Mining recording to AI agent invocation in the ServiceNow Otto panel

1.  A repetitive task in Task Mining is recorded \(Business user\). When the recording is complete, the user submits an automation request. The task timeline and a summary of user interactions are saved as an attachment to the automation request record.
2.  The automation request appears in Automation Center. A technical user reviews the request. There is no automated notification that informs the Automation Center user about the creation of the automation request in Task Mining.
3.  The automation request in Automation Center is opened \(Technical user\) and automations are generated. Automation Center reads the attachment and uses AI to break down the task into discrete automations.
4.  Each automation is categorized as one of the following:
    -   UI block: An on-screen interaction performed in a browser, such as entering data into a ServiceNow form. Automation Center generates an AI Desktop Actions UI block for these automations using screenshots from the task recording.
    -   Non-UI block: A background interaction with an application that does not require on-screen control, such as reading data from a Microsoft Excel file. Automation Center creates a tool with instructions for the existing background application handler.
5.  The automations are reviewed \(Technical user\). If the output is unsatisfactory, the user can provide additional instructions and regenerate. Because this is AI-generated, results may vary between runs.
6.  When satisfied with the automations, the technical user selects **Create agent**. Automation Center sends the automation details to AI Agent Studio, which creates an agent pre-populated with instructions, a role description, input parameters, and AI Desktop Actions tools.
7.  The technical user reviews the generated agent in AI Agent Studio, corrects any inaccurate instructions, and tests the AI Desktop Actions tools. UI block anchors may require manual adjustment because Task Mining and AI Desktop Actions capture anchor data differently. Anchors are the UI elements that AI Desktop Actions uses to identify where to click or type
8.  After testing and validation, the technical user activates the agent and assigns it to the appropriate roles. Authorized users can then invoke the agent from the ServiceNow Otto panel by describing the task they want to perform. You can also schedule the agent to run when some triggers are met. The agent will run the task as scheduled.

## Limitations and requirements

Consider the following when using this feature:

-   **Windows requirement**: Task Mining recording and AI Desktop Actions agent execution require a Windows machine. Automation Center configuration and agent creation can be performed on any supported operating system.
-   **Supported scenario**: This feature currently supports only Excel-to-browser interactions, where data is copied from a Microsoft Excel file and it is entered into a form in a browser.
-   **AI-generated output variability**: Automations and agent instructions are generated by AI. Each run may produce different results. Review all AI-generated output before creating or activating an agent.
-   **UI-block anchor adjustment**: AI Desktop Actions UI blocks require anchors that identify the UI element to interact with. Anchors captured from Task Mining recordings may not match the format AI Desktop Actions expects and may require manual correction in the AI Desktop Actions editor.
-   **No cross-product notification**: Automation Center users don't receive a notification when a Task Mining user submits an automation request. The business user and the technical user must coordinate directly.
-   **Plugin dependencies**: Both Automation Center and AI Desktop Actions must be installed on the target instance before you can create an agent. ServiceNow Otto for Automation Center must be installed to use this feature.
-   **AI skill dependencies**: User task step summarization skill must be activated. For more information, see [Activate skills for ServiceNow Otto for Automation Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/activate-skill.md).

-   **[Generate automations from a Task Mining request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/generate-automations-tm.md)**  
Use the **Automations** tab on an automation request to break down a Task Mining recording into discrete automations that Automation Center categorizes as UI-block or non-UI-block interactions.
-   **[Create an agent from automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/create-agent-automations.md)**  
After reviewing the automations on an automation request, create an AI agent in AI Agent Studio that uses those automations as tools to execute the recorded task on a Windows machine.

**Parent Topic:**[Integration with Task Mining](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/integrating-with-task-mining.md)

**Related topics**  


[Generate automations from a Task Mining request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/generate-automations-tm.md)

[Create an agent from automations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/automation-center/create-agent-automations.md)

