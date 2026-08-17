---
title: Playbooks as an MCP tool
description: Expose a playbook as a tool in an MCP server, enabling MCP clients to trigger and execute the playbook through the Model Context Protocol \(MCP\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/build-workflows/workflow-studio/playbook-as-mcp-tool.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2026-07-23"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Creating and managing Playbooks, Build Playbooks, Playbooks, Workflow Studio, Build workflows]
---

# Playbooks as an MCP tool

Expose a playbook as a tool in an MCP server, enabling MCP clients to trigger and execute the playbook through the Model Context Protocol \(MCP\).

ServiceNow® MCP Server Console lets you create MCP servers and expose specific tools to MCP clients. When you add a playbook as a tool in an MCP server, MCP clients can invoke the playbook as part of an agentic workflow.

## Dependencies

Before you can expose a playbook as an MCP tool, the playbook must meet compatibility requirements. If you create a playbook or want to expose an existing playbook through an MCP server, make sure that the playbook meets the following requirements:

-   **Activity and lane start configuration**

    All playbook activities and lanes must start immediately when triggered. Delayed start configurations aren't supported in MCP execution.

-   **Supported activity types**

    The playbook may only contain the following activity types:

    -   Create Record Form
    -   Record Form
    -   Questionnaire
    -   Send Email
    -   Knowledge
    -   Instruction
    -   Decisions
    These activity types are supported because their completion semantics map to form submission or mark-complete actions, which MCP can handle asynchronously. Activity types with complex state management or long-running operations aren't supported.

-   **Subflows and actions**

    Any subflows or actions referenced within the playbook must be explicitly marked with Execution Type: MCP-compatible. If a subflow or custom action is not marked as MCP-compatible, the entire playbook is set to incompatible. All dependencies are scanned and validated before the playbook can be exposed as a tool.

-   **Form field types**

    Only primitive field types are supported in MCP playbook execution. Reference fields, complex widgets such as rich text editors and advanced pickers, attachment fields, and user-defined custom types aren't supported.


## Next steps

In ServiceNow® MCP Server Console, create a tool with the playbook and add it to an MCP server. When an MCP client is configured to use the MCP server, the client can invoke the playbook through the tool you created.

## Example: Enabling a playbook as an MCP tool

We take an example of enabling an employee onboarding playbook to new employees through an MCP client such as Claude.

-   **Step 1: Create a playbook for employee onboarding**

    As a playbook author, in Workflow Studio, create and activate a playbook for employee onboarding that is compatible to add as an MCP tool to an MCP server. \[Omitted image "example-playbook-employee-onboarding.png"\] Alt text: An employee onboarding workflow as playbook that can be enabled as an MCP tool to be triggered from an MCP client.

-   **Step 2: Create a Playbook MCP tool**

    As an system admin or MCP server admin, create an MCP tool of type Playbook. Select the employee onboarding playbook and add the tool to an MCP server. For more information, see [Add a playbook as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-playbook-as-mcp-tool.md).

-   **Step 3: Configure the MCP client**

    Configure MCP clients to connect to the server and use the tool. For more information, see [Connecting to an MCP server from an MCP client](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/connect-mcp-server-client.md)

-   **Step 4: Use the playbook from the MCP client**

    As an employee, use the configured MCP client to trigger the playbook. For example, trigger the playbook from a Claude chat. \[Omitted image "example-playbook-claude-trigger.png"\] Alt text: End user can trigger the playbook through a Claude chat.

    Claude searches for the available tools and runs the employee onboarding playbook that you have enabled through MCP tool. Claude prompts you for the required inputs. You can either enter the information or upload a document that contains the required information. \[Omitted image "example-playbook-claude-screen2.png"\] Alt text: The playbook is now triggered and prompts the user for inputs.

    The playbook then automatically moves to the next activity in the workflow and prompts for relevant information.

    After all the activities of the playbook are completed, Claude displays a confirmation message with a summary. \[Omitted image "example-playbook-claude-summary.png"\] Alt text: The playbook is complete. Claude displays the confirmation along with the summary.


-   **[Add a playbook as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/add-playbook-as-mcp-tool.md)**  
Create a tool in the MCP Server Console and expose it in an MCP server so that MCP clients can invoke the playbook through the MCP.

**Parent Topic:**[Creating and managing Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/creating-managing-playbooks.md)

