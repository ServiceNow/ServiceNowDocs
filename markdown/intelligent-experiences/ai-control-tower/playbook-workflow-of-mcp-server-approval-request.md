---
title: MCP Server Approval Workflow
description: When an MCP Server is submitted, it must be reviewed and approved by an AI steward.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-control-tower/playbook-workflow-of-mcp-server-approval-request.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP Servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# MCP Server Approval Workflow

When an MCP Server is submitted, it must be reviewed and approved by an AI steward.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

## Procedure

1.  Navigate to **Al Control Tower** &gt; **AI assets** &gt; **Approvals**.

2.  Select the MCP server from the asset type filter or navigate to Lifecycle and filter by the current state of **New**.

3.  Select the MCP Server record with the status of **New**.

4.  Click **Start Review**.

    **Note:** Within the AI Agent Studio, the MCP Server shows a status of AI Steward review during this phase. Product Owners can select **View approval record** in AI Agent Studio to go directly to the MCP Server record in the AI Control Tower.

    A playbook is triggered to guide the approval process through these phases: Assess, Build and Test, and Deploy.

5.  Assess Phase.

    1.  Complete the assessment tasks.

        Within this phase, the AI steward can create and assign tasks to the appropriate individuals.

    2.  Click **Mark Complete** for the Assess phase.

6.  Build and Test Phase.

    1.  Complete the Build and Test phase activities.

        **Note:** The Build and Test phase involves out-of-application testing and validation activities such as running a test AI agent using the MCP Server as a tool and validating the output received.

    2.  Click **Mark Complete** for the Build and test phase.

7.  Deploy Phase

    1.  Click **Mark as Complete** for the Deploy phase.

        **Note:** The Deploy phase is the final step to deploy and enable the MCP Server for usage.

    2.  Reload the page

        **Note:**

        The AI Gateway setup tab appears only after an MCP server request is approved. The AI steward can pause transactions whenever needed through this tab. For information on the tabs appearing in the MCP server record, see [MCP server record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-control-tower/view-the-mcp-server-record.md).


## What to do next

[Configure Client registration and AI Gateway Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown)for authentication to enable agents to use the MCP Server through AI Gateway.

