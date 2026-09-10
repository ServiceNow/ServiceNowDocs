---
title: Add a generative AI skill tool to an AI agent
description: Add a generative AI skill to an AI agent to expand its capabilities with reusable operations and custom functionality.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/add-skill-new.html
release: australia
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
breadcrumb: [Add tools and information, Create an AI agent, AI Agent Studio, Enable AI experiences]
---

# Add a generative AI skill tool to an AI agent

Add a generative AI skill to an AI agent to expand its capabilities with reusable operations and custom functionality.

## Before you begin

If you want to add a custom skill to an AI agent, the skill must be published and activated in the . For more information on deploying custom skills, see [Finalize and publish a custom skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/publish-skill.md) and [Activate a custom skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/activate-skill.md).

When an AI agent uses a skill as a tool, the user the AI agent is running as must pass the ACL of the skill. Ensure that the security configurations for the skill are met by the AI agent and agentic workflow. For more information on setting skill-level ACLs, see [Configure access control lists for a skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skill-kit/nask-access-control.md).

Access failures at run time rather than on save. Tool calls fail and the trace log records an access error against the tool, not a configuration warning. When a tool fails for some users and not others, compare the invoking user roles against the ACL of the underlying skill first. If you [manually test an agentic AI asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/test-ai-asset-new.md), it will flag access issues by the invoking user if there are any.

Role required: sn\_aia.admin

## About this task

A generative AI skill is a reusable operation that extends the capabilities of an AI agent. When adding a skill tool, you can configure its execution mode, output display, and processing messages to ensure the tool works effectively within your AI agent's workflow.

## Procedure

1.  In the Tools section, select **Add tools**, then **Create new tool**, then select **Skill**.

2.  Select an AI skill from the **AI Skill** dropdown.

    The selected skill's name, description, and inputs are displayed automatically.

3.  Describe how the AI agent should use the tool.

    Providing a description increases the likelihood that the AI agent calls the correct tool to accomplish its task.

4.  Select an execution mode under **Execution mode**.

    Choose **Supervised** to require human oversight when the tool executes, or **Autonomous** to allow the tool to run without human intervention.

5.  Toggle **Display output to users** to control whether the tool's output is shown to users.

6.  If display output is enabled, select an output widget from the **Widget** dropdown.

    Widgets can only be used by assistants built in Premium Chat experiences. Select the widget type that best formats the tool's output for users.

7.  Choose whether to display a refined widget message under **Display refined widget message**.

8.  Expand the **Advanced settings** section to configure output transformation and processing messages.

    1.  Select an output transformation format from the **Output transformation format** dropdown.

        Raw output data usually needs to be transformed into a format that is user-friendly and readable. You can also transform data into smaller formats to reduce the amount of data the AI agent needs to analyze. Transforming data involves tradeoffs between data completeness and latency.

        The available output transformation formats are:

        -   **None**: Output data isn't changed into a different format and users will see raw data.
        -   **Concise**: Output data is changed into the most minimal format for users, with less data for the AI agent to analyze.
        -   **Verbose**: Output data is changed into a summary-like format for users, with slightly less data for the AI agent to analyze.
        -   **Paraphrase**: Output data is changed into a format featuring direct statements for users, with no reduction in data.
        -   **Custom**: Output data is changed into a format you specify \(consider data loss and performance issues\).
    2.  Write processing messages for users under **Write processing messages for users**.

        Describe the action that happens while the tool is running in the **In-progress message** field and the final action when the tool completes in the **Completion message** field. For example, users can see "Executing skill" when the tool is in progress and "Skill execution complete" when the tool is done.


## Result

You have added a generative AI skill tool to your AI agent with the appropriate execution mode, output settings, and processing messages configured.

