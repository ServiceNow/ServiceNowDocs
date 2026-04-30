---
title: MCP server record
description: Explore the MCP server record and its associated tabs.
locale: en-US
release: zurich
product: AI Control Tower
classification: ai-control-tower
topic_type: concept
last_updated: "2025-11-23"
reading_time_minutes: 3
breadcrumb: [AI Gateway, Explore, AI Control Tower, Enable AI experiences]
---

# MCP server record

Explore the MCP server record and its associated tabs.

The MCP server record has the following tabs:

1.  **Details**: Displays all the asset details along with the MCP server URL at the bottom of the page.
2.  **Approvals**: Displays all the approval requests for the MCP server.

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

    For more information on workflow of MCP server approval request, see [MCP server approval workflow](../task/playbook-workflow-of-mcp-server-approval-request.md)

3.  **KPIs &amp; Metrics**: Displays the MCP tools observability metrics for each server, which is approved and running. In the KPIs &amp; Metrics tab, the AI steward can view different tools, which have been invoked across gateway usage from different hosts. The tab shows the total number of requests sent, the success rate, and any latency observed.

    **Note:** Similarly, at the [AI Gateway tab in AI Control Tower](ai-gateway-tab.md) tab on the landing page of AI Control Tower, you can view the various servers that have been used, along with the total number of requests or transactions and the corresponding success rate.

4.  **AI Gateway setup**: The AI Gateway setup tab appears only after an MCP server request is approved. From the AI Gateway setup tab, you can pause the AI Gateway transaction of the MCP server and add an MCP Client integration. The AI Gateway tab is accessible for all AI Control Tower workspace users.

    The AI Gateway setup tab has three sections:

    -   **AI Gateway MCP server details**- Displays the following URLs:

        -   **AI Gateway MCP server URL**- The Gateway endpoint that clients connect to
        -   **Authorization endpoint URL**- OAuth authorization endpoint.
        -   **Token endpoint URL**- OAuth token exchange endpoint.
        **Note:** All the three URLs are generated automatically and can’t be modified.

        If an MCP server is identified as malicious for a certain period, the AI stewards can pause all transactions directed to that server through the AI Gateway. Once the risk is resolved, transactions can be resumed. Similarly, at the AI Gateway level, it’s possible to pause all transactions across all servers from the [AI Gateway](ai-gateway.md) page on the Configurations section of AI Control Tower.

    -   **MCP Client Integration**- Displays Registered clients for the server. Each agent builder requires its own client registration and MCP client Integration generates a client ID and client secret. If you want to enable ServiceNow Agent Studio for a linear MCP server, then you can create an MCP client integration by selecting **Add**.

        **Note:** For more information Gateway setup and MCP Client Integration, see [AI Gateway setup and Client Registration](../task/mcp-client-integration-of-copilot-studio-via-ai-gateway.md)

    -   **Global MCP Clients**- Global MCP clients are set up separately from server records. You can configure them on the Configurations page of AI Control Tower in the [AI Gateway](ai-gateway.md) section. Once they're created, they're automatically available across all MCP servers, so there's no need to set up individual client integrations for each server.
5.  **Related Variants**: The Related Variants tab provides a one-to-one mapping of all the MCP server entries from AI Agent Studio, so each entry is visible and trackable in AI Control Tower. In the Related Variants tab, you can have multiple MCP servers of the same variant.

**Note:** The AI steward can activate sensitive data protection for any transaction across servers by selecting **Activate PII check**. By activating, the AI gateway blocks those transactions, which involve sharing sensitive information to the MCP server.

