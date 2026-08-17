---
title: Rack allocation workflow
description: The rack allocation agentic workflow reserves rack unit space in a datacenter by evaluating placement policies, capacity metrics, and change request requirements to find suitable rack allocations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/telecom-media-technology/now-assist-for-telecom-media-and-technology/rack-allocation-workflow.html
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 1
breadcrumb: [Customer Service Problem Management, Use agentic workflows, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Rack allocation workflow

The rack allocation agentic workflow reserves rack unit space in a datacenter by evaluating placement policies, capacity metrics, and change request requirements to find suitable rack allocations.

## Before you begin

Role required: sn\_ni\_core.dc\_ops\_agent or sn\_ni\_core.inventory\_agent

The rack allocation agentic workflow reserves rack unit space in a datacenter by evaluating placement policies, capacity metrics, and change request requirements to find suitable rack allocations.

Access the rack allocation workflow.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Select **Rack Allocation Workflow**.

Test the agentic workflow.

To access the use case testing page:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Testing**.
2.  On the Overview page, select **Rack allocation workflow**.

AI agents in the rack allocation workflow.

The Rack Allocation Workflow uses the Rack placement AI agent to execute allocation steps. The LLM matches the agent's name and description to workflow steps to select the appropriate agent.

<table id="table_bhl_3y3_vjc"><thead><tr><th>

AI agent

</th><th>

AI agent role

</th></tr></thead><tbody><tr><td>

Rack placement AI agent

</td><td>

Finds a datacenter rack allocation that fits a change request's capacity requirements.

 The agent runs autonomously based on the workflow instructions.

 **Tools used by the agent**

 -   `find_rack_placement` — Finds racks that can accommodate the requested resources. Applies placement policies and capacity constraints. Returns a ranked list of suitable racks.
-   `validate_change_request` — Validates the change request. Verifies required fields are present and properly formatted. Returns validation status.
-   `finalize_allocation` — Finalizes the rack allocation flow: writes a work note summarizing the outcome and moves the change request to Design Complete state.
-   `retrieve_change_request` — Reads the change request from CMDB. Extracts target data center, RU, power, weight, temperature, and equipment requirements.
-   `retrieve_policy` — Retrieves placement policies from published Knowledge Base articles for the target datacenter and individual racks.

</td></tr></tbody>
</table>