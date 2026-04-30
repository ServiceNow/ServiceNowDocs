---
title: MCP server approval workflow
description: Explore the MCP server approval workflow.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2025-11-23"
reading_time_minutes: 1
breadcrumb: [Process flow of MCP servers Via AI Gateway, AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# MCP server approval workflow

Explore the MCP server approval workflow.

## Before you begin

Role required: AI steward \[sn\_ai\_governance.ai\_steward\]

## Procedure

1.  Navigate to **Al Control Tower** &gt; **AI assets** &gt; **Approvals**.

2.  Select the MCP server from the asset type filter or navigate to Lifecycle and filter by the current state: **New**.

3.  Select the MCP Server record with its Status: **New**.

4.  Click **Start Review**.

    **Note:** Within AI Agent Studio, the MCP Server shows a status of AI Steward review during this phase. Product Owners can select View approval record in AI Agent Studio to go straight to the MCP Server record in AI Control Tower.

    A playbook is triggered to guide the approval process through three phases: Assess, Build and Test, and Deploy.

5.  Click **Mark as Complete** for the Assess phase.

    **Note:** The Asses phase includes Architecture review, Risk Assessment, and Stakeholder review.

6.  Complete the Build and Test phase activities.

    **Note:** The Build and Test phase involves out-of-application testing and validation activities such as running a test AI agent using the MCP Server as a tool and validating output received.

7.  Click **Mark as Complete** for the Build and test phase.

8.  Click **Mark as Complete** for the Deploy phase.

    **Note:** The Deploy phase is the final step to deploy and allow the MCP Server for usage.

9.  Select **Save**.

    **Note:**

    The AI Gateway setup tab appears only after an MCP server request is approved. The AI steward can pause transactions whenever needed through this tab. For information on the tabs appearing in the MCP server record, see [MCP server record](../concept/view-the-mcp-server-record.md)


