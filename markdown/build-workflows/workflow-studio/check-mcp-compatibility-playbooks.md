---
title: Check the compatibility of playbooks
description: Verify that the playbook is compatible to be used as an MCP tool.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/check-mcp-compatibility-playbooks.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2026-09-21"
reading_time_minutes: 1
keywords: [MCP, playbooks, compatibility, tools]
breadcrumb: [Playbooks as an MCP tool, Playbooks, Workflow Studio, Build workflows]
---

# Check the compatibility of playbooks

Verify that the playbook is compatible to be used as an MCP tool.

## Before you begin

Role required: workflow\_mcp\_tool\_admin

## About this task

When you try to [Add a playbook as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/add-playbook-as-mcp-tool.md) but are unable to see a playbook in the MCP tool list, perform this procedure to verify that the playbook is compatible.

## Procedure

1.  Select **All**.

2.  In the search box, enter `sys_workflow_mcp_staging_tool.list`.

3.  In the **MCP Staging Workflow Tools** list, locate the playbook by name or by sorting the table.

4.  If you don't see your playbook in the list, run a new compatibility scan.

    |Option|Description|
    |------|-----------|
    |**__Full scan compatibility check__**|Scans all the playbooks in your instance for compatibility. Select this option when the table is empty and you run the compatibility check for the first time.|
    |**__Quick scan compatibility check__**|Runs the compatibility scan only on new playbooks. Select this option if you import playbooks to your instance.|

5.  Check the **Compatibility Status** column of the playbook.

    For incompatible playbooks, open the record to see the incompatible reason. After you update and republish the playbook, the compatibility status updates automatically. For more information about compatibility, see [Playbooks as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/playbook-as-mcp-tool.md).

    When the playbook compatibility status is **Compatible**, you can add it to an MCP server as an MCP tool.

    To check the compatibility status of subflows and actions used in the playbook, select **All** and enter `sn_fd_genai_mcp_staging_action_tool.list` \(for actions\) or `sn_fd_genai_mcp_staging_subflow_tool.list`\(for subflows\) in the search box. To be compatible as an MCP tool, the subflows and actions need an AI ACL. For more information, see [Create an AI ACL for a Subflow or Action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/create-ai-acl.md).


## What to do next

Add the playbook as an MCP tool to an MCP server. For more information, see [Add a playbook as an MCP tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/build-workflows/workflow-studio/add-playbook-as-mcp-tool.md).

