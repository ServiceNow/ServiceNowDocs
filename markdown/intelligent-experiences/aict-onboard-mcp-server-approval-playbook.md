---
title: Onboard MCP server approval playbook
description: The Onboard playbook tracks the MCP server through assessment, testing, and deployment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-onboard-mcp-server-approval-playbook.html
release: australia
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [MCP server approval playbook workflow, Working with MCP server records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Onboard MCP server approval playbook

The Onboard playbook tracks the MCP server through assessment, testing, and deployment.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** and select an MCP server.

2.  Access phase:

    1.  Navigate to the **Lifecycle** tab and select **Access**.

    2.  Select **Create new task**.

    3.  Complete all tasks for this phase.

    4.  Select **Mark complete**.

3.  Build and test phase:

    1.  Select **Build and test**.

    2.  Create and complete tasks for this phase.

    3.  Select **Mark complete**.

        **Note:** When the MCP server approval enforcement is active on your instance, agents will not be able to connect to the server until the Deploy phase is complete and the server reaches Approved status.

4.  Deploy phase:

    1.  Select **Deploy**.

    2.  Create and complete the remaining tasks.

    3.  Reload the page.


## Result

The Onboard playbook status updates to Complete. The MCP server status updates to Deployed and Approved and managed status updates to Managed. The MCP server is now available for use in AI Agent Studio and fully configured for client registration.

