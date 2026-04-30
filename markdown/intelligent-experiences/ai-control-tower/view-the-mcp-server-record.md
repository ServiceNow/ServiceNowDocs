---
title: MCP server record
description: Explore the MCP server record and its tabs in the AI Control Tower.
locale: en-US
release: yokohama
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-11-23"
reading_time_minutes: 1
breadcrumb: [Explore AI Gateway, Exploring AI Control Tower, AI Control Tower, Enable AI experiences]
---

# MCP server record

Explore the MCP server record and its tabs in the AI Control Tower.

The MCP server record has the following tabs:

-   **Details**: Displays all the asset details along with the MCP server URL at the bottom of the page.
-   **Approvals**: Displays all the approval requests for the particular MCP server.

    **Note:**

    When MCP servers are synced to the AI Gateway with the AI Control Tower Core \(with Now Assist\), an option appears in AI Control Tower to start the approval process. However, with AI Control Tower Pro license version, the button doesn’t appear after the synchronization job runs, and the Lifecycle Status is shown as 'None'.

    This is a known behavior and as a workaround, confirm to set the lifecycle phase to "New" and the lifecycle status to "AI Steward review" for the relevant sn\_ai\_governance\_asset\_governance\_details record.

    This can be achieved by running a script manually:

    ```
    var assetGovernanceRecord = new GlideRecord('sn_ai_governance_asset_governance_details');
    
    if (assetGovernanceRecord.get('<sys_id of asset governance record>')) {
    
        assetGovernanceRecord.setValue('status', 5);
    
        assetGovernanceRecord.setDisplayValue('lifecycle_phase','New');
    
        assetGovernanceRecord.update();
    
    }
    ```

    For information on workflow of MCP server approval request, see [MCP server approval request](../task/playbook-workflow-of-mcp-server-approval-request.md)

-   **KPIs &amp; Metrics**: Displays the MCP tools observability metrics. When you connect to AI Gateway, it starts showing which tool was connected, the number of requests sent, the success rate, and any latency.
-   **AI Gateway setup**: The AI Gateway tab appears only after an MCP server request is approved. AI Gateway setup tab shows all the AI Gateway MCP server details. From the AI Gateway setup tab, you can pause the AI Gateway transaction of the MCP server and add an MCP Client integration. The AI Gateway tab is accessible for all AI Control Tower workspace users.

